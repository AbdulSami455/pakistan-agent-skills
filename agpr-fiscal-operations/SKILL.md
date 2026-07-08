---
name: agpr-fiscal-operations
description: Pakistan fiscal operations skill. Use when analyzing, summarizing, comparing, or extracting information from official federal fiscal-operations or accounts releases, especially for actual receipts, expenditure, deficit, borrowing, and cash-balance movements rather than budget estimates.
---

# AGPR Fiscal Operations

## Overview

Use this skill for questions about the government's actual fiscal outturns and cash-flow execution. This covers federal receipts, payments, financing, and deficit-related figures that appear in fiscal-operations statements, accounts, and similar official releases.

This is an execution/outturn skill, not a budget-estimate skill and not a tax-head breakdown skill.

## Coverage

- Actual federal receipts and expenditure
- Current and development expenditure as executed
- Financing and borrowing flows
- Cash balances and treasury movements, where reported
- Consolidated or federal-only fiscal operations tables, depending on the source release
- Year-to-date and month-to-month outturns when available in official fiscal statements

## Use This Skill For

- finding the government's actual fiscal deficit or surplus for a period
- comparing budgeted and realized expenditure
- tracing receipts, spending, and borrowing through the fiscal year
- reconciling treasury or accounts figures with the Pakistan Economic Survey
- analyzing whether a change was in current spending, development spending, or financing

## When Not to Use This Skill

- For budgeted allocations before execution, use `federal-budget-documents` or `psdp-federal-development-programme`.
- For tax-head detail, sector contribution, or withholding-category revenue breakdowns, use `fbr-yearbook`.
- For broad macro commentary or year-end summaries, use `pes-fiscal-financial-and-debt`.
- For provincial development budgets or provincial fiscal outturns, use the relevant provincial budget or statistics skill.

## Routing Rules

- Use this skill when the question is about what actually happened in government accounts.
- Use budget-document skills when the question is about what was approved or allocated.
- Use PES only when a high-level summary is enough; use this skill when the actual line-item or fiscal-operation figure matters.
- If the question is about a specific tax head or collection category, route to FBR skills instead.

## Extraction Workflow

1. Identify the fiscal year, month, or period covered by the release.
2. Determine whether the release is federal-only or consolidated with provincial figures.
3. Separate receipts, expenditure, deficit, and financing before drawing conclusions.
4. Preserve gross and net figures exactly when both are reported.
5. Note whether the release is provisional, revised, or cumulative year-to-date.

## Technical Rules

- Do not compare a budget estimate with an actual outturn without labeling the difference.
- Distinguish current expenditure from development expenditure.
- Keep financing flows separate from deficit figures.
- Preserve the source's sign convention for deficits, surpluses, and borrowing.
- If the release combines multiple layers of government, do not present it as federal-only without checking the table heading.

## Validation Checklist

- Confirm the period and fiscal year.
- Verify whether the figure is a receipt, expenditure, deficit, or financing item.
- Check whether the release is federal-only or consolidated.
- Preserve gross vs net, and current vs development, where relevant.
- Cross-check the figure against the source table heading before extracting it.

## Common Pitfalls

- Treating budget allocations as realized spending.
- Mixing federal and consolidated fiscal figures.
- Collapsing financing and deficit into one number.
- Ignoring sign conventions for surplus/deficit items.
- Quoting an interim month as a full-year result.

## Reference

- See [AGPR Fiscal Operations Reference](references/agpr-fiscal-operations.md) for source-family notes, interpretation rules, and official links.
