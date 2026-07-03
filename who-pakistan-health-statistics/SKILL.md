---
name: who-pakistan-health-statistics
description: WHO Pakistan health statistics skill. Use when analyzing, summarizing, comparing, or extracting information from WHO country profiles, World Health Statistics reports, or WHO Pakistan publications on health indicators, disease burden, immunization coverage, health workforce, and health-system performance for Pakistan.
---

# WHO Pakistan Health Statistics

## Overview

Use this skill for questions about Pakistan's health indicators as published by the World Health Organization (WHO), including WHO country profiles, World Health Statistics annual reports, and WHO Pakistan office publications. This covers internationally standardized health metrics — distinct from Pakistan's own health statistics in the Pakistan Economic Survey, provincial development statistics, or PBS health surveys.

## Coverage

- WHO country profile for Pakistan: summary health indicators updated periodically on the WHO website.
- World Health Statistics: WHO's annual compilation of global health indicators, with Pakistan-specific rows for metrics such as life expectancy, maternal mortality ratio, under-five mortality rate, immunization coverage, health expenditure, and health workforce density.
- WHO Pakistan office publications: situation reports, disease-specific bulletins (e.g., polio, dengue, COVID-19), and health-system assessments when published for Pakistan.
- Typical indicators: life expectancy at birth, maternal and child mortality rates, immunization coverage (DTP3, measles, etc.), disease incidence/prevalence (TB, malaria, HIV/AIDS), health expenditure as percent of GDP, physician/nurse/midwife density, hospital bed density, cause-of-death breakdowns.

## Use This Skill For

- extracting internationally comparable health indicators for Pakistan
- comparing Pakistan's health metrics with regional or global benchmarks cited in WHO reports
- sourcing WHO-estimated mortality, morbidity, or immunization coverage figures
- identifying health workforce density or health expenditure indicators from WHO databases
- cross-checking Pakistan's official health statistics against WHO estimates

## Routing Rules

- Use this skill for WHO-published health indicators with international methodology. For Pakistan's own health statistics in the annual economic narrative, prefer `pes-social-sectors` (Chapter 11: Health and Nutrition).
- For province- or district-level health facility or manpower statistics within Pakistan, prefer provincial development statistics skills or `pakistan-education-statistics`-style sector reports rather than WHO aggregates.
- For UNICEF's child-focused indicators (child mortality, nutrition, WASH, education access), prefer `unicef-pakistan-data` when the question is specifically about children; WHO and UNICEF may cite overlapping indicators with different estimation methods.
- WHO estimates may differ from PBS or Ministry of National Health Services figures due to modeling, imputation, or different reference periods — do not treat them as identical without checking.

## Extraction Workflow

1. Identify whether the question needs a WHO country profile indicator, a World Health Statistics table row, or a WHO Pakistan office publication.
2. Preserve the reference year and whether the figure is an estimate, projection, or reported value.
3. Note the indicator definition (e.g., maternal mortality ratio per 100,000 live births vs. absolute deaths).
4. When comparing across years, check whether WHO revised historical estimates in a new edition.
5. Distinguish WHO global database figures from Pakistan government-reported figures cited within WHO documents.

## Technical Rules

- Preserve WHO indicator definitions exactly; do not relabel metrics (e.g., "under-five mortality rate" is per 1,000 live births, not a count).
- Health expenditure figures may be reported as percent of GDP, percent of government expenditure, or per capita USD — preserve the basis.
- WHO estimates for Pakistan may use modeling when official data is incomplete; note when a figure is modeled rather than directly reported.
- Immunization coverage rates are typically reported as percent of target population; do not confuse with absolute number of vaccinated children.

## Validation Checklist

- Confirm the reference year and whether the figure is an estimate or reported value.
- Verify the indicator definition and unit before quoting.
- Check whether WHO revised the figure in a subsequent edition.
- Distinguish WHO estimates from Pakistan government figures when both appear.

## Common Pitfalls

- Treating WHO estimates as identical to Pakistan Ministry of Health or PBS figures.
- Mixing maternal mortality ratio (rate) with absolute maternal deaths (count).
- Citing an outdated WHO country profile when a newer World Health Statistics edition exists.
- Conflating WHO health indicators with UNICEF child-specific indicators that use different estimation methods.

## Reference

- See [WHO Pakistan Health Reference](references/who-pakistan-health-statistics.md) for source structure and extraction notes.
