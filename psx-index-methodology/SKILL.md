---
name: psx-index-methodology
description: Pakistan Stock Exchange (PSX) index construction methodology skill. Use when a task concerns how the KSE-100 Index, KSE-30, KMI-30 (KSE-Meezan Shariah-compliant index), or PSX All Share Index are constructed — free-float market-cap weighting, constituent selection criteria, quarterly review/rebalancing mechanics, and Shariah-screening criteria for KMI-30 — rather than raw historical index-level or price data, ticker/sector discovery, or individual company fundamentals.
---

# PSX Index Methodology

## Overview

Use this skill for questions about how Pakistan Stock Exchange indices are built and maintained — the weighting methodology, constituent-selection rules, periodic review/rebalancing process, and (for KMI-30) Shariah-compliance screening — rather than for pulling actual historical index values, individual stock prices, tickers, sector classifications, or company financial statements. This is the methodology/construction layer that explains *how* an index number is derived and *why* its composition changes, not a data-retrieval skill.

## Coverage

- **KSE-100 Index**: PSX's principal benchmark index, comprising the largest companies by free-float market capitalization selected to represent the largest companies from each sector plus the next-largest companies by market cap overall, subject to a minimum free-float and liquidity screen. It is a free-float market-capitalization-weighted index (constituent weights based on shares actually available for trading, excluding closely-held/locked-in shares, not total issued shares), rebased periodically and reviewed on a periodic schedule (commonly referenced as semi-annual, though the exact current review cadence should be verified against PSX's current published methodology document rather than assumed — verify current cadence).
- **KSE-30 Index**: A narrower free-float-weighted index of the 30 most liquid/largest companies (methodology historically emphasizing free-float market capitalization with a liquidity/free-float-adjustment screen), intended as an alternative benchmark more tightly focused on the most tradable large-caps than the broader KSE-100.
- **KMI-30 (KSE-Meezan Index)**: A Shariah-compliant index jointly developed by PSX and Al Meezan Investment Management, comprising 30 Shariah-compliant companies selected by free-float market capitalization from among companies that pass a Shariah-compliance screen. The Shariah screen applies both business-activity criteria (excluding companies whose core business involves interest-based finance, alcohol, gambling, conventional insurance, and other impermissible activities) and financial-ratio criteria (thresholds on interest-bearing debt-to-assets, interest-bearing investments/cash-to-assets, and non-compliant/interest income as a share of total revenue) — the specific numeric thresholds for these financial ratios are set by the Shariah advisory process and should be verified against Al Meezan/PSX's current published KMI-30 Shariah screening criteria rather than stated from memory (verify current thresholds).
- **All Share Index (PSX All Share Index / KSE All Share Index)**: A broader, free-float market-cap-weighted index intended to capture the overall market's performance across effectively all eligible listed companies (subject to a minimum listing/eligibility screen), rather than a curated large-cap subset — used as a broad-market performance gauge distinct from the more selective KSE-100/KSE-30/KMI-30.
- **Free-float weighting mechanics**: All major PSX indices use free-float-adjusted market capitalization (share price times free-float shares, where free-float excludes government/sponsor/strategic/locked-in holdings as defined by PSX's free-float methodology) rather than full market capitalization, meaning a company's index weight can differ substantially from its total market cap depending on its free-float ratio.
- **Rebalancing/review mechanics**: Index constituents and their free-float factors are reviewed on a periodic cycle, at which point companies may be added or removed based on updated market-cap/liquidity/free-float rankings (and, for KMI-30, updated Shariah-compliance status), and free-float factors are recalculated; between review dates, share-count/free-float adjustments for corporate actions (new issues, buybacks) are typically applied on an ad hoc basis per PSX's methodology rules.

## Use This Skill For

- explaining how KSE-100, KSE-30, KMI-30, or the All Share Index are weighted (free-float market-cap methodology)
- explaining constituent-selection criteria and eligibility screens for any of these indices
- explaining the periodic review/rebalancing process and what triggers a constituent addition or removal
- explaining KMI-30's Shariah-compliance screening criteria (business-activity and financial-ratio screens)
- distinguishing what makes an index free-float-weighted versus full-market-cap-weighted

## When Not to Use This Skill

- For actual historical index-level values, OHLC price series, or point-in-time index readings — use `psx-historical-data`.
- For ticker symbols, sector classifications, or which companies are listed/traded on PSX — use `psx-market-discovery`.
- For individual company fundamentals, quotes, or financial snapshots — use `psx-company-snapshots`.
- For debt-market instruments or scrip eligibility criteria unrelated to equity-index construction — use `psx-debt-and-eligibility`.

## Routing Rules

- If the question asks for an actual index value, chart, or historical time series, route to `psx-historical-data` instead.
- If the question asks which sector a company belongs to or its ticker symbol, route to `psx-market-discovery` instead.
- If the question asks for a specific company's financial ratios, quote, or fundamentals (as opposed to how an index's screening ratios work generically), route to `psx-company-snapshots` instead.
- If the question is about mutual funds tracking or benchmarked to these indices (e.g., Islamic/Shariah-compliant fund performance), cross-check `mufap-mutual-funds` for the fund-side data.

## Extraction Workflow

1. Identify which specific index is in question (KSE-100, KSE-30, KMI-30, or All Share Index) — their eligibility screens and purposes differ, and methodology detail should not be generalized across them without checking.
2. Confirm whether the question is about weighting mechanics (free-float market cap), selection criteria (which companies qualify), or review/rebalancing timing (when composition changes) — these are three distinct methodology components.
3. For KMI-30, separate the business-activity Shariah screen (qualitative, sector-based exclusion) from the financial-ratio Shariah screen (quantitative thresholds on debt, interest-bearing assets, and non-compliant income) — do not conflate the two screening layers.
4. Note that free-float weighting means index weight is not proportional to total market capitalization; flag this distinction whenever a question implies otherwise.
5. Flag specific review-cadence timing and KMI-30 financial-ratio thresholds as needing verification against PSX's/Al Meezan's current published methodology documents.

## Technical Rules

- Do not describe any PSX benchmark index as full-market-cap-weighted; all major PSX indices (KSE-100, KSE-30, KMI-30, All Share) use free-float-adjusted market capitalization.
- Do not state a specific current periodic-review cadence (e.g., "reviewed every six months") as a fixed, unverifiable fact without noting it should be checked against PSX's current methodology document.
- Do not state specific KMI-30 Shariah financial-ratio thresholds (e.g., a debt-to-assets percentage cutoff) without hedging that current thresholds should be verified against Al Meezan/PSX's published screening criteria, since Shariah screening parameters can be revised by the Shariah advisory process.
- Distinguish the business-activity Shariah screen (categorical exclusion of certain sectors) from the financial-ratio Shariah screen (quantitative balance-sheet/income-statement thresholds) for KMI-30; a company can pass one screen and fail the other.
- Do not conflate KSE-100 (broad large-cap benchmark) with KSE-30 (narrower, more liquidity-focused) or KMI-30 (Shariah-screened subset); they have different eligibility populations even though there is overlap in constituents.

## Validation Checklist

- Confirm which specific index (KSE-100, KSE-30, KMI-30, All Share) the question concerns before citing methodology detail.
- Confirm whether weighting, selection-criteria, or rebalancing-timing is the actual subject of the question.
- For KMI-30, confirm whether the business-activity screen or the financial-ratio screen (or both) is relevant to the question.
- Flag any specific review-cadence date or Shariah-ratio threshold as needing current-source verification.

## Common Pitfalls

- Describing a PSX index as weighted by full/total market capitalization rather than free-float-adjusted market capitalization.
- Treating KSE-100, KSE-30, and KMI-30 as interchangeable or as differing only in constituent count, when their eligibility/screening criteria differ substantively (especially KMI-30's Shariah screen).
- Stating precise current KMI-30 Shariah financial-ratio thresholds or review-cycle dates as fixed facts without verification.
- Conflating the qualitative business-activity Shariah screen with the quantitative financial-ratio Shariah screen for KMI-30.
- Using this skill to answer a request for actual index values or company data, which belongs in `psx-historical-data`, `psx-market-discovery`, or `psx-company-snapshots`.

## Reference

- See [PSX Index Methodology Reference](references/psx-index-methodology.md) for index-specific citations, Shariah-screening detail, and extraction notes.
