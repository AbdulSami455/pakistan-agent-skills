---
name: balochistan-development-statistics
description: Balochistan Development Statistics skill. Use when analyzing, summarizing, comparing, or extracting information from the Balochistan Bureau of Statistics' annual "Balochistan Development Statistics" (or "Balochistan in Figures"), especially for province-specific socioeconomic indicators across agriculture, population, education, health, and infrastructure sectors.
---

# Balochistan Development Statistics

## Overview

Use this skill for province-level socioeconomic statistics for Balochistan drawn from the Balochistan Bureau of Statistics' annual "Balochistan Development Statistics" report (sometimes issued in a condensed "Balochistan in Figures" form). This is the right skill when the question needs Balochistan-specific figures rather than national aggregates, and when the indicator set spans multiple sectors in one annual compendium rather than a single-topic federal report.

## Coverage

- Published annually by the Balochistan Bureau of Statistics, Government of Balochistan.
- Typical structure: multi-chapter statistical compendium covering area and population, agriculture and livestock, industry, education, health, labour force, prices, transport and communication, energy, finance and banking, and social welfare — each chapter presenting time-series tables specific to Balochistan districts/divisions.
- Condensed companion booklets may present headline indicators drawn from the same underlying data, useful for quick figures rather than full time series.
- Document is structure-based with sector chapters and annexed tables; exact chapter numbering and page layout vary by edition.

## Use This Skill For

- extracting Balochistan-specific (not national) figures for any covered sector
- comparing district- or division-level statistics within Balochistan
- sourcing a province-level time series where national publications (e.g., PBS) do not disaggregate by province
- cross-checking provincial-level indicators against national totals reported elsewhere

## Routing Rules

- Use this skill specifically for Balochistan; use `punjab-development-statistics` for Punjab, `sindh-development-statistics` for Sindh, or `kp-development-statistics` for Khyber Pakhtunkhwa.
- If the question is about national aggregates rather than a single province's breakdown, prefer a national-level skill (e.g., a PBS or PES skill) instead.
- Use this skill instead of PES chapters when district- or division-level granularity within Balochistan is required; PES typically reports only at the national or provincial-aggregate level.
- Balochistan's sparse population and large geographic area mean district-level figures can have high sampling variance; note this when interpreting small-district statistics.

## Extraction Workflow

1. Identify the report edition/year and confirm whether the requested indicator is in the full Development Statistics volume or a condensed figures booklet.
2. Identify the sector chapter relevant to the question (agriculture, education, health, etc.) before searching for a figure.
3. Determine whether the requested granularity is province-wide, division-wide, or district-wide, and extract at that exact level.
4. Preserve original units and the reference year/period exactly as tabulated.
5. Note whether a series is a stock (e.g., number of schools) or a flow/rate (e.g., enrollment growth rate).

## Technical Rules

- District and division boundaries can be redrawn between editions; note the administrative geography version if relevant to a comparison.
- Do not merge Balochistan Bureau of Statistics figures with PBS national figures without checking definitional consistency (e.g., survey year, methodology).
- Keep sector chapters distinct; a "health" indicator and an "education" indicator should not be combined into one composite score.
- Preserve rural/urban breakdowns where the source table provides them rather than collapsing to a province-wide average.

## Validation Checklist

- Confirm whether the figure is district-, division-, or province-level.
- Verify the report edition/year before quoting a time series point.
- Check whether the source is the full Development Statistics volume or a condensed figures booklet.
- Confirm units and whether a rate or absolute count is being quoted.

## Common Pitfalls

- Treating a district-level figure as representative of the whole province, especially in sparsely populated districts.
- Confusing Balochistan Bureau of Statistics figures with national PBS figures that may use different methodology or reference periods.
- Citing condensed booklet headline numbers without checking the full report for the underlying time series.
- Losing track of administrative boundary changes when comparing district data across years.

## Reference

- See [Balochistan Development Statistics Reference](references/balochistan-development-statistics.md) for chapter structure and indicator notes.
