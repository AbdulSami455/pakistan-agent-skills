---
name: pakistan-geology-mineral-resources
description: Pakistan geology and mineral resources skill. Use when analyzing, summarizing, comparing, or extracting information from Geological Survey of Pakistan and official mineral-sector references, especially for formations, resource occurrences, province-wise mineral deposits, and geology-linked mining context.
---

# Pakistan Geology and Mineral Resources

## Overview

Use this skill for Pakistan's geology and official mineral-resource references: formations, basins, ore occurrences, resource belts, and province-wise mineral descriptions. This is the right skill when the task needs earth-science or mineral-resource context rather than macro mining output, tourism geography, or company-level mining news.

## Coverage

- Geological Survey of Pakistan publications, maps, and summaries.
- Federal and provincial mines and minerals department reference material where official resource occurrence lists or licensing context are described.
- Stratigraphic and basin-level context relevant to resources such as coal, copper, gold, salt, gypsum, limestone, chromite, iron ore, marble, and precious stones.
- Province- and district-linked mineral occurrence references where officially listed.
- Geological context for sedimentary basins, tectonic belts, and extractive-resource zones.

## Use This Skill For

- identifying where a mineral occurs in Pakistan according to official references
- summarizing a geological belt or basin associated with a resource
- distinguishing geology/resource occurrence from actual annual production statistics
- mapping mineral types to provinces or named districts
- extracting formation or stratigraphic names from official geology references

## When Not to Use This Skill

- For annual mining-output figures in a macroeconomic report, use `pes-real-sectors` instead.
- For earthquake and tectonic hazard reporting, use `pakistan-earthquake-seismic-hazard` instead.
- For tourism-oriented mountain or cave descriptions, use `pakistan-tourism-heritage` instead.
- For company listings, stock-market exposure, or project finance, use the relevant corporate or PSX skill instead.

## Routing Rules

- Use this skill when the task is geological or resource-occurrence oriented.
- If the user asks "how much was produced" or "what was the sector growth rate," route to `pes-real-sectors`.
- If the task concerns legal licensing or project approvals, this skill may provide background geology but should not be used as the licensing authority of record.
- Keep geology narrative distinct from mining-company or market claims.

## Extraction Workflow

1. Identify the mineral, formation, basin, or geological belt in the question.
2. Confirm whether the source is describing an occurrence, a reserve/resource statement, a stratigraphic unit, or a production narrative.
3. Preserve the geography exactly: province, district, basin, or belt.
4. Keep lithology, stratigraphy, and mineral-resource terms distinct from one another.
5. If multiple sources are involved, separate federal geology references from provincial mining-department material.

## Technical Rules

- A resource occurrence or prospect is not the same as active production.
- Geological formations and administrative districts are different indexing systems; preserve both when the source provides both.
- Reserve and resource terminology may be used inconsistently outside formal technical reporting; do not upgrade an occurrence note into a proven reserve claim.
- Some mineral belts cross provincial boundaries; do not force them into a single-province interpretation if the source does not.
- Keep ornamental stone categories such as marble and granite distinct from metallic minerals and industrial minerals.

## Validation Checklist

- Confirm whether the source is geological, production-related, or licensing-related.
- Verify the mineral name and province/district association.
- Check whether the statement is about occurrence, reserve/resource, or extraction.
- Preserve formal formation/basin names exactly as written.

## Common Pitfalls

- Treating an occurrence map as proof of commercial extraction.
- Mixing geological formations with current administrative units without labeling both.
- Conflating macro mining output with geology-source descriptions.
- Repeating informal reserve claims as official geological fact.

## Reference

- See [Pakistan Geology and Mineral Resources Reference](references/pakistan-geology-mineral-resources.md) for source structure and extraction notes.
