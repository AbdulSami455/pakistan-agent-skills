# PSX Market Discovery Reference

## Sources

- PSX Data Portal (official, authoritative): `https://dps.psx.com.pk`
- PSX corporate site (market summary, sector/index pages): `https://www.psx.com.pk`
- `psxdata` Python package: `https://pypi.org/project/psxdata/` (GitHub: `https://github.com/mtauha/psxdata`) — convenience scraper, not the source of record; verify against the Data Portal for anything citation-grade.

## Sector Classification (illustrative, not exhaustive)

PSX groups listed companies into sector indices used for sector-wise performance reporting. Commonly tracked sectors include:

- Commercial Banks
- Cement
- Oil & Gas Exploration Companies
- Oil & Gas Marketing Companies
- Fertilizer
- Textile Composite / Textile Spinning / Textile Weaving
- Technology & Communication
- Automobile Assembler / Automobile Parts & Accessories
- Power Generation & Distribution
- Insurance
- Food & Personal Care Products
- Chemical
- Engineering
- Pharmaceuticals
- Cable & Electrical Goods
- Real Estate Investment Trust (REIT)

Sector composition and naming can be revised by PSX; treat this list as illustrative and verify current sector names against the PSX website before citing a company's sector affiliation.

## Index Methodology Notes

| Index | Constituents | Selection Basis | Notes |
|---|---|---|---|
| KSE-100 | 100 companies | Free-float market capitalization + liquidity, with at least one company from most sectors by capitalization | The flagship benchmark; base value 1,000 as of Nov 1, 1991 |
| KSE-30 | 30 companies | Free-float market capitalization and liquidity (no sector-representation rule) | Distinct from KSE-100's sector-representation methodology |
| KMI-30 | 30 companies | Shariah-compliant screening (jointly maintained with Al Meezan Investments) + liquidity/size | Do not conflate with KSE-30 — different screening criteria entirely |
| PSX All Share Index | All eligible listed companies | Broadest coverage, minimal exclusions | Used for aggregate market-return calculations rather than a "top N" benchmark |

Indices are rebalanced periodically (commonly semi-annually for KSE-100/KSE-30); a constituent snapshot from one period should not be assumed current without checking the latest rebalancing announcement.

## Board Classification

- **Main Board**: standard listing board for established companies meeting PSX's main listing requirements.
- **Growth Enterprise Market (GEM) Board**: for smaller or growth-stage companies with relaxed listing requirements relative to the Main Board.
- Board placement affects listing/disclosure requirements and typical liquidity profile; it is independent of sector classification and index membership.

## Extraction Notes

- When cross-referencing `psxdata.sectors()` output, check for aggregate/summary rows (e.g., a "Total" or "All Sectors" row) that should not be counted as an individual sector.
- When cross-referencing `psxdata.indices(name)`, confirm the exact index name string the package expects (e.g., `"KSE100"` without a hyphen) versus the commonly written name (KSE-100) — package naming conventions and human-readable names often differ.
- If the package returns unexpectedly few or many tickers/constituents, treat this as a signal to verify against the PSX Data Portal rather than assuming the discrepancy is real market movement.
