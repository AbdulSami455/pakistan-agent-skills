---
name: pbs-pslm
description: PBS Pakistan Social and Living Standards Measurement (PSLM) survey skill. Use when analyzing, summarizing, comparing, or extracting information from the Pakistan Bureau of Statistics (PBS) PSLM survey, especially for poverty rates, household consumption patterns, and access to services at the district or provincial level.
---

# PBS PSLM

## Overview

Use this skill for questions about Pakistan's Pakistan Social and Living Standards Measurement (PSLM) survey, conducted by the Pakistan Bureau of Statistics (PBS). This is the right skill when the task needs household- or district-level micro detail on poverty, consumption, and access to services — a different survey instrument from the Pakistan Economic Survey's social protection chapter, with finer geographic and household granularity.

## Coverage

- Conducted periodically by PBS, alternating between a national/provincial round (larger sample, used for poverty and socio-economic indicators at province level) and a district-level round (used to generate district-level estimates); published as "PSLM" survey reports with a key findings volume and detailed statistical tables.
- Typical structure: household demographic and education module, health module, water supply and sanitation module, housing characteristics module, household consumption/expenditure-based poverty estimates, and access-to-services indicators (education, health facilities, water, electricity, etc.).
- Poverty estimates are typically presented using the official national poverty line methodology, broken down by national, provincial, and (in district-round years) district level.
- Some rounds include immunization coverage, contraceptive use, and other social-indicator modules alongside the core consumption/poverty data.

## Use This Skill For

- extracting poverty headcount rates by province or district
- pulling household consumption or expenditure pattern statistics
- extracting access-to-services indicators (water, sanitation, electricity, education, health facility access)
- comparing socio-economic indicators across districts or provinces
- pulling housing characteristic statistics (housing unit type, room count, tenure)

## Routing Rules

- Use this skill for district- or household-level poverty, consumption, and access-to-services detail drawn from the PSLM instrument.
- For the national poverty and inequality narrative summarized in the annual economic survey, use `pes-social-sectors` (Chapter 16: Social Protection) instead — that chapter cites topline poverty trend figures, this skill is the underlying survey with district/household granularity.
- For employment and labour force statistics, use `pbs-labour-force-survey` instead — PSLM and LFS are separate PBS survey instruments with different sampling and modules, even though both may report some overlapping demographic context.
- If a question asks for a specific district's poverty rate or service-access indicator, this skill is the correct source — PES does not report at district granularity.

## Extraction Workflow

1. Identify whether the question needs national, provincial, or district-level granularity — confirm whether the relevant PSLM round was a district-level round, since not every round generates district estimates.
2. Locate the matching module table (poverty/consumption, education, health, water/sanitation, housing).
3. Preserve the poverty line methodology and reference year used for any poverty headcount figure; methodology can be revised between rounds.
4. Note whether a consumption or expenditure figure is a mean, median, or distributional (quintile/decile) statistic.
5. If comparing across rounds, confirm both rounds use the same poverty line methodology and survey year basis before treating the comparison as valid.

## Technical Rules

- Do not compare poverty headcount rates across PSLM rounds that used different poverty line methodologies without flagging the methodology change.
- District-level estimates are only available in district-round survey years; do not assume every PSLM round has district granularity.
- Household consumption/expenditure figures and access-to-services indicators come from different survey modules; do not blend them into a single indicator.
- Keep national, provincial, and district figures clearly labeled — they are not interchangeable even when discussing the "same" indicator.
- Preserve whether an access-to-services indicator is measured as a household-level percentage or an individual-level percentage.

## Validation Checklist

- Confirm the survey round/year and whether it is a national/provincial or district-level round.
- Verify the poverty line methodology used for any poverty rate cited.
- Check the geographic level (national, provincial, district) matches what was asked.
- Confirm which module (poverty/consumption, health, education, water/sanitation, housing) the indicator comes from.

## Common Pitfalls

- Citing a district-level figure from a round that did not actually produce district estimates.
- Comparing poverty rates across rounds with different poverty line methodologies as if they were directly comparable.
- Confusing PSLM's household consumption-based poverty measure with PES's high-level poverty narrative without noting they may diverge.
- Mixing PSLM access-to-services indicators with PBS Labour Force Survey indicators, which come from a separate survey instrument.

## Reference

- See [PSLM Reference](references/pslm.md) for survey structure and extraction notes.
