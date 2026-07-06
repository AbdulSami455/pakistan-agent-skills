---
name: psx-debt-and-eligibility
description: PSX debt-market and margin-eligibility skill. Use when identifying listed debt instruments (TFCs, Sukuks) or margin-trading-eligible stocks on the Pakistan Stock Exchange, whether via the psxdata package or PSX's official debt-market and margin-eligibility disclosures.
---

# PSX Debt and Eligibility

## Overview

Use this skill for two specialized, non-equity PSX datasets: listed debt instruments (corporate debt securities) and the margin-trading-eligible stock list. These sit apart from ordinary equity ticker/quote/history workflows because they carry their own instrument categories, eligibility rules, and regulatory framing.

Two data-access paths exist and should not be conflated:
- **Official source (authoritative)**: PSX's own debt market and margin trading system (MTS) disclosures at `https://www.psx.com.pk` and the PSX Data Portal (`https://dps.psx.com.pk`).
- **`psxdata` Python package** (`debt_market()`, `eligible_scrips()`): a convenience scraper; early-stage (0.1.0-alpha), single-maintainer. For anything citation-grade, verify against PSX's own published debt-market and eligible-securities lists.

## Domain Knowledge

- **TFCs (Term Finance Certificates)**: long-term corporate debt instruments issued by companies to raise fixed-income capital, functioning similarly to corporate bonds — they pay periodic profit/markup and are redeemed at or before maturity. TFCs can be listed (tradable on PSX) or privately placed.
- **Sukuks**: Shariah-compliant debt-like instruments structured to avoid interest (riba) — typically based on an underlying asset, lease, or partnership structure (e.g., Ijarah Sukuk, Diminishing Musharakah Sukuk) rather than a simple interest-bearing loan. Sukuks and TFCs serve a similar fixed-income-market role but have materially different legal/contractual structures; do not describe a Sukuk as "just an Islamic TFC" without noting the structural difference.
- **Margin Trading System (MTS)**: PSX's regulated mechanism allowing investors to trade certain stocks using broker-financed leverage. Only stocks meeting PSX/SECP eligibility criteria (typically related to free float, market capitalization, price stability, and liquidity) are included in the MTS-eligible scrip list — being listed on PSX does not automatically make a stock margin-eligible.
- **Margin Financing (MF) and Securities Lending and Borrowing (SLB)**: related but distinct leveraged/short-selling mechanisms with their own eligible-securities lists; do not assume the MTS-eligible list is identical to the MF- or SLB-eligible list.
- Eligible-scrip lists are reviewed and revised periodically by PSX/SECP (e.g., following changes in a stock's liquidity or free float) — treat any eligibility list as a point-in-time snapshot.

## Use This Skill For

- retrieving listed debt market instruments (TFCs, Sukuks)
- retrieving the margin-trading-eligible stock list
- explaining the structural difference between a TFC and a Sukuk
- explaining what margin eligibility means and how it differs from ordinary listing
- documenting or extending `psxdata.debt_market()` / `psxdata.eligible_scrips()` workflows

## When Not to Use This Skill

- For ordinary equity tickers, sectors, or index constituents — use `psx-market-discovery`.
- For a company's live quote or fundamentals — use `psx-company-snapshots`.
- For historical OHLCV equity price series — use `psx-historical-data`.
- For mutual fund NAV/AUM or voluntary pension scheme data — use `mufap-mutual-funds`.
- For government debt/securities (T-bills, PIBs, Sukuk issued by the government) — treat as out of scope for this equity-market-focused skill; that is a debt-management/SBP-auction topic, not a PSX corporate-debt-market topic.

## Function Surface (psxdata package)

- `psxdata.debt_market()` retrieves debt market instruments such as TFCs or Sukuks listed/traded on PSX.
- `psxdata.eligible_scrips()` retrieves the margin-eligible stock list.

## Workflow

1. Confirm whether the task concerns debt instruments (TFCs/Sukuks) or equity margin eligibility — these are unrelated datasets that happen to share this skill for being "specialized, non-standard" PSX data.
2. If debt instruments: identify whether the question is about a specific instrument's structure (TFC vs. Sukuk) or the list of currently listed/traded instruments.
3. If eligibility: confirm which leverage mechanism is meant (MTS, MF, or SLB) before quoting an "eligible" list, since these lists differ.
4. Cross-check against PSX's own published lists for anything citation-grade, given the underlying package's early-stage status.
5. Note the as-of date/period for any eligibility or debt-instrument list, since both are revised periodically.

## Technical Rules

- Keep debt-instrument rows (TFC/Sukuk) distinct from equity-style records; do not coerce them into the same schema, since fields like coupon/profit rate and maturity date have no direct equity equivalent.
- Do not treat the MTS-eligible list as interchangeable with MF- or SLB-eligible lists.
- Preserve instrument-type and category fields exactly; they carry the primary meaning of a debt-market row.
- Fail clearly rather than silently returning a partial or ambiguous result if the upstream table structure changes.

## Validation Checklist

- Confirm whether the request is about debt instruments or margin eligibility before answering.
- If about debt instruments, confirm whether the specific instrument is a TFC or a Sukuk, and do not conflate the two structurally.
- If about eligibility, confirm which mechanism (MTS/MF/SLB) is intended.
- Confirm the as-of date of any list before presenting it as current.

## Common Pitfalls

- Describing a Sukuk as functionally identical to a TFC without noting the Shariah-compliant structural difference.
- Assuming every PSX-listed stock is margin-eligible.
- Conflating MTS-eligible, MF-eligible, and SLB-eligible scrip lists.
- Treating psxdata package output as equivalent in authority to PSX's own published debt-market/eligibility lists.

## Package Usage

```python
import psxdata

debt = psxdata.debt_market()
scrips = psxdata.eligible_scrips()
```

## Reference

- See [PSX Debt and Eligibility Reference](references/psx-debt-and-eligibility.md) for TFC/Sukuk structure notes and eligibility-mechanism definitions.
