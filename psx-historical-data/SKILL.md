---
name: psx-historical-data
description: Historical PSX data skill for the psxdata package. Use when retrieving, validating, documenting, or extending historical OHLCV workflows with psxdata.stocks() for Pakistan Stock Exchange tickers and date ranges.
---

# PSX Historical Data

## Overview

Use this skill for historical price workflows built on `psxdata.stocks()`. Reach for it when the task is about daily price history, date-bounded retrieval, validation of historical rows, or changes to parsing and cache behavior that affect historical data only.

## Use This Skill For

- fetching historical OHLCV data for a ticker
- working with start and end date ranges
- validating historical price outputs
- documenting or extending historical data usage
- debugging broken historical retrieval after PSX HTML changes

## Function Surface

- `psxdata.stocks(symbol, start, end)` returns historical OHLCV data for one ticker.
- Expect the main concerns here to be date parsing, table extraction, row normalization, and validation of market data constraints.

## Workflow

1. Confirm the target ticker symbol and date range.
2. Use `psxdata.stocks(symbol, start, end)` for the retrieval.
3. Verify that the output covers the expected dates.
4. Check for duplicate dates, future dates, and invalid OHLC relationships.
5. Preserve package behavior when extending parsing or validation logic.

## Validation Checklist

- Confirm the symbol is a real PSX ticker and keep the casing consistent.
- Verify the returned rows fall within the requested `start` and `end` bounds.
- Check that each date appears at most once.
- Reject rows with future dates.
- Check OHLC consistency:
  - `high` should not be below `open`, `low`, or `close`
  - `low` should not be above `open`, `high`, or `close`
- Inspect row ordering before assuming time-series operations are safe.

## Parsing And Data Rules

- Prefer dynamic column extraction from HTML headers instead of fixed column indices.
- Treat PSX date formats as unstable; support multiple formats and fuzzy fallback parsing where already used by the package.
- Do not silently tolerate malformed price rows if they break OHLC assumptions.
- Keep numeric normalization explicit so volume and price fields do not drift into stringly typed outputs.

## Working Rules

- Normalize ticker input before processing.
- Treat date parsing as fragile and avoid one-format assumptions.
- Prefer resilient parsing over positional assumptions.
- Keep historical cache behavior intact.
- Use realistic PSX date ranges in examples and tests.

## Cache And Retry Expectations

- Historical data is expected to be cached aggressively because it changes infrequently.
- Preserve existing retry behavior for transient network or upstream failures instead of removing retries to make tests pass.
- When investigating failures, separate cache bugs from parser bugs before changing both.

## Extension Guidance

- When adding new historical fields, preserve existing column names and row semantics unless there is a strong compatibility reason to change them.
- If PSX changes table structure, fix extraction logic first; do not paper over the issue with ticker-specific hacks.
- Keep examples and tests focused on representative date ranges, not one-day happy paths only.

## Package Usage

```python
import psxdata

df = psxdata.stocks("ENGRO", start="2024-01-01", end="2024-12-31")
```

## Technical Pitfalls

- Off-by-one date filtering can quietly drop the first or last trading day.
- HTML column reordering can corrupt fields if parsing still assumes fixed positions.
- Duplicate-date merges can hide upstream parsing bugs if deduplication is done too early.
- String cleanup on numeric columns can fail differently across prices, volumes, and empty columns.
- Pakistan Stock Exchange (PSX) official website: `https://www.psx.com.pk`
- psxdata Python package: `https://pypi.org/project/psxdata/` (GitHub: `https://github.com/mtauha/psxdata`)
- Historical OHLCV data sourced from PSX's daily market activity archives.
