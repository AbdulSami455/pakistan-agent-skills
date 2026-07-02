---
name: pes-real-sectors
description: Pakistan Economic Survey real sectors skill. Use when analyzing, summarizing, comparing, or extracting information from the Pakistan Economic Survey on agriculture, manufacturing, and mining, especially for crop output, industrial production, sector performance, and real-economy drivers.
---

# PES Real Sectors

## Overview

Use this skill for Pakistan Economic Survey questions about the real economy, especially agriculture, manufacturing, and mining. This is the right skill when the task is about crops, output changes, production groups, industrial recovery, or sector-specific real activity.

## Chapter Coverage

- Chapter 2: Agriculture: starts at survey page `21`
- Chapter 3: Manufacturing and Mining: starts at survey page `43`

## Use This Skill For

- extracting production or area figures for crops
- summarizing agriculture performance and crop-specific outcomes
- analyzing large-scale manufacturing trends
- comparing manufacturing groups or industrial subsectors
- extracting mining or industrial production indicators

## Routing Rules

- Use Chapter 2 for crops, edible oil, agricultural production, and farm-sector discussion.
- Use Chapter 3 for large-scale manufacturing, industrial groups, mining, and production contributions.
- If a question spans real-sector growth and macro headline GDP, use this skill for the underlying sector detail and the macro skill for topline framing.

## Extraction Workflow

1. Identify whether the question is about agriculture or industrial activity.
2. Find the table or paragraph with the relevant commodity, sector, or production group.
3. Preserve table units exactly, such as `000 hectares`, `000 tonnes`, `000 acres`, or percentage change.
4. Keep provisional markers such as `(P)` in the answer when relevant.
5. If comparing two years, ensure both values come from the same table and unit basis.

## Technical Rules

- Crop tables can switch units across sections; do not assume hectares, acres, and tonnes are interchangeable.
- Separate area changes from production changes.
- Preserve sign and direction of percentage changes exactly.
- In manufacturing tables, keep group-level weights distinct from growth rates and contribution points.
- Do not generalize one crop or one manufacturing group into a whole-sector conclusion unless the chapter does so.

## Validation Checklist

- Confirm the unit before quoting a crop figure.
- Check whether the figure is actual, target, estimate, or provisional.
- For manufacturing, verify whether the question is asking for growth, weight, or point contribution.
- Make sure a positive group outcome is not offset by other groups before making a broad statement.

## Common Pitfalls

- Mixing crop area with crop output.
- Missing provisional tags in agricultural tables.
- Confusing manufacturing growth percentages with weighted contribution values.
- Using one industrial group to describe the full manufacturing trend without support.

## Reference

- See [Real Sectors Reference](references/real-sectors.md) for chapter routing, unit discipline, and table-handling notes.
