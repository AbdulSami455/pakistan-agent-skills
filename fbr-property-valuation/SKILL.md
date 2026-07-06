---
name: fbr-property-valuation
description: FBR property valuation skill. Use when analyzing, summarizing, comparing, or extracting information from FBR notified property valuation tables and SROs, especially for city-wise property valuation rates used to compute capital gains tax and withholding tax on property transactions, as distinct from provincial DC (Deputy Commissioner) rates used for stamp duty.
---

# FBR Property Valuation

## Overview

Use this skill for FBR's notified property valuation tables, issued through SROs (Statutory Regulatory Orders) under Section 68 of the Income Tax Ordinance, 2001, on a per-city, irregular basis. These valuation rates set the minimum ("fair market") value FBR uses for federal tax purposes (capital gains tax, withholding tax on sale/purchase) on property transactions, distinct from market/DC (Deputy Commissioner) rates, which are a separate, typically lower, provincial valuation used for stamp duty and registration fee purposes.

## Coverage

- City-wise valuation tables: notified per-square-yard, per-square-foot, or per-marla rates for specified areas/sectors/blocks/phases within a city.
- **Coverage is incomplete and uneven across the country.** FBR has historically notified valuation tables for its major/high-transaction-volume cities first and in the most detail — most notably **Islamabad, Karachi, and Lahore** — with progressively less granular or later-arriving coverage for other large cities (e.g., Rawalpindi, Faisalabad, Multan, Peshawar, Quetta, Gujranwala, Sialkot, Hyderabad, and other provincial/divisional headquarters). Many smaller cities, towns, and rural areas have **no FBR-notified valuation table at all**, in which case FBR falls back to the DC rate (or another statutory default) for tax purposes in that area — do not assume every location in Pakistan has an FBR table.
- Revision cadence is **periodic but irregular, not on a guaranteed fixed schedule**. In practice, FBR has revised valuation tables roughly on an annual-ish cadence in recent years (as part of a broader push to align notified values closer to actual market values), but specific cities have gone multiple years without revision, and revisions for different cities are not synchronized — one city's table may be updated while another's remains unchanged for a longer period. Do not assume a fixed "every year" or "every July" revision cycle applies uniformly; always check the specific SRO date for the city/area in question.
- Valuation tables apply to both residential and commercial property categories where notified, and may distinguish open plots from constructed property (with constructed property sometimes valued via a combination of land rate plus a separate construction/covered-area rate).

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
- Confirm whether the city/area in question has an FBR-notified table at all before assuming one exists — coverage is incomplete, especially for smaller cities.

## Common Pitfalls

- Confusing FBR notified valuation rates with provincial DC rates, which serve a different (stamp duty) purpose and are typically lower.
- Applying a superseded SRO's rate to a transaction that falls under a newer notification.
- Assuming every city or every area within a notified city has a published valuation rate.
- Mixing up per-square-yard and per-marla rates when comparing tables across cities.
- Assuming a fixed annual revision cycle applies uniformly to every city's table when revisions are actually irregular and city-specific.

## Reference

- See [FBR Property Valuation Reference](references/fbr-property-valuation.md) for city coverage notes, revision-cadence caveats, and source-verification guidance.
