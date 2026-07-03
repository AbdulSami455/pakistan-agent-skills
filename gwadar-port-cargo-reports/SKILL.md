---
name: gwadar-port-cargo-reports
description: Gwadar Port Cargo Reports skill. Use when analyzing, summarizing, comparing, or extracting information from Gwadar Port Authority's periodic shipping and cargo handling reports, especially for vessel arrival/berthing statistics and cargo throughput by commodity type at Gwadar Port.
---

# Gwadar Port Cargo Reports

## Overview

Use this skill for Gwadar Port Authority's operational shipping and cargo statistics, covering periodic reports on vessel movement and cargo throughput. This is the right skill for Gwadar Port-level operational data, as distinct from national trade-volume statistics or annual narrative reports on the maritime sector.

## Coverage

- Published by Gwadar Port Authority (GPA) on a periodic basis, covering vessel arrivals, berthing, and cargo handled at Gwadar Port's terminals.
- Typical content: vessel-wise arrival and berthing records (vessel name, type, arrival date, berth assigned); cargo handled per vessel or per terminal, broken down by commodity type (e.g., containers, bulk cargo, POL products, general cargo); cumulative throughput statistics (monthly or fiscal-year-to-date); sometimes vessel waiting-time or port productivity indicators.
- Periodic/monthly summaries may aggregate reports into commodity-wise or terminal-wise totals for the period.
- Document/data is operational and tabular; Gwadar Port's reporting frequency and detail level may differ from Karachi Port or Port Qasim given its smaller operational scale.

## Use This Skill For

- extracting vessel arrival/berthing counts for a specific date or period at Gwadar Port
- identifying cargo throughput by commodity type for a given period at Gwadar Port
- tracking cumulative fiscal-year-to-date cargo volumes at Gwadar Port
- distinguishing Gwadar Port's own statistics from national port/maritime aggregate figures

## Routing Rules

- Use this skill for Gwadar Port-specific operational data. If the question is about Karachi Port, use `karachi-port-cargo-reports`; if about Port Qasim, use `port-qasim-cargo-reports`.
- Use this skill instead of PES or TDAP trade skills when the question is about physical cargo/vessel handling rather than customs-recorded trade value; tonnage handled at a port and the value of goods traded are different concepts that should not be conflated.
- If the question is about national-level total seaborne trade volume, this skill alone (Gwadar Port only) is insufficient; note that Karachi Port and Port Qasim handle separate, non-overlapping volumes.

## Extraction Workflow

1. Identify the exact date or period the report covers before extracting any figure.
2. Distinguish vessel-count statistics (arrivals/berthings) from cargo-volume statistics (tonnage/TEU handled); these are different metrics.
3. Preserve commodity-type detail rather than collapsing into "total cargo" unless asked.
4. Check whether a cumulative figure is monthly or fiscal-year-to-date before describing a trend.
5. Note that Gwadar Port's operational volume is typically much smaller than Karachi or Port Qasim; do not extrapolate national trends from Gwadar-only figures.

## Technical Rules

- Container volumes are typically measured in TEUs (twenty-foot equivalent units), while bulk and liquid cargo are measured in metric tons; do not mix these units without conversion context.
- Vessel count and cargo tonnage do not scale linearly (vessel sizes vary widely); do not infer tonnage trends from vessel-count trends alone.
- Keep Gwadar Port's figures separate from Karachi Port Trust or Port Qasim Authority figures; they are independently operated and reported.
- Periodic reports are aggregates; confirm which type of document is being read before treating a figure as a period total.

## Validation Checklist

- Confirm the exact date or period covered before quoting a figure.
- Verify whether the figure is a vessel count or a cargo volume.
- Check the unit (TEU vs. metric tons) before quoting a cargo figure.
- Confirm the figure is specific to Gwadar Port and not conflated with other Pakistani ports.

## Common Pitfalls

- Conflating Gwadar Port's cargo statistics with Karachi Port's or Port Qasim's separate statistics.
- Mixing TEU container counts with metric-ton bulk cargo figures as if they were the same unit.
- Treating Gwadar Port volumes as representative of national port throughput.
- Citing port cargo tonnage as if it were equivalent to the customs-recorded trade value of the goods.

## Reference

- See [Gwadar Port Cargo Reports Reference](references/gwadar-port-cargo-reports.md) for terminal and commodity-category notes.
