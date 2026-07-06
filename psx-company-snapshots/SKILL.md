---
name: psx-company-snapshots
description: PSX single-company data skill. Use when retrieving a live quote or financial fundamentals for one Pakistan Stock Exchange-listed company, whether via the psxdata package or PSX's official disclosures (PSX Data Portal, company financial statements filed under PSX/SECP disclosure rules).
---

# PSX Company Snapshots

## Overview

Use this skill for company-level data on one PSX-listed ticker: its current tradable quote or its reported financial fundamentals. This is not a market-wide listing skill (see `psx-market-discovery`) and not a historical time-series skill (see `psx-historical-data`).

Two data-access paths exist and should not be conflated:
- **Official source (authoritative)**: PSX Data Portal (`https://dps.psx.com.pk`) for live/end-of-day quotes, and the company's own filings (quarterly/annual financial statements, notices) filed under PSX listing regulations and SECP's corporate disclosure requirements — these are the legally authoritative fundamentals, not any third-party aggregation.
- **`psxdata` Python package**: a convenience scraper wrapping PSX pages; early-stage (0.1.0-alpha), single-maintainer. Fine for exploratory work; for anything citation-grade (a report figure, a research paper claim), verify against the company's actual filed financial statements or the PSX Data Portal.

## Domain Knowledge

- **Quote fields** typically include last traded price, change (absolute and percentage), volume, and day's high/low — these reflect the most recent trading session, not a real-time tick-by-tick feed, unless the source explicitly says otherwise.
- **Fundamentals** for a PSX company are grounded in figures the company itself files: quarterly and annual financial statements (balance sheet, profit & loss, cash flow), submitted under the Companies Act 2017 and PSX/SECP disclosure timelines. Common fundamentals fields include EPS (earnings per share), P/E ratio, book value per share, dividend yield/payout, and market capitalization.
- **Corporate actions** (bonus shares, right shares, cash dividends, stock splits) directly affect period-over-period comparability of price and per-share figures — a company's EPS or share price before and after a bonus/right issue is not directly comparable without adjustment.
- **Circuit breakers**: PSX enforces daily price movement limits (a percentage band around the previous close) for most securities; a stock hitting its upper or lower circuit does not necessarily reflect the "true" market-clearing price for that session.
- Financial year-ends vary by company (most Pakistani companies use a June 30 fiscal year-end, but some — e.g., companies aligned with a parent's calendar year — do not); do not assume a uniform reporting calendar across companies when comparing fundamentals.

## Use This Skill For

- retrieving a company's current/latest quote
- retrieving a company's reported fundamentals (EPS, P/E, book value, dividend data)
- explaining how a corporate action (bonus/right share, dividend) affects interpretation of a quote or fundamentals figure
- documenting or extending `psxdata` company-level workflows (`quote()`, `fundamentals()`)

## When Not to Use This Skill

- For the listed ticker universe, sector classification, or index constituents — use `psx-market-discovery`.
- For historical OHLCV price series over a date range — use `psx-historical-data`.
- For debt instruments or margin-eligible scrip lists — use `psx-debt-and-eligibility`.
- For formal company registration/legal status (as opposed to trading/financial data) — use `secp-company-registry`.

## Function Surface (psxdata package)

- `psxdata.quote(symbol)` retrieves the current quote view for one ticker.
- `psxdata.fundamentals(symbol)` retrieves financial report or fundamentals data for one ticker.

## Workflow

1. Confirm the target company's ticker symbol (PSX symbols are typically 3-5 uppercase letters, e.g., `LUCK` for Lucky Cement, `ENGRO` for Engro Corporation).
2. Determine whether the task needs a quote (current tradable view) or fundamentals (reported financial data).
3. If precision matters, cross-check package output against the PSX Data Portal or the company's actual filed financial statements rather than relying on the package alone.
4. Check for recent corporate actions (bonus/right shares, dividends) that would affect comparability of the figure being discussed.
5. Note the company's fiscal year-end before describing a fundamentals figure as "latest annual" or "latest quarterly."

## Technical Rules

- Treat quote data as time-sensitive and tied to the most recent session close (or live session if explicitly real-time) — do not present it as a static fact without a timestamp.
- Distinguish "missing data" (a field not reported/not applicable) from a parsing failure; do not silently treat both the same way.
- Do not compare EPS or per-share figures across a bonus/right-share event without noting the adjustment, since share count changes mechanically affect per-share metrics.
- Keep fundamentals period-tagged (which quarter/year) rather than presenting a bare number.

## Validation Checklist

- Confirm the returned data corresponds to the requested symbol only (not a similarly-named or delisted ticker).
- Check for a recent bonus/right share or stock split before treating a per-share metric as directly comparable to a prior period.
- Confirm which fiscal period a fundamentals figure belongs to.
- Cross-check any citation-grade figure against the PSX Data Portal or the company's own filed statements.

## Common Pitfalls

- Presenting a stale cached quote as current without a timestamp caveat.
- Comparing EPS/book-value-per-share across a bonus or right issue without adjusting for the share-count change.
- Treating psxdata package output as equivalent in authority to the company's actual SECP/PSX filings.
- Assuming every PSX company uses a June 30 fiscal year-end.

## Package Usage

```python
import psxdata

quote = psxdata.quote("LUCK")
fundamentals = psxdata.fundamentals("LUCK")
```

## Reference

- See [PSX Company Snapshots Reference](references/psx-company-snapshots.md) for fundamentals field definitions and corporate-action handling notes.
