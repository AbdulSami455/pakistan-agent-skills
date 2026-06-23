---
name: psx-debt-and-eligibility
description: Debt and eligibility skill for the psxdata package. Use when retrieving, documenting, or extending debt market and margin-eligibility workflows with psxdata.debt_market() and psxdata.eligible_scrips().
---

# PSX Debt and Eligibility

## Overview

Use this skill for package workflows involving PSX debt instruments and margin-eligible stock lists.

## Use This Skill For

- retrieving debt market instruments
- retrieving margin-eligible stocks
- documenting debt or eligibility package usage
- extending package handling for these datasets

## Workflow

1. Confirm whether the task is about debt instruments or eligible scrips.
2. Use the matching package function.
3. Verify dataset naming and field consistency.
4. Preserve output shape when changing parsing logic.
5. Keep examples aligned with the package’s intended dataset scope.

## Working Rules

- Use `psxdata.debt_market()` for debt market instruments.
- Use `psxdata.eligible_scrips()` for margin-eligible stocks.
- Keep debt and eligibility examples distinct from equity price history.
- Avoid blending this skill with ticker discovery or quote workflows.

## Package Usage

```python
import psxdata

debt = psxdata.debt_market()
scrips = psxdata.eligible_scrips()
```
