---
name: unhcr-pakistan-refugee-data
description: UNHCR Operational Data Portal Pakistan skill. Use when retrieving or analyzing registered Afghan refugee or Proof of Registration (PoR) holder population trends and demographics in Pakistan from UNHCR's Operational Data Portal structured downloadable datasets.
---

# UNHCR Pakistan Refugee Data

## Overview

Use this skill for questions about the registered Afghan refugee population in Pakistan: population size and trends, Proof of Registration (PoR) card holder counts, demographic breakdowns (age, gender), and location/camp distribution. This skill is built on UNHCR's Operational Data Portal (ODP) for Pakistan, which provides structured downloadable data (typically CSV) rather than a press-release or narrative document.

## Important Distinction

This skill covers a **specific displaced/refugee population**, not Pakistan's general population. Do not conflate this with:

- **PBS Population Census** data, which counts Pakistani citizens and residents nationally — Afghan refugees holding PoR cards or Afghan Citizen Cards are a distinct population tracked separately by UNHCR, not as part of the citizen census count.
- General immigration or visa statistics, which are a different administrative category.

If a task asks about "Pakistan's population," route to census-related sources, not this skill. If a task asks specifically about Afghan refugees, registered refugee numbers, or PoR holders, use this skill.

## Data Surface

UNHCR's Operational Data Portal for Pakistan provides structured datasets, typically as downloadable CSV/XLSX files, rather than a programmatic API with a stable endpoint contract. Treat this as a data-workflow skill around downloadable structured files, not a live API integration. Typical fields/structure include:

- **Population figures**: total registered Afghan refugees, broken down by registration status (e.g., PoR card holders, Afghan Citizen Card holders where tracked separately)
- **Demographic breakdowns**: age bands and gender splits
- **Geographic distribution**: population by province/region within Pakistan, and in some releases, by refugee village/camp versus urban/out-of-camp residence
- **Time series**: population trend data across years, useful for tracking growth, repatriation, or registration-drive effects
- **Repatriation/voluntary-return statistics**: where available, figures on repatriation to Afghanistan via UNHCR-facilitated voluntary return

## Use This Skill For

- retrieving the current or historical registered Afghan refugee population in Pakistan
- breaking down the refugee population by age, gender, or province
- tracking year-over-year trends in registration, repatriation, or new arrivals
- distinguishing PoR card holders from Afghan Citizen Card holders or undocumented populations where the dataset makes that distinction
- providing context for refugee-related policy or humanitarian questions specific to Pakistan

## Workflow

1. Identify the specific metric needed: total population, demographic breakdown, geographic distribution, or trend over time.
2. Locate the relevant downloadable dataset on UNHCR's Operational Data Portal for Pakistan (search "UNHCR Operational Data Portal Pakistan" if the direct portal URL has changed, since portal structure is periodically reorganized).
3. Confirm the "as of" date of the dataset — refugee population figures are typically updated periodically (e.g., monthly or quarterly) and are not real-time.
4. Distinguish PoR card holders from any other registration category reported (e.g., Afghan Citizen Card holders) before quoting a total population figure.
5. When reporting trends, use consistent registration-category definitions across the years being compared, since registration-drive policy changes can cause discontinuities that look like population changes.

## Validation Checklist

- Confirm the dataset's "as of" / reporting date before quoting any figure.
- Confirm whether the figure is PoR card holders only, or a combined total across registration categories.
- Check that demographic breakdowns (age/gender) sum to the reported total population figure.
- Verify geographic distribution figures reference the same reporting period as the national total being compared against.

## Working Rules

- Treat ODP downloads as periodically refreshed structured files, not a live queryable API — re-download or re-check the portal for an updated extract rather than assuming cached figures are current.
- Always state the reporting period alongside any population or demographic figure.
- Keep refugee-population figures clearly separated from PBS census figures in any combined analysis; label the source explicitly.
- Note any methodology or registration-category change UNHCR documents alongside the dataset, since these affect trend comparability.

## Technical Pitfalls

- Treating a population count from one reporting period as current without checking the "as of" date.
- Summing PoR holders and Afghan Citizen Card holders without checking whether the dataset already provides a combined total (double-counting risk).
- Confusing repatriation/voluntary-return figures (outflow) with new-registration figures (a different process) when explaining a population change.
- Mistakenly treating this refugee population data as part of, or comparable to, the national citizen population reported by the PBS census.

## Reference

- UNHCR Pakistan Operational Data Portal: `https://data.unhcr.org/en/country/pak`
- UNHCR Pakistan situation page: `https://www.unhcr.org/us/where-we-work/countries/pakistan`
- Downloadable datasets: `https://data.unhcr.org/en/situations` (population statistics, factsheets)
- Confirm the current portal URL and release cadence at time of use, since portal structure can be reorganized.
- See [UNHCR Pakistan Refugee Data Reference](references/unhcr-pakistan-refugee-data.md) for registration categories, persons-of-concern definitions, and the 2023-2025 repatriation-plan discontinuity in the time series.
