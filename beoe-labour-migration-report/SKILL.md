---
name: beoe-labour-migration-report
description: BE&OE Labour Migration Report skill. Use when extracting or summarizing annual statistics on Pakistani overseas worker registration and deployment by destination country, occupation category, or province of origin from the Bureau of Emigration & Overseas Employment's "Labour Migration Report."
---

# BE&OE Labour Migration Report

## Overview

Use this skill for questions about how many Pakistani workers went abroad for employment, where they went, what occupations they were deployed in, and which province they came from. This covers the Bureau of Emigration & Overseas Employment's (BE&OE) annual "Labour Migration Report," the official statistical publication on registered overseas labour deployment.

## Coverage

Typical report structure includes:

- Overall annual (and often multi-year trend) deployment totals: total number of workers registered for overseas employment in the year
- Destination-country breakdown: deployment figures by country, with Gulf states (Saudi Arabia, UAE, Oman, Qatar, Bahrain, Kuwait) typically dominating the totals
- Occupation-category breakdown: deployment by skill/occupation category (e.g., unskilled, semi-skilled, skilled, highly qualified, and sometimes specific trades)
- Province/region of origin breakdown: deployment figures attributed to the worker's province of domicile (Punjab, Sindh, Khyber Pakhtunkhwa, Balochistan, Gilgit-Baltistan, Azad Jammu & Kashmir, federal areas)
- Sometimes includes registration data from Protectorates of Emigrants offices and licensed overseas employment promoters
- Historical trend tables showing year-over-year deployment figures, often going back multiple decades

## Use This Skill For

- extracting total annual overseas worker deployment figures
- breaking down deployment by destination country
- breaking down deployment by occupation/skill category
- breaking down deployment by province of origin
- comparing year-over-year trends in labour migration outflows
- identifying which destination countries or occupation categories are growing or shrinking in share

## Routing Rules

- This skill is specific to outbound labour migration (Pakistani workers going abroad for employment) — it is not about inbound migration, refugees, or general population movement.
- For inbound refugee/displaced population data, see `unhcr-pakistan-refugee-data` — that skill covers a distinct population (registered Afghan refugees in Pakistan), not Pakistani emigrant workers.
- Remittance flows resulting from this labour migration are covered separately by `pkr-remittances-tracker`; use that skill for the financial/remittance side rather than this skill, which covers headcount/deployment statistics only.

## Extraction Workflow

1. Identify the exact report year (or range, if a multi-year trend table is being used) before extracting any figure.
2. Distinguish "registered" workers from "deployed" workers if the report makes this distinction — registration and actual deployment can differ.
3. Extract destination-country figures from the country-breakdown table rather than inferring from narrative text.
4. Extract occupation-category figures using the report's own category labels rather than re-bucketing into different skill tiers.
5. Extract province-of-origin figures carefully — totals across provinces should reconcile to the national total; flag if they do not.

## Technical Rules

- Preserve the report's own occupation-category taxonomy; do not merge or split categories without noting the change.
- Country names and groupings can shift slightly between report years (e.g., GCC aggregation vs. individual country listing) — note which form a given table uses.
- Annual totals are a flow measure for that year, not a cumulative stock of all Pakistanis currently working abroad.
- Province-of-origin figures reflect domicile/registration province, not necessarily current residence.

## Validation Checklist

- Confirm the report year and whether the figure is annual or a multi-year cumulative trend.
- Confirm whether province-level breakdowns sum to the reported national total.
- Check whether "registered" and "deployed" figures are being conflated.
- Verify destination-country figures against the country-breakdown table rather than summary narrative.

## Common Pitfalls

- Treating annual deployment flow as a cumulative stock of overseas Pakistani workers.
- Confusing this skill's labour-migration-by-destination data with remittance inflow data (different metric, different skill).
- Mixing up occupation-category labels across report years if the taxonomy changed.
- Reporting national totals without checking whether informal/undocumented migration (not captured by BE&OE registration) is implicitly excluded.

## Reference

- The Bureau of Emigration & Overseas Employment publishes the "Labour Migration Report" on its official website/portal; table structure and category definitions can vary by year.
