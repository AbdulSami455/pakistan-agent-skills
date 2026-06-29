---
name: irsa-reservoir-data
description: IRSA Daily Reservoir Data skill. Use when analyzing, summarizing, comparing, or extracting information from the Indus River System Authority's Daily Data on Tarbela, Mangla, and Chashma reservoir water levels, inflows, discharges, and canal withdrawals, especially for day-to-day or short-period hydrological operational tracking.
---

# IRSA Reservoir Data

## Overview

Use this skill for Pakistan's daily operational hydrological data published by the Indus River System Authority (IRSA), covering reservoir levels and river system flows at Tarbela, Mangla, and Chashma, plus canal withdrawals. This is the right skill for day-by-day or short-period operational water data, not for annual narrative-style water-resources commentary found elsewhere.

## Coverage

- Published daily by IRSA on the "Daily Data" page of pakirsa.gov.pk (the authority's actual operating domain — note this is distinct from irsa.gov.pk, which is not the correct source).
- Typical content per daily release: reservoir water level (feet) and live storage (acre-feet) for Tarbela, Mangla, and Chashma; daily inflow and outflow/discharge at each reservoir and key barrages; canal head withdrawals (e.g., for major canal commands); comparison against the same date in the previous year and against minimum operating level/conservation level thresholds.
- Data is presented as daily tables/bulletins, not as a narrative report; there is no fixed "page structure" — each day's bulletin follows a consistent tabular template.

## Use This Skill For

- extracting a specific date's reservoir level, live storage, inflow, or outflow for Tarbela, Mangla, or Chashma
- comparing current reservoir levels against the prior year's level on the same date
- tracking short-period (daily/weekly) trends in river system inflows or canal withdrawals
- assessing how close a reservoir is to its minimum operating level or conservation/dead storage level
- supporting flood or drought-risk monitoring with real-time hydrological figures

## When Not to Use This Skill

- For annual water-resources policy narrative, irrigation infrastructure investment, or broader water-sector discussion — check whether a PES chapter or another sectoral skill is more appropriate.
- For event-driven flood casualty, evacuation, or damage figures — use `ndma-flood-sitreps` instead; IRSA data is steady-state operational reporting, not emergency updates.
- For long-term generation capacity planning involving hydel projects — use `igcep-capacity-plan` instead.

## Routing Rules

- Use this skill for IRSA's daily operational data specifically. If a question is about annual water-resources policy narrative, irrigation infrastructure investment, or broader water-sector discussion, that falls outside this skill's scope — check whether a PES chapter or another sectoral skill is more appropriate, since this skill does not cover narrative content.
- Do not confuse this skill's daily tabular data with NDMA flood situation reports; IRSA data is steady-state operational reporting, while flood sitreps are event-driven emergency updates (see `ndma-flood-sitreps` if available).
- Always use pakirsa.gov.pk as the source; irsa.gov.pk is not IRSA's operating domain for this data.

## Extraction Workflow

1. Identify the exact date (or date range) of the bulletin being referenced.
2. Identify which reservoir/barrage (Tarbela, Mangla, Chashma, or a specific barrage) the figure belongs to.
3. Distinguish "level" (feet, an elevation reading) from "storage" (acre-feet, a volume) from "inflow/outflow" (cusecs, a flow rate).
4. Note the same-date-prior-year comparison figure separately from the current reading if both are present.
5. Check the reservoir's stated minimum operating level or dead storage level before describing a reading as critically low.

## Technical Rules

- Keep units exact: water level in feet, storage in acre-feet (or MAF for larger aggregates), flow in cusecs.
- Tarbela, Mangla, and Chashma have different capacities and operating thresholds; do not apply one reservoir's threshold to another.
- Inflow and outflow/discharge are distinct figures; a reservoir can be filling (inflow > outflow) or depleting (outflow > inflow) — preserve the direction.
- Canal withdrawal figures are downstream of reservoir releases and should not be confused with reservoir discharge itself.

## Validation Checklist

- Confirm the exact date of the data point before quoting it.
- Verify whether the unit is feet (level), acre-feet (storage), or cusecs (flow) before quoting a figure.
- Check which specific reservoir or barrage the figure refers to.
- If comparing to "last year," confirm the comparison date is the same calendar date, not just the same month.

## Common Pitfalls

- Citing irsa.gov.pk as the source instead of the correct pakirsa.gov.pk Daily Data page.
- Confusing reservoir water level (feet) with live storage (acre-feet).
- Treating a single day's reading as a seasonal trend without checking surrounding days.
- Mixing up inflow and outflow direction, which reverses the interpretation of whether a reservoir is filling or depleting.

## Reference

- See [IRSA Reservoir Data Reference](references/irsa-reservoir-data.md) for reservoir thresholds and unit definitions.
