---
name: pakistan-admin-boundaries
description: Pakistan administrative boundary reference skill for the HDX COD-AB Pakistan dataset. Use when looking up, joining, or standardizing province, division, district, or tehsil names and codes for geocoding or cross-referencing district-level statistics, census data, or agriculture census records.
---

# Pakistan Admin Boundaries

## Overview

Use this skill when a task needs Pakistan's administrative hierarchy — province, division, district, tehsil — with standard codes, typically to join or standardize location references across other datasets. This is a supporting utility skill: other skills that report district-level statistics (e.g., PES district tables, census data, agriculture census) should reference this skill for consistent geocoding rather than re-deriving boundary names independently.

This skill describes a **structured open dataset, not an installed software package**. There is no `import` statement or function call to demonstrate — the "data surface" below describes the dataset's structure so an agent can query, join, or look up against it consistently.

## Use This Skill For

- standardizing a district or tehsil name to its official administrative-hierarchy form
- joining district-level statistics from one source to district-level statistics from another using consistent naming/codes
- resolving ambiguous or renamed district names (district boundaries and names in Pakistan have changed over time, e.g., new districts carved from existing ones)
- providing the province/division a given district belongs to
- supporting geocoding consistency for other skills (census, agriculture census, PES district tables)

## When Not to Use This Skill

- For extracting population counts or demographic data — use `pakistan-census-bulletins` instead; this skill only provides boundary names and codes.
- For actual district-level statistics (crop output, health indicators, education enrollment) — use the relevant sectoral skill; this skill is a geocoding utility only.
- For provincial boundary geometry for GIS analysis — this skill describes the dataset but does not replace a GIS workflow.

## Data Surface

The reference dataset is **HDX COD-AB Pakistan** (UN OCHA Common Operational Datasets — Administrative Boundaries), distributed as shapefiles and GeoJSON, with an associated hierarchy table. The hierarchy has four standard levels:

- **Admin0**: Pakistan (country level)
- **Admin1**: Province/Territory (e.g., Punjab, Sindh, Khyber Pakhtunkhwa, Balochistan, Gilgit-Baltistan, Azad Jammu & Kashmir, Islamabad Capital Territory)
- **Admin2**: Division (a grouping of districts within a province; not used uniformly in every reporting context)
- **Admin3**: District
- **Admin4**: Tehsil (sometimes called Taluka in Sindh, or Sub-Division in some regions)

Each level typically carries: a name field, a standardized P-code (Pakistan administrative unit code, following the COD-AB/PCode convention), and a parent-level reference (e.g., each district record references its parent division/province code).

## Workflow

1. Identify the administrative level needed (province, division, district, or tehsil) for the task at hand.
2. Look up the target unit by name first; if the name is ambiguous (duplicate district names across provinces are rare but tehsil-name collisions across districts are common), disambiguate using the parent-level reference.
3. Use the P-code, not the name string, as the stable join key when reconciling data from multiple sources — names can have spelling variants (e.g., "Rawalpindi" vs. "Rawalpindi District").
4. When joining historical data, check whether the district existed under its current boundaries at the time the historical data was collected — Pakistan has created new districts by splitting existing ones multiple times (e.g., in Khyber Pakhtunkhwa and Punjab).
5. Confirm dataset vintage/version before treating boundaries as current — COD-AB is periodically updated by OCHA and older cached copies may not reflect the latest district splits.

## Validation Checklist

- Confirm the P-code uniquely resolves to one unit and one parent at each level.
- Confirm district name spelling against the dataset's canonical name field rather than a commonly used alternate spelling.
- Check whether a named district/tehsil existed at the time period relevant to the task, especially for newer districts created via splits.
- Verify parent-child consistency (a tehsil's claimed parent district actually belongs to the claimed parent province) before trusting a join.

## Working Rules

- Prefer P-codes over name strings for any join or merge operation across datasets.
- Treat division-level grouping as inconsistently used across reporting sources; do not assume every dataset reports at division level just because COD-AB includes it.
- When a task references an older or merged district name, map it forward to its current administrative form and note the mapping explicitly.
- Keep tehsil-level lookups scoped to their parent district to avoid name collisions.

## Technical Pitfalls

- District boundary changes (new districts split from existing ones) mean a name-only join across years can silently misattribute population or statistics to the wrong unit.
- Gilgit-Baltistan and Azad Jammu & Kashmir are sometimes excluded or treated separately in national statistical datasets — check whether the dataset being joined actually includes them before assuming full national coverage. For territory-specific statistics, use `ajk-development-statistics` or `gb-development-statistics`.
- Division-level administrative units are not used uniformly by every Pakistani government data source, so a division-level join may fail silently if the source dataset only reports at district level.
- Shapefile/GeoJSON attribute field names can vary by COD-AB release version (e.g., `ADM2_EN` vs. similar naming); confirm field names against the specific dataset version in use rather than assuming a fixed schema.

## Reference

- See [Pakistan Admin Boundaries Reference](references/pakistan-admin-boundaries.md) for the province/territory list, known district splits, and P-code conventions.
- HDX (Humanitarian Data Exchange) COD-AB Pakistan dataset, maintained by UN OCHA, is the authoritative source for boundary geometry and the P-code hierarchy
- HDX dataset page: `https://data.humdata.org/dataset/cod-ab-pak`
- UN OCHA Pakistan: `https://www.unocha.org/pakistan`
- Pakistan OCHA HDX page: `https://data.humdata.org/organization/ocha-pakistan`
- Check the dataset's HDX page for the current version/vintage before relying on cached copies.
