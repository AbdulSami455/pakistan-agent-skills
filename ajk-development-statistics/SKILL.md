---
name: ajk-development-statistics
description: Azad Jammu & Kashmir Development Statistics skill. Use when analyzing, summarizing, comparing, or extracting information from the AJK Bureau of Statistics' annual "AJK Development Statistics" (or "AJK in Figures"), especially for territory-specific socioeconomic indicators across agriculture, population, education, health, and infrastructure sectors.
---

# Azad Jammu & Kashmir Development Statistics

## Overview

Use this skill for territory-level socioeconomic statistics for Azad Jammu & Kashmir (AJK) drawn from the AJK Bureau of Statistics' annual "AJK Development Statistics" report (sometimes issued in a condensed "AJK in Figures" form). This is the right skill when the question needs AJK-specific figures rather than national aggregates, and when the indicator set spans multiple sectors in one annual compendium rather than a single-topic federal report.

## Coverage

- Published annually by the Bureau of Statistics, Planning & Development Department, Government of Azad Jammu & Kashmir.
- Typical structure: multi-chapter statistical compendium covering area and population, agriculture and livestock, industry, education, health, labour force, prices, transport and communication, energy, finance and banking, and social welfare — each chapter presenting time-series tables specific to AJK districts.
- Condensed companion booklets may present headline indicators drawn from the same underlying data, useful for quick figures rather than full time series.
- Document is structure-based with sector chapters and annexed tables; exact chapter numbering and page layout vary by edition.

## Use This Skill For

- extracting AJK-specific (not national) figures for any covered sector
- comparing district-level statistics within Azad Jammu & Kashmir
- sourcing a territory-level time series where national publications (e.g., PBS) do not disaggregate by territory
- cross-checking AJK-level indicators against national totals reported elsewhere

## Routing Rules

- Use this skill specifically for Azad Jammu & Kashmir; use `gb-development-statistics` for Gilgit-Baltistan, or the four provincial skills (`punjab-development-statistics`, `sindh-development-statistics`, `kp-development-statistics`, `balochistan-development-statistics`) for the provinces.
- If the question is about national aggregates rather than a single territory's breakdown, prefer a national-level skill (e.g., a PBS or PES skill) instead.
- Use this skill instead of PES chapters when district-level granularity within AJK is required; PES typically reports only at the national or provincial-aggregate level and may omit or treat AJK separately.
- AJK is not a province under Pakistan's constitutional framework but is treated as a distinct administrative territory for statistical reporting; preserve this distinction when comparing to provincial figures.

## Extraction Workflow

1. Identify the report edition/year and confirm whether the requested indicator is in the full Development Statistics volume or a condensed figures booklet.
2. Identify the sector chapter relevant to the question (agriculture, education, health, etc.) before searching for a figure.
3. Determine whether the requested granularity is territory-wide or district-wide, and extract at that exact level.
4. Preserve original units and the reference year/period exactly as tabulated.
5. Note whether a series is a stock (e.g., number of schools) or a flow/rate (e.g., enrollment growth rate).

## Technical Rules

- District boundaries can change between editions; note the administrative geography version if relevant to a comparison.
- Do not merge AJK Bureau of Statistics figures with PBS national figures without checking definitional consistency (e.g., survey year, methodology).
- Keep sector chapters distinct; a "health" indicator and an "education" indicator should not be combined into one composite score.
- Preserve rural/urban breakdowns where the source table provides them rather than collapsing to a territory-wide average.

## Validation Checklist

- Confirm whether the figure is district- or territory-level.
- Verify the report edition/year before quoting a time series point.
- Check whether the source is the full Development Statistics volume or a condensed figures booklet.
- Confirm units and whether a rate or absolute count is being quoted.

## Common Pitfalls

- Treating a district-level figure as representative of the whole territory.
- Confusing AJK Bureau of Statistics figures with national PBS figures that may use different methodology or reference periods.
- Citing condensed booklet headline numbers without checking the full report for the underlying time series.
- Conflating AJK statistics with KP or GB figures when administrative boundaries differ.

## Reference

- See [AJK Development Statistics Reference](references/ajk-development-statistics.md) for chapter structure and indicator notes.
