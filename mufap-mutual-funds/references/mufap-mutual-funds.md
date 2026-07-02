# MUFAP Mutual Funds Reference

## Source

- Mutual Funds Association of Pakistan (MUFAP), the trade body for SECP-licensed Asset Management Companies
- MUFAP official website: `https://www.mufap.com.pk`
- Fund Directory: `https://www.mufap.com.pk/FundProfile/FundDirectory`
- NAV and Sales Load (daily industry statistics): `https://www.mufap.com.pk/Industry/IndustryStatDaily?tab=3`
- Performance Summary: `https://www.mufap.com.pk/Industry/IndustryStatDaily?tab=1`

## Document/Data Structure

- Fund Directory: lists all active open-end schemes with sponsoring AMC, SECP category, and fund manager.
- Fund Profile/Detail pages: per-fund NAV history, benchmark, inception date, and payout history.
- Industry Statistics (daily): NAV and sales load across all funds for a given date, plus performance summary and payout tables.
- SECP fund categories typically include: money market, income, aggressive income, equity, index-tracker, asset allocation, fund of funds, and their Shariah-compliant (Islamic) counterparts, plus voluntary pension scheme sub-funds.

## Key Indicator Types

- Net Asset Value (NAV) per unit, by fund and date
- assets under management (AUM), by fund, AMC, or category
- fund category and benchmark
- sales load (front-end/back-end charges)
- payout/dividend distributions

## Extraction Notes

- Always confirm the sponsoring AMC alongside a fund name, since similar fund names can exist across different AMCs.
- Keep conventional and Shariah-compliant (Islamic) fund categories distinct in any comparison.
- NAV (per-unit price) and AUM (total fund size) are different figures; do not conflate them.
- Cross-reference `secp-insurance-industry-statistics` and `secp-company-registry` only when the question extends beyond mutual fund data into insurance or company-registration territory — MUFAP itself does not cover those domains.
