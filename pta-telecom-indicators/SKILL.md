---
name: pta-telecom-indicators
description: PTA Telecom Indicators skill. Use when extracting granular subscriber, teledensity, broadband penetration, or operator-level revenue data from the Pakistan Telecommunication Authority's published Telecom Indicators tables or PTA Annual Report.
---

# PTA Telecom Indicators

## Overview

Use this skill for granular, operator- or subscriber-level telecom data: cellular/broadband/fixed-line subscriber counts, teledensity, broadband penetration, and revenue broken down by operator or service category. This is the regulator's own structured indicator data, distinct from macro-level digital-economy narrative.

## Coverage

PTA publishes data in two main forms:

- **Telecom Indicators** tables (updated periodically, often monthly/quarterly), typically covering: total cellular subscribers, total broadband subscribers, fixed-line subscribers, teledensity (%), broadband penetration (%), and sometimes 3G/4G subscriber counts
- **PTA Annual Report**, a fuller narrative-plus-tables document covering: sector overview, operator-level market share, revenue and investment figures, regulatory actions, spectrum allocation, consumer protection/complaints data, and policy developments for the fiscal year

Typical structure of the Annual Report includes a sector performance chapter, financial/revenue chapter (often broken down by cellular, fixed-line, LDI, broadband/ISP categories), and an annexure section with detailed indicator tables by operator.

## Use This Skill For

- extracting cellular, broadband, or fixed-line subscriber counts for a specific period
- calculating or quoting teledensity and broadband penetration rates
- finding operator-level (e.g., Jazz, Telenor/Ufone-PTCL group entities, Zong) subscriber or revenue figures
- extracting telecom sector revenue broken down by category (cellular, fixed, LDI, broadband/ISP)
- tracking trends in subscriber growth or churn across reporting periods

## Routing Rules

- Use this skill, not `pes-infrastructure-digital-and-climate`, when the task needs operator-level or subscriber-level granularity (e.g., "how many broadband subscribers did operator X have in Q2").
- Use `pes-infrastructure-digital-and-climate` instead when the task is about the Economic Survey's macro-narrative framing of IT/telecom — e.g., IT export growth, digital transformation policy, or broad connectivity narrative without operator-level breakdown.
- If a task needs both (e.g., "what does PES say about telecom growth and what do the actual PTA subscriber numbers show"), use both skills together and label which source each figure came from.

## Extraction Workflow

1. Identify whether the question needs a point-in-time indicator (use Telecom Indicators tables) or a fuller annual narrative/financial breakdown (use the Annual Report).
2. Identify the specific reporting period — PTA indicator tables are typically updated monthly or quarterly; confirm the "as of" date before quoting a figure.
3. Distinguish subscriber categories carefully: cellular/mobile, fixed-line (wireline), broadband (which may include both fixed and mobile broadband), and WLL where still reported.
4. For operator-level figures, extract from the annexure/operator-breakdown tables rather than sector aggregates.
5. Preserve revenue figures' currency and whether they are gross revenue, net revenue, or specific to a sub-category (cellular vs. fixed vs. LDI vs. ISP).

## Technical Rules

- Teledensity and broadband penetration are typically expressed as percentages of population (or of population using a specific denominator basis) — note the denominator basis if stated.
- Mobile broadband and fixed broadband subscriber counts can be reported separately or combined; do not assume which without checking the table header.
- Operator names and corporate structures can change (mergers, rebranding) — verify which operator a historical figure refers to if comparing across years.
- Preserve whether a figure is a stock (total subscribers at period end) or a flow (net additions during the period).

## Validation Checklist

- Confirm the reporting period ("as of" date) for any indicator quoted.
- Confirm whether broadband figures include both fixed and mobile broadband or only one.
- Check whether revenue figures are sector-wide or operator-specific, and which sub-category they cover.
- Verify operator names against the current PTA-licensed operator list if reporting market-share comparisons.

## Common Pitfalls

- Treating "broadband subscribers" as fixed-broadband only when it may include mobile broadband (and vice versa).
- Reporting teledensity without noting the denominator basis or reporting period.
- Mixing up SIM/connection counts with unique subscriber counts, since multi-SIM ownership is common.
- Citing PES's macro IT/telecom narrative as if it carries the same subscriber-level granularity as PTA's own indicator tables.

## Reference

- PTA publishes Telecom Indicators and Annual Reports on its official website; exact table numbering and indicator sets can shift between releases.
