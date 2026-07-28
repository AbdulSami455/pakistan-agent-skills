# REER and Balance of Payments Methodology Reference

## Source

- State Bank of Pakistan, Real Effective Exchange Rate statistics and methodology notes: `https://www.sbp.org.pk`
- SBP Balance of Payments statistics (for actual BOP/current-account data tables, see `sbp-balance-of-payments-bulletin` instead of this methodology skill): `https://www.sbp.org.pk`
- IMF Information Notice System (INS) methodology for effective exchange rates (used as an external cross-check on trade-weighting approaches): `https://www.imf.org`

## REER Construction Formula

REER = NEER × Relative Price Index (RPI), where:

- **NEER (Nominal Effective Exchange Rate)**: a trade-weighted basket of bilateral nominal exchange rates between the PKR and Pakistan's trading partners'/competitors' currencies.
- **RPI (Relative Price Index)**: deflates the NEER for inflation differentials between Pakistan and its trading partners, using CPI as the deflator.

A REER index value above the base-year level (100) generally signals real appreciation (loss of price competitiveness); a value below signals real depreciation (competitiveness gain).

## Trade-Weight Basket

- SBP derives basket weights from merchandise trade, manufacturing, and (in some revisions) tourism data for trading partners/competitors, calculated as multi-year trade-pattern averages.
- SBP has periodically revised both the number of countries in the basket (e.g., a documented expansion from 25 to 37 countries in one revision) and the specific country composition, reflecting shifts in Pakistan's trade patterns (e.g., toward China and other Asian economies).
- The IMF's own effective-exchange-rate weighting methodology (used as a cross-check/reference point) has used specific historical trade-pattern windows in its own revisions (e.g., a 2016-18 pattern window in one IMF revision) — this is a separate IMF-maintained series, not identical to SBP's own REER basket.
- The current basket size and composition should always be confirmed against SBP's latest REER revision-study note rather than assumed fixed, since both have changed more than once.

## Base Year

SBP's published REER series has used a base year of 2010=100 in documented releases. Confirm the currently active base year against SBP's latest statistics/REER release, since base years are periodically rebased alongside weight revisions.

## Current Account Structural Drivers

- **Goods-trade deficit**: structurally persistent, driven by import dependence on energy and intermediate/capital goods.
- **Services trade**: a partial offset to the goods deficit.
- **Workers' remittances**: large enough relative to GDP to materially affect the current account balance; analyzed as a quasi-structural inflow rather than a residual item (see `pakistan-remittance-macro-linkages` for the deeper remittance-REER-consumption linkage).
- **External sustainability assessment**: the IMF, World Bank, and SBP assess sustainability using the current account balance alongside reserve-adequacy metrics (e.g., import-cover months) and financing composition (official vs. market-based, maturity structure) — never the current account balance alone.

## Interpreting a Current Account Improvement

Distinguish two very different sources of improvement before calling it "durable":

- **Import-compression-driven** — often reflects demand slowdown or administrative import restrictions; typically a fragile, reversible improvement.
- **Export/remittance-growth-driven** — reflects underlying competitiveness or structural inflow growth; a more durable improvement.

## Extraction Notes

- Never describe REER as simply "the exchange rate adjusted for inflation" without noting the trade-weighted, multilateral-basket construction — it is not a bilateral real exchange rate against a single currency such as the USD.
- Always separate the NEER (nominal) contribution from the RPI (inflation-differential) contribution when interpreting a REER movement; nominal PKR depreciation does not automatically imply real competitiveness gain.
- Cite the specific REER base year and basket-weight vintage in use; do not assume either is fixed over time.
