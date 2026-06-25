---
name: provincial-budget-documents
description: Provincial budget documents skill. Use when analyzing, summarizing, comparing, or extracting information from a provincial Finance Department's budget books (Punjab, Sindh, Khyber Pakhtunkhwa, or Balochistan), especially for provincial allocations, the Annual Development Programme (ADP), and own-receipts, which the Pakistan Economic Survey's fiscal chapter does not cover since it is federal-consolidated only.
---

# Provincial Budget Documents

## Overview

Use this skill for provincial government budget documents published by the Finance Department of Punjab, Sindh, Khyber Pakhtunkhwa, or Balochistan. The Pakistan Economic Survey's fiscal chapter reports federal-consolidated fiscal figures only; this skill is necessary whenever the question needs province-specific allocations, development spending, or own-source revenue.

## Coverage

- White Paper / Budget speech: each province's narrative summary of budget priorities and headline allocations.
- Schedule of New Expenditure and Annual Budget Statement: detailed current and development expenditure by department/grant.
- Annual Development Programme (ADP): province-specific development scheme allocations, often listed scheme-by-scheme.
- Own-receipts/own-source revenue tables: provincial tax and non-tax revenue (e.g. provincial sales tax on services, agriculture income tax, property tax) distinct from federal transfers under the NFC award.

## Use This Skill For

- extracting a specific province's total or department-wise budget allocation for a fiscal year
- identifying ADP scheme-wise development allocations for a province
- extracting a province's own-receipts (own-source revenue) figures and their composition
- comparing budget allocations or development spending across two or more provinces for the same fiscal year
- distinguishing a province's own revenue from its federal transfer (NFC share) in the budget

## Routing Rules

- Use this skill whenever the question specifically names a province or otherwise needs sub-national fiscal detail.
- The Pakistan Economic Survey's fiscal chapter (`pes-fiscal-financial-and-debt`) is federal-consolidated; it will not have province-specific ADP or own-receipts detail, so route there only for the federal/consolidated picture or NFC transfer totals.
- If the question is about the federal budget's own documents rather than a province's, prefer `federal-budget-documents`.
- If the question is about provincial tax collection statistics in granular tax-head form, note that FBR's `fbr-yearbook` covers federal taxes only; provincial revenue authorities (e.g. PRA, SRB, KPRA, BRA) are the source for provincial tax-head detail, which this skill's budget documents summarize at a higher level.

## Extraction Workflow

1. Identify which specific province's budget document the question needs; treat each province's budget as a separate, non-interchangeable document.
2. Confirm the fiscal year, and whether the figure requested is a budget estimate, revised estimate, or actual/outturn figure if the document presents all three.
3. For ADP questions, locate the specific scheme or sector heading within the ADP table rather than relying on the aggregate ADP size alone.
4. For own-receipts questions, separate provincial tax revenue (e.g. provincial sales tax on services, agriculture income tax) from non-tax receipts and from the federal NFC transfer, which is a distinct budget line.
5. When comparing provinces, align by the same fiscal year and the same budget-estimate/revised/actual basis before drawing conclusions.

## Technical Rules

- Do not conflate a province's own-source revenue with its total resources, which include the federal NFC transfer and may include loans/grants.
- Keep current expenditure and development expenditure (ADP) separate; they serve different budget functions and are reported in different tables.
- Preserve each province's department and grant naming conventions exactly, since they are not standardized identically across provinces.
- Label every figure as budget estimate, revised estimate, or actual, consistent with how the source document presents it.

## Validation Checklist

- Confirm which province's document is being cited and that it is not mixed up with another province's figures.
- Verify whether the cited figure is from the ADP (development) or the current budget.
- Check whether own-receipts figures exclude the federal NFC transfer as they should.
- Confirm the fiscal year and estimate/actual basis match across any cross-province comparison.

## Common Pitfalls

- Treating one province's budget structure or terminology as identical to another's.
- Mixing federal NFC transfers into a province's "own-receipts" figure.
- Confusing ADP (development) allocations with total provincial expenditure.
- Comparing a budget estimate from one province against a revised estimate from another without flagging the basis mismatch.

## Reference

- See [Provincial Budget Documents Reference](references/provincial-budget-documents.md) for document structure and extraction notes.
