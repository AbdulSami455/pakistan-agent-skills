# Balance of Payments Bulletin Reference

## Source

- State Bank of Pakistan, External Sector statistics: `https://www.sbp.org.pk` under Statistics / Balance of Payments, Reserves, and External Debt.
- Data is typically published as downloadable tables (CSV/Excel) alongside a short summary note, rather than as a single long narrative PDF.

## Typical Release Structure

- Summary table: current account components (trade balance, services, primary income, secondary income/remittances) and the resulting current account balance for the period.
- Financial account summary: foreign direct investment, portfolio investment, and loans.
- Reserves table: SBP reserves, bank reserves, and total liquid foreign reserves, often with a weekly series and a monthly average.
- External debt servicing table: scheduled vs. actual principal and interest payments for the period.

## Indicator Guide

- current account balance (surplus/deficit) for the period
- trade balance (goods) and services balance
- remittance inflows for the period (cross-check with `pkr-remittances-tracker` for country-level detail)
- SBP reserves, bank reserves, total liquid reserves
- external debt servicing (principal, interest) due and paid

## Extraction Notes

- SBP publishes data at multiple cadences: weekly reserves updates, monthly balance of payments, and quarterly external debt summaries. Always match the cadence to the question.
- Figures are commonly revised in subsequent releases; prefer the most recent bulletin covering the same period unless the question specifically asks for the originally reported figure.
- When summing months into a quarter or fiscal-year-to-date figure, state that this is a derived total, not an official cumulative line, unless the bulletin itself provides one.
- Reserves are typically reported in US dollars as of a specific date (often a Friday for weekly data); always retain that date.
