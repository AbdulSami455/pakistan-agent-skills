---
name: psx-historical-data
description: Historical PSX data skill for the psxdata package. Use when retrieving, validating, documenting, or extending historical OHLCV workflows with psxdata.stocks() for Pakistan Stock Exchange tickers and date ranges.
---

# PSX Historical Data

## Overview

Use this skill for historical price workflows built on `psxdata.stocks()`.

## Use This Skill For

- fetching historical OHLCV data for a ticker
- working with start and end date ranges
- validating historical price outputs
- documenting or extending historical data usage

## Workflow

1. Confirm the target ticker symbol and date range.
2. Use `psxdata.stocks(symbol, start, end)` for the retrieval.
3. Verify that the output covers the expected dates.
4. Check for duplicate dates, future dates, and invalid OHLC relationships.
5. Preserve package behavior when extending parsing or validation logic.

## Working Rules

- Normalize ticker input before processing.
- Treat date parsing as fragile and avoid one-format assumptions.
- Prefer resilient parsing over positional assumptions.
- Keep historical cache behavior intact.
- Use realistic PSX date ranges in examples and tests.

## Package Usage

```python
import psxdata

df = psxdata.stocks("ENGRO", start="2024-01-01", end="2024-12-31")
```

