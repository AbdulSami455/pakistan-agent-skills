---
name: pakistan-railways-yearbook
description: Pakistan Railways Yearbook skill. Use when analyzing, summarizing, comparing, or extracting information from the Pakistan Railways annual Yearbook, especially for passenger and freight traffic volumes, route/section performance, and the organization's financial performance.
---

# Pakistan Railways Yearbook

## Overview

Use this skill for Pakistan Railways' own annual statistical and financial reporting, drawn from the Pakistan Railways Yearbook. This is the right skill for passenger/freight volume statistics and Pakistan Railways' financial performance, as distinct from the Pakistan Economic Survey's brief transport-sector narrative.

## Coverage

- Published annually by Pakistan Railways (Ministry of Railways), covering the preceding fiscal year.
- Typical structure: passenger traffic statistics (passengers carried, passenger-kilometers, by class and by major route/section); freight traffic statistics (tonnage carried, ton-kilometers, by major commodity group such as cement, coal, POL, container/general goods); locomotive and rolling stock inventory and utilization; financial performance (revenue by passenger/freight segment, operating expenses, profit/loss position, government subsidy); infrastructure statistics (track length, stations, electrification where applicable); safety statistics (accidents, incidents) in some editions.
- Document is structure-based with annexed statistical and financial tables; exact chapter/page layout varies by edition.

## Use This Skill For

- extracting passenger or freight volume statistics for a specific year
- comparing freight tonnage by commodity group across years
- sourcing Pakistan Railways' revenue, expense, or subsidy figures
- tracking locomotive/rolling stock fleet size and utilization
- describing route/section-level traffic performance

## Routing Rules

- Use this skill for Pakistan Railways' own detailed statistical and financial reporting. Use `pes-infrastructure-digital-and-climate` only for the Pakistan Economic Survey's transport and communications chapter, which summarizes rail performance briefly and does not carry route-level or commodity-level granularity.
- If the question is about freight competition with road transport or broader logistics-sector policy, treat the Yearbook as a data source only; policy narrative may sit elsewhere.

## Extraction Workflow

1. Identify the fiscal year covered by the Yearbook edition before extracting any figure.
2. Distinguish passenger statistics (passengers carried, passenger-km) from freight statistics (tonnage, ton-km); these are reported separately.
3. Preserve commodity-group detail for freight (e.g., cement, coal, POL, containers) rather than collapsing into "total freight" unless asked.
4. Separate revenue/expense figures by segment (passenger vs. freight) if the source table does so.
5. Note whether a financial figure is operating revenue/expense or includes government subsidy/grant.

## Technical Rules

- Passenger-kilometers and ton-kilometers are distance-weighted measures, distinct from raw passenger/tonnage counts; do not conflate them.
- Keep locomotive/rolling stock counts (a stock measure) separate from utilization rates (a flow/efficiency measure).
- Financial figures should specify whether they are pre- or post-subsidy; Pakistan Railways has historically operated with a government subsidy that materially affects the "profit/loss" framing.
- Route/section-level figures should retain the named route; do not generalize a single route's performance to the national network.

## Validation Checklist

- Confirm the fiscal year before quoting any traffic or financial figure.
- Verify whether a figure is passenger or freight before quoting volume statistics.
- Check whether tonnage/passenger figures are raw counts or distance-weighted (ton-km/passenger-km).
- Confirm whether a financial figure includes government subsidy.

## Common Pitfalls

- Conflating passenger count with passenger-kilometers, which can move in different directions if average trip length changes.
- Treating freight tonnage growth as profitability without checking the financial statements separately.
- Citing a single commodity group's freight figure as representative of total freight volume.
- Omitting the subsidy context when describing Pakistan Railways' financial performance.

## Reference

- See [Pakistan Railways Yearbook Reference](references/pakistan-railways-yearbook.md) for structure notes and metric definitions.
