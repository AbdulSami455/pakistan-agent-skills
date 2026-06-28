---
name: i2i-startup-ecosystem-report
description: Invest2Innovate Pakistan Startup Ecosystem Report skill. Use when analyzing, summarizing, comparing, or extracting information from Invest2Innovate's periodic "Pakistan Startup Ecosystem Report," especially for startup funding trends, sector breakdown of funded companies, and ecosystem player mapping (investors, accelerators, incubators) across report editions.
---

# I2I Startup Ecosystem Report

## Overview

Use this skill for Pakistan's startup ecosystem statistics and qualitative mapping drawn from Invest2Innovate's (I2I) "Pakistan Startup Ecosystem Report." This is the right skill for funding trends, sector breakdowns, and ecosystem-player landscape (investors, accelerators, incubators) as reported periodically by I2I, distinct from SBP's macro-level IT/ICT export analysis or PES's digital economy chapter.

## Coverage

- Published periodically by Invest2Innovate (i2i.pk), roughly every two to three years (editions have appeared around 2014, 2016, 2019, 2021, and 2024); always confirm the specific edition and its reference period before extracting a figure.
- Typical structure: ecosystem overview and methodology; funding trend statistics (total deals, total disclosed funding value, year-over-year trend) usually drawing on secondary sources such as Crunchbase/Tracxn/Data Darbar in addition to I2I's own survey; sector breakdown of funded startups (e.g., fintech, e-commerce, logistics, healthtech, edtech); stage breakdown (seed, pre-seed, Series A and beyond); ecosystem-player directory (active VCs, angel networks, accelerators, incubators, government and donor-supported programs); qualitative commentary on regulatory environment, talent pipeline, and ecosystem challenges; sometimes city-level breakdown (Karachi, Lahore, Islamabad concentration).
- Document is structure-based with data visualizations and narrative sections; exact chapter order and page layout vary significantly by edition since multi-year gaps allow major format changes.

## Use This Skill For

- extracting total startup funding figures or deal counts for a specific report edition's reference period
- identifying sector-wise or stage-wise breakdown of startup funding in Pakistan
- mapping active ecosystem players (VCs, accelerators, incubators) as captured by a specific edition
- comparing ecosystem trends across two different I2I report editions (e.g., 2019 vs. 2021 vs. 2024)
- sourcing qualitative commentary on Pakistan's startup regulatory or talent environment

## Routing Rules

- Use this skill for I2I's startup-ecosystem-specific framing. Use `sbp-ict-exports-special-section` for SBP's macro analysis of IT/ICT export trends, which is about export earnings rather than venture funding or ecosystem mapping.
- Use `pes-infrastructure-digital-and-climate` only for the Pakistan Economic Survey's brief digital-economy or IT-sector narrative; PES does not carry I2I's startup-funding or ecosystem-player granularity.
- Do not treat I2I's periodic snapshot as a continuous time series; gaps between editions (sometimes 2-3 years) mean intervening-year trends are not directly observable from this source.

## Extraction Workflow

1. Identify the specific report edition (by year) before extracting any figure, since methodology and data sources can shift between editions.
2. Identify whether a funding figure is "disclosed funding" (publicly reported deal values) versus an estimate, since many deals do not disclose value.
3. Preserve sector and stage breakdowns separately; do not merge them into a single category.
4. Note the reference period each edition covers, since it is usually the multi-year window since the prior edition, not just the publication year.
5. Distinguish I2I's own primary survey findings from secondary-source aggregation (e.g., Crunchbase-derived statistics) if the report differentiates them.

## Technical Rules

- Funding totals are typically in USD; preserve currency and confirm whether a figure is cumulative or single-year.
- "Number of deals" and "total disclosed value" are separate metrics; a high deal count does not imply high disclosed value, since many seed-stage deals are undisclosed.
- Ecosystem-player lists (accelerators, incubators, VCs) are a snapshot as of the report's research period; do not present them as current beyond that period without verification.
- Sector taxonomies may differ slightly between editions (e.g., "fintech" scope); do not assume identical category boundaries across editions when comparing trends.

## Validation Checklist

- Confirm the report edition (year) before quoting any funding or ecosystem figure.
- Verify whether a funding figure is disclosed-value-based or includes estimates for undisclosed deals.
- Check whether sector/stage categories match across editions before computing a trend.
- Confirm the reference period (which years of activity) the edition actually covers.

## Common Pitfalls

- Treating the report's publication year as the funding reference year; the data window is often the preceding one to three years.
- Comparing deal counts across editions without checking for changes in data-source methodology.
- Citing an ecosystem-player list as exhaustive or as currently accurate beyond the report's research period.
- Confusing this report's venture-funding focus with SBP's export-earnings-focused IT/ICT analysis.

## Reference

- See [I2I Startup Ecosystem Reference](references/i2i-startup-ecosystem-report.md) for edition tracking and category notes.
