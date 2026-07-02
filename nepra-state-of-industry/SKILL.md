---
name: nepra-state-of-industry
description: NEPRA State of Industry Report skill. Use when analyzing, summarizing, comparing, or extracting information from NEPRA's annual State of Industry Report, especially for realized (historical) power generation, transmission, distribution, and supply performance, as distinct from forward-looking capacity planning.
---

# NEPRA State of Industry Report

## Overview

Use this skill for Pakistan's power sector performance as reported in NEPRA's (National Electric Power Regulatory Authority) annual State of Industry (SOI) Report. This is the right skill for realized, historical generation, transmission, distribution, and financial performance of the power sector for a completed fiscal year — not for future capacity planning or a specific project's tariff.

## Coverage

- Published annually by NEPRA, covering the power sector's performance for the most recently completed fiscal year.
- Typical structure: generation mix and installed/dependable capacity actually operated during the year; transmission system performance and losses; distribution company (DISCO)-wise performance including transmission & distribution (T&D) losses and recovery/collection ratios; supply reliability metrics (e.g., SAIDI/SAIFI-style outage statistics where reported); sector financial performance including circular debt commentary; licensing and regulatory activity summary.
- Data is presented per DISCO/company and at the national aggregate level; both levels should be kept distinct.

## Use This Skill For

- extracting realized generation mix (fuel-wise share) for a specific fiscal year
- pulling DISCO-wise transmission & distribution (T&D) losses or recovery ratios
- comparing year-over-year power sector performance metrics
- extracting supply reliability or outage statistics for the sector or a specific DISCO
- summarizing circular debt or sector financial performance commentary from the SOI report

## When Not to Use This Skill

- For forward-looking, multi-year capacity expansion planning — use `igcep-capacity-plan` instead; SOI covers what actually happened, IGCEP covers what is planned.
- For the tariff awarded to a specific generation or distribution licensee — use `nepra-tariff-determinations` instead.
- For the Pakistan Economic Survey's narrative-level energy chapter — use `pes-infrastructure-digital-and-climate` instead.

## Routing Rules

- Use this skill for realized/historical power sector performance for a completed fiscal year. Use `igcep-capacity-plan` for forward-looking capacity planning scenarios.
- Use `nepra-tariff-determinations` when the question is about the specific tariff rate or decision awarded to a named licensee or project, rather than sector-wide performance.
- If the question only needs a high-level narrative summary of the energy sector rather than DISCO-level or fuel-mix-level detail, `pes-infrastructure-digital-and-climate` may be sufficient instead.

## Extraction Workflow

1. Identify the specific fiscal year the SOI report edition covers before extracting any figure.
2. Determine whether the question needs a national aggregate or DISCO-specific figure.
3. Locate the matching table: generation mix, T&D losses, recovery ratio, reliability metrics, or financial performance.
4. Preserve whether a capacity or generation figure is installed capacity, dependable capacity, or actual energy generated (these are distinct concepts).
5. When comparing across years, confirm both editions use the same DISCO boundaries, since distribution territories or company structures can change.

## Technical Rules

- Distinguish installed capacity (nameplate MW), dependable capacity, and actual energy generated (GWh) — these are not interchangeable.
- T&D losses and recovery/collection ratios are DISCO-specific and should not be averaged into a national figure without noting it is a weighted aggregate.
- Circular debt figures in the SOI report are a snapshot tied to the report's reference date; do not treat them as continuously updated.
- Keep realized (SOI) figures separate from planned/forecast (IGCEP) figures even when discussing the same fiscal year.

## Validation Checklist

- Confirm the fiscal year of the SOI edition being cited.
- Verify whether a capacity figure is installed, dependable, or actual generation.
- Check whether a performance metric is national-aggregate or DISCO-specific.
- Confirm DISCO structure/boundaries are consistent before comparing across report editions.

## Common Pitfalls

- Treating IGCEP's planned capacity figures as if they were SOI's realized figures, or vice versa.
- Averaging DISCO-wise T&D losses into a national figure without weighting or flagging the method.
- Confusing installed capacity with actual energy generated when citing a "capacity" figure.
- Citing circular debt as a real-time figure rather than a point-in-time snapshot from the report's reference date.

## Reference

- See [NEPRA State of Industry Reference](references/nepra-state-of-industry.md) for report structure and extraction notes.
