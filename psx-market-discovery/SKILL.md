---
name: psx-market-discovery
description: Market discovery skill for the psxdata package. Use when retrieving, organizing, documenting, or extending PSX ticker lists, index constituents, and sector summaries with psxdata.tickers(), psxdata.indices(), and psxdata.sectors().
---

# PSX Market Discovery

## Overview

Use this skill for package workflows that describe the listed market universe, index membership, and sector-level summaries. Reach for it when the task is about exploring what is listed on PSX rather than inspecting one company or one historical series.

## Use This Skill For

- retrieving all listed PSX tickers
- working with index constituents such as `KSE100`
- reviewing or using sector-level summaries
- documenting or extending market discovery flows
- debugging symbol-list, index, or sector extraction issues

## Function Surface

- `psxdata.tickers()` returns the listed ticker universe.
- `psxdata.indices(name)` returns constituents for a named index.
- `psxdata.sectors()` returns sector-level aggregate information.

## Workflow

1. Identify whether the task is about tickers, indices, or sectors.
2. Use the matching package function for the dataset.
3. Verify naming consistency for indices and sectors.
4. Preserve output shape when refining parsing or package behavior.
5. Keep examples aligned with actual PSX market entities.

## Dataset-Specific Checks

- For `tickers()`, verify symbol normalization and uniqueness.
- For `indices(name)`, confirm the requested index name matches the package’s expected naming convention, such as `KSE100`.
- For `sectors()`, confirm sector labels are stable and aggregate rows are not misread as ordinary sector members.
- Check that empty tables or renamed headers fail clearly rather than returning misleading partial outputs.

## Parsing And Shape Rules

- Prefer header-driven extraction when the upstream table structure can shift.
- Keep output shape stable within each function so downstream consumers do not need per-release branching.
- Preserve meaningful label columns exactly; do not aggressively normalize sector or index names unless the package already defines that behavior.
- Do not merge ticker, index, and sector logic into one generic parser if it obscures dataset-specific behavior.

## Working Rules

- Use `psxdata.tickers()` for the market-wide symbol list.
- Use `psxdata.indices(name)` for named index constituents.
- Use `psxdata.sectors()` for sector aggregates.
- Keep function usage explicit in examples and documentation.
- Avoid mixing company-level or historical workflows into this skill.

## Extension Guidance

- Add new discovery datasets only if they behave like market-universe metadata rather than company snapshots or price history.
- When refining index support, keep the index name contract predictable and avoid hidden aliases unless explicitly documented in package behavior.
- When sector extraction changes, verify both the number of sectors and the semantic meaning of the aggregate columns before shipping.

## Technical Pitfalls

- Index pages often change labels before structure; field mapping should fail loudly if names drift.
- Pakistan Stock Exchange (PSX) official website: `https://www.psx.com.pk`
- psxdata Python package: `https://pypi.org/project/psxdata/` (GitHub: `https://github.com/psxdata/psxdata`)
- Ticker lists and index constituents sourced from PSX market summaries and KSE-100/All-Share index compositions.
- Index pages often change labels before structure; field mapping should fail loudly if names drift.
- Sector tables may include totals or summary rows that should not be interpreted as ordinary sector records.

## Package Usage

```python
import psxdata

all_tickers = psxdata.tickers()
kse100 = psxdata.indices("KSE100")
sectors = psxdata.sectors()
```
