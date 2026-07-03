---
name: pes-social-sectors
description: Pakistan Economic Survey social sectors skill. Use when analyzing, summarizing, comparing, or extracting information from the Pakistan Economic Survey on education, health and nutrition, population, labour force and employment, and social protection, especially for enrolment, health manpower, demographic trends, welfare, poverty, and inequality.
---

# PES Social Sectors

## Overview

Use this skill for Pakistan Economic Survey questions about education, health, nutrition, population, labour, employment, poverty, inequality, and social protection. This is the right skill when the task is about human-development indicators or household welfare outcomes in the survey.

## Chapter Coverage

- Chapter 10: Education: starts at survey page `169`
- Chapter 11: Health and Nutrition: starts at survey page `189`
- Chapter 12: Population, Labour Force and Employment: starts at survey page `209`
- Chapter 16: Social Protection: starts at survey page `275`

## Use This Skill For

- extracting school enrolment or school-count figures
- summarizing health manpower or health-service statistics
- analyzing population growth, labour force, or employment indicators
- extracting poverty, inequality, or social protection metrics
- comparing social indicators across years or provinces

## Routing Rules

- Use Chapter 10 for schooling, enrolment, institutions, and teacher counts.
- Use Chapter 11 for health manpower, health systems, and nutrition-related material.
- For internationally comparable health indicators (mortality, immunization, health expenditure), prefer `who-pakistan-health-statistics`.
- For child-specific indicators (child mortality, stunting, WASH, out-of-school children), prefer `unicef-pakistan-data`.
- Use Chapter 12 for population size, demographic structure, labour force, and employment.
- Use Chapter 16 for poverty, inequality, welfare, and social protection outcomes.
- For BISP/Benazir cash transfer beneficiary counts or disbursement detail, prefer `bisp-social-protection-statistics`; this chapter summarizes social protection at a narrative level.
- For survey-based poverty headcount rates with district granularity, prefer `pbs-pslm`.

## Extraction Workflow

1. Identify the social-domain topic before reading.
2. Pull the exact table or subsection that contains the indicator.
3. Preserve the population group, age band, or provincial scope when present.
4. Keep time basis exact: calendar year, fiscal year, survey year, or projected year.
5. If the indicator is estimated or provisional, say so.

## Technical Rules

- Do not merge enrolment, literacy, attendance, and institution counts into a single education indicator.
- Health tables may use calendar-year reporting; keep that distinction explicit.
- Population, labour, and poverty indicators often come from different underlying sources; do not present them as one measurement system.
- For inequality and poverty, preserve whether the discussion is national or provincial.
- Keep social-indicator improvement separate from welfare deterioration if the chapter presents both together.

## Validation Checklist

- Check whether the figure is national, provincial, age-specific, or institution-specific.
- Verify whether the data is reported in a calendar year or fiscal-year frame.
- Confirm whether the metric is a level, rate, ratio, or count.
- If comparing across years, ensure the measurement basis is unchanged.

## Common Pitfalls

- Confusing enrolment growth with attendance or literacy improvement.
- Treating registered health personnel counts as direct service-delivery quality measures.
- Mixing national poverty numbers with provincial inequality values.
- Missing the survey’s distinction between progress in some social indicators and deterioration in consumption-based poverty.

## Reference

- See [Social Sectors Reference](references/social-sectors.md) for chapter routing, scope discipline, and indicator-handling notes.
