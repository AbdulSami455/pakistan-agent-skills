---
name: gwadar-port-cargo-reports
description: Gwadar Port Cargo Reports skill. Use when analyzing, summarizing, comparing, or extracting information from Gwadar Port Authority's periodic shipping and cargo handling reports, especially for vessel arrival/berthing statistics and cargo throughput by commodity type at Gwadar Port — noting that Gwadar's actual operational volume and public reporting frequency are much smaller/sparser than Karachi Port or Port Qasim.
---

# Gwadar Port Cargo Reports

## Overview

Use this skill for Gwadar Port Authority's operational shipping and cargo statistics, covering periodic reports on vessel movement and cargo throughput. This is the right skill for Gwadar Port-level operational data, as distinct from national trade-volume statistics or annual narrative reports on the maritime sector.

**Important caveat up front:** despite Gwadar Port's high strategic profile under the China-Pakistan Economic Corridor (CPEC), its actual operational cargo throughput has historically been **much lower and far more irregular** than Karachi Port or Port Qasim, which together handle the overwhelming majority of Pakistan's seaborne trade. Gwadar has operated well below its designed capacity for most of its history, with intermittent commercial shipping activity, periods of near-dormancy, and public reporting that is sparser and less frequent/standardized than Karachi Port Trust's or Port Qasim Authority's regular statistical bulletins. Treat any Gwadar cargo figure as a small-scale, possibly incomplete data point rather than assuming Gwadar-level reporting has the same regularity or granularity as the two major ports — and be prepared to fall back to other sources (see Routing Rules) when GPA-specific data is thin or unavailable for a requested period.

## Coverage

- Published by Gwadar Port Authority (GPA) on a periodic basis (frequency is irregular in practice), covering vessel arrivals, berthing, and cargo handled at Gwadar Port's terminals.
- Typical content when available: vessel-wise arrival and berthing records (vessel name, type, arrival date, berth assigned); cargo handled per vessel or per terminal, broken down by commodity type; cumulative throughput statistics (monthly or fiscal-year-to-date); sometimes vessel waiting-time or port productivity indicators.
- Realistic commodity mix at Gwadar, reflecting its early-stage/limited operational status: mostly **bulk and general cargo** (e.g., wheat, fertilizer, construction materials, project cargo related to CPEC infrastructure works) rather than significant containerized trade. Container (TEU) throughput at Gwadar has historically been minimal to negligible compared to Karachi Port's or Port Qasim's container terminals — do not assume Gwadar has a comparable container business just because it is a modern deep-water port.
- Periodic/monthly summaries, where they exist, may aggregate reports into commodity-wise or terminal-wise totals for the period, but continuity across periods is not guaranteed — gaps in publicly available reporting are common.
- Document/data is operational and tabular where available; Gwadar Port's reporting frequency and detail level differ substantially from Karachi Port or Port Qasim given its much smaller operational scale and the port's phased development status.

## Use This Skill For

- extracting vessel arrival/berthing counts for a specific date or period at Gwadar Port
- identifying cargo throughput by commodity type for a given period at Gwadar Port
- tracking cumulative fiscal-year-to-date cargo volumes at Gwadar Port
- distinguishing Gwadar Port's own statistics from national port/maritime aggregate figures

## Routing Rules

- Use this skill for Gwadar Port-specific operational data. If the question is about Karachi Port, use `karachi-port-cargo-reports`; if about Port Qasim, use `port-qasim-cargo-reports`.
- Use this skill instead of PES or TDAP trade skills when the question is about physical cargo/vessel handling rather than customs-recorded trade value; tonnage handled at a port and the value of goods traded are different concepts that should not be conflated.
- If the question is about national-level total seaborne trade volume, this skill alone (Gwadar Port only) is insufficient; note that Karachi Port and Port Qasim handle the overwhelming majority of Pakistan's seaborne cargo, and Gwadar's contribution to the national total is comparatively marginal.
- **When GPA-specific data is sparse, outdated, or unavailable for the requested period**, do not fabricate a plausible-looking figure. Instead, note the gap explicitly and suggest fallback sources that sometimes carry Gwadar-related throughput or project-status updates: the **Ministry of Maritime Affairs** (Gwadar Port's parent federal ministry, which periodically reports on port performance in budget documents and policy statements), and the **CPEC Authority** (which publishes updates on Gwadar-related infrastructure and operational milestones as part of CPEC progress reporting). These are secondary/fallback sources, not substitutes for GPA's own data when it exists.
- If the question is really about Gwadar's broader development (Free Zone, airport, city infrastructure) rather than port cargo/vessel statistics, flag that this skill covers port cargo operations specifically, not the wider Gwadar development project.

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
- If no current GPA data is available for the requested period, confirm this gap explicitly rather than estimating or inferring a number, and note fallback sources checked (Ministry of Maritime Affairs, CPEC Authority).

## Common Pitfalls

- Conflating Gwadar Port's cargo statistics with Karachi Port's or Port Qasim's separate statistics.
- Mixing TEU container counts with metric-ton bulk cargo figures as if they were the same unit.
- Treating Gwadar Port volumes as representative of national port throughput — Gwadar is a small fraction of Pakistan's total seaborne cargo compared to Karachi Port and Port Qasim.
- Citing port cargo tonnage as if it were equivalent to the customs-recorded trade value of the goods.
- Assuming Gwadar has regular, Karachi/Port-Qasim-style monthly reporting cadence and granularity when its actual public reporting has historically been sparse and irregular.
- Assuming significant containerized (TEU) trade at Gwadar when its realistic cargo mix has been dominated by bulk/general and project-related cargo.

## Reference

- See [Gwadar Port Cargo Reports Reference](references/gwadar-port-cargo-reports.md) for terminal/commodity notes, the low-throughput caveat, and fallback-source guidance.
