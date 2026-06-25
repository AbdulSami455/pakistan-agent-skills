---
name: sbp-financial-soundness-indicators
description: SBP Financial Soundness Indicators skill. Use when analyzing, summarizing, comparing, or extracting information from State Bank of Pakistan Quarterly Compendium or Financial Soundness Indicators (FSI) data, especially for bank-wise or system-wide non-performing loans (NPLs), capital adequacy ratio (CAR), and profitability indicators.
---

# SBP Financial Soundness Indicators

## Overview

Use this skill for State Bank of Pakistan Financial Soundness Indicators (FSI) data, published as a quarterly compendium of bank-level and system-level prudential ratios. This is the right skill for granular, ratio-based banking sector metrics rather than narrative commentary about the banking system.

## Coverage

- System-wide and bank-wise capital adequacy ratio (CAR) and its components (Tier 1, Tier 2 capital).
- Asset quality indicators: gross and net non-performing loans (NPLs), NPL ratios, and provisioning coverage.
- Profitability indicators: return on assets (ROA), return on equity (ROE), and net interest margin.
- Liquidity indicators: liquid assets to total assets, advances-to-deposits ratio.
- Published quarterly, generally with a lag, on `https://www.sbp.org.pk/ecodata/fsi.asp`.

## Use This Skill For

- extracting system-wide or bank-wise CAR for a specific quarter
- extracting gross or net NPL ratios and provisioning coverage
- comparing profitability ratios (ROA, ROE) across quarters or across banks
- tracking liquidity ratios such as advances-to-deposits ratio
- identifying trends in asset quality or capital buffers over multiple quarters

## Routing Rules

- Use this skill for specific prudential ratios (CAR, NPL, ROA, ROE) at the bank or system level.
- If the question is about a systemic risk narrative or stress-testing discussion rather than the underlying ratios themselves, prefer `sbp-financial-stability-review`.
- If the question is about monetary aggregates, credit growth, or money supply rather than bank soundness ratios, prefer `sbp-annual-report` or `pes-fiscal-financial-and-debt`.
- If the question is about a specific MPC rate decision rather than banking sector health, prefer `sbp-monetary-policy-statement`.

## Extraction Workflow

1. Identify whether the question needs a system-wide aggregate or a bank-wise breakdown.
2. Identify the exact quarter (e.g. "Q2 FY 2026" or "as of December 2025") since FSI data is point-in-time, not flow-based.
3. Locate the specific indicator table (capital, asset quality, profitability, or liquidity) rather than treating the compendium as one block.
4. Preserve whether a ratio is gross or net (especially for NPLs) and whether it is annualized (for ROA/ROE).
5. When comparing across quarters, align by the same reporting date convention SBP uses (typically end-of-quarter).

## Technical Rules

- Always specify whether an NPL figure is gross NPLs, net NPLs, or the NPL ratio (NPLs to gross advances).
- Distinguish CAR from Tier 1 capital ratio; they are related but not the same number.
- Keep bank-wise figures separate from system-wide aggregates in any comparison.
- Treat ROA/ROE as period ratios (often annualized) and note the basis if stated.

## Validation Checklist

- Confirm the reporting quarter and "as of" date for any cited ratio.
- Check whether the NPL figure is a ratio (percent) or an absolute rupee amount.
- Verify CAR is compared against the regulatory minimum requirement in effect for that period, since minimums can change.
- Confirm whether a profitability figure is for a single quarter or a cumulative year-to-date period.

## Common Pitfalls

- Confusing gross NPL ratio with net NPL ratio (after provisioning).
- Treating CAR and Tier 1 ratio as interchangeable.
- Comparing a single bank's ratio directly against a system-wide aggregate without noting the difference in scope.
- Citing a stale quarter's FSI data as current without checking the publication lag.

## Reference

- See [Financial Soundness Indicators Reference](references/financial-soundness-indicators.md) for compendium structure and extraction notes.
