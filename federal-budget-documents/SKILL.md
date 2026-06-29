---
name: federal-budget-documents
description: Federal budget documents skill. Use when analyzing, summarizing, comparing, or extracting information from Pakistan's Ministry of Finance federal budget documents, including the Budget in Brief, Budget Speech, Finance Bill, and Demand for Grants, especially for forward-looking allocations, revenue targets, and proposed tax/spending measures rather than realized outturns.
---

# Federal Budget Documents

## Overview

Use this skill for Pakistan's annual federal budget documents released around the June budget cycle: Budget in Brief, Budget Speech, Finance Bill, and Demand for Grants. These documents are forward-looking, presenting proposed allocations and targets for the upcoming fiscal year, in contrast to the Pakistan Economic Survey, which reports backward-looking outturns for the year just ending.

## Coverage

- Budget in Brief: a condensed summary of budget estimates, revenue and expenditure totals, and key fiscal aggregates for the upcoming fiscal year.
- Budget Speech: the Finance Minister's speech presenting the budget, including policy rationale and headline new measures.
- Finance Bill: the legal text proposing tax law amendments (income tax, sales tax, customs duties, federal excise) to take effect with the budget.
- Demand for Grants: ministry-wise and department-wise expenditure allocations requiring parliamentary approval.

## Use This Skill For

- extracting proposed revenue targets or expenditure allocations for the upcoming fiscal year
- summarizing new tax measures announced in the Budget Speech or Finance Bill
- identifying ministry-wise or department-wise allocations from the Demand for Grants
- comparing this year's budgeted figures with the prior year's budgeted (not realized) figures
- tracing a specific tax law change from the Budget Speech announcement to its Finance Bill text

## Routing Rules

- Use this skill for budgeted/proposed figures for the upcoming fiscal year, not realized outturns.
- If the question is about actual fiscal performance, deficits, or outturns for a year already underway or completed, prefer `pes-fiscal-financial-and-debt`.
- If the question is about detailed tax collection statistics by tax head once the year is complete, prefer `fbr-yearbook`.
- If the question is about a specific province's budget rather than the federal budget, prefer `provincial-budget-documents`.
- If the question is about customs tariff schedules specifically (HS codes, duty rates) rather than the broader budget, prefer `fbr-customs-tariff`, since the Finance Bill may reference tariff changes but the Fifth Schedule itself is the authoritative tariff source.

## Extraction Workflow

1. Identify which specific document the question needs: Budget in Brief for aggregate figures, Budget Speech for policy narrative, Finance Bill for exact legal text, or Demand for Grants for line-item allocations.
2. Confirm the fiscal year the budget targets (e.g. "FY 2026-27 Budget" proposed in June 2026).
3. Distinguish "budgeted" or "estimated" figures from any "revised estimates" for the outgoing year that may appear alongside the new budget for comparison.
4. For tax measures, trace the announcement in the Budget Speech to the precise legal language in the Finance Bill before treating it as final, since speech language can be approximate.
5. For Demand for Grants, preserve the exact ministry/department/grant-number structure rather than collapsing allocations into an aggregate.

## Technical Rules

- Always label a figure as "budget estimate," "revised estimate," or "actual" — budget documents often show all three for context.
- Do not treat Budget Speech announcements as enacted law until confirmed against the Finance Bill text or its passage.
- Keep current-year-budgeted and prior-year-budgeted figures clearly separated when making year-over-year comparisons.
- Preserve grant numbers and ministry names exactly as listed in the Demand for Grants.

## Validation Checklist

- Confirm whether a cited figure is for the upcoming fiscal year (proposed) or a revised estimate for the outgoing year.
- Verify tax measure descriptions against the Finance Bill's actual clause language, not just the speech summary.
- Check that ministry/department allocations are matched to the correct grant number.
- Confirm whether totals include or exclude one-off or supplementary grants.

## Common Pitfalls

- Treating budgeted figures as realized fiscal performance.
- Quoting a Budget Speech tax announcement without verifying it survived into the Finance Bill unchanged.
- Confusing current and development expenditure when reading Demand for Grants.
- Mixing up budget estimates for the new year with revised estimates for the year ending.

## Reference

- See [Federal Budget Documents Reference](references/federal-budget-documents.md) for document structure and extraction notes.
