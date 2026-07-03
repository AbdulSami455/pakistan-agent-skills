---
name: karachi-port-cargo-reports
description: Karachi Port Cargo Reports skill. Use when analyzing, summarizing, comparing, or extracting information from Karachi Port Trust's daily and periodic shipping and cargo handling reports, especially for vessel arrival/berthing statistics and cargo throughput by commodity type at Karachi Port.
---

# Karachi Port Cargo Reports

## Overview

Use this skill for Karachi Port Trust's operational shipping and cargo statistics, covering daily or periodic reports on vessel movement and cargo throughput. This is the right skill for Karachi Port-level operational data, as distinct from national trade-volume statistics or annual narrative reports on the maritime sector.

## Coverage

- Published by Karachi Port Trust (KPT) on a daily/periodic basis, covering vessel arrivals, berthing, and cargo handled at Karachi Port's terminals.
- Typical content: vessel-wise arrival and berthing schedule (vessel name, type, arrival date, berth assigned); cargo handled per vessel or per terminal, broken down by commodity type (e.g., containers, bulk grain, coal, POL products, general cargo); cumulative throughput statistics (daily, monthly, or fiscal-year-to-date) by terminal; sometimes vessel waiting-time or port productivity indicators.
- Periodic/monthly summaries may aggregate the daily reports into commodity-wise or terminal-wise totals for the period.
- Document/data is operational and tabular; there is no fixed narrative page structure, and reports are typically short, frequently issued bulletins or statistical summaries rather than long-form documents.

## Use This Skill For

- extracting vessel arrival/berthing counts for a specific date or period at Karachi Port
- identifying cargo throughput by commodity type (containers, bulk, liquid cargo) for a given period
- comparing terminal-wise cargo handling performance within Karachi Port
- tracking cumulative fiscal-year-to-date cargo volumes at Karachi Port
- distinguishing Karachi Port's own statistics from national port/maritime aggregate figures

## Routing Rules

- Use this skill for Karachi Port-specific operational data. If the question is about Port Qasim, use `port-qasim-cargo-reports`; if about Gwadar Port, use `gwadar-port-cargo-reports`.
- Use this skill instead of PES or TDAP trade skills when the question is about physical cargo/vessel handling rather than customs-recorded trade value; tonnage handled at a port and the value of goods traded are different concepts that should not be conflated.
- If the question is about national-level total seaborne trade volume, this skill alone (Karachi Port only) is insufficient; note that Port Qasim and Gwadar Port handle separate, non-overlapping volumes.

## Extraction Workflow

1. Identify the exact date or period the report covers before extracting any figure.
2. Distinguish vessel-count statistics (arrivals/berthings) from cargo-volume statistics (tonnage/TEU handled); these are different metrics.
3. Preserve commodity-type detail (containers, bulk grain, coal, POL, general cargo) rather than collapsing into "total cargo" unless asked.
4. Note which terminal within Karachi Port a figure belongs to, if the report specifies terminal-wise detail.
5. Check whether a cumulative figure is daily, monthly, or fiscal-year-to-date before describing a trend.

## Technical Rules

- Container volumes are typically measured in TEUs (twenty-foot equivalent units), while bulk and liquid cargo are measured in metric tons; do not mix these units without conversion context.
- Vessel count and cargo tonnage do not scale linearly (vessel sizes vary widely); do not infer tonnage trends from vessel-count trends alone.
- Keep Karachi Port's figures separate from Port Qasim Authority or Gwadar Port Authority figures; they are independently operated and reported.
- Daily reports are operational snapshots; monthly/periodic summaries are aggregates — confirm which type of document is being read before treating a figure as a period total.

## Validation Checklist

- Confirm the exact date or period covered before quoting a figure.
- Verify whether the figure is a vessel count or a cargo volume.
- Check the unit (TEU vs. metric tons) before quoting a cargo figure.
- Confirm the figure is specific to Karachi Port and not conflated with other Pakistani ports.

## Common Pitfalls

- Conflating Karachi Port's cargo statistics with Port Qasim's or Gwadar Port's separate statistics.
- Mixing TEU container counts with metric-ton bulk cargo figures as if they were the same unit.
- Treating a single day's vessel/cargo snapshot as representative of a monthly or annual trend.
- Citing port cargo tonnage as if it were equivalent to the customs-recorded trade value of the goods.

## Reference

- See [Karachi Port Cargo Reports Reference](references/karachi-port-cargo-reports.md) for terminal and commodity-category notes.
