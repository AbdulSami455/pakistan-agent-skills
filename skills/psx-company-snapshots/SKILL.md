---
name: psx-company-snapshots
description: Company snapshot skill for the psxdata package. Use when retrieving, documenting, or extending company-level quote and fundamentals workflows with psxdata.quote() and psxdata.fundamentals() for Pakistan Stock Exchange tickers.
---

# PSX Company Snapshots

## Overview

Use this skill for company-level package workflows that need current quote data or fundamentals for a single PSX ticker.

## Use This Skill For

- retrieving a live quote for one ticker
- retrieving fundamentals for one ticker
- documenting company-level package usage
- extending quote or fundamentals handling

## Workflow

1. Confirm the target company symbol.
2. Choose quote data or fundamentals based on the task.
3. Use the matching package function.
4. Check that the returned fields match expected package behavior.
5. Preserve short-lived caching and validation behavior where applicable.

## Working Rules

- Use `psxdata.quote(symbol)` for live quote retrieval.
- Use `psxdata.fundamentals(symbol)` for company financial data.
- Treat quote data as volatile and avoid stale assumptions.
- Keep examples focused on one company symbol at a time.
- Avoid pulling in index or sector workflows here.

## Package Usage

```python
import psxdata

quote = psxdata.quote("LUCK")
fundamentals = psxdata.fundamentals("LUCK")
```

