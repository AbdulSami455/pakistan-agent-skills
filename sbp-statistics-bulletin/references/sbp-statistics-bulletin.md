# SBP Statistics Bulletin Reference

## Official Sources

- State Bank of Pakistan: `https://www.sbp.org.pk/`
- SBP statistics and data pages: use the official SBP site navigation for statistics, data, and publications.

## Common Release Families

The SBP statistical ecosystem usually includes:

- statistical bulletins or supplements with time-series tables
- weekly or periodic banking and reserves updates
- exchange-rate tables
- interest-rate and policy-rate series
- banking-sector balance-sheet tables
- monetary aggregates and domestic-credit tables

## Interpretation Notes

- Preserve frequency first: weekly, monthly, quarterly, annual, and as-of-date series should not be merged without saying so.
- Treat reserves, deposits, advances, and money supply as stock measures unless the source explicitly says otherwise.
- Use the source's exact date stamp for point-in-time values.
- If a figure appears in both a bulletin and a policy document, treat the bulletin as the cleaner series source and the policy document as commentary.

## Extraction Notes

- Always record the unit, currency, and basis.
- If a series has a break in methodology or reporting format, flag the break before comparing pre- and post-break values.
- For FX and rate series, keep the official SBP label intact rather than renaming the field to a generic shorthand.
- When a user asks for "latest" data, verify the most recent bulletin or update rather than relying on memory.

## Common Data Families

- reserves
- exchange rates
- policy rates
- scheduled-bank deposits and advances
- monetary aggregates
- banking-sector assets and liabilities
