# Census Bulletins Reference

## Source

- Pakistan Bureau of Statistics (PBS), Population & Housing Census bulletins (most recently the Digital Census)
- Published at `https://www.pbs.gov.pk` in stages: provisional results followed by detailed final tables
- Census-specific products: `https://www.pbs.gov.pk/censusarchive/`

## Document Structure

- National summary bulletin: total population, total households, average household size, sex ratio, urban/rural split.
- Provincial bulletins: same indicators broken down by province.
- Divisional and district bulletins: progressively finer administrative breakdowns.
- Tehsil-level tables: typically released with the final detailed results rather than the provisional release.
- Housing census component: household counts, average household size, and (in later/final releases) housing-unit characteristics.

## Key Indicator Types

- total population by administrative unit (national, province, division, district, tehsil)
- sex split (male/female) and urban/rural split
- number of households and average household size
- population growth rate relative to the prior census round

## Extraction Notes

- Always note whether a cited figure is provisional or final, and the census round/year.
- Administrative boundaries (especially districts and tehsils) can change between census rounds; flag this before comparing across rounds.
- Sub-national totals should reconcile to their parent unit's total; investigate mismatches as a release-stage or boundary issue rather than assuming a data error.
- Household counts and population counts are reported separately; do not conflate the two when discussing "count" figures.
