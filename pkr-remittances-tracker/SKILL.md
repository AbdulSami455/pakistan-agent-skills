---
name: pkr-remittances-tracker
description: PKR workers' remittances tracker skill. Use when analyzing, summarizing, comparing, or extracting information from State Bank of Pakistan monthly workers' remittances data tables, especially when the task needs a country/corridor-wise breakdown published as structured tables (CSV/Excel) rather than narrative text.
---

# PKR Remittances Tracker

## Overview

Use this skill for SBP's monthly workers' remittances data, published as structured statistical tables broken down by sending country/corridor. Unlike a narrative PDF report, this data is typically released as CSV/Excel-style tables on SBP's website, so extraction should be framed around reading structured rows and columns rather than parsing prose.

## Coverage

- Total monthly workers' remittance inflows in US dollars.
- Country/corridor-wise breakdown: remittances by sending country (e.g. Saudi Arabia, UAE, USA, UK, other GCC) for each month.
- Multi-month and multi-year time series tables allowing month-on-month and year-on-year comparison.
- Published monthly by SBP, usually within the first half of the following month.

## Use This Skill For

- extracting total remittance inflows for a specific month
- extracting the country/corridor breakdown of remittances for a specific month
- comparing remittance inflows month-on-month or year-on-year, in aggregate or by corridor
- identifying which sending countries/corridors are the largest or fastest-growing sources of remittances over a stated period
- reconciling a specific month's remittance figure against the cumulative fiscal-year-to-date total

## Routing Rules

- Use this skill specifically for SBP's structured remittance tables at monthly/country-corridor granularity.
- If the question is about the PES's annual remittances narrative within the external sector chapter, prefer `pes-external-sector` for the full-year framing, and use this skill when month-level or corridor-level detail is needed.
- If the question is about the current account or reserves more broadly rather than remittances specifically, prefer `sbp-balance-of-payments-bulletin`.
- Treat this data source as tabular, not narrative: do not expect a chapter/section structure the way PES or SBP's Annual Report have one.

## Extraction Workflow

1. Identify the exact month (and year) the question needs; remittance tables are organized by calendar month even when discussed in a fiscal-year context.
2. If a country/corridor breakdown is needed, locate the specific country's column/row in the table rather than the aggregate total only.
3. When asked for a cumulative figure (e.g. "July-March FY 2026"), sum the individual monthly figures from the table and state explicitly that the total is a derived sum, unless SBP's table already provides a year-to-date column.
4. Preserve the exact US dollar figures and the period label; do not convert to PKR unless the question specifically asks for a rupee equivalent, and if so, state the exchange rate basis used.
5. For year-on-year comparisons, align the same calendar month across years rather than comparing a calendar month to a different fiscal-year sub-period.

## Technical Rules

- Treat each row/column intersection (month x country) as the atomic data point; do not interpolate missing months or countries.
- Do not blend remittance data with export/import or current account figures; remittances are one component cited separately in the broader balance of payments.
- Keep "total remittances" distinct from any single corridor's figure when reporting comparisons.
- When SBP revises a prior month's figure in a later release, prefer the most recently published value unless the task specifically wants the originally reported figure.

## Validation Checklist

- Confirm the exact month and year match what was requested.
- Verify whether a country/corridor figure is being compared against the correct total (monthly total, not a different period's total).
- Check whether a cumulative period figure is an official SBP year-to-date total or a manually summed total.
- Confirm currency units (USD) and note if any rupee conversion was introduced and on what exchange-rate basis.

## Reference

- State Bank of Pakistan: `https://www.sbp.org.pk`
- Remittances data: `https://www.sbp.org.pk/ecodata/index2.asp` (Economic Data section, Workers' Remittances)
- Published as monthly CSV/Excel tables; table structure is consistent but column headers may be revised.

## Common Pitfalls

- Confusing fiscal-year-to-date sums with calendar-year sums when aggregating monthly remittance data.
- Treating a provisional monthly figure as final without checking for later revision.
- Mixing up total remittances with a single corridor's contribution when summarizing "remittance performance."
- Comparing year-on-year growth using mismatched months (e.g. comparing a 28-day February to a 31-day month elsewhere) without noting the difference.
