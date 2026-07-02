---
name: ljcp-judicial-statistics
description: Law & Justice Commission of Pakistan (LJCP) judicial statistics skill. Use when analyzing, summarizing, comparing, or extracting information from LJCP's court statistics — case pendency, institution, and disposal figures across the Supreme Court, High Courts, Federal Shariat Court, and subordinate judiciary — as distinct from bill-tracking or statutory text.
---

# LJCP Judicial Statistics

## Overview

Use this skill for Pakistan's court performance and caseload statistics compiled and published by the Law & Justice Commission of Pakistan (LJCP), the federal body chaired by the Chief Justice of Pakistan that monitors judicial reform. This is the right skill for case pendency, institution (new filings), and disposal figures across courts — not for legislative bill status or the text of laws themselves.

## Coverage

- National Judicial Policy-linked quarterly/annual judicial statistics covering the Supreme Court, High Courts (Lahore, Sindh, Peshawar, Balochistan, Islamabad), Federal Shariat Court, and subordinate (district) judiciary.
- Typical figures: case institution (new cases filed), disposal (cases decided/resolved), and pendency (backlog) — usually broken down by court/tier and sometimes by case category (civil, criminal, constitutional).
- Judicial performance and case-clearance-rate commentary tied to the National Judicial Policy's backlog-reduction targets.
- LJCP also publishes law reform reports and recommendations, which are qualitative/legal-reform documents rather than statistical tables — keep these separate from the caseload statistics.

## Use This Skill For

- extracting case pendency, institution, or disposal figures for a specific court or tier
- comparing judicial backlog trends across reporting periods
- identifying clearance rates (disposal relative to institution) for a court
- summarizing which court tier carries the largest share of pending cases
- distinguishing case statistics from LJCP's separate law-reform policy recommendations

## When Not to Use This Skill

- For the status of a specific bill moving through the National Assembly or Senate — use `parliament-legislative-tracker` instead; that skill covers legislative process, this skill covers court caseloads.
- For the text or interpretation of a specific law or judgment — this skill provides statistics only, not full-text legal research.
- For provincial assembly legislative activity — out of scope for both this skill and `parliament-legislative-tracker`, which covers the federal legislature only.

## Routing Rules

- Use this skill for court caseload statistics (pendency, institution, disposal). Use `parliament-legislative-tracker` for bill status through the National Assembly or Senate — these are entirely separate branches of government with separate reporting.
- If a question conflates "judicial backlog" with "pending legislation," clarify which is meant before answering, since both use the word "pending" but refer to different institutions.
- LJCP's law-reform recommendation reports are qualitative policy documents, not part of this skill's statistical caseload coverage; flag if a question needs the former instead.

## Extraction Workflow

1. Identify the specific court/tier (Supreme Court, a named High Court, Federal Shariat Court, or subordinate judiciary) the question refers to.
2. Confirm the reporting period (quarter/year) for the statistics needed.
3. Distinguish institution (new filings), disposal (cases resolved), and pendency (backlog carried forward) — these three figures together reconcile as: pendency(start) + institution − disposal = pendency(end).
4. If a clearance rate is needed, compute or extract it as disposal relative to institution for the same period, and state the period explicitly.
5. Note whether a case-category breakdown (civil, criminal, constitutional) is available or whether the figure is a court-wide total.

## Technical Rules

- Keep institution, disposal, and pendency as three distinct figures; do not infer one from another without confirming the reconciliation holds for the specific period and court.
- Court tiers (Supreme Court, High Courts, Federal Shariat Court, subordinate judiciary) have very different caseload volumes; do not compare absolute pendency across tiers without normalizing or explicitly noting the scale difference.
- High Court figures are province/territory-specific (Lahore, Sindh, Peshawar, Balochistan, Islamabad); do not sum them into a "High Court total" unless the source itself provides that aggregate.
- Judicial statistics reporting periods may not align exactly with fiscal years; confirm the specific period covered before comparing to fiscal-year-based figures from other skills.

## Validation Checklist

- Confirm which court/tier the cited figure belongs to.
- Verify the reporting period and whether it is a quarter, year, or cumulative figure.
- Check that institution, disposal, and pendency are not conflated when reporting caseload figures.
- Confirm whether a High Court figure is for a specific province/territory or a national High Court aggregate.

## Common Pitfalls

- Confusing LJCP judicial caseload "pendency" with pending legislation from `parliament-legislative-tracker`.
- Summing High Court figures across provinces without checking whether the source already provides a national aggregate.
- Treating a single quarter's disposal figure as representative of the full year's clearance rate.
- Mixing LJCP's qualitative law-reform recommendations with its quantitative caseload statistics as if they were the same type of source.

## Reference

- See [LJCP Judicial Statistics Reference](references/ljcp-judicial-statistics.md) for data structure and extraction notes.
