---
name: mnfsr-agri-statistics
description: MNFSR (Ministry of National Food Security & Research) agriculture statistics skill. Use when analyzing, summarizing, comparing, or extracting information from Pakistan's annual crop area, production, and yield statistics for major and minor crops, especially year-over-year output trends distinct from the decennial Agricultural Census.
---

# MNFSR Agriculture Statistics

## Overview

Use this skill for Pakistan's annual crop-level agricultural output data — area sown, production, and yield — compiled through the Ministry of National Food Security & Research (MNFSR) and provincial crop reporting systems. This is the right skill for a specific crop's year-to-year performance, not for farm-structure census data or the Pakistan Economic Survey's summarized agriculture narrative.

## Coverage

- Annual (crop-season) statistics for major crops (wheat, cotton, rice, sugarcane, maize) and minor crops, reported as area sown (hectares), production (tonnes), and yield (kg/hectare or maund/acre depending on the table).
- Data is compiled from provincial crop reporting/estimation systems and consolidated at the federal level by MNFSR, typically by Kharif and Rabi season.
- Livestock and fisheries production volumes (milk, meat, eggs, fish catch) are also compiled under MNFSR's broader food security mandate, distinct from the Livestock Census headcounts.
- Figures are typically presented as provisional estimates during the season, followed by final figures once harvest data is consolidated.

## Use This Skill For

- extracting a specific crop's area sown, production, or yield for a given crop year/season
- comparing year-over-year crop output trends for wheat, cotton, rice, sugarcane, or other major crops
- pulling province-wise crop area/production breakdowns
- extracting livestock or fisheries production volumes (milk, meat, fish catch) rather than headcounts
- distinguishing Kharif-season from Rabi-season crop statistics

## When Not to Use This Skill

- For farm-structure data (farm size, land tenure, irrigation source) or livestock headcounts from the decennial census — use `pbs-agriculture-census` instead; that census captures structure at a point in time, this skill tracks annual output.
- For the Pakistan Economic Survey's summarized agriculture-sector growth narrative — use `pes-real-sectors` (Chapter 2: Agriculture) instead, which cites headline figures from this same underlying data but does not carry crop-by-crop or province-wise detail.
- For agricultural credit, price support, or input-subsidy policy rather than output statistics.

## Routing Rules

- Use this skill for annual crop area/production/yield time series by crop, not for census-round farm-structure data — see `pbs-agriculture-census` for the latter.
- Use `pes-real-sectors` when only a high-level agriculture-sector growth figure is needed rather than crop-by-crop or province-wise detail.
- If a livestock or fisheries question is about production volume (milk, meat, fish catch) rather than animal headcount, this skill is the correct source; for headcounts, use `pbs-agriculture-census`.

## Extraction Workflow

1. Identify the specific crop and crop year/season (Kharif or Rabi) needed.
2. Confirm whether the figure required is area sown, production, or yield — these are related but distinct measures.
3. Locate the matching provincial or national table, noting whether the release is provisional or final.
4. Preserve the unit exactly as reported (hectares vs. acres for area; tonnes vs. maunds for production; kg/hectare vs. maund/acre for yield) since provincial and federal tables sometimes use different conventions.
5. When comparing across years, confirm both years use consistent units and whether either figure is still provisional.

## Technical Rules

- Area, production, and yield are three distinct figures; yield is derived (production/area) and should not be assumed constant when only one of the other two changes.
- Kharif and Rabi season crops are distinct groupings (e.g., cotton and rice are Kharif; wheat is Rabi); do not sum across seasons without labeling a combined "crop year" total explicitly.
- Provisional estimates issued during a growing season can differ materially from final post-harvest figures; always note whether a cited figure is provisional or final.
- Livestock/fisheries production volumes (this skill) are conceptually distinct from livestock headcounts (`pbs-agriculture-census`); do not conflate the two when discussing "livestock statistics."

## Validation Checklist

- Confirm the crop, crop year, and season (Kharif/Rabi) for any cited figure.
- Verify whether the figure is area, production, or yield.
- Check whether the release is provisional or final.
- Confirm units (hectares/acres, tonnes/maunds) match between any two figures being compared.

## Common Pitfalls

- Comparing a provisional in-season estimate to a prior year's final figure as if both were on equal footing.
- Mixing hectare-based and acre-based area figures, or tonne-based and maund-based production figures, without conversion.
- Treating this skill's annual output series as equivalent to the decennial Agricultural Census's structural farm data.
- Summing Kharif and Rabi crop figures into an undifferentiated "annual" total without flagging the seasonal blend.

## Reference

- See [MNFSR Agriculture Statistics Reference](references/mnfsr-agri-statistics.md) for data structure and extraction notes.
