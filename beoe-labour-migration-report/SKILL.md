---
name: beoe-labour-migration-report
description: BE&OE Labour Migration Report skill. Use when extracting or summarizing annual statistics on Pakistani overseas worker registration and deployment by destination country, occupation/skill category, or province of origin from the Bureau of Emigration & Overseas Employment's "Labour Migration Report," as distinct from OPF's diaspora-welfare mandate or SBP/PBS remittance data.
---

# BE&OE Labour Migration Report

## Overview

Use this skill for questions about how many Pakistani workers went abroad for employment, where they went, what occupations they were registered under, and which province they came from. This covers the Bureau of Emigration & Overseas Employment's (BE&OE) annual "Labour Migration Report" (sometimes also circulated as a "Yearbook" or periodic statistical bulletin), the official statistical publication on registered overseas labour deployment. BE&OE operates under the Ministry of Overseas Pakistanis & Human Resource Development and is the body that registers emigrants and licenses/regulates Overseas Employment Promoters (OEPs, i.e., recruiting agents) before workers travel abroad for work.

## Coverage

Typical report structure includes:

- Overall annual (and often multi-year trend) deployment totals: total number of workers registered for overseas employment in the year, and cumulative totals since BE&OE record-keeping began (often cited from 1971 onward).
- Destination-country breakdown: deployment figures by country. Gulf Cooperation Council (GCC) states have historically dominated overseas Pakistani labour deployment, in roughly this order of scale over most years: Saudi Arabia (typically the largest single destination by a wide margin), United Arab Emirates (second largest), Oman, Qatar, Bahrain, and Kuwait. Non-Gulf destinations (e.g., Malaysia, UK, other European and East Asian markets) appear in the tables but are a much smaller share historically. Exact rank order and share can shift year to year with labour-market demand and visa-policy changes in destination countries — do not assume a fixed ranking without checking the specific year's table.
- Occupation/skill-category breakdown: BE&OE's own registration taxonomy groups workers into skill tiers, broadly:
  - **Unskilled** — laborers and workers with no defined trade/craft skill (historically the largest single category of Pakistani labour deployment).
  - **Semi-skilled** — workers with basic trade exposure but not formally certified (e.g., helpers, assistants in a trade).
  - **Skilled** — workers with a recognized trade/craft skill (e.g., electricians, plumbers, welders, drivers, masons, tailors).
  - **Highly skilled** — workers with specialized technical skill, often requiring some formal training or experience (e.g., technicians, supervisors, foremen).
  - **Highly qualified / Professional** — workers with formal professional qualifications (e.g., engineers, doctors, nurses, accountants, teachers, IT professionals).
  - Note: exact category labels and the granularity of sub-trades listed can vary somewhat by report year; always extract using the report's own category headers rather than a fixed external taxonomy.
- Province/region of origin breakdown: deployment figures attributed to the worker's province of domicile (Punjab, Sindh, Khyber Pakhtunkhwa, Balochistan, Gilgit-Baltistan, Azad Jammu & Kashmir, Islamabad Capital Territory/federal areas). Punjab has historically supplied the largest share of registered overseas workers, consistent with its population share.
- Registration/processing data: numbers processed through Protectorate of Emigrants (POE) offices and through licensed Overseas Employment Promoters (OEPs), versus direct-employer/government-to-government arrangements.
- Historical trend tables showing year-over-year deployment figures, often going back multiple decades, useful for identifying migration surges (e.g., post-1973 oil-boom Gulf demand, and periodic dips tied to destination-country policy changes such as Saudi Nitaqat-type localization drives or COVID-19-era travel restrictions in 2020).

## Use This Skill For

- extracting total annual overseas worker deployment (registration) figures
- breaking down deployment by destination country
- breaking down deployment by occupation/skill category (unskilled, semi-skilled, skilled, highly skilled, highly qualified/professional)
- breaking down deployment by province of origin
- comparing year-over-year trends in labour migration outflows
- identifying which destination countries or occupation categories are growing or shrinking in share
- explaining BE&OE's role in registering emigrants and licensing Overseas Employment Promoters (OEPs)

## When Not to Use This Skill

- For the Overseas Pakistanis Foundation's (OPF) welfare, housing, education, and repatriation-assistance services for the existing diaspora — OPF and BE&OE sit under the same ministry (Ministry of Overseas Pakistanis & Human Resource Development) but have fundamentally different mandates: BE&OE handles outbound registration/regulation of workers *before and during* deployment, while OPF handles welfare services for workers and their families *after* they are already abroad (or upon return). This skill does not cover OPF welfare fund statistics, OPF housing schemes, or OPF school/scholarship programs.
- For inbound refugee/displaced population data, see `unhcr-pakistan-refugee-data` — that skill covers a distinct population (registered Afghan refugees in Pakistan), not Pakistani emigrant workers.
- For remittance flows (the financial inflow resulting from this labour migration), see `pkr-remittances-tracker` — this skill covers headcount/deployment statistics only, not dollar values remitted.

## Routing Rules

- This skill is specific to outbound labour migration (Pakistani workers going abroad for employment) — it is not about inbound migration, refugees, or general population movement.
- If the question is about diaspora welfare (housing schemes, welfare fund payouts, repatriation of deceased workers' bodies, OPF schools) rather than registration/deployment numbers, route to OPF's own material — this skill does not cover it, and no dedicated OPF skill should be assumed to exist unless confirmed separately.
- If the question is about remittance dollar amounts rather than worker headcounts, route to `pkr-remittances-tracker`.
- If the question is about Afghan refugees or other inbound displaced populations, route to `unhcr-pakistan-refugee-data`.

## Extraction Workflow

1. Identify the exact report year (or range, if a multi-year trend table is being used) before extracting any figure.
2. Distinguish "registered" workers from "deployed" workers if the report makes this distinction — registration through BE&OE/POE and actual physical deployment can differ slightly due to processing lags.
3. Extract destination-country figures from the country-breakdown table rather than inferring from narrative text; note whether GCC states are aggregated or listed individually in that year's table.
4. Extract occupation-category figures using the report's own category labels (unskilled/semi-skilled/skilled/highly skilled/highly qualified) rather than re-bucketing into different skill tiers.
5. Extract province-of-origin figures carefully — totals across provinces should reconcile to the national total; flag if they do not.
6. If the question involves OEP-processed vs. direct/government-arranged deployment, extract that split separately rather than assuming all deployment is agent-mediated.

## Technical Rules

- Preserve the report's own occupation-category taxonomy; do not merge or split categories without noting the change.
- Country names and groupings can shift slightly between report years (e.g., GCC aggregation vs. individual country listing) — note which form a given table uses.
- Annual totals are a flow measure for that year, not a cumulative stock of all Pakistanis currently working abroad.
- Province-of-origin figures reflect domicile/registration province, not necessarily current residence.
- Do not conflate BE&OE's outbound registration mandate with OPF's welfare mandate; they are separate agencies under the same ministry with non-overlapping statistical outputs.

## Validation Checklist

- Confirm the report year and whether the figure is annual or a multi-year cumulative trend.
- Confirm whether province-level breakdowns sum to the reported national total.
- Check whether "registered" and "deployed" figures are being conflated.
- Verify destination-country figures against the country-breakdown table rather than summary narrative.
- Confirm the question is genuinely about BE&OE deployment data and not misrouted OPF welfare or remittance-value content.

## Common Pitfalls

- Treating annual deployment flow as a cumulative stock of overseas Pakistani workers.
- Confusing this skill's labour-migration-by-destination data with remittance inflow data (different metric, different skill).
- Mixing up occupation-category labels across report years if the taxonomy changed.
- Reporting national totals without checking whether informal/undocumented migration (not captured by BE&OE registration) is implicitly excluded.
- Conflating BE&OE (outbound regulation/registration) with OPF (diaspora welfare) — they are different agencies with different statistical outputs despite sharing a parent ministry.

## Reference

- See [BE&OE Labour Migration Report Reference](references/beoe-labour-migration-report.md) for occupation taxonomy, destination-country patterns, and source notes.
