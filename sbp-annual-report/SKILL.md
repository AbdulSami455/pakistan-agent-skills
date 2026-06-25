---
name: sbp-annual-report
description: SBP Annual Report skill. Use when analyzing, summarizing, comparing, or extracting information from the State Bank of Pakistan Annual Report, especially its "State of the Economy" narrative and statistical annexes, where the task needs SBP's own monetary and external sector framing rather than the Ministry of Finance's Pakistan Economic Survey.
---

# SBP Annual Report

## Overview

Use this skill for questions about the State Bank of Pakistan's Annual Report, published as part of SBP's statutory reporting (the "State of the Economy" report plus statistical annexes). This is SBP's own central-bank perspective on the economy and is distinct in framing, mandate, and emphasis from the Ministry of Finance's Pakistan Economic Survey.

## Coverage

- "State of the Economy" narrative section: covers real sector, fiscal, monetary, and external sector performance from the central bank's vantage point, typically for the fiscal year just closed.
- Statistical annexes: detailed tables on monetary aggregates, banking sector data, balance of payments, and government borrowing from SBP.
- Published annually, generally with a stronger monetary-policy and financial-stability framing than the PES.

## Use This Skill For

- summarizing SBP's own assessment of the fiscal year's macroeconomic performance
- extracting SBP's narrative on monetary policy conduct and its rationale across the year
- pulling statistical annex tables on money supply, credit to private sector, or banking aggregates
- comparing SBP's framing of external sector developments with the same period's PES treatment
- identifying SBP's stated risks or outlook for the following fiscal year

## Routing Rules

- Use this skill when the user specifically wants the State Bank's own narrative or its annexed statistics, not the government's consolidated economic survey.
- If the question is purely about a single MPC rate decision, prefer `sbp-monetary-policy-statement`, which is meeting-specific and more current.
- If the question is about systemic bank soundness (NPLs, CAR) prefer `sbp-financial-soundness-indicators`; for a systemic risk narrative prefer `sbp-financial-stability-review`.
- If the question is about the government's own fiscal-year narrative across all sectors, prefer the relevant `pes-*` skill; use this skill when the user explicitly wants SBP's perspective or when reconciling differences between SBP and the Ministry of Finance.
- For monthly/quarterly external statistics rather than the annual narrative, prefer `sbp-balance-of-payments-bulletin`.

## Extraction Workflow

1. Identify whether the question needs the narrative ("State of the Economy") section or a statistical annex table.
2. Locate the relevant subsection by topic heading (e.g. monetary policy review, banking sector, external sector) rather than scanning the full report.
3. Preserve the exact fiscal year the report covers and distinguish it from the report's publication date.
4. Note whether figures are SBP's own estimates or are sourced from other agencies (PBS, Ministry of Finance) and cited within the report.
5. When comparing to PES, keep the two sources separate in the answer and flag any numerical discrepancy rather than silently reconciling it.

## Technical Rules

- Do not present SBP Annual Report figures as identical to PES figures without checking; period definitions and provisional/final status can differ.
- Preserve whether monetary aggregates are stock (end-of-period) or flow (change-over-period) figures.
- Keep banking-sector statistics distinct from FSI-style soundness indicators unless the annex explicitly contains them.
- Attribute outlook or risk statements to SBP specifically when contrasting with government messaging.

## Validation Checklist

- Confirm the fiscal year covered matches the year referenced in the question.
- Check whether a cited figure comes from the narrative text or a statistical annex table, and prefer the table for precise values.
- Verify monetary aggregate figures are not confused between broad money (M2) and reserve money.
- Note any explicit SBP caveats about data provisionality.

## Common Pitfalls

- Treating SBP Annual Report and PES as interchangeable sources for the same indicator without checking definitions.
- Confusing the report's narrative outlook with realized historical performance.
- Mixing up money-supply growth rates with credit-growth rates.
- Citing annex table totals without checking the stated unit (billions of rupees vs. percent of GDP).

## Reference

- See [Annual Report Reference](references/annual-report.md) for report structure and extraction notes.
