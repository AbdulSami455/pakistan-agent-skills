# MNFSR Agriculture Statistics Reference

## Source

- Ministry of National Food Security & Research (MNFSR), Government of Pakistan
- MNFSR official website: `https://mnfsr.gov.pk`
- Crop area/production/yield statistics are compiled from provincial crop reporting systems and consolidated by MNFSR's Economic Wing/Food Security division; also cross-published in the Pakistan Economic Survey's statistical annex.
- Provincial crop reporting services (agriculture departments of Punjab, Sindh, KP, Balochistan) are the primary data-collection layer feeding into MNFSR's national consolidation.

## Document Structure

- Season-wise release: Kharif season crops (cotton, rice, maize, sugarcane) and Rabi season crops (wheat and others), typically reported separately.
- Per-crop tables: area sown (hectares), production (tonnes), and yield (kg/hectare), usually with province-wise breakdowns.
- Provisional-to-final progression: early-season estimates are revised as harvest data is consolidated; final figures are typically published after the harvest season concludes.
- Livestock and fisheries production volumes (milk, meat, eggs, fish catch) reported separately from crop statistics, under the same ministry's food security mandate.

## Key Indicator Types

- crop area sown (hectares/acres) by crop and province
- crop production (tonnes/maunds) by crop and province
- crop yield (kg/hectare or maund/acre) by crop and province
- livestock/fisheries production volumes (milk, meat, fish catch)

## Extraction Notes

- Always state the crop year/season (Kharif or Rabi) and whether the figure is provisional or final.
- Preserve the unit convention exactly as reported; provincial and federal sources sometimes differ between metric (hectares/tonnes) and traditional (acres/maunds) units.
- Cross-reference `pbs-agriculture-census` only for structural farm data (farm size, tenure, irrigation source) or livestock headcounts — this skill covers annual output, not census-round structure.
- The Pakistan Economic Survey's agriculture chapter (`pes-real-sectors`) cites headline figures from this same underlying data; use this skill instead when crop-by-crop or province-wise granularity is needed.
