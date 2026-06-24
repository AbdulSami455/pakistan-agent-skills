---
name: tdap-trade-reports
description: TDAP Trade Reports skill. Use when analyzing, summarizing, comparing, or extracting information from the Trade Development Authority of Pakistan's Monthly Trade Reports and Annual Trade Reports, especially for export and import summaries by product category, destination market, and trade-promotion-oriented detail at a more granular or higher-frequency level than the Pakistan Economic Survey.
---

# TDAP Trade Reports

## Overview

Use this skill for Pakistan's export/import statistics as published by the Trade Development Authority of Pakistan (TDAP), in its Monthly Trade Reports and Annual Trade Reports. This is the right skill for monthly-cadence, trade-promotion-agency framing of trade performance — product-category and destination-market detail intended to support exporters — rather than the Pakistan Economic Survey's annual macro-level external sector narrative.

## Coverage

- Published by TDAP (tdap.gov.pk); Monthly Trade Reports issued monthly, Annual Trade Reports issued yearly, both based on PBS customs trade data compiled and re-presented with trade-promotion framing.
- Typical structure: overall export/import summary for the month or year, with year-over-year and month-over-month comparisons; product-category breakdown (textiles, leather, rice, surgical goods, sports goods, IT services where covered, etc.); destination-market breakdown (major export destinations such as the US, EU, China, and regional partners); commentary on specific sector performance, trade missions, or exhibitions; sometimes import breakdown by major commodity groups.
- Document is structure-based with monthly/annual statistical tables; exact section order and length vary by edition.

## Use This Skill For

- extracting monthly or annual export/import totals by product category
- identifying top destination markets for a specific export category
- tracking month-over-month or year-over-year growth in a specific sector's exports
- sourcing trade-promotion-agency commentary on sector-specific performance or initiatives
- cross-checking PBS-based customs trade figures at a finer product/market granularity than PES provides

## Routing Rules

- Use this skill for monthly-cadence, granular, product/market-level trade detail. Use `pes-external-sector` for the Pakistan Economic Survey's annual narrative on trade and payments, current account, remittances, and reserves — PES does not carry TDAP's product/market granularity or monthly cadence.
- If the question is about balance-of-payments framing (current account, reserves) rather than customs-recorded merchandise trade, route to `pes-external-sector` or an SBP balance-of-payments skill instead.
- Use this skill only for trade-promotion-agency framed reports; do not use it for PBS's own primary trade statistics releases if a separate PBS trade skill exists.

## Extraction Workflow

1. Identify whether the report is a Monthly Trade Report or an Annual Trade Report, and the exact month/year covered.
2. Identify whether the figure is an export or import value, and which product category or destination market it belongs to.
3. Preserve the comparison basis (month-over-month, year-over-year, or cumulative fiscal-year-to-date) exactly as stated.
4. Keep currency units (typically US$ million) exact; do not convert to PKR unless asked.
5. Separate trade-promotion commentary (missions, exhibitions, policy asks) from the underlying statistical figures.

## Technical Rules

- Product categories should be preserved at the granularity TDAP uses (e.g., "knitwear" vs. "woven garments" within textiles), not flattened into "textiles" generally unless asked for an aggregate.
- Destination-market figures are typically export-side; do not assume the same breakdown exists for imports unless the report provides it.
- Cumulative fiscal-year-to-date figures (e.g., "July-March") must be kept distinct from single-month figures.
- TDAP figures originate from PBS customs data; note this lineage if asked about the ultimate data source.

## Validation Checklist

- Confirm whether the report is monthly or annual before quoting a figure.
- Verify the exact month or fiscal-year period covered.
- Check whether the figure is for a single product category, a sector aggregate, or total exports/imports.
- Confirm the comparison basis (MoM, YoY, or cumulative) before describing growth or decline.

## Common Pitfalls

- Treating a single month's figure as representative of the full fiscal year.
- Conflating TDAP's promotion-oriented commentary with hard customs statistics.
- Mixing export destination-market detail with import source-country detail without checking which the report actually provides.
- Using this skill's figures interchangeably with PES's external sector figures without checking for reporting basis or period differences.

## Reference

- See [TDAP Trade Reports Reference](references/tdap-trade-reports.md) for structure notes and category definitions.
