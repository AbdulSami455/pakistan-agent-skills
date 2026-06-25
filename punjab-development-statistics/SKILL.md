---
name: punjab-development-statistics
description: Punjab Development Statistics skill. Use when analyzing, summarizing, comparing, or extracting information from the Punjab Bureau of Statistics' annual "Punjab Development Statistics" (also published as "Punjab in Figures"), especially for province-specific socioeconomic indicators across agriculture, population, education, health, and infrastructure sectors.
---

# Punjab Development Statistics

## Overview

Use this skill for province-level socioeconomic statistics for Punjab drawn from the Punjab Bureau of Statistics' annual "Punjab Development Statistics" report (also issued in a condensed form as "Punjab in Figures"). This is the right skill when the question needs Punjab-specific figures rather than national aggregates, and when the indicator set spans multiple sectors in one annual compendium rather than a single-topic federal report.

## Coverage

- Published annually by the Punjab Bureau of Statistics (Government of Punjab).
- Typical structure: multi-chapter statistical compendium covering area and population, agriculture and livestock, industry, education, health, labour force, prices, transport and communication, energy, finance and banking, and social welfare — each chapter presenting time-series tables specific to Punjab districts/divisions.
- "Punjab in Figures" is a shorter companion booklet with headline indicators drawn from the same underlying data, useful for quick figures rather than full time series.
- Document is structure-based with sector chapters and annexed tables; exact chapter numbering and page layout vary by edition.

## Use This Skill For

- extracting Punjab-specific (not national) figures for any covered sector
- comparing district- or division-level statistics within Punjab
- sourcing a province-level time series where national publications (e.g., PBS) do not disaggregate by province
- cross-checking provincial-level indicators against national totals reported elsewhere

## Routing Rules

- Use this skill specifically for Punjab; use `sindh-development-statistics` for the equivalent Sindh Bureau of Statistics publication, and the KP or Balochistan equivalents for those provinces if such skills exist.
- If the question is about national aggregates rather than a single province's breakdown, prefer a national-level skill (e.g., a PBS or PES skill) instead.
- Use this skill instead of PES chapters when district- or division-level granularity within Punjab is required; PES typically reports only at the national or provincial-aggregate level.

## Extraction Workflow

1. Identify the report edition/year and confirm whether the requested indicator is in the full "Development Statistics" volume or the condensed "Punjab in Figures."
2. Identify the sector chapter relevant to the question (agriculture, education, health, etc.) before searching for a figure.
3. Determine whether the requested granularity is province-wide, division-wide, or district-wide, and extract at that exact level.
4. Preserve original units and the reference year/period exactly as tabulated.
5. Note whether a series is a stock (e.g., number of schools) or a flow/rate (e.g., enrollment growth rate).

## Technical Rules

- District and division boundaries can be redrawn between editions; note the administrative geography version if relevant to a comparison.
- Do not merge Punjab Bureau of Statistics figures with PBS national figures without checking definitional consistency (e.g., survey year, methodology).
- Keep sector chapters distinct; a "health" indicator and an "education" indicator should not be combined into one composite score.
- Preserve rural/urban breakdowns where the source table provides them rather than collapsing to a province-wide average.

## Validation Checklist

- Confirm whether the figure is district-, division-, or province-level.
- Verify the report edition/year before quoting a time series point.
- Check whether the source is the full Development Statistics volume or the condensed Punjab in Figures booklet.
- Confirm units and whether a rate or absolute count is being quoted.

## Common Pitfalls

- Treating a district-level figure as representative of the whole province.
- Confusing Punjab Bureau of Statistics figures with national PBS figures that may use different methodology or reference periods.
- Citing "Punjab in Figures" headline numbers without checking the full report for the underlying time series.
- Losing track of administrative boundary changes when comparing district data across years.

## Reference

- See [Punjab Development Statistics Reference](references/punjab-development-statistics.md) for chapter structure and indicator notes.
