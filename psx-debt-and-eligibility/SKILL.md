---
name: psx-debt-and-eligibility
description: Debt and eligibility skill for the psxdata package. Use when retrieving, documenting, or extending debt market and margin-eligibility workflows with psxdata.debt_market() and psxdata.eligible_scrips().
---

# PSX Debt and Eligibility

## Overview

Use this skill for package workflows involving PSX debt instruments and margin-eligible stock lists. Reach for it when the task is about non-standard equity datasets that sit beside the main ticker and quote workflows.

## Use This Skill For

- retrieving debt market instruments
- retrieving margin-eligible stocks
- documenting debt or eligibility package usage
- extending package handling for these datasets
- debugging extraction issues in specialized PSX reference datasets

## Function Surface

- `psxdata.debt_market()` retrieves debt market instruments such as TFCs or Sukuks.
- `psxdata.eligible_scrips()` retrieves the margin-eligible stock list.
- These functions usually require more care around labeling, category fields, and upstream table variations than simple ticker lists.

## Workflow

1. Confirm whether the task is about debt instruments or eligible scrips.
2. Use the matching package function.
3. Verify dataset naming and field consistency.
4. Preserve output shape when changing parsing logic.
5. Keep examples aligned with the package’s intended dataset scope.

## Dataset Rules

- Keep debt-market rows distinct from equity price-history concepts.
- Keep eligibility rows distinct from broad ticker-universe datasets.
- Preserve category or instrument-type fields where present; they often carry the main business meaning of the row.
- Fail clearly if the upstream table becomes structurally incompatible instead of returning ambiguous partial results.

## Working Rules

- Use `psxdata.debt_market()` for debt market instruments.
- Use `psxdata.eligible_scrips()` for margin-eligible stocks.
- Keep debt and eligibility examples distinct from equity price history.
- Avoid blending this skill with ticker discovery or quote workflows.

## Validation Checklist

- Check that debt instruments retain their instrument identity and are not coerced into equity-style records.
- Verify eligible-scrip rows represent the current eligibility dataset and not a stale cached snapshot beyond intended behavior.
- Inspect field names for silent drift after upstream table changes.
- Confirm row counts are plausible before trusting the output.

## Extension Guidance

- Add new specialized PSX reference datasets here only if they are closer to debt or eligibility lists than to company snapshots or historical price series.
- When package behavior changes, preserve column meaning first and row formatting second.
- Avoid generic normalization that erases distinctions between instrument classes.

## Technical Pitfalls

- Reusing equity-oriented cleanup logic on debt instruments can destroy instrument-specific meaning.
- Pakistan Stock Exchange (PSX) official website: `https://www.psx.com.pk`
- psxdata Python package: `https://pypi.org/project/psxdata/` (GitHub: `https://github.com/mtauha/psxdata`)
- Debt market and margin eligibility data sourced directly from PSX daily disclosures.
- Empty or sparse cells can shift columns if parsing logic assumes every row is dense.
- Reusing equity-oriented cleanup logic on debt instruments can destroy instrument-specific meaning.

## Package Usage

```python
import psxdata

debt = psxdata.debt_market()
scrips = psxdata.eligible_scrips()
```
