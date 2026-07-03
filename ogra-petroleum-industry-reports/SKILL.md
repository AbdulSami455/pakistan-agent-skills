---
name: ogra-petroleum-industry-reports
description: OGRA petroleum industry reports skill. Use when analyzing, summarizing, comparing, or extracting information from the Oil and Gas Regulatory Authority's annual "State of the Regulated Petroleum Industry" report, OGRA annual reports, or petroleum-sector statistical publications, especially for oil/gas production, consumption, pipeline infrastructure, LPG/LNG, and regulated petroleum pricing data.
---

# OGRA Petroleum Industry Reports

## Overview

Use this skill for questions about Pakistan's regulated petroleum and natural gas sector as reported by the Oil and Gas Regulatory Authority (OGRA). This covers OGRA's annual "State of the Regulated Petroleum Industry" report and related statistical publications on oil/gas production, consumption, pipeline infrastructure, LPG/LNG supply, and regulated pricing — distinct from power-sector reporting under NEPRA or macro energy narratives in the PES.

## Coverage

- Published annually by OGRA, typically as the "State of the Regulated Petroleum Industry" report plus supporting statistical annexes.
- Typical content: indigenous crude oil and natural gas production volumes; petroleum product consumption by type (motor spirit, HSD, furnace oil, etc.); natural gas allocation by sector (power, fertilizer, domestic, CNG, industry); pipeline and storage infrastructure statistics; LPG and LNG import/supply volumes; regulated consumer prices for petroleum products and natural gas; refinery throughput and capacity utilization.
- OGRA also publishes periodic price notifications and tariff determinations for regulated petroleum products; this skill covers the annual statistical/industry reports, not individual price-notification bulletins unless the question is about the historical price series within the annual report.

## Use This Skill For

- extracting indigenous crude oil or natural gas production volumes
- breaking down petroleum product consumption by product type
- extracting natural gas allocation or consumption by sector
- identifying LPG/LNG supply or import volumes
- comparing regulated petroleum product prices over time as tabulated in OGRA reports
- sourcing pipeline infrastructure or refinery throughput statistics for the regulated petroleum sector

## Routing Rules

- Use this skill for the regulated petroleum and natural gas sector (OGRA's mandate). For electricity generation, distribution, or DISCO-level power statistics, use `nepra-state-of-industry` instead.
- For forward-looking power capacity planning, use `igcep-capacity-plan`; OGRA reports cover realized petroleum-sector performance, not power-sector capacity plans.
- For the Pakistan Economic Survey's narrative-level energy chapter (covering both power and petroleum at a high level), use `pes-infrastructure-digital-and-climate` for the summary narrative and this skill for petroleum-specific detail.
- For customs-recorded petroleum import values or trade volumes, prefer `pes-external-sector` or `tdap-trade-reports`; this skill covers regulated domestic production, consumption, and pricing rather than customs trade records.
- Individual NEPRA electricity tariff determinations are covered by `nepra-tariff-determinations`; OGRA covers petroleum product and natural gas pricing under its own regulatory framework.

## Extraction Workflow

1. Identify the report year and whether the question needs production, consumption, infrastructure, or pricing data.
2. Locate the relevant statistical table by product type or sector rather than relying on narrative summary text.
3. Preserve whether a figure is indigenous production, imports, or total supply — OGRA reports typically distinguish these.
4. Note the unit (barrels, MMCFD, metric tons, liters) exactly as tabulated.
5. For price data, confirm whether the figure is a regulated consumer price, a producer price, or an import parity reference price.

## Technical Rules

- Do not mix crude oil production figures with petroleum product consumption figures; they are different product categories with different units.
- Natural gas is typically reported in MMCFD (million cubic feet per day) or BCM (billion cubic meters); preserve the unit used in the source table.
- LPG and LNG are distinct supply categories; do not conflate LPG cylinder supply with LNG terminal regasification volumes.
- Regulated prices in OGRA reports reflect notified prices at a point in time; they may differ from market/import-parity references cited elsewhere in the same report.

## Validation Checklist

- Confirm the report year and whether the figure is production, consumption, or supply (including imports).
- Verify the product category (crude, motor spirit, HSD, natural gas, LPG, LNG) matches the question.
- Check the unit before quoting any volume figure.
- Distinguish indigenous production from total supply when both appear in the same table.

## Common Pitfalls

- Conflating OGRA petroleum-sector data with NEPRA power-sector data as if they were the same regulatory domain.
- Mixing crude oil production (barrels) with petroleum product consumption (metric tons or liters) without noting the product distinction.
- Citing a regulated consumer price as if it were the import-parity or producer price.
- Treating natural gas allocation to the power sector as equivalent to actual electricity generated from gas.

## Reference

- See [OGRA Petroleum Industry Reference](references/ogra-petroleum-industry-reports.md) for report structure and extraction notes.
