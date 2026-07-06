---
name: psx-historical-data
description: PSX historical price-series skill. Use when retrieving, validating, or analyzing daily OHLCV (open/high/low/close/volume) history for a Pakistan Stock Exchange ticker over a date range, whether via the psxdata package or PSX's official historical data archives.
---

# PSX Historical Data

## Overview

Use this skill for date-bounded historical price series on one PSX ticker. This is not a live-quote skill (see `psx-company-snapshots`) and not a market-universe skill (see `psx-market-discovery`) — it is specifically about a time series of daily trading data.

Two data-access paths exist and should not be conflated:
- **Official source (authoritative)**: PSX Data Portal's historical data section (`https://dps.psx.com.pk`), which publishes daily market summaries and closing-price archives.
- **`psxdata` Python package** (`psxdata.stocks()`): a convenience scraper; early-stage (0.1.0-alpha), single-maintainer. Adequate for exploratory analysis; for citation-grade time series (e.g., a backtest used in a research paper), cross-check against the official archive, since a scraper built on an unstable, low-adoption package can silently drop or misalign rows if the source page changes.

## Domain Knowledge — PSX-Specific Historical Data Quirks

- **Corporate action adjustments**: bonus shares, right shares, and stock splits create a mechanical discontinuity in a raw price series — a stock's closing price the day before and after a bonus/right issue is not directly comparable without adjustment (an ex-bonus/ex-right price drop is expected and is not a market movement). If the data source does not provide split/bonus-adjusted historical prices, flag this explicitly rather than treating the raw series as return-equivalent.
- **Circuit breakers**: PSX's daily price-movement limit (a percentage band around the previous close) means some sessions show identical or near-identical high/low/close values when a stock is "locked" at its circuit limit — this is a real trading constraint, not a data error, but it also means the recorded close does not necessarily reflect unconstrained market-clearing price for that session.
- **Trading calendar**: PSX trading days exclude weekends and gazetted public holidays specific to Pakistan (which differ from other countries' market calendars); do not assume a standard 252-trading-day year without checking Pakistan's specific holiday calendar for the years in question.
- **Delisted or suspended tickers**: a company can be suspended from trading (regulatory action, corporate restructuring) or delisted entirely; a historical series that stops abruptly may reflect suspension/delisting rather than a data-retrieval failure — verify company status before assuming a gap is a scraping bug.
- **Symbol reuse/changes**: tickers can occasionally be reassigned or a company's symbol changed after a merger, name change, or restructuring; a continuous-looking series spanning such an event may actually represent two different corporate entities.

## Use This Skill For

- fetching historical OHLCV data for a ticker over a date range
- validating historical price data for internal consistency (OHLC relationships, duplicate/missing dates)
- explaining a price discontinuity in a historical series (corporate action vs. circuit breaker vs. data gap)
- documenting or extending `psxdata.stocks()` workflows

## When Not to Use This Skill

- For a company's current/live quote — use `psx-company-snapshots`.
- For the listed ticker universe, sectors, or index constituents — use `psx-market-discovery`.
- For debt instruments or margin-eligible scrip lists — use `psx-debt-and-eligibility`.

## Function Surface (psxdata package)

- `psxdata.stocks(symbol, start, end)` returns historical OHLCV data for one ticker over the given date range.

## Workflow

1. Confirm the target ticker symbol and the exact date range needed.
2. Retrieve the series via `psxdata.stocks(symbol, start, end)` or the PSX Data Portal archive.
3. Check for duplicate dates, future dates, and OHLC relationship violations (high below open/low/close; low above open/high/close).
4. Check whether any known corporate action (bonus/right share, split) falls within the date range — if so, flag whether the series is adjusted or raw.
5. Check for unexpected gaps and determine whether they reflect a holiday, a trading suspension, or a retrieval issue before treating the series as complete.

## Technical Rules

- Reject or flag rows with future dates.
- Reject or flag duplicate dates for the same symbol rather than silently deduplicating in a way that could hide an upstream parsing bug.
- Enforce OHLC consistency: high must be ≥ open, low, and close; low must be ≤ open, high, and close.
- Do not treat an identical high/low/close across consecutive sessions as a data error without checking whether a circuit-breaker lock explains it.
- Do not silently merge data across a known symbol change (post-merger/rename) as if it were one continuous entity without noting the change.

## Validation Checklist

- Confirm the returned rows fall within the requested start/end bounds.
- Confirm each date appears at most once for the given symbol.
- Confirm OHLC relationships hold for every row.
- Check whether a known corporate action falls within the range and whether the series is split/bonus-adjusted.
- If there is a gap in the series, determine whether it corresponds to a market holiday, a trading suspension, or a genuine data problem.

## Common Pitfalls

- Treating a raw (unadjusted) price series as directly comparable across a bonus/right-share event.
- Misreading a circuit-breaker-locked session as a parsing error.
- Assuming a standard global trading calendar instead of Pakistan's actual market holiday calendar.
- Silently bridging a series across a ticker symbol reassignment or corporate merger without flagging the discontinuity.
- Trusting `psxdata` output as citation-grade without cross-checking the PSX Data Portal archive.

## Package Usage

```python
import psxdata

df = psxdata.stocks("ENGRO", start="2024-01-01", end="2024-12-31")
```

## Reference

- See [PSX Historical Data Reference](references/psx-historical-data.md) for corporate-action adjustment notes and trading-calendar guidance.
