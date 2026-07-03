---
name: sindh-development-statistics
description: Sindh Development Statistics skill. Use when analyzing, summarizing, comparing, or extracting information from the Sindh Bureau of Statistics' annual "Sindh Development Statistics" report, especially for province-specific socioeconomic indicators across agriculture, population, education, health, and infrastructure sectors.
---

# Sindh Development Statistics

## Overview

Use this skill for province-level socioeconomic statistics for Sindh drawn from the Sindh Bureau of Statistics' annual "Sindh Development Statistics" report. This is the right skill when the question needs Sindh-specific figures rather than national aggregates, and when the indicator set spans multiple sectors in one annual compendium rather than a single-topic federal report.

## Coverage

- Published annually by the Sindh Bureau of Statistics (Government of Sindh).
- Typical structure: multi-chapter statistical compendium covering area and population, agriculture and livestock, industry, education, health, labour force, prices, transport and communication, energy, finance and banking, and social welfare — each chapter presenting time-series tables specific to Sindh districts.
- Document is structure-based with sector chapters and annexed tables; exact chapter numbering and page layout vary by edition.

## Use This Skill For

- extracting Sindh-specific (not national) figures for any covered sector
- comparing district-level statistics within Sindh, including the Karachi division's distinct urban profile versus other Sindh districts
- sourcing a province-level time series where national publications (e.g., PBS) do not disaggregate by province
- cross-checking provincial-level indicators against national totals reported elsewhere

## Routing Rules

- Use this skill specifically for Sindh; use `punjab-development-statistics` for Punjab, `kp-development-statistics` for Khyber Pakhtunkhwa, or `balochistan-development-statistics` for Balochistan.
- If the question is about national aggregates rather than a single province's breakdown, prefer a national-level skill (e.g., a PBS or PES skill) instead.
- Use this skill instead of PES chapters when district-level granularity within Sindh is required; PES typically reports only at the national or provincial-aggregate level.

## Extraction Workflow

1. Identify the report edition/year and the sector chapter relevant to the question before searching for a figure.
2. Determine whether the requested granularity is province-wide or district-wide, noting that Karachi's districts are often reported separately from other Sindh districts.
3. Preserve original units and the reference year/period exactly as tabulated.
4. Note whether a series is a stock (e.g., number of health facilities) or a flow/rate (e.g., literacy rate).
5. Keep rural/urban breakdowns distinct where provided, since Sindh's rural-urban divide is pronounced and often analytically relevant.

## Technical Rules

- District boundaries can be redrawn between editions (including Karachi's internal district structure); note the administrative geography version if relevant to a comparison.
- Do not merge Sindh Bureau of Statistics figures with PBS national figures without checking definitional consistency (e.g., survey year, methodology).
- Keep sector chapters distinct; do not combine indicators across sectors into one composite score.
- Preserve rural/urban breakdowns where the source table provides them.

## Validation Checklist

- Confirm whether the figure is district-level or province-level.
- Verify the report edition/year before quoting a time series point.
- Check whether the figure is specific to Karachi division or to Sindh's other districts, since both can be miscategorized as "Sindh" generally.
- Confirm units and whether a rate or absolute count is being quoted.

## Common Pitfalls

- Treating Karachi-specific figures as representative of all of Sindh, or vice versa.
- Confusing Sindh Bureau of Statistics figures with national PBS figures that may use different methodology or reference periods.
- Losing track of administrative boundary changes when comparing district data across years.
- Quoting a stock figure (count) as if it were a rate, or vice versa.

## Reference

- See [Sindh Development Statistics Reference](references/sindh-development-statistics.md) for chapter structure and indicator notes.
