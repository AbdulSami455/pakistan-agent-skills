# PKR Remittances Tracker Reference

## Country/Corridor Breakdown SBP Publishes

SBP's monthly workers' remittances table breaks total inflows down by sending country/corridor. The standard set of corridors reported (column headers may shift slightly release to release, but the core set has been stable for years) typically includes:

- **Saudi Arabia** — historically the single largest or near-largest source corridor, reflecting the large Pakistani labor diaspora there.
- **United Arab Emirates (UAE)** — historically the other largest corridor alongside Saudi Arabia.
- **USA**
- **UK**
- **Other GCC countries** — typically reported as a group covering Bahrain, Kuwait, Qatar, and Oman (sometimes each may also appear individually in more granular releases; check the specific table's row structure).
- **EU countries** — often grouped, though some individual EU countries may be broken out in more detailed annexures.
- **Malaysia**
- **Other countries** — a residual/"rest of the world" category capturing corridors not separately itemized.

Saudi Arabia, UAE, and the other GCC states collectively have typically accounted for a majority of total remittances in most years, reflecting the concentration of overseas Pakistani workers in the Gulf. Do not assume a fixed percentage split, however — corridor shares shift year to year with labor migration patterns, exchange-rate differentials, and use of formal vs. informal transfer channels; always pull the specific month's actual table rather than assuming last year's split still holds.

## "Home Remittances" vs. Balance of Payments "Remittances"

These are two related but distinct SBP series, and conflating them is a common extraction error:

- **Home Remittances (SBP's tabular monthly series)**: This is the series described in this skill's Coverage — a monthly, country/corridor-wise tabular series published on SBP's website (Economic Data / statistics section), reporting the actual cash inflows received through formal banking and exchange-company channels each calendar month. This is the series to use when a task asks for "remittances in [month]" or a country-breakdown for a specific month.
- **Balance of Payments (BOP) "remittances" / "secondary income" line item**: SBP's Balance of Payments statistics (and the State Bank's Annual Report / BOP bulletin) report remittances as a component of the current account, typically under secondary income. The BOP framework:
  - May group remittances slightly differently, or present them alongside other current transfers, depending on the exact BOP presentation (SBP largely follows the IMF's Balance of Payments and International Investment Position Manual, BPM6, conventions for its official BOP statistics).
  - Can have different timing/revision characteristics than the monthly Home Remittances table — BOP data is compiled and revised as part of a broader quarterly/annual external-sector reconciliation process, whereas the Home Remittances table is a more immediate monthly cash-flow report.
  - Over a full fiscal year the two series' totals are generally close (both ultimately reflect the same underlying inflows), but a given month's Home Remittances figure should not be assumed to reconcile exactly, line for line, with whatever a same-period BOP release shows, especially before final BOP revisions are made.
  - For current account, reserves, or broader external-sector analysis, `sbp-balance-of-payments-bulletin` (if available) is the correct skill; use this skill (`pkr-remittances-tracker`) specifically for the monthly/corridor-level Home Remittances table.

**Extraction rule**: If a task cites a remittances figure sourced from the BOP tables or from the PES external-sector chapter, label it as a BOP-sourced figure, not a Home Remittances table figure, even if the numbers are close — do not silently merge the two series into one number without noting the source.

## Fiscal-Year-to-Date vs. Standalone Monthly Figures

Pakistan's fiscal year runs July–June. SBP's remittance commentary (and most secondary reporting on it, including in the press) commonly cites two different kinds of figures that should not be conflated:

- **Standalone monthly figure**: the total (and corridor breakdown) for one specific calendar month, e.g., "remittances in March were $X billion."
- **Fiscal-year-to-date (FYTD) cumulative figure**: the running total from the start of the current fiscal year (July 1) through the month in question, e.g., "remittances for July–March FY[year] totaled $Y billion." This is a sum of the standalone monthly figures for that fiscal year so far, not an independently measured statistic — though SBP's own releases often state the FYTD cumulative directly rather than requiring the reader to sum it.
- When SBP's press release or table states both figures side by side (as is typical — e.g., "remittances in March 2025 were $X billion, up N% YoY; July–March FY25 remittances totaled $Y billion, up M% YoY"), preserve which figure is which explicitly. Do not report a FYTD cumulative number as if it were a single month's inflow, and vice versa.
- If asked to compute a FYTD figure that SBP hasn't directly published for the exact requested cutoff month, sum the individual published monthly figures and state explicitly that the total is a derived/manually summed figure rather than an SBP-published cumulative.
- Year-on-year (YoY) growth for a FYTD figure compares the same partial-year window in the prior fiscal year (e.g., July–March FY25 vs. July–March FY24), not the full prior fiscal year — a common pitfall is comparing a partial-year cumulative against a prior full-year total.

## Extraction Notes

- Preserve US dollar denomination; SBP's remittance tables are reported in USD, not PKR, unless a specific rupee-equivalent conversion table is separately cited.
- SBP figures are subject to revision in subsequent monthly releases; prefer the most recently published value for a given month unless the task specifically asks for the figure as originally reported.
- "Workers' remittances" in SBP usage refers to remittances sent by overseas Pakistani workers/diaspora through formal channels; it does not capture informal (hundi/hawala) transfers, which are outside SBP's measured series by definition.

## Reference

- State Bank of Pakistan: `https://www.sbp.org.pk`
- Home Remittances data (Economic Data section): `https://www.sbp.org.pk/ecodata/index2.asp`
- SBP monthly remittances press releases (narrative summary alongside the tabular data): SBP's press releases / publications section
- SBP Balance of Payments statistics (for the BOP-framework remittances line item): SBP's external sector / BOP statistics pages
- Pakistan's fiscal year: July 1 – June 30
