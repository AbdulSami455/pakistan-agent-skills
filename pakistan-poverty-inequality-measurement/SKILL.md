---
name: pakistan-poverty-inequality-measurement
description: Pakistan poverty and inequality measurement methodology skill. Use when an analyst needs to explain HOW Pakistan's official poverty line, Gini coefficient, or Multidimensional Poverty Index (MPI) are constructed from PSLM/HIES microdata, or why poverty/inequality figures differ across sources or survey rounds — not simply to fetch a headline poverty rate.
---

# Pakistan Poverty and Inequality Measurement Methodology

## Overview

Use this skill when a task requires understanding the construction methodology behind Pakistan's poverty and inequality statistics — the Cost of Basic Needs (CBN) poverty-line methodology, how the Gini coefficient is derived from HIES/PSLM consumption or income microdata, and how the national Multidimensional Poverty Index (MPI) is built from PSLM indicators using the Alkire-Foster method. This is the measurement-methodology layer; it does not host the headline poverty/Gini figures themselves.

## Coverage

- **Cost of Basic Needs (CBN) poverty line**: Pakistan's official poverty line methodology, adopted since 2013-14, defines poverty using the CBN approach — establishing the minimum expenditure per adult equivalent needed to meet basic nutritional requirements (a calorie threshold) plus an allowance for essential non-food needs (housing, clothing, transport, education). The poverty line is expressed in rupees per adult equivalent per month and is updated between HIES rounds using CPI-based inflation adjustment. Because that CPI adjustment uses the general consumer price index (whose basket reflects broader, not specifically poor-household, consumption patterns), the inflation-adjusted poverty line between survey rounds can drift from what a fresh expenditure survey would show directly.
- **Data source**: Official poverty estimates are produced by the Planning Commission using the Household Income and Expenditure Survey (HIES), fielded by PBS; the closely related PSLM survey (which shares fieldwork infrastructure with HIES in many rounds) supplies the broader socio-economic and access-to-services indicators used for the MPI and other social indicators.
- **Gini coefficient**: Computed from the household consumption (or income, depending on the specific published series) distribution captured in HIES/PSLM microdata — it summarizes dispersion across the full distribution (typically via the Lorenz curve) rather than a poverty headcount, and consumption-based and income-based Gini estimates are not directly comparable to each other or to international income-based Gini figures without noting the base variable used.
- **Multidimensional Poverty Index (MPI)**: Pakistan's national MPI was developed jointly by the Ministry of Planning, UNDP, and the Oxford Poverty and Human Development Initiative (OPHI), using the Alkire-Foster counting methodology. It is built on three equally weighted dimensions (education, health, living standards) using a larger indicator set (developed for the national measure, more granular than the 10 indicators used in the global MPI) drawn from PSLM survey data, distinct in construction and typically higher in headline rate than the CBN consumption-based poverty measure, since it captures deprivation in access/outcomes rather than expenditure alone.
- **Round-to-round comparability**: Poverty and Gini figures are only strictly comparable across HIES/PSLM rounds that use the same poverty-line methodology and survey design; Pakistan's poverty series has at least one major methodology break (the pre-2013-14 caloric-intake-only approach vs. the CBN approach adopted from 2013-14 onward), and district-level estimates are only available in district-round survey years, not every round.

## Use This Skill For

- explaining how Pakistan's official CBN poverty line is constructed and how it is updated between HIES survey rounds
- explaining how the Gini coefficient is derived from HIES/PSLM microdata and what "consumption-based" vs. "income-based" Gini means for comparability
- explaining the Alkire-Foster construction of Pakistan's national MPI and why its headline rate differs from the CBN monetary poverty rate
- assessing whether a poverty-rate comparison across two PSLM/HIES rounds is methodologically valid (same poverty-line approach, same survey design)
- explaining why a district-level poverty or inequality figure may not exist for a given survey round

## When Not to Use This Skill

- For the headline poverty rate, consumption tables, or access-to-services indicators from a specific PSLM round — use `pbs-pslm`.
- For the Pakistan Economic Survey's summarized poverty/inequality narrative — use `pes-social-sectors`.
- For BISP beneficiary counts or cash-transfer targeting data (which uses its own proxy-means-test scorecard, a different instrument from HIES/PSLM poverty measurement) — use `bisp-social-protection-statistics`.

## Routing Rules

- If the task needs an actual published poverty rate, Gini figure, or district-level statistic, route to `pbs-pslm` first, then use this skill to correctly qualify what methodology produced it.
- If the task is about the annual economic-survey-level poverty narrative rather than survey microdata methodology, route to `pes-social-sectors`.
- If the task concerns BISP's proxy-means-test targeting methodology specifically (a distinct poverty-targeting instrument from the official CBN poverty line), route to `bisp-social-protection-statistics`.
- If the task is about labor-market informality rather than poverty/inequality, route to `pakistan-labor-informality-measurement`.

## Extraction Workflow

1. Identify what is being asked: the monetary (CBN) poverty rate, the Gini coefficient, or the MPI — these are three methodologically distinct measures and are not interchangeable.
2. For any poverty or Gini figure, confirm the survey round/year it is drawn from and whether the figure is a directly-surveyed HIES estimate or a CPI-inflation-adjusted interim update of an earlier survey's poverty line.
3. For Gini figures, confirm whether the underlying variable is household consumption or household income, since Pakistan's official series and cross-country comparisons can differ on this basis.
4. For MPI figures, confirm the indicator set and reference year, and note that the national MPI (15-indicator, Pakistan-specific) is a different construction from the global UNDP MPI (10-indicator) even when both are labeled "MPI Pakistan."
5. Before comparing poverty/Gini figures across two rounds, confirm both use the same poverty-line methodology (CBN, post-2013-14) and the same geographic/round type (national/provincial vs. district-capable round).

## Technical Rules

- Do not describe Pakistan's official poverty rate as based on a simple caloric-intake cutoff; the current official methodology (since 2013-14) is the Cost of Basic Needs approach, which combines a food-energy-intake-anchored food component with a non-food allowance.
- Do not compare a CPI-inflation-adjusted interim poverty rate (produced between HIES rounds) with a freshly surveyed HIES-round poverty rate as if both carry equal methodological weight; flag the interim/adjusted status explicitly.
- Do not treat the national MPI rate and the CBN monetary poverty rate as measuring the same thing; they use different indicators, dimensions, and weighting logic and will generally produce different headline percentages for the same year.
- Do not present a district-level poverty or inequality figure without confirming the cited PSLM/HIES round actually produced district-level estimates, since not every round has district granularity.
- Do not blend consumption-based and income-based Gini coefficients into a single trend line without flagging the base-variable switch.

## Validation Checklist

- Confirm which measure (CBN poverty rate, Gini, MPI) is being cited and do not conflate them.
- Confirm the survey round/year and whether the poverty-line methodology matches the post-2013-14 CBN approach.
- Confirm whether a cited figure is a fresh survey estimate or a CPI-adjusted interim update.
- For Gini, confirm the base variable (consumption vs. income).
- For MPI, confirm which MPI construction (Pakistan national vs. UNDP global) is being referenced.
- For district-level claims, confirm the survey round supports district estimates.

## Common Pitfalls

- Citing an old caloric-intake-only poverty methodology description for Pakistan's current official (CBN, post-2013-14) poverty rate.
- Treating the national MPI headline rate and the CBN monetary poverty rate as the same statistic, when they are constructed differently and will diverge.
- Comparing poverty rates across HIES rounds without checking for a methodology break.
- Mixing consumption-based and income-based Gini coefficients in a single comparison without noting the switch.
- Assuming every PSLM/HIES round provides district-level poverty estimates.

## Reference

- See [Poverty and Inequality Measurement Reference](references/pakistan-poverty-inequality-measurement.md) for CBN methodology detail, MPI construction, and sourcing notes.
