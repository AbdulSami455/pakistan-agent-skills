---
name: pakistan-protected-areas-biodiversity
description: Pakistan protected areas and biodiversity skill. Use when analyzing, summarizing, comparing, or extracting information from official protected-area, wetland, wildlife, and biodiversity references in Pakistan, especially for national parks, wildlife sanctuaries, game reserves, Ramsar sites, and species-conservation context.
---

# Pakistan Protected Areas and Biodiversity

## Overview

Use this skill for Pakistan's protected-area system and biodiversity references: national parks, wildlife sanctuaries, game reserves, wetlands, Ramsar sites, and officially framed species-conservation context. This is the right skill when the task is about conservation status and ecological designation, not tourism promotion or general geography.

## Coverage

- Federal and provincial wildlife and environment department lists of protected areas.
- Ramsar Convention wetland listings for Pakistani sites.
- Official biodiversity strategy or conservation-plan material where habitat and species priorities are described.
- Protected-area attributes such as designation type, province, managing authority, and broad ecological significance.
- Official species-conservation references where tied to protected-area management or biodiversity planning.

## Use This Skill For

- identifying whether a site is a national park, wildlife sanctuary, game reserve, or wetland of international importance
- comparing protected-area types across provinces
- sourcing the official authority or jurisdiction responsible for a protected area
- summarizing biodiversity or habitat importance attached to a protected landscape
- distinguishing conservation designation from general travel popularity

## When Not to Use This Skill

- For tourist-destination descriptions or visitor orientation, use `pakistan-tourism-heritage` instead.
- For UNESCO cultural-heritage inscription status, use `pakistan-unesco-heritage-sites` instead.
- For forest-cover or land-cover change metrics, use `pakistan-forests-land-cover` instead.

## Routing Rules

- Use this skill when the main question is about conservation status, designation, habitat, or species-management context.
- If the question is "can I visit this place" or "what are the attractions," route to `pakistan-tourism-heritage`.
- If the site is a wetland with both conservation and hydrology relevance, use this skill for designation status and `pakistan-river-basin-hydrology` or `pmd-weather-climate-data` for water conditions.
- Keep Ramsar status distinct from national protected-area categories; a site can be both, but the labels are not interchangeable.

## Extraction Workflow

1. Identify the site and determine whether it is terrestrial, wetland, marine/coastal, or mixed.
2. Confirm the designation type and the responsible authority.
3. Preserve province or territory location exactly.
4. If species context is requested, preserve whether the source is describing habitat, flagship species, or legal protection status.
5. Separate broad biodiversity narrative from formal legal designation.

## Technical Rules

- National park, wildlife sanctuary, and game reserve are distinct administrative categories; do not collapse them into a generic "park" label.
- Ramsar designation is an international wetland-status label, not a substitute for local legal category.
- Species presence in a protected area is not the same as species abundance or trend; do not infer population strength unless the source says so.
- Protected-area jurisdiction is often provincial; do not assume a federal authority manages every site.

## Validation Checklist

- Confirm the designation type and province/territory.
- Verify whether the source is an official protected-area list, a biodiversity strategy, or a species-specific note.
- Check whether the site also has Ramsar or another international status and label it separately.
- Confirm that conservation status is not being confused with tourism branding.

## Common Pitfalls

- Treating all protected sites as national parks.
- Confusing Ramsar status with UNESCO status.
- Using tourism descriptions as if they were formal conservation records.
- Inferring species population trends from a simple species-presence mention.

## Reference

- See [Pakistan Protected Areas and Biodiversity Reference](references/pakistan-protected-areas-biodiversity.md) for source structure and designation notes.
