# PSX Index Methodology Reference

## Source

- Pakistan Stock Exchange (PSX): `https://www.psx.com.pk`
- PSX Indices methodology page/documents (search PSX's "Indices" or "Products" section for the current published index methodology PDFs for KSE-100, KSE-30, and the All Share Index): `https://www.psx.com.pk/psx/exchange/indices`
- Al Meezan Investment Management — KMI-30 Index and Shariah screening criteria: `https://www.almeezangroup.com`
- Mutual Funds Association of Pakistan (MUFAP) for Shariah-compliant/Islamic fund benchmarking context: `https://www.mufap.com.pk`

## KSE-100 Index

- PSX's flagship benchmark, first introduced in 1991 (base value conventionally referenced as 1,000 at that time), representing the largest companies by free-float market capitalization.
- Selection approach: the index is designed to include the largest company (by market capitalization) from each sector represented on the exchange, plus the next-largest companies overall by market capitalization across sectors, until 100 constituents are reached — subject to minimum free-float and trading/liquidity screens set out in PSX's published methodology.
- Weighting: free-float market-capitalization-weighted — a constituent's index weight reflects its share price multiplied by its free-float share count (shares available for public trading, excluding government, sponsor/director, and other locked-in/strategic holdings as defined by PSX's free-float methodology), not its full issued share capital.
- Review: constituents and free-float factors are reviewed on a periodic cycle set by PSX's index committee/methodology document; the exact current cadence (e.g., semi-annual review dates) should be confirmed against PSX's current published methodology rather than assumed fixed, since review frequency and criteria have been subject to methodology updates over the index's history.

## KSE-30 Index

- Introduced as a narrower benchmark than KSE-100, comprising 30 companies selected primarily on a free-float market-capitalization basis with an emphasis on liquidity, intended to better reflect the segment of the market most accessible to large/institutional trading activity.
- Like KSE-100, it is free-float-weighted; its constituent list overlaps substantially with KSE-100's largest/most liquid names but is not identical, since KSE-100 also ensures sector representation that KSE-30's more liquidity/size-focused screen does not guarantee.

## KMI-30 (KSE-Meezan Index)

- A joint index product of PSX and Al Meezan Investment Management, launched to provide a benchmark for Shariah-compliant equity investing in Pakistan; comprises 30 Shariah-compliant companies selected by free-float market capitalization from the pool of PSX-listed companies that pass Al Meezan's Shariah screening process.
- **Business-activity screen**: excludes companies whose core business involves interest-based conventional banking/financial services, conventional insurance, alcohol, gambling/gaming, tobacco (in some screening frameworks), pork-related products, and other activities considered non-compliant under the Shariah advisory's criteria.
- **Financial-ratio screens**: even companies in permissible business lines are further screened against quantitative thresholds — commonly structured around (a) interest-bearing debt as a proportion of total assets or market capitalization, (b) interest-bearing deposits/investments as a proportion of total assets or market capitalization, and (c) non-compliant/interest-based income as a proportion of total revenue — each subject to a maximum threshold set by the Shariah advisory board. The precise current percentage thresholds should be verified against Al Meezan's/PSX's currently published KMI-30 Shariah screening criteria document rather than stated from memory, as these thresholds are periodically reviewed (verify current thresholds).
- KMI-30 is rebalanced/reviewed periodically (both for market-cap-based constituent changes and re-screening of Shariah compliance), meaning a constituent can be removed if it subsequently fails either the business-activity or financial-ratio screen even without a market-cap-driven reason for removal.

## All Share Index

- A broad-market, free-float-weighted index intended to represent overall market performance across substantially all eligible listed companies on PSX (subject to a minimum listing-history/eligibility screen), rather than a curated large-cap or liquidity-focused subset.
- Used as a broad-market performance benchmark distinct from the more selective KSE-100/KSE-30, useful when a task needs a market-wide return series rather than large-cap-only performance.

## Extraction Notes

- Always name the specific index (KSE-100, KSE-30, KMI-30, All Share) before describing methodology; do not generalize one index's screening rules to another.
- Emphasize free-float weighting as the common mechanical thread across all four indices, while noting their differing eligibility/screening populations.
- For KMI-30, keep the qualitative business-activity screen and the quantitative financial-ratio screen conceptually separate, and hedge specific ratio thresholds.
- Route any request for actual index values, constituent lists as of a specific date, or historical performance to `psx-historical-data`/`psx-market-discovery`, since this reference covers construction methodology, not data.
