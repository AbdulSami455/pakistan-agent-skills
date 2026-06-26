---
name: fbr-yearbook
description: FBR Year Book skill. Use when analyzing, summarizing, comparing, or extracting information from the Federal Board of Revenue Year Book, especially for granular tax collection statistics broken down by tax head, sector, or withholding category, which is more detailed than the high-level revenue figures in the Pakistan Economic Survey's fiscal chapter.
---

# FBR Year Book

## Overview

Use this skill for the Federal Board of Revenue (FBR) Year Book, an annual statistical publication with detailed tax collection breakdowns. This is the right skill when a task needs granular figures — by tax head, sector, or withholding category — that go beyond the aggregate revenue numbers reported in the Pakistan Economic Survey's fiscal chapter.

## Coverage

- Tax-head breakdown: direct taxes (income tax), and indirect taxes (sales tax, federal excise duty, customs duty), each with sub-components.
- Sector-wise collection: tax contribution by major economic sectors (e.g. manufacturing, telecom, oil and gas, banking).
- Withholding tax categories: collection broken down by withholding tax provisions (e.g. salary, contracts, imports, dividends, profit on debt).
- Time-series tables: multi-year collection trends by tax head, usually for the past five to ten years.
- Published annually by FBR, typically covering the fiscal year just completed.

## Use This Skill For

- extracting tax collection figures for a specific tax head (income tax, sales tax, FED, customs)
- identifying sector-wise tax contribution for a specific industry
- extracting withholding tax collection by category (e.g. salary withholding vs. import withholding)
- tracing a tax head's collection trend across multiple fiscal years
- reconciling FBR Year Book detail against the PES's aggregate revenue figure for the same year

## Routing Rules

- Use this skill when the task needs tax-head, sector, or withholding-category granularity.
- If the question only needs the high-level total FBR tax collection or tax-to-GDP ratio for the year, the PES fiscal chapter (`pes-fiscal-financial-and-debt`) may already have it; use this skill when more detail is required or to verify the PES figure against the underlying breakdown.
- If the question is about customs tariff rates or HS-code-level duty structure rather than collection statistics, prefer `fbr-customs-tariff`.
- If the question is about property valuation rates used for withholding tax on property transactions, prefer `fbr-property-valuation`.

## Extraction Workflow

1. Identify the specific tax head, sector, or withholding category the question needs.
2. Locate the corresponding table in the Year Book rather than relying on summary chapters alone.
3. Confirm the fiscal year and whether the figure is provisional or final/audited collection.
4. Preserve the exact tax-head terminology FBR uses (e.g. distinguishing "sales tax on goods" from "sales tax on services," where applicable, given provincial sales tax on services is collected separately by provinces).
5. When comparing across years, align by fiscal year and check for any reclassification of tax heads between editions.

## Technical Rules

- Do not merge federal sales tax (on goods) with provincial sales tax on services; FBR generally collects only the federal component.
- Keep gross collection figures separate from net collection (after refunds) where the Year Book distinguishes them.
- Preserve sector classifications exactly as FBR labels them; do not re-bucket sectors without noting the change.
- Withholding tax categories should be quoted with their specific provision/category label, not collapsed into "withholding tax" generally.

## Validation Checklist

- Confirm whether a collection figure is gross or net of refunds.
- Verify the fiscal year and provisional/final status of the figure.
- Check that sector or withholding-category labels match FBR's own terminology, not an assumed equivalent.
- Cross-check tax-head totals against the aggregate revenue figure for consistency before using both in the same answer.

## Common Pitfalls

- Confusing federal sales tax with provincial sales tax on services.
- Treating provisional collection figures as final audited figures.
- Mixing up withholding tax sub-categories (e.g. salary vs. contracts vs. imports).
- Double-counting a tax head that appears in both a summary table and a detailed breakdown table.

## Reference

- See [FBR Year Book Reference](references/fbr-yearbook.md) for table structure and extraction notes.
