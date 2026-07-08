---
name: pakistan-river-basin-hydrology
description: Pakistan river basin hydrology skill. Use when analyzing, summarizing, comparing, or extracting information from Pakistan's river-flow, barrage, canal-withdrawal, and flood-forecasting bulletins, especially for basin-level hydrological conditions across the Indus system and its major tributaries.
---

# Pakistan River Basin Hydrology

## Overview

Use this skill for Pakistan's operational river-system hydrology: river discharges, barrage flows, canal withdrawals, basin conditions, and short-horizon flood forecasting across the Indus basin and its tributaries. This skill sits between weather and reservoir storage: it is the right skill when the question is about what is happening in the river network itself, not just rainfall at a station or storage in a single reservoir.

## Coverage

- IRSA daily operational hydrology tables covering river inflows, outflows, reservoir-linked flows, and canal head withdrawals.
- PMD Flood Forecasting Division bulletins for riverine flood outlooks and basin-specific forecast warnings.
- WAPDA or water-sector operational summaries where river flows, barrage releases, or canal commands are tabulated by site.
- Basin geography and hydrological routing across the Indus main stem and major tributaries: Jhelum, Chenab, Ravi, Sutlej, and Kabul rivers.
- Seasonal low-flow and flood-season conditions where the question requires operational river context rather than policy narrative.

## Use This Skill For

- extracting discharge or flow figures for a named river, barrage, or control point
- comparing flows across tributaries or barrages on a given date or over a short period
- interpreting whether a basin segment is in high-flow, low-flow, or rising/falling condition
- identifying canal withdrawals relative to upstream releases
- sourcing basin-level flood warnings or river routing context from official operational bulletins

## When Not to Use This Skill

- For station rainfall, temperature, or seasonal weather outlooks, use `pmd-weather-climate-data` instead.
- For reservoir-specific storage, levels, and live-storage thresholds at Tarbela, Mangla, or Chashma, use `irsa-reservoir-data` instead.
- For disaster-impact figures such as deaths, evacuations, damaged houses, or relief camps, use `ndma-flood-sitreps` instead.
- For long-term climate-policy narrative or infrastructure investment discussion, use `pes-infrastructure-digital-and-climate` instead.

## Routing Rules

- Use this skill when the unit of analysis is the river system, barrage network, or canal command rather than a weather station or a single reservoir.
- If the question asks what caused the hydrological condition, pair this skill with `pmd-weather-climate-data` for rainfall drivers and keep the meteorological and hydrological layers distinct.
- If the question asks how much water is stored rather than how much is flowing through the system, route to `irsa-reservoir-data`.
- If the question concerns flood response rather than flood hydrology, route to `ndma-flood-sitreps`.

## Extraction Workflow

1. Identify the river, barrage, canal head, or basin reach named in the question.
2. Confirm the reporting date and whether the figure is observed, operationally reported, or forecast.
3. Preserve the variable type exactly: inflow, outflow, discharge, release, withdrawal, or forecast peak.
4. Note the unit, which is typically cusecs for discharge and withdrawal.
5. If comparing multiple sites, preserve upstream/downstream ordering rather than treating locations as interchangeable.

## Technical Rules

- Do not conflate reservoir outflow with downstream barrage discharge or canal withdrawal; these are related but distinct control points.
- River-flow values are operational snapshots or daily totals, not seasonal climatology; do not generalize a single reading into a long-term trend without additional dates.
- Tributary names and control points matter: a high Chenab flow does not imply the same condition on the Ravi or Sutlej.
- Flood forecasts are forward-looking and probabilistic in practice; do not present a warning bulletin as realized flow unless the bulletin itself reports observations.
- Canal withdrawals are water diversions from the river system and should not be added to river discharge as if they are independent flow sources.

## Validation Checklist

- Confirm the site name and whether it is a river gauge, barrage, reservoir outlet, or canal head.
- Verify the date and whether the value is observed or forecast.
- Check the unit before quoting.
- For comparisons, confirm the same reporting time basis is used across sites.

## Common Pitfalls

- Mixing river discharge with reservoir storage or weather-station rainfall.
- Treating a flood forecast warning as an observed flood peak.
- Comparing two sites without preserving their upstream/downstream relationship.
- Confusing canal withdrawal data with river discharge itself.

## Reference

- See [Pakistan River Basin Hydrology Reference](references/pakistan-river-basin-hydrology.md) for source structure, basin components, and extraction notes.
