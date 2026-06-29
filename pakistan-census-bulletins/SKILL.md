---
name: pakistan-census-bulletins
description: PBS Population & Housing Census (Digital Census) bulletins skill. Use when analyzing, summarizing, comparing, or extracting information from Pakistan Bureau of Statistics (PBS) Population & Housing Census bulletins, especially for population, household, and demographic counts by administrative unit (province, division, district, tehsil).
---

# Pakistan Census Bulletins

## Overview

Use this skill for questions about Pakistan's decadal Population & Housing Census (most recently conducted as the Digital Census), published by the Pakistan Bureau of Statistics (PBS). This is the right skill when the task needs structural population, household, or demographic counts tied to a specific administrative unit — province, division, district, or tehsil — rather than an annual social-sector summary.

## Coverage

- Conducted roughly once a decade by PBS; results are released as census bulletins/tables at successive administrative levels (national, provincial, divisional, district, tehsil), sometimes with separate provisional and final result releases.
- Typical content: total population counts (by sex, and urban/rural classification), number of households and average household size, and basic demographic structure (age distribution where published at this stage), all tabulated by administrative unit.
- Bulletins are usually released in stages — provisional results first (often at province/district level), followed by detailed final tables that go down to tehsil level and may add housing-unit characteristics.
- Because this is a census, figures are full enumeration counts for a specific census reference date, not sample-based estimates.

## Use This Skill For

- extracting population counts for a specific province, division, district, or tehsil
- pulling household counts or average household size by administrative unit
- comparing population growth between census rounds for a given area
- extracting urban/rural population splits by administrative unit
- identifying the male/female population split for a given area

## When Not to Use This Skill

- For the annual narrative on population growth rate, demographic structure, and labour force — use `pes-social-sectors` (Chapter 12: Population, Labour Force and Employment) instead.
- For household consumption, poverty, or service-access detail — use `pbs-pslm` instead.
- For standardizing district/tehsil names and codes — use `pakistan-admin-boundaries` instead; this skill provides census figures, not boundary reconciliation.
- For inter-census population estimates — this skill covers census enumeration only, not annual projections.

## Routing Rules

- Use this skill for administrative-unit-level population/household counts tied to a specific census round.
- For the annual narrative on population growth rate, demographic structure, and labour force drawn into the year's economic survey, use `pes-social-sectors` (Chapter 12: Population, Labour Force and Employment) instead — that chapter cites topline, inter-census growth-rate estimates, this skill is the actual census enumeration by administrative unit.
- For household consumption, poverty, or service-access detail (not raw population/household counts), use `pbs-pslm` instead.
- If a question needs a district- or tehsil-specific population figure, this skill is the correct source — PES does not report population at that granularity.

## Extraction Workflow

1. Identify the exact administrative unit (national, province, division, district, tehsil) and census round the question needs.
2. Confirm whether the figure should come from provisional or final census results — early bulletins are explicitly marked provisional and may later be revised.
3. Locate the matching bulletin table; census tables are typically organized hierarchically (national totals, then provincial breakdowns, then district/tehsil detail within each province).
4. Preserve the sex split (male/female) and urban/rural classification exactly as tabulated; do not infer one from the other.
5. When comparing across census rounds, confirm both rounds used comparable administrative boundaries — district and tehsil boundaries are sometimes redrawn between censuses.

## Technical Rules

- Always state the census round/year and whether the figure is provisional or final.
- Do not assume administrative boundaries are identical across census rounds; new districts/tehsils are occasionally created between censuses, which affects direct comparisons.
- Household counts and average household size are derived from the housing census component; keep separate from pure population headcounts.
- Urban/rural classification follows the census's own definitions, which may differ from informal usage.
- Sub-national totals (district, tehsil) should sum to their parent provincial total; a mismatch usually indicates a different release stage (provisional vs. final) or boundary change.

## Validation Checklist

- Confirm the census round/year and the administrative level (national, province, division, district, tehsil) of the cited figure.
- Verify whether the figure is provisional or final.
- Check whether sex and urban/rural splits are both present or only one dimension is reported in the cited table.
- Confirm administrative boundaries are consistent if comparing across census rounds.

## Common Pitfalls

- Quoting provisional figures as final, or vice versa, without checking the bulletin's release stage.
- Comparing district/tehsil population across census rounds without accounting for boundary changes.
- Confusing household counts with population counts.
- Using this census's point-in-time figures as if they were an annually updated population series.

## Reference

- See [Census Bulletins Reference](references/census-bulletins.md) for bulletin structure and extraction notes.
