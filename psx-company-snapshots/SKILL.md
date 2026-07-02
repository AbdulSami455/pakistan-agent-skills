---
name: psx-company-snapshots
description: Company snapshot skill for the psxdata package. Use when retrieving, documenting, or extending company-level quote and fundamentals workflows with psxdata.quote() and psxdata.fundamentals() for Pakistan Stock Exchange tickers.
---

# PSX Company Snapshots

## Overview

Use this skill for company-level package workflows that need current quote data or fundamentals for a single PSX ticker. Reach for it when the task is about one company’s latest tradable view or reported financial information, not broad market listings or historical series.

## Use This Skill For

- retrieving a live quote for one ticker
- retrieving fundamentals for one ticker
- documenting company-level package usage
- extending quote or fundamentals handling
- debugging quote or fundamentals extraction issues for a single company

## Function Surface

- `psxdata.quote(symbol)` retrieves the current quote view for one ticker.
- `psxdata.fundamentals(symbol)` retrieves financial report or company fundamentals data for one ticker.
- The main concerns are field stability, freshness, symbol normalization, and preserving dataset semantics.

## Workflow

1. Confirm the target company symbol.
2. Choose quote data or fundamentals based on the task.
3. Use the matching package function.
4. Check that the returned fields match expected package behavior.
5. Preserve short-lived caching and validation behavior where applicable.

## Quote Handling Rules

- Treat quote data as short-lived and time-sensitive.
- Keep quote retrieval focused on one symbol per call path unless the package adds explicit batch behavior.
- Validate that field names remain stable when upstream pages change labels or order.
- Distinguish missing quote data from parser failure; do not collapse both into the same behavior without intent.

## Fundamentals Handling Rules

- Preserve report-level structure if the package returns multiple periods or grouped financial fields.
- Be careful with partially missing fundamentals rows; missing values should not silently shift columns.
- Keep company identity fields tied to the requested symbol so cross-company leakage is impossible.

## Working Rules

- Use `psxdata.quote(symbol)` for live quote retrieval.
- Use `psxdata.fundamentals(symbol)` for company financial data.
- Treat quote data as volatile and avoid stale assumptions.
- Keep examples focused on one company symbol at a time.
- Avoid pulling in index or sector workflows here.

## Extension Guidance

- When adding fields, prefer preserving existing naming and value semantics over cosmetic reshaping.
- If upstream HTML changes, update extraction logic before changing user-facing outputs.
- Keep cache behavior appropriate to data freshness:
  - quote data should remain short-lived
  - fundamentals can usually tolerate less frequent refresh

## Validation Checklist

- Confirm the returned data is for the requested symbol only.
- Check for field drift caused by column reordering or renamed headers.
- Verify missing financial values do not corrupt adjacent fields.
- Inspect whether quote freshness assumptions still match cache duration.

## Technical Pitfalls

- Field names can change between PSX website revisions.
- Pakistan Stock Exchange (PSX) official website: `https://www.psx.com.pk`
- psxdata Python package: `https://pypi.org/project/psxdata/` (GitHub: `https://github.com/mtauha/psxdata`)
- Validate that field names remain stable when upstream pages change labels or order.
- Fundamentals tables often break through missing cells, merged headers, or period-grouping changes.
- Over-normalizing labels can make new upstream fields indistinguishable from old ones.

## Package Usage

```python
import psxdata

quote = psxdata.quote("LUCK")
fundamentals = psxdata.fundamentals("LUCK")
```
