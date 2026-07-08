---
name: pakistan-agro-climatic-zones
description: Pakistan agro-climatic zones skill. Use when analyzing, summarizing, comparing, or extracting information from official agro-ecological, crop-zoning, and farming-calendar references in Pakistan, especially for crop suitability, seasonal calendars, and region-specific agricultural-climate context.
---

# Pakistan Agro-Climatic Zones

## Overview

Use this skill for Pakistan's agro-climatic and agro-ecological zoning references: crop suitability, sowing and harvest windows, rainfall-temperature farming context, and regional agricultural calendars. This is the right skill when the task links geography and climate to agricultural decision-making rather than asking for macro crop output.

## Coverage

- Pakistan Agricultural Research Council and related official agronomy references.
- Provincial agriculture-extension materials describing crop calendars and zone-specific recommendations.
- Official agro-ecological or agro-climatic zone frameworks for Pakistan.
- Crop-wise suitability or cropping-pattern references linked to geography, altitude, irrigation, or rainfall regime.
- Regional distinctions across irrigated plains, arid zones, mountain valleys, barani areas, and coastal belts.

## Use This Skill For

- identifying which crops are suited to a region or zone
- extracting sowing and harvesting windows from official calendars
- comparing agro-climatic conditions across regions
- framing how irrigation, rainfall, altitude, or temperature shape cropping patterns
- distinguishing agronomic suitability from actual production outcomes

## When Not to Use This Skill

- For actual crop production figures, use `pes-real-sectors` or `mnfsr-agri-statistics` instead.
- For station-level weather observations or rainfall totals, use `pmd-weather-climate-data` instead.
- For forest and rangeland cover, use `pakistan-forests-land-cover` instead.

## Routing Rules

- Use this skill when the question is about "where a crop fits" or "when it is grown," not how much was harvested nationally.
- If the task needs both suitability and output, use this skill for zone logic and `pes-real-sectors` or `mnfsr-agri-statistics` for production figures.
- If the source is a local agronomy advisory, keep it distinct from national agro-ecological zoning language.
- Distinguish irrigated and rainfed/barani recommendations whenever the source does.

## Extraction Workflow

1. Identify the crop, region, or agro-climatic zone requested.
2. Confirm whether the source is giving crop-suitability guidance, a crop calendar, or a broader zone classification.
3. Preserve the seasonal window exactly: Kharif, Rabi, sowing period, harvest period, or multi-crop sequence.
4. Note the controlling condition where provided: irrigation, altitude, rainfall, salinity, temperature, or soil type.
5. If multiple regions are compared, keep province and agro-ecological setting distinct.

## Technical Rules

- Suitability guidance is not the same as realized crop output.
- Kharif and Rabi timing varies by crop and region; do not flatten them into one national calendar.
- Barani, canal-irrigated, and high-altitude systems follow different agronomic logic; preserve the distinction.
- Soil or salinity constraints should not be dropped when the source attaches them to a crop recommendation.

## Validation Checklist

- Confirm the crop and regional scope.
- Verify whether the statement is a calendar, suitability note, or zone-classification rule.
- Check whether irrigation status matters to the recommendation.
- Preserve seasonal labels exactly.

## Common Pitfalls

- Treating a crop's presence in a region as proof that it is climatically optimal there.
- Using national production tables as if they were agronomic zoning references.
- Ignoring irrigation differences when quoting suitability.
- Generalizing one province's crop calendar to the whole country.

## Reference

- See [Pakistan Agro-Climatic Zones Reference](references/pakistan-agro-climatic-zones.md) for source structure and extraction notes.
