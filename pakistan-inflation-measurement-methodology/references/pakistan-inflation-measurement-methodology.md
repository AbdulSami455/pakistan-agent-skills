# Pakistan Inflation Measurement Methodology Reference

## Source

- PBS Price Statistics hub (CPI/SPI/WPI methodology notes and FAQs): `https://www.pbs.gov.pk/price-statistics/`
- PBS FAQs (includes methodology clarifications): `https://www.pbs.gov.pk/content/faqs`
- Pakistan Economic Survey FY25, Chapter on Inflation (narrative + summary methodology context): `https://www.finance.gov.pk/survey/chapter_25/7_Inflation.pdf`
- Pakistan Economic Survey, Inflation chapter (alternate/earlier edition path used by Finance Division): `https://www.finance.gov.pk/survey/chapter_22/PES07-INFLATION.pdf`
- SBP Inflation Monitor (monthly note explaining headline vs. core inflation movement): `https://www.sbp.org.pk/publications/Inflation_Monitor/2026/Jan/Jan.pdf`
- SBP Working Paper 18, "Evaluating Core Inflation Measures in Pakistan" (Lodhi) — listing/abstract: `https://ideas.repec.org/p/sbp/wpaper/18.html`
- PIDE research note on price statistics methodology in Pakistan (PIDE domain may return HTTP 403 to automated fetches in some environments but is a well-known, legitimate Pakistani public-policy think tank — verify manually if fetching): `https://pide.org.pk/research/price-statistics-methodology-in-pakistan/`

## Index Construction (CPI)

- **Formula**: PBS computes CPI using a weighted Laspeyres-type formula — current-period prices applied to base-period expenditure weights (quantities fixed at the base period). This is standard international CPI-compilation practice but implies known substitution bias between rebasing events (the fixed-weight index cannot capture consumers substituting toward relatively cheaper goods as relative prices shift).
- **Weight source and base year**: CPI weights are derived from a household budget/expenditure survey; historically PBS has used HIES (Household Integrated Economic Survey) rounds to derive weights, with the survey reference year also serving as the index base year. Confirm the currently active base year and survey source against the latest PBS Price Statistics methodology note before citing a specific year, as PBS has rebased CPI multiple times historically and has indicated an intent to rebase price statistics on a roughly five-year cycle going forward.
- **Basket structure**: Items are grouped under a COICOP-style 12-main-group classification. Urban and rural baskets are compiled separately with different item counts and weights, reflecting differing consumption patterns; the national headline CPI combines both. Exact current item counts, market/city coverage, and group weights should be sourced from the latest PBS methodology note rather than cited as static facts, since these details change at each rebasing.

## Core Inflation Methodology (SBP)

- **NFNE (Non-Food Non-Energy)**: Computed by excluding the food group and specified energy items (e.g., electricity, gas, motor fuels such as petrol/diesel/CNG) from the CPI basket, then re-weighting the remaining items. Intended to capture demand-side, "underlying" inflation net of supply-driven food/energy volatility.
- **20% Trimmed Mean**: Computed by ranking all CPI items by their individual period-on-period price-change rate, then excluding roughly the top 10% and bottom 10% of items by cumulative expenditure weight (i.e., trimming both tails), and averaging the remaining ~80% of weighted items. This is a statistical-outlier-exclusion approach rather than a category-based exclusion, so it can diverge from NFNE in months where food or energy items are not actually the extreme movers.
- Both measures are published regularly in SBP's monthly Inflation Monitor and referenced in Monetary Policy Statements as inputs to the MPC's inflation outlook assessment.

## SPI and WPI as Distinct Constructions

- **SPI (Sensitive Price Indicator)**: Weekly, tracks a fixed basket of essential/daily-use items, reported by city and income group/quintile — designed as a fast, narrow affordability gauge, not a full cost-of-living index.
- **WPI (Wholesale Price Index)**: Monthly, tracks wholesale-level commodity prices under a distinct commodity classification from the retail CPI basket; wholesale price movements do not mechanically pass through to retail CPI on a fixed lag.
- None of CPI, SPI, or WPI should be treated as a substitute estimate for either of the others; each has its own basket, weighting, and update cadence maintained by PBS.

## Extraction Notes

- Always state whether a cited inflation figure is headline CPI, NFNE core, trimmed-mean core, SPI, or WPI, and the change basis (MoM/YoY/fiscal-year average).
- Flag any long-run CPI comparison that spans a base-year/basket rebasing, since weights and item coverage change at each revision.
- Treat any specific numeric detail (current base year, item counts, group weights) as needing verification against the latest PBS Price Statistics methodology release before being stated as current fact.
