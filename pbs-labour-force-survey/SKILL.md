---
name: pbs-labour-force-survey
description: PBS Labour Force Survey (LFS) skill. Use when analyzing, summarizing, comparing, or extracting information from the Pakistan Bureau of Statistics (PBS) Labour Force Survey, especially for detailed employment, unemployment, and labour-force-participation statistics broken down by demographic group, region or province, formal versus informal sector, and underemployment.
---

# PBS Labour Force Survey

## Overview

Use this skill for questions about Pakistan's Labour Force Survey (LFS), conducted by the Pakistan Bureau of Statistics (PBS). This is the right skill when the task needs granular employment data — by age, sex, education, region, sector formality, or underemployment status — rather than a single headline labour force or unemployment rate.

## Coverage

- Conducted periodically by PBS (historically annual, with some rounds at a different cadence); published as the "Labour Force Survey" report with detailed statistical tables and a summary/key findings volume.
- Typical structure: definitions and concepts section (labour force, employed, unemployed, underemployed, formal/informal sector), headline national indicators (labour force participation rate, unemployment rate, employment-to-population ratio), then detailed tables disaggregated by sex, age group, area (urban/rural), province, education level, industry/sector (agriculture, manufacturing, services, etc.), employment status (employer, employee, self-employed, unpaid family worker), and formal vs. informal sector classification.
- A separate set of tables typically covers underemployment (time-related underemployment, those working fewer hours than desired) and unemployment by duration and education level.
- Some rounds include child labour or youth-specific modules.

## Use This Skill For

- extracting labour force participation rate or unemployment rate by demographic group (sex, age, education)
- pulling employment statistics by industry/sector or employment status
- comparing formal versus informal sector employment shares
- extracting underemployment statistics
- pulling province- or region-level (urban/rural) breakdowns of labour indicators

## Routing Rules

- Use this skill for demographic-, sector-, or region-disaggregated labour statistics drawn from the LFS instrument itself.
- For the headline national labour force, employment, and unemployment figures summarized in the annual economic narrative, use `pes-social-sectors` (Chapter 12: Population, Labour Force and Employment) instead — that chapter cites the topline LFS figures, this skill is for the underlying disaggregated detail.
- If a question needs poverty or consumption context alongside employment status, check `pbs-pslm` for the household welfare side; LFS itself does not measure poverty or consumption.
- Use this skill specifically when the question references demographic breakdowns, informal sector definitions, or underemployment, which PES typically does not disaggregate.

## Extraction Workflow

1. Identify the demographic, sectoral, or regional breakdown the question needs (sex, age band, education, urban/rural, province, industry, formal/informal).
2. Locate the matching disaggregated table; LFS reports typically organize tables by indicator first, then provide cross-tabulations by demographic variables.
3. Preserve the exact definition used for "labour force," "employed," "unemployed," and "underemployed" as stated in the survey's concepts section — these are technical definitions, not colloquial usage.
4. Note the survey round/reference period precisely, since LFS rounds are not always annual and reference periods can shift.
5. When citing formal/informal sector splits, confirm which definition of informality the survey applies (the LFS typically defines informal employment based on registration, contract, and social-security criteria).

## Technical Rules

- Do not blend "unemployed" with "underemployed" — these are distinct technical categories in LFS terminology.
- Labour force participation rate, employment-to-population ratio, and unemployment rate are related but distinct measures; do not substitute one for another.
- Keep sex, age, and education disaggregations separate unless the cited table is already a cross-tabulation of multiple variables.
- Formal/informal sector classification follows specific survey criteria (registration, contract, benefits); do not infer informality from industry type alone.
- Urban/rural and provincial breakdowns are separate dimensions; confirm which one a table actually disaggregates by.

## Validation Checklist

- Confirm the survey round and reference period of the cited figure.
- Verify which technical category (employed, unemployed, underemployed, out of labour force) the figure refers to.
- Check the demographic or regional disaggregation matches what was asked.
- Confirm whether a sector-formality split uses the survey's own informal-sector definition.

## Common Pitfalls

- Treating the unemployment rate and the underemployment rate as the same statistic.
- Citing a single demographic subgroup's rate as the national headline figure.
- Assuming industry sector (e.g. agriculture) implies informal employment without checking the survey's actual formality classification.
- Comparing LFS rounds with different reference periods as if they were directly comparable annual data points.

## Reference

- See [Labour Force Survey Reference](references/labour-force-survey.md) for report structure and extraction notes.
