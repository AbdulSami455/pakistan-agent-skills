---
name: psx-market-discovery
description: PSX market-universe skill. Use when identifying listed tickers, sector classifications, or index constituents (KSE-100, KSE-30, KMI-30, All Share) on the Pakistan Stock Exchange, whether via the psxdata package or PSX's official Data Portal.
---

# PSX Market Discovery

## Overview

Use this skill for questions about what is listed on the Pakistan Stock Exchange (PSX): the ticker universe, sector classifications, and index membership. This is a market-structure skill, not a single-company or historical-price skill — reach for it when the task is "what exists / what belongs to what," not "what happened to one stock."

Two data-access paths exist and should not be conflated:
- **Official source (authoritative)**: the PSX Data Portal (`https://dps.psx.com.pk`) and PSX's own market summary/sector/index pages at `https://www.psx.com.pk`, which are the system of record.
- **`psxdata` Python package** (`https://pypi.org/project/psxdata/`, GitHub `mtauha/psxdata`): a convenience wrapper that scrapes PSX pages. As of this writing it is an early-stage (0.1.0-alpha), single-maintainer, low-adoption package — treat its output as a convenience shortcut, not a guaranteed-stable data contract. For any task where correctness matters more than convenience (research papers, financial reports, anything citation-worthy), cross-check against the official PSX Data Portal rather than trusting the package alone.

## Market Structure Reference

- **Sectors**: PSX classifies listed companies into sector indices such as Commercial Banks, Cement, Oil & Gas Exploration, Oil & Gas Marketing, Fertilizer, Textile Composite, Technology & Communication, Automobile Assembler, Power Generation & Distribution, Insurance, Food & Personal Care Products, Chemical, Engineering, and others. Sector membership determines which sector index (if any) a company contributes to — do not assume a company's informal "industry" label matches PSX's official sector classification exactly.
- **Major indices**:
  - **KSE-100**: the flagship benchmark index of the 100 largest, most liquid companies by free-float market capitalization (with some methodology-driven exceptions), rebalanced periodically (semi-annually) by the index committee.
  - **KSE-30**: a free-float-weighted index of the 30 largest, most liquid companies — distinct methodology emphasis from KSE-100.
  - **KMI-30**: the KMI (KSE Meezan Index) of 30 Shariah-compliant companies, screened and maintained jointly with Al Meezan Investments — do not conflate with KSE-30, which has no Shariah screening.
  - **PSX All Share Index**: the broadest index, covering all eligible listed companies rather than a fixed-size subset.
- **Board classification**: listed companies sit on the Main Board, Growth Enterprise Market (GEM board, for smaller/growth companies), or (historically) the SME board — board placement affects listing requirements and typically liquidity, not sector classification.
- Index constituents change at each rebalancing (free-float, market-cap, and liquidity screens are re-applied); a constituent list is a point-in-time snapshot, not a permanent roster.

## Use This Skill For

- retrieving the listed ticker universe or checking whether a symbol is currently listed
- identifying KSE-100 / KSE-30 / KMI-30 / All Share index constituents at a point in time
- classifying a company by its PSX sector
- explaining the difference between KSE-100, KSE-30, and KMI-30 methodologies
- documenting or extending `psxdata` market-discovery workflows (`tickers()`, `indices()`, `sectors()`)

## When Not to Use This Skill

- For one company's live quote or financial fundamentals — use `psx-company-snapshots`.
- For historical OHLCV price series — use `psx-historical-data`.
- For debt instruments (TFCs/Sukuks) or margin-eligible scrip lists — use `psx-debt-and-eligibility`.
- For mutual fund NAV/AUM data (distinct from listed-equity data) — use `mufap-mutual-funds`.
- For company registration/legal-status data (as opposed to listing/trading data) — use `secp-company-registry`.

## Function Surface (psxdata package)

- `psxdata.tickers()` returns the listed ticker universe.
- `psxdata.indices(name)` returns constituents for a named index, e.g. `"KSE100"`.
- `psxdata.sectors()` returns sector-level aggregate information.

## Workflow

1. Identify whether the task needs the full ticker universe, one index's constituents, or sector-level grouping.
2. If precision matters (citations, reports, financial analysis), check the PSX Data Portal directly rather than relying solely on the package; use the package for quick/exploratory lookups.
3. Confirm the requested index name matches PSX's actual index names — do not assume "KSE-30" and "KMI-30" are interchangeable, or that "All Share" is a synonym for KSE-100.
4. Verify sector labels against PSX's official sector list rather than an informal industry taxonomy.
5. Treat any constituent list as dated to a specific rebalancing period; flag that membership changes periodically.

## Technical Rules

- Index pages and sector tables can change their HTML labels before their structure does; field mapping should fail loudly rather than silently mis-map columns if names drift.
- Sector tables may include aggregate/total rows — do not treat these as ordinary sector members.
- Do not treat KSE-30 and KMI-30 as the same index under different names; one is liquidity/size-based, the other is Shariah-screened.
- Do not assume every listed company belongs to a widely-tracked index — most listed companies are outside KSE-100/KSE-30/KMI-30.

## Validation Checklist

- Confirm which specific index is being asked about before returning constituents (KSE-100 vs KSE-30 vs KMI-30 vs All Share).
- Confirm the point-in-time nature of any constituent list — flag that it may be stale relative to the latest rebalancing.
- Cross-check package output against the PSX Data Portal when the task requires citation-grade accuracy.
- Confirm sector labels match PSX's own sector taxonomy rather than a generic industry classification.

## Common Pitfalls

- Treating psxdata package output as equivalent in authority to PSX's own Data Portal.
- Confusing KSE-30 (liquidity/size-based) with KMI-30 (Shariah-screened) or treating "All Share" as another name for KSE-100.
- Presenting an index constituent list without noting it is a snapshot subject to periodic rebalancing.
- Misreading a sector-table aggregate/total row as an individual sector member.

## Package Usage

```python
import psxdata

all_tickers = psxdata.tickers()
kse100 = psxdata.indices("KSE100")
sectors = psxdata.sectors()
```

## Reference

- See [PSX Market Discovery Reference](references/psx-market-discovery.md) for the fuller sector list, index methodology notes, and official-source links.
