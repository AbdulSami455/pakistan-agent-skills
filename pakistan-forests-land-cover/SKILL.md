---
name: pakistan-forests-land-cover
description: Pakistan forests and land-cover skill. Use when analyzing, summarizing, comparing, or extracting information from official forestry, rangeland, mangrove, afforestation, and land-cover references in Pakistan, especially for forest extent, land-use change, and province-wise ecological management context.
---

# Pakistan Forests and Land Cover

## Overview

Use this skill for Pakistan's forest and land-cover references: forest extent, mangroves, plantations, afforestation programs, rangelands, and official land-use or vegetation summaries. This is the right skill when the question is about ecological cover and land management rather than protected-area designation or climate narrative alone.

## Coverage

- Provincial forest-department publications and official forestry summaries.
- Federal or intergovernmental reports on forest cover, land degradation, watershed forestry, and mangrove management.
- Official plantation and afforestation program summaries where area, survival, or management context is reported.
- Land-cover and vegetation summaries published through official Pakistan government or officially adopted technical programs.
- Forestry-linked ecological topics such as scrub forest, conifer forest, riverine forest, irrigated plantations, mangroves, and rangelands.

## Use This Skill For

- extracting forest-area or mangrove-area figures from official sources
- comparing forestry or plantation indicators across provinces or over time
- identifying forest-type distribution or land-cover categories
- summarizing afforestation or watershed-forestry program context
- separating land-cover statistics from protected-area designation

## When Not to Use This Skill

- For protected-area legal status or wildlife-management designation, use `pakistan-protected-areas-biodiversity` instead.
- For rainfall, drought, or climate normals, use `pmd-weather-climate-data` instead.
- For broader climate-policy narrative in the annual economic survey, use `pes-infrastructure-digital-and-climate` instead.

## Routing Rules

- Use this skill when the core question is how much ecological cover exists, what type it is, and how it changed or is managed.
- If the user asks whether a place is legally protected, route to `pakistan-protected-areas-biodiversity`.
- If the question is about agricultural land-use suitability rather than forestry cover, route to `pakistan-agro-climatic-zones`.
- Keep plantation-program claims separate from system-wide forest-cover estimates.

## Extraction Workflow

1. Identify whether the source is about forest cover, land cover, plantations, mangroves, or rangelands.
2. Confirm the geography and whether the figure is national, provincial, or site-specific.
3. Preserve the unit exactly, typically hectares, acres, or percent cover.
4. Note whether the figure is mapped/estimated cover, planted area, surviving plantation area, or administrative target.
5. If comparing years, confirm the method or source edition is consistent.

## Technical Rules

- Forest cover, tree cover, and plantation area are not interchangeable.
- Mangrove figures often refer to a specific coastal zone and should not be generalized to national forestry conditions.
- Administrative targets for planting are not the same as verified planted area or survival rates.
- Land-cover products may use remote-sensing classifications that differ from administrative forestry categories; preserve the source framing.

## Validation Checklist

- Confirm the type of area measure being cited: natural forest, plantation, tree cover, or total land cover.
- Verify the geography and reporting year.
- Check whether the source reports observed/estimated cover or only program targets.
- Confirm the unit before quoting.

## Common Pitfalls

- Treating plantation targets as realized forest cover.
- Blending mangrove area with inland forest statistics without labeling the distinction.
- Assuming two editions are directly comparable when classification methods changed.
- Confusing protected areas with forests; some forests are protected, but not every protected area is forested.

## Reference

- See [Pakistan Forests and Land Cover Reference](references/pakistan-forests-land-cover.md) for source structure and extraction notes.
