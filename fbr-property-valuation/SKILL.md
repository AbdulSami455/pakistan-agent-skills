---
name: fbr-property-valuation
description: FBR property valuation skill. Use when analyzing, summarizing, comparing, or extracting information from FBR notified property valuation tables and SROs, especially for city-wise property valuation rates used to compute capital gains tax and withholding tax on property transactions.
---

# FBR Property Valuation

## Overview

Use this skill for FBR's notified property valuation tables, issued through SROs (Statutory Regulatory Orders) on a per-city, irregular basis. These valuation rates set the minimum value FBR uses for tax purposes (capital gains tax, withholding tax) on property transactions, distinct from market/DC (Deputy Commissioner) rates.

## Coverage

- City-wise valuation tables: notified per-square-yard or per-square-foot rates for specified areas/sectors/blocks within a city.
- Coverage is irregular and city-specific — not all cities are notified at the same time, and tables are revised periodically through new SROs rather than on a fixed annual cycle.
- Valuation tables apply to both residential and commercial property categories where notified, and may distinguish open plots from constructed property.

## Use This Skill For

- looking up the FBR-notified valuation rate for a specific area/sector/block in a notified city
- determining which SRO is currently in force for a given city's valuation table
- comparing valuation rates before and after a specific SRO revision
- explaining how the notified valuation rate interacts with capital gains tax or withholding tax computation on a property transaction
- identifying whether a given city/area has an FBR-notified valuation table at all, since coverage is incomplete

## Routing Rules

- Use this skill specifically for FBR's own notified valuation tables used for federal tax purposes (capital gains tax, withholding tax under the Income Tax Ordinance).
- Do not confuse FBR valuation tables with provincial Deputy Commissioner (DC) rates, which are a separate, typically lower, valuation used for provincial stamp duty; if the question is about DC rates or provincial stamp duty, that falls outside this skill's source material.
- If the question is about FBR's aggregate withholding tax collection statistics on property rather than the per-area rate itself, prefer `fbr-yearbook`.
- If the question is about provincial budget allocations rather than property valuation, prefer `provincial-budget-documents`.

## Extraction Workflow

1. Identify the exact city and area/sector/block named in the question; FBR valuation tables are granular and rates vary significantly within the same city.
2. Identify the specific SRO currently notified for that city/area, since rates are revised through new SROs rather than a single consolidated annual table.
3. Distinguish residential vs. commercial categories, and open plot vs. constructed property valuation, where the table provides separate rates.
4. Note the effective date of the SRO in force; do not apply a superseded SRO's rates to a transaction dated after a newer SRO took effect.
5. When the question is about tax computation, clarify that the notified value is a floor/reference value FBR uses, not necessarily the actual transaction price.

## Technical Rules

- Always cite the specific SRO number and its notified date when stating a valuation rate, since multiple SROs can apply to the same city over time.
- Do not apply a valuation rate from one city or area to another without explicit confirmation; rates are not transferable across locations.
- Preserve the unit of measurement exactly as notified (per square yard, per square foot, or per marla) since units vary by table.
- Treat unnotified areas as having no FBR valuation table; do not assume a default or estimated rate exists.

## Validation Checklist

- Confirm the city and specific area/sector/block match the notified table being cited.
- Verify the SRO number and effective date used are the most recent applicable to the transaction date in question.
- Check whether the rate cited is for residential, commercial, or a combined category.
- Confirm the unit of measurement before using the rate in any calculation.

## Common Pitfalls

- Confusing FBR notified valuation rates with provincial DC rates, which serve a different (stamp duty) purpose and are typically lower.
- Applying a superseded SRO's rate to a transaction that falls under a newer notification.
- Assuming every city or every area within a notified city has a published valuation rate.
- Mixing up per-square-yard and per-marla rates when comparing tables across cities.
