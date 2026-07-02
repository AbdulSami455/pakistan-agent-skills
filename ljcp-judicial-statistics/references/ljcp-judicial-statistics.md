# LJCP Judicial Statistics Reference

## Source

- Law & Justice Commission of Pakistan (LJCP), a federal institution chaired by the Chief Justice of Pakistan
- LJCP official website: `https://www.ljcp.gov.pk`
- Judicial statistics and annual reports are published under the site's reports/publications section, alongside law-reform recommendation reports.

## Document Structure

- Court-wise statistics tables: Supreme Court, individual High Courts (Lahore, Sindh, Peshawar, Balochistan, Islamabad), Federal Shariat Court, and subordinate (district) judiciary.
- Per-court figures: institution (new cases filed), disposal (cases resolved), and pendency (backlog carried forward), typically for a quarter or year.
- Case-category breakdowns (civil, criminal, constitutional) where available, in addition to court-wide totals.
- Separate law-reform reports and recommendations (qualitative), distinct from the statistical caseload tables.

## Key Indicator Types

- case institution (new filings) by court/tier and period
- case disposal (resolved cases) by court/tier and period
- case pendency (backlog) by court/tier and period
- clearance rate (disposal relative to institution) where derivable

## Extraction Notes

- Always state the court/tier and reporting period alongside any cited figure.
- Institution, disposal, and pendency should reconcile across consecutive periods (pendency(start) + institution − disposal = pendency(end)); investigate mismatches as a reporting-lag or definitional issue rather than assuming an error.
- Do not sum High Court figures across provinces/territories into a national total unless the source explicitly provides that aggregate.
- Cross-reference `parliament-legislative-tracker` only when a question is actually about legislative bill status, not judicial caseloads — the two track entirely different institutions despite overlapping terminology like "pending."
