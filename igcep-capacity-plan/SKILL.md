---
name: igcep-capacity-plan
description: IGCEP (Indicative Generation Capacity Expansion Plan) skill. Use when analyzing, summarizing, comparing, or extracting information from NTDC/NPCC's Indicative Generation Capacity Expansion Plan, especially for long-term generation capacity addition forecasts, planning assumptions, demand projections, and least-cost generation mix scenarios across different planning horizons.
---

# IGCEP Capacity Plan

## Overview

Use this skill for questions about Pakistan's long-term generation capacity expansion planning, drawn from the Indicative Generation Capacity Expansion Plan (IGCEP) prepared by NTDC/NPCC (National Transmission and Despatch Company / National Power Control Centre) and reviewed/approved by NEPRA. This is the right skill when the task is about planned or forecast future capacity additions and planning assumptions, not realized historical generation or a single licensee's tariff.

## Coverage

- Multiple editions exist, each covering a rolling ~10-year planning horizon (e.g., IGCEP 2021-30, 2022-31, 2024-34); always identify which edition and horizon is in scope.
- Typical structure: demand forecast methodology and load growth assumptions; existing and committed generation capacity inventory; least-cost capacity expansion plan under multiple scenarios (e.g., with/without imported coal, with/without specific hydel or renewable projects); transmission system requirements implied by the plan; fuel mix and indicative tariff/cost assumptions for candidate projects; sensitivity analysis on demand, fuel price, or hydrology assumptions.
- Document is structure-based (chapters/annexes with planning tables and scenario charts), not fixed-page across editions; each edition resets numbering.

## Use This Skill For

- extracting planned capacity additions by year, technology, or project
- comparing planning assumptions or scenarios across IGCEP editions
- summarizing demand growth forecasts underlying the expansion plan
- identifying which power projects are designated "committed" versus "candidate" in a given plan
- describing the least-cost generation mix recommended for a future horizon

## Routing Rules

- Use this skill for forward-looking, multi-year capacity planning. Use `nepra-state-of-industry` for realized, historical capacity and generation performance.
- Use `nepra-tariff-determinations` for the actual tariff awarded to a specific project once it reaches a determination stage; IGCEP only carries indicative/assumed cost inputs for planning purposes.
- Use `pes-infrastructure-digital-and-climate` only for the Pakistan Economic Survey's narrative-level energy chapter; IGCEP carries the underlying technical planning detail PES does not.

## Extraction Workflow

1. Identify the IGCEP edition and its stated planning horizon (e.g., 2024-34) before extracting any figure.
2. Distinguish "existing," "committed," and "candidate" capacity categories; do not merge them into a single capacity total without labeling.
3. Identify which demand or fuel-price scenario a figure belongs to if the plan presents multiple scenarios.
4. Preserve project-level detail (name, technology, MW, expected commissioning year) rather than only headline totals.
5. Note whether figures are nameplate MW or net/dependable MW.

## Technical Rules

- Do not conflate one IGCEP edition's forecast with another edition's revised forecast; editions are sequential updates, not cumulative additions.
- Scenario labels (base case, low demand, high demand, optimized least-cost) must be preserved exactly when quoting a projection.
- Candidate project lists are planning recommendations, not guaranteed builds; do not present them as committed capacity.
- Keep transmission-system implications separate from generation capacity figures.

## Validation Checklist

- Confirm which IGCEP edition and horizon a figure is drawn from.
- Verify whether a capacity figure is existing, committed, or candidate.
- Check which demand/scenario case the figure belongs to.
- Confirm nameplate versus net/dependable capacity basis before quoting MW figures.

## Common Pitfalls

- Treating candidate or indicative projects as confirmed future capacity.
- Mixing figures from two different IGCEP editions as if they were one continuous series.
- Quoting a least-cost scenario figure as the only or final plan when multiple scenarios are presented.
- Losing track of which planning horizon (start and end year) a chart or table covers.

## Reference

- See [IGCEP Reference](references/igcep-capacity-plan.md) for edition tracking and planning-category definitions.
