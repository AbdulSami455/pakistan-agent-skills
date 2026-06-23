---
name: psx-market-discovery
description: Market discovery skill for the psxdata package. Use when retrieving, organizing, documenting, or extending PSX ticker lists, index constituents, and sector summaries with psxdata.tickers(), psxdata.indices(), and psxdata.sectors().
---

# PSX Market Discovery

## Overview

Use this skill for package workflows that describe the listed market universe, index membership, and sector-level summaries.

## Use This Skill For

- retrieving all listed PSX tickers
- working with index constituents such as `KSE100`
- reviewing or using sector-level summaries
- documenting or extending market discovery flows

## Workflow

1. Identify whether the task is about tickers, indices, or sectors.
2. Use the matching package function for the dataset.
3. Verify naming consistency for indices and sectors.
4. Preserve output shape when refining parsing or package behavior.
5. Keep examples aligned with actual PSX market entities.

## Working Rules

- Use `psxdata.tickers()` for the market-wide symbol list.
- Use `psxdata.indices(name)` for named index constituents.
- Use `psxdata.sectors()` for sector aggregates.
- Keep function usage explicit in examples and documentation.
- Avoid mixing company-level or historical workflows into this skill.

## Package Usage

```python
import psxdata

all_tickers = psxdata.tickers()
kse100 = psxdata.indices("KSE100")
sectors = psxdata.sectors()
```

