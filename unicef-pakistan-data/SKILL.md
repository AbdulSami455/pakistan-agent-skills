---
name: unicef-pakistan-data
description: UNICEF Pakistan data skill. Use when analyzing, summarizing, comparing, or extracting information from UNICEF Pakistan publications, Multiple Indicator Cluster Surveys (MICS), or UNICEF Data Portal indicators on child mortality, nutrition, immunization, WASH, education access, and child protection for Pakistan.
---

# UNICEF Pakistan Data

## Overview

Use this skill for questions about child-focused development indicators for Pakistan as published by UNICEF, including the UNICEF Data Portal, Multiple Indicator Cluster Survey (MICS) reports for Pakistan, and UNICEF Pakistan office publications. This covers internationally standardized child welfare metrics — distinct from Pakistan's own education and health statistics or WHO's broader health-system indicators.

## Coverage

- UNICEF Data Portal (Pakistan country page): summary indicators on child mortality, nutrition, immunization, WASH (water, sanitation, hygiene), education access, and child protection.
- Multiple Indicator Cluster Survey (MICS): periodic household surveys conducted in Pakistan with UNICEF support, providing detailed subnational breakdowns for child and maternal indicators.
- UNICEF Pakistan publications: situation analyses, sectoral reports (nutrition, education, child protection), and humanitarian updates when published.
- Typical indicators: under-five mortality rate, infant mortality rate, stunting/wasting/overweight prevalence among children under five, immunization coverage, access to improved drinking water and sanitation, net attendance/adjusted net attendance rates, out-of-school children counts, birth registration rates.

## Use This Skill For

- extracting child mortality, nutrition, or immunization indicators for Pakistan
- sourcing MICS survey results with provincial or district breakdowns
- identifying WASH access indicators for children and households
- comparing Pakistan's child development indicators with regional benchmarks cited in UNICEF reports
- cross-checking Pakistan's official child statistics against UNICEF estimates

## Routing Rules

- Use this skill for UNICEF-published child-focused indicators. For the Pakistan Economic Survey's health and education narrative, prefer `pes-social-sectors` (Chapters 10 and 11).
- For school-level enrollment statistics from Pakistan's own annual education census, prefer `pakistan-education-statistics`.
- For WHO health-system indicators (health workforce, health expenditure, disease burden at population level), prefer `who-pakistan-health-statistics`.
- For provincial-level health or education facility counts, prefer provincial development statistics skills.
- UNICEF and WHO may report overlapping indicators (e.g., under-five mortality) with different estimation methods — do not treat them as identical without checking.

## Extraction Workflow

1. Identify whether the question needs a UNICEF Data Portal indicator, a MICS survey table, or a UNICEF Pakistan office publication.
2. Preserve the survey round or reference year and whether the figure is an estimate or directly measured.
3. Note the indicator definition and population scope (e.g., children under five, children of primary school age).
4. For MICS results, preserve provincial or district breakdowns when the question is subnational.
5. Distinguish UNICEF global database figures from Pakistan government-reported figures cited within UNICEF documents.

## Technical Rules

- Preserve UNICEF indicator definitions exactly; stunting, wasting, and overweight have specific anthropometric thresholds — do not relabel.
- Immunization coverage rates are percent of target-age children; do not confuse with absolute counts.
- MICS survey rounds are periodic (not annual); confirm the survey year before quoting subnational breakdowns.
- Out-of-school children counts depend on the age band and school-level definition used in the survey instrument.

## Validation Checklist

- Confirm the survey round or reference year.
- Verify the indicator definition, age band, and unit before quoting.
- Check whether the figure is national, provincial, or district-level.
- Distinguish UNICEF estimates from Pakistan government figures when both appear.

## Common Pitfalls

- Treating UNICEF estimates as identical to PBS or Ministry figures.
- Mixing stunting prevalence (percent) with absolute number of stunted children (count) without the underlying population.
- Citing an older MICS round when a newer survey exists.
- Conflating net attendance rate with gross enrollment rate or with school enrollment from Pakistan's own education census.

## Reference

- See [UNICEF Pakistan Data Reference](references/unicef-pakistan-data.md) for source structure and extraction notes.
