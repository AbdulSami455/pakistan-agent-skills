---
name: parc-agri-extension
description: PARC (Pakistan Agricultural Research Council) skill. Use when explaining Pakistan's agricultural research infrastructure, crop/livestock research programs, or farmer extension and technology-transfer services, as distinct from annual crop production statistics or the decennial agriculture census.
---

# PARC Agricultural Research & Extension

## Overview

Use this skill for the Pakistan Agricultural Research Council (PARC), the apex national agricultural research organization, and its role in research, capacity building, and technology transfer to farmers. This is an institutional/research-structure reference skill — not a crop-statistics source (use `mnfsr-agri-statistics` or `pbs-agriculture-census` for that) and not a live extension-advisory service.

## Coverage

- PARC's mandate: apex-level coordination of agricultural research at the national level, working alongside provincial agricultural research institutes, agricultural universities, and provincial agriculture/livestock/forestry departments.
- Divisions: PARC is organized into technical divisions (Plant Sciences, Animal Sciences, Social Sciences, Natural Resources, Agricultural Engineering) and services divisions (Finance, Coordination & Monitoring), each covering a distinct research/support function.
- Governance: PARC's Board of Governors includes provincial Secretaries of Agriculture/Livestock/Forestry Departments and Vice Chancellors of agricultural universities alongside farmer representation, reflecting its coordinating (not sole-implementer) role across the national agricultural research system.
- Extension and technology transfer: PARC supports farmer capacity building through training and workshops, and facilitates transfer of research findings/technologies to the farming community — this extension function is distinct from PARC's own research-generation function.
- Related programs: PARC has been associated with specific technology-transfer or agricultural-linkage initiatives (e.g., programs connecting research output to farmer-level application) alongside its core research divisions.

## Use This Skill For

- explaining PARC's role as the apex national agricultural research coordinating body
- describing PARC's technical division structure (plant sciences, animal sciences, natural resources, etc.)
- explaining the general concept of agricultural extension/technology transfer to farmers and PARC's role in it
- clarifying PARC's relationship to provincial agricultural research institutes and universities
- distinguishing PARC's research/extension mandate from crop-production statistics reporting

## When Not to Use This Skill

- For annual crop area/production/yield statistics — use `mnfsr-agri-statistics` instead; PARC conducts and coordinates research, it is not the primary statistical-reporting body for annual crop output.
- For decennial farm-structure or livestock-headcount census data — use `pbs-agriculture-census` instead.
- For the Pakistan Economic Survey's agriculture-sector narrative — use `pes-real-sectors` instead.
- For a specific, current farmer-advisory service's live operational details — this skill provides institutional/structural background, not a live agricultural-extension helpdesk.

## Routing Rules

- Use this skill for PARC's research-coordination structure, technical divisions, and general extension/technology-transfer role.
- If the question needs annual crop output statistics rather than research-institution structure, route to `mnfsr-agri-statistics`.
- If the question needs census-round farm-structure or livestock-headcount data, route to `pbs-agriculture-census`.
- If the question needs the Economic Survey's high-level agriculture narrative, route to `pes-real-sectors`.

## Extraction Workflow

1. Identify whether the question concerns PARC's own research-coordination role, a specific technical division's focus area, or its extension/technology-transfer function to farmers.
2. If the question involves a specific research finding or crop-technology recommendation, note that PARC coordinates/conducts research but confirm whether the specific claim needs verification against PARC's current published research rather than treated as generally asserted fact.
3. Clarify PARC's coordinating role relative to provincial research institutes and universities — PARC is not necessarily the sole or exclusive implementer of agricultural research nationally.
4. If the question is really about production statistics or census data rather than research/extension structure, redirect to the appropriate statistics skill.

## Technical Rules

- Keep PARC's research/extension-coordination role distinct from crop-production statistics reporting (a different institutional function covered by other skills).
- PARC's Board of Governors structure reflects a coordinating role across federal and provincial agricultural institutions, not sole federal control over all agricultural research in Pakistan.
- Extension/technology-transfer (getting research findings to farmers) is a distinct function from research generation itself; do not conflate the two when describing PARC's activities.

## Validation Checklist

- Confirm whether the question needs PARC's institutional/research structure or actual crop/livestock statistics, and route accordingly.
- Verify PARC's coordinating (not exclusive) role relative to provincial research institutes and universities is accurately represented.
- Check that extension/technology-transfer activities are not conflated with PARC's core research-generation function.

## Common Pitfalls

- Treating PARC as the source for annual crop-production statistics rather than `mnfsr-agri-statistics`.
- Treating PARC as the source for census-round farm-structure data rather than `pbs-agriculture-census`.
- Describing PARC as the sole implementer of Pakistani agricultural research rather than an apex coordinating body working with provincial institutes and universities.
- Conflating PARC's extension/technology-transfer function with its core research-generation function.

## Reference

- See [PARC Reference](references/parc-agri-extension.md) for organizational structure and extraction notes.
