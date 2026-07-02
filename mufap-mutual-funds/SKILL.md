---
name: mufap-mutual-funds
description: MUFAP (Mutual Funds Association of Pakistan) skill. Use when analyzing, summarizing, comparing, or extracting information from MUFAP's mutual fund industry data, especially fund-wise Net Asset Value (NAV), fund category performance, and industry-wide assets under management (AUM) for Pakistan's mutual fund and voluntary pension scheme industry.
---

# MUFAP Mutual Funds

## Overview

Use this skill for Pakistan's mutual fund and voluntary pension scheme industry data as published by the Mutual Funds Association of Pakistan (MUFAP), the trade body for SECP-licensed Asset Management Companies (AMCs). This is the right skill for fund-level NAV, category performance, and industry AUM figures — not for company-registry or corporate-filing data.

## Coverage

- Daily Net Asset Value (NAV) and sales load data for open-end mutual fund schemes, published per fund/scheme.
- Fund categorization by SECP-defined category (e.g., money market, income, equity, index-tracker, asset allocation, Shariah-compliant/Islamic equivalents of each), which determines the appropriate performance benchmark and risk profile.
- Industry-wide statistics: total assets under management (AUM), category-wise AUM breakdown, and AMC-wise market share.
- Fund directory and profile data: AMC (Asset Management Company) sponsor, fund manager, inception date, and benchmark for each scheme.
- Payout/dividend distribution data for funds that distribute income.

## Use This Skill For

- extracting a specific mutual fund's NAV on a given date
- pulling category-wise or AMC-wise assets under management (AUM)
- comparing performance across funds within the same SECP category
- identifying which AMC manages a specific fund and the fund's benchmark
- tracking industry-wide AUM growth over time

## When Not to Use This Skill

- For SECP's insurer-wise premium and asset statistics — use `secp-insurance-industry-statistics` instead.
- For company incorporation, registration, or corporate-filing data — use `secp-company-registry` instead; MUFAP covers fund performance, not entity registration.
- For PSX-listed equity data (stock prices, indices) rather than mutual fund units — use the relevant `psx-*` skill instead.
- For systemic risk to the asset management/mutual fund sector as part of overall financial stability — prefer `sbp-financial-stability-review`, which covers NBFI/mutual fund risk narrative rather than fund-level NAV data.

## Routing Rules

- Use this skill for fund-level or industry-level mutual fund data (NAV, AUM, category performance) sourced from MUFAP.
- If the question is about insurance rather than mutual funds, prefer `secp-insurance-industry-statistics`.
- If the question is about a company's registration status or corporate filings rather than fund performance, prefer `secp-company-registry`.
- If the question is about a specific PSX-listed stock rather than a mutual fund unit, prefer the appropriate `psx-*` skill instead.

## Extraction Workflow

1. Identify the specific fund/scheme by its full name and confirm the AMC that manages it, since similarly named funds can exist across different AMCs.
2. Confirm the SECP category (money market, income, equity, asset allocation, Shariah-compliant variant, etc.) before comparing performance across funds — cross-category comparisons are not meaningful.
3. Note the exact date of the NAV or AUM figure; these change daily (NAV) or are reported as of a specific cutoff (AUM/industry statistics).
4. Distinguish per-unit NAV from a fund's total AUM (size) — these are different figures reported together.
5. When comparing performance, check whether the figure is a simple return or an annualized/benchmarked return, and over what period.

## Technical Rules

- Keep conventional and Shariah-compliant (Islamic) fund categories distinct even when they share a similar strategy label (e.g., "equity" vs. "Islamic equity").
- NAV is a per-unit price; AUM is the fund's total size; do not conflate the two when discussing fund "size" or "value."
- Category benchmarks differ (e.g., money market funds benchmark against short-term rates, equity funds against a KSE index); use the fund's own stated benchmark rather than assuming a generic one.
- Fund names can be similar across AMCs (e.g., multiple "Income Fund" products); always confirm the sponsoring AMC before citing a figure.

## Validation Checklist

- Confirm the fund's full name and sponsoring AMC.
- Verify the SECP category before making any cross-fund performance comparison.
- Check the exact date of the NAV or AUM figure being cited.
- Confirm whether a performance figure is conventional or Shariah-compliant before comparing it to a peer fund.

## Common Pitfalls

- Comparing NAV growth across funds in different SECP categories as if they were peers.
- Confusing a fund's NAV (per-unit price) with its AUM (total size).
- Mixing up two similarly named funds managed by different AMCs.
- Treating MUFAP fund data as a substitute for SECP's company-registry or insurance-statistics skills, which cover different regulated entities.

## Reference

- See [MUFAP Mutual Funds Reference](references/mufap-mutual-funds.md) for data structure and extraction notes.
