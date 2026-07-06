# PSX Debt and Eligibility Reference

## Sources

- PSX corporate site (debt market, margin trading system pages): `https://www.psx.com.pk`
- PSX Data Portal: `https://dps.psx.com.pk`
- `psxdata` Python package: `https://pypi.org/project/psxdata/` (GitHub: `https://github.com/mtauha/psxdata`) — convenience scraper, not the source of record.

## Debt Instrument Types

- **Term Finance Certificate (TFC)**: a corporate fixed-income instrument, typically issued for medium- to long-term financing. Pays periodic profit/markup (often floating, tied to a benchmark such as KIBOR plus a spread) and is redeemed at or before maturity. Can be secured or unsecured, listed or privately placed.
- **Sukuk**: a Shariah-compliant instrument structured around an underlying tangible asset, lease (Ijarah), or partnership/profit-sharing arrangement (Musharakah/Mudarabah), rather than a straightforward interest-bearing loan. Common structures used in Pakistan include Ijarah Sukuk (asset-lease-based) and Diminishing Musharakah Sukuk (declining co-ownership).
- Both TFCs and Sukuks serve the corporate fixed-income financing role that bonds serve in other markets, but their legal/contractual structures are materially different, and Sukuks require Shariah-compliance certification from a Shariah advisor/board.

## Margin Trading Eligibility Mechanisms

| Mechanism | Purpose | Eligible-list scope |
|---|---|---|
| MTS (Margin Trading System) | Broker-financed leveraged trading | Stocks meeting PSX/SECP eligibility criteria (free float, market cap, price stability, liquidity) |
| MF (Margin Financing) | An older/parallel leverage mechanism | Its own eligible-securities list, not necessarily identical to MTS |
| SLB (Securities Lending and Borrowing) | Enables short-selling via borrowed securities | Its own eligible-securities list for lending/borrowing purposes |

Eligibility for each mechanism is reviewed periodically by PSX in coordination with SECP; a stock's inclusion can change if its liquidity, free float, or price behavior shifts. Do not assume PSX listing alone implies eligibility for any of these mechanisms.

## Extraction Notes

- When retrieving `psxdata.debt_market()` output, preserve the instrument-type field (TFC vs. Sukuk) exactly — do not merge them into a single generic "bond" category, since their regulatory and Shariah-compliance treatment differs.
- When retrieving `psxdata.eligible_scrips()` output, confirm which specific mechanism (MTS by default, unless otherwise specified) the list represents before using it to answer an eligibility question.
- Debt-market listing volumes on PSX are considerably smaller than the equity market; do not expect the same data richness or update frequency as equity ticker/quote data.
