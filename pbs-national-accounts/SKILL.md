---
name: pbs-national-accounts
description: PBS National Accounts skill. Use when analyzing, summarizing, comparing, or extracting information from the Pakistan Bureau of Statistics Quarterly National Accounts (QNA) releases or annual national accounts publications, especially for quarterly GDP growth, sectoral value-added breakdowns, or expenditure-side GDP components at a higher frequency than the Pakistan Economic Survey.
---

# PBS National Accounts

## Overview

Use this skill for questions about Pakistan's official national accounts statistics published by the Pakistan Bureau of Statistics (PBS), particularly the Quarterly National Accounts (QNA) releases and the annual national accounts compendium. This is the right skill when the task needs quarterly GDP growth, sectoral value-added detail, or expenditure-side GDP components at a higher frequency or with more methodological detail than the Pakistan Economic Survey's annual macro chapter provides.

## Coverage

- Quarterly National Accounts (QNA): published by PBS on a quarterly basis, reporting GDP at current and constant prices, growth rates by quarter, and sectoral value-added breakdowns (agriculture, industry, services) for the reference quarter and cumulative fiscal-year-to-date figures.
- Annual National Accounts: PBS publishes a more comprehensive annual national accounts volume with detailed supply-use tables, sectoral accounts, and historical time series.
- Typical indicators: GDP growth rate (overall and by sector), gross value added by economic activity, expenditure-side components (consumption, investment, government spending, net exports), GDP at current prices and constant prices (with base year noted).
- PBS is the official producer of national accounts statistics; the Pakistan Economic Survey cites PBS national accounts figures but does not replace PBS as the primary source for quarterly or methodological detail.

## Use This Skill For

- extracting quarterly GDP growth rates or fiscal-year-to-date GDP growth
- breaking down GDP growth by sector (agriculture, industry, services)
- extracting expenditure-side GDP components (private consumption, investment, government consumption, net exports)
- comparing provisional vs. revised national accounts figures across release vintages
- sourcing the official base year and constant-price methodology for GDP series

## Routing Rules

- Use this skill for quarterly or detailed annual national accounts data from PBS. For the Pakistan Economic Survey's annual macro narrative (headline GDP growth, broad stabilization commentary), prefer `pes-macro-and-prices` — that chapter summarizes the year using PBS figures but does not carry quarterly detail.
- If the question is about inflation rather than real GDP growth, prefer `pbs-cpi-spi-wpi-bulletins` for high-frequency price data or `pes-macro-and-prices` for the annual inflation narrative.
- If the question is about fiscal aggregates (deficit, revenue, expenditure) rather than GDP, prefer `pes-fiscal-financial-and-debt` or `federal-budget-documents`.
- SBP's own GDP commentary in the Annual Report or Monetary Policy Statement should be cross-referenced with PBS national accounts for the underlying figures; prefer this skill for the official PBS numbers.

## Extraction Workflow

1. Identify whether the question needs quarterly data (QNA release) or annual data (annual national accounts volume).
2. Confirm the reference quarter or fiscal year and whether the figure is provisional or revised.
3. Preserve whether the figure is at current prices or constant prices, and note the base year for constant-price series.
4. For sectoral breakdowns, extract from the value-added table rather than inferring from narrative text.
5. Distinguish quarter-on-quarter growth from year-on-year or fiscal-year-to-date cumulative growth.

## Technical Rules

- Do not mix current-price and constant-price GDP figures without explicit labeling.
- Preserve the base year used for constant-price calculations (Pakistan has rebased its national accounts periodically; the base year changes across vintages).
- Quarter-on-quarter, year-on-year, and fiscal-year-to-date growth rates are different metrics; label the basis explicitly.
- Provisional QNA figures are often revised in subsequent releases; note the release vintage if comparing across periods.

## Validation Checklist

- Confirm the reference quarter or fiscal year.
- Verify whether the figure is at current or constant prices.
- Check the base year for constant-price series.
- Confirm whether the growth rate is quarter-on-quarter, year-on-year, or fiscal-year-to-date.
- Note whether the figure is provisional or revised.

## Common Pitfalls

- Citing PES headline GDP growth without checking whether a more recent PBS QNA revision exists.
- Mixing current-price GDP levels with constant-price growth rates.
- Confusing fiscal-year-to-date cumulative growth with single-quarter growth.
- Using an outdated base year when comparing GDP levels across years that span a rebasing event.

## Reference

- See [PBS National Accounts Reference](references/national-accounts.md) for release structure and extraction notes.
