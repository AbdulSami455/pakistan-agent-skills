---
name: pbs-agriculture-census
description: PBS Agricultural and Livestock Census skill. Use when analyzing, summarizing, comparing, or extracting information from the Pakistan Bureau of Statistics (PBS) Integrated Agricultural Census or Livestock Census "Main Findings Report", especially for farm size distribution, land tenure, irrigation source, and livestock counts at a structural farm-unit level.
---

# PBS Agriculture Census

## Overview

Use this skill for questions about Pakistan's decennial Agricultural Census and Livestock Census, conducted by the Pakistan Bureau of Statistics (PBS). This is the right skill when the task needs structural, farm-unit-level detail — farm size, land tenure, irrigation source, livestock holdings — rather than an annual production or output figure.

## Coverage

- Conducted roughly once a decade by PBS (Agricultural Census Organization); the most recent rounds are published as "Main Findings Report" volumes for the Agricultural Census and, separately, the Livestock Census.
- Agricultural Census typically covers: number and area of farms by size class, land tenure type (owner, owner-cum-tenant, tenant), irrigation source (canal, tube well, well, other), cropping pattern at the holding level, farm machinery ownership, and use of agricultural credit/inputs, usually broken down by province and sometimes district.
- Livestock Census typically covers: livestock counts (cattle, buffalo, sheep, goats, poultry, etc.) by species, herd size distribution, and ownership patterns by province and district.
- Because this is a census (not a sample survey), figures are presented as full enumeration counts rather than survey estimates with margins of error.
- Publication is infrequent — only when a census round is conducted — so figures should always be dated to the specific census year/round.

## Use This Skill For

- extracting farm size distribution or average farm size by province
- pulling land tenure breakdowns (owner vs tenant vs owner-cum-tenant)
- extracting irrigation source statistics at the farm level
- pulling livestock counts by species, province, or district
- comparing structural agricultural characteristics across census rounds (e.g. 2010 vs prior rounds)

## Routing Rules

- Use this skill for farm-structure or livestock-headcount questions tied to a census round (decennial), not for annual crop output.
- For annual crop area/production/yield time series by crop, use `mnfsr-agri-statistics` instead — that report tracks year-to-year output, this census tracks farm structure at a point in time.
- For the annual macro-level agriculture narrative (sector growth, current-year performance), use `pes-real-sectors` (Chapter 2: Agriculture) instead.
- If a question asks about livestock production volumes (milk, meat) rather than headcounts, check whether the figure belongs to `pes-real-sectors` or `mnfsr-agri-statistics` annual series instead of this census.

## Extraction Workflow

1. Identify the census round/year the question refers to (census data is only as current as the last conducted round).
2. Determine whether the question is about the Agricultural Census (farm structure) or the Livestock Census (animal headcounts).
3. Locate the matching "Main Findings Report" table — farm size class tables, tenure tables, and irrigation-source tables are typically presented separately by province.
4. Preserve farm size class boundaries and tenure category labels exactly as defined in the census (these definitions can differ from colloquial usage).
5. For livestock, preserve species-level breakdowns; do not aggregate species into a single "livestock" count unless the source table does so.

## Technical Rules

- Do not treat census figures as annually updated; cite the specific census round/year for every figure.
- Farm size class boundaries (e.g. "under 1 hectare," "1 to <2.5 hectares") are census-specific definitions; preserve them exactly.
- Land tenure categories (owner, owner-cum-tenant, tenant) are mutually exclusive classifications in the census; do not blend them.
- Livestock counts are headcounts, not production volumes (milk, meat, eggs) — keep these conceptually separate.
- Province/district livestock and farm counts should be checked against the national total for consistency before being combined or compared.

## Validation Checklist

- Confirm the census round/year associated with the cited figure.
- Verify whether the question is about farm structure (Agricultural Census) or animal headcounts (Livestock Census).
- Check that farm size class or tenure category labels match the census's own definitions.
- Confirm whether a livestock figure is a headcount or a production volume before answering.

## Common Pitfalls

- Citing decade-old census figures as if they were current-year statistics.
- Confusing livestock headcounts with livestock production volumes (milk, meat).
- Blending farm size class boundaries from different census rounds, which may use different class definitions.
- Treating this structural census as a substitute for the annual crop-output series in `mnfsr-agri-statistics`.

## Reference

- See [Agriculture Census Reference](references/agriculture-census.md) for census structure and extraction notes.
