---
name: sbp-financial-stability-review
description: SBP Financial Stability Review skill. Use when analyzing, summarizing, comparing, or extracting information from the State Bank of Pakistan's annual Financial Stability Review, especially for its systemic risk assessment of banks, non-bank financial institutions (NBFIs), and the insurance sector.
---

# SBP Financial Stability Review

## Overview

Use this skill for the State Bank of Pakistan's annual Financial Stability Review (FSR), which provides a systemic, forward-looking risk assessment of the financial sector rather than a snapshot of individual ratios. This is the right skill for narrative discussion of systemic vulnerabilities, stress-test results, and the SBP's own view of where risks are building.

## Coverage

- Banking sector risk assessment: credit risk, market risk, liquidity risk, and concentration risk at a system level.
- Non-bank financial institutions (NBFIs): risk discussion for entities such as DFIs, leasing companies, and microfinance banks.
- Insurance sector risk commentary, usually a smaller section relative to banking.
- Systemic risk survey results and stress-testing summaries, where included.
- Published annually by SBP, distinct from the quarterly FSI ratio tables.

## Use This Skill For

- summarizing SBP's assessment of systemic risk to the banking sector for a given year
- extracting stress-test results or scenario analysis described in the review
- identifying SBP's stated vulnerabilities in NBFIs or the insurance sector
- comparing systemic risk narrative across consecutive annual reviews
- extracting the review's outlook or policy recommendations for financial sector resilience

## Routing Rules

- Use this skill for the narrative, systemic risk assessment, not for the underlying quarterly ratios.
- If the question is about specific CAR, NPL, or profitability figures, prefer `sbp-financial-soundness-indicators`.
- If the question is about insurance industry statistics (premiums, assets, takaful figures) rather than systemic risk narrative, prefer `secp-insurance-industry-statistics`.
- If the question is about monetary policy decisions rather than financial-sector risk, prefer `sbp-monetary-policy-statement`.
- If the question is about SBP's broader annual economic narrative, prefer `sbp-annual-report`; use this skill specifically when the focus is systemic financial risk.

## Extraction Workflow

1. Identify whether the question is about banks, NBFIs, insurance, or a cross-cutting systemic risk theme.
2. Locate the relevant sector chapter or risk theme section in the review.
3. Preserve whether a statement is a current assessment, a stress-test scenario result, or a forward-looking risk flag.
4. Note the review's coverage year/period explicitly, since publication can lag the assessment period.
5. When the review references specific ratios (e.g. CAR, NPLs) to support its narrative, cross-check consistency with `sbp-financial-soundness-indicators` if precision is needed.

## Technical Rules

- Do not present stress-test results as realized outcomes; they are hypothetical scenario analyses.
- Keep banking-sector risk commentary distinct from NBFI and insurance-sector commentary.
- Preserve qualifiers such as "moderate," "elevated," or "contained" risk language exactly as the review states them.
- Attribute systemic risk survey findings to the survey respondents (often financial sector experts), not to SBP's own independent assessment, when the review distinguishes the two.

## Validation Checklist

- Confirm which fiscal year or assessment period the review covers.
- Check whether a risk statement applies to the banking sector specifically or the financial system broadly.
- Verify stress-test assumptions (e.g. shock size) are reported alongside the result.
- Distinguish the review's narrative risk language from any FSI-style ratio it cites for support.

## Common Pitfalls

- Treating a stress-test outcome as an actual current condition of the banking system.
- Conflating banking-sector risk narrative with NBFI or insurance-sector risk narrative.
- Citing the review's risk assessment without the coverage period, leading to stale comparisons.
- Confusing systemic risk survey perception data with SBP's own analytical conclusions.

## Reference

- See [Financial Stability Review Reference](references/financial-stability-review.md) for review structure and extraction notes.
