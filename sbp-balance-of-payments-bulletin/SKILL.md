---
name: sbp-balance-of-payments-bulletin
description: SBP Balance of Payments bulletin skill. Use when analyzing, summarizing, comparing, or extracting information from State Bank of Pakistan monthly or quarterly statistical bulletins on the balance of payments, foreign exchange reserves, and external debt servicing, especially when the task needs higher-frequency data than the annual external-sector chapter in the Pakistan Economic Survey.
---

# SBP Balance of Payments Bulletin

## Overview

Use this skill for State Bank of Pakistan statistical releases on the balance of payments, reserves, and external debt servicing published on a monthly or quarterly cadence. This is the right skill whenever a task needs a specific month's or quarter's external-sector figures rather than an annual summary.

## Coverage

- Monthly/quarterly balance of payments summary: current account, capital and financial account, and overall balance.
- Foreign exchange reserves data: SBP reserves, reserves held by banks, and total liquid reserves, usually reported weekly or monthly.
- External debt servicing data: principal and interest payments due and paid, typically reported monthly or quarterly alongside external debt stock updates.
- Source: SBP statistics pages under External Sector / Balance of Payments on `https://www.sbp.org.pk`.

## Use This Skill For

- extracting current account balance for a specific month or quarter
- tracking foreign exchange reserves levels and week-on-week or month-on-month changes
- extracting external debt servicing (principal and interest) due or paid in a period
- comparing balance of payments components across consecutive months or quarters within a fiscal year
- reconciling monthly data against the annual figures reported elsewhere

## Routing Rules

- Use this skill for any sub-annual (monthly, quarterly, or weekly) external-sector statistic.
- If the question is about the PES's annual external-sector narrative (trade, remittances, current account framed for the full fiscal year), prefer `pes-external-sector` instead.
- If the question is about SBP's own annual narrative framing of the external sector, prefer `sbp-annual-report`.
- If the question is specifically about workers' remittances by country/corridor, prefer `pkr-remittances-tracker`, since that skill is structured around SBP's remittance tables specifically.
- If the question is about external debt stock and sustainability narrative rather than period-by-period servicing flows, prefer `pes-fiscal-financial-and-debt`.

## Extraction Workflow

1. Identify the exact period (month, quarter, or week) the question is about, since SBP publishes overlapping cadences (weekly reserves, monthly BOP, quarterly summaries).
2. Locate the specific bulletin or data table for that period rather than the nearest annual summary.
3. Preserve whether a current account figure is a surplus or deficit and keep the sign explicit.
4. Separate gross reserves, net reserves, and liquid foreign reserves; these are commonly conflated.
5. For debt servicing, distinguish principal repayments from interest payments and note whether the figure is "due" or "paid."
6. When aggregating multiple months into a sub-period total (e.g. July-March), state explicitly that the figure is a sum across the cited bulletins, not a single official release.

## Technical Rules

- Always state the reporting period explicitly (e.g. "March 2026" vs. "Q3 FY 2026") since SBP bulletins use both monthly and quarterly framing.
- Do not blend SBP's gross reserves figure with the State Bank-only component without labeling which one is being used.
- Keep external debt servicing figures denominated as given (US dollars) and do not convert without stating the exchange rate basis.
- Treat weekly reserves data as a different series cadence from the monthly balance of payments summary; do not average across mismatched cadences silently.

## Validation Checklist

- Confirm the exact period label matches the bulletin queried.
- Verify whether the current account figure is provisional or revised in a later bulletin.
- Check reserves are reported as "SBP reserves," "bank reserves," or "total liquid reserves" before quoting a number.
- Confirm debt servicing figures are not double counted across overlapping monthly and quarterly releases.

## Common Pitfalls

- Citing reserves levels without specifying SBP-only vs. total liquid reserves.
- Confusing year-on-year monthly comparisons with month-on-month comparisons.
- Treating a quarterly bulletin total as additive with monthly bulletins covering the same months without checking for revisions.
- Mixing up debt servicing due dates with actual payment dates.

## Reference

- See [Balance of Payments Bulletin Reference](references/balance-of-payments-bulletin.md) for bulletin structure and extraction notes.
