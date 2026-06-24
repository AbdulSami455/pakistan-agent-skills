# TDAP Trade Reports Reference

## Source

- Trade Development Authority of Pakistan (TDAP): `https://tdap.gov.pk`
- Monthly Trade Reports and Annual Trade Reports are typically found under TDAP's research/publications or trade statistics section.

## Structure Notes

- Headline export/import summary with YoY and MoM comparison
- Product-category breakdown (textiles and sub-categories, rice, leather, surgical/sports goods, engineering goods, IT/ITeS where covered)
- Destination-market breakdown for major exports
- Sector commentary and trade-promotion activity (missions, exhibitions, MOUs)
- Import commodity breakdown (varies by edition)

## Data Lineage

- TDAP reports are built on PBS customs-recorded trade data, re-presented with trade-promotion framing and sector commentary; they are not an independent primary source distinct from PBS.

## Extraction Notes

- Always anchor figures to the specific month or fiscal year; TDAP's monthly cadence makes period precision especially important.
- Keep product-category labels as granular as TDAP presents them rather than re-aggregating.
