---
name: ndma-flood-sitreps
description: NDMA flood/disaster situation report skill. Use when tracking event-driven flood, monsoon, or disaster casualty, evacuation, relief, or damage figures from the National Disaster Management Authority's daily Situation Reports (SITREPs), especially during an active monsoon or flood emergency.
---

# NDMA Flood SITREPs

## Overview

Use this skill for Pakistan's event-driven disaster situation reporting, published daily (or as needed) by the National Disaster Management Authority (NDMA) during floods, monsoon emergencies, earthquakes, or other disasters. This is the right skill for casualty counts, relief camp status, and damage figures tied to a specific unfolding event — not for steady-state hydrological data or annual disaster-risk policy narrative.

## Coverage

- Daily Situation Reports (SITREPs) numbered sequentially within an event/season (e.g., "SITREP-51," "SITREP-87" for the 2025 monsoon), issued while an emergency is active and discontinued once the event concludes (e.g., after monsoon withdrawal).
- Typical SITREP content: rainfall spells and intensity, affected districts/provinces, fatalities and injuries, houses damaged/destroyed, livestock losses, infrastructure damage (roads, bridges), relief camps and persons sheltered, rescue operations conducted, and cumulative season-to-date totals.
- Published as PDF documents under the NDMA website's SITREPs section, organized by month/event.
- NDMA also issues broader "Situation Report" bulletins for non-flood disasters (earthquakes, landslides, glacial lake outburst floods) using a similar structure.

## Use This Skill For

- extracting fatality, injury, or displacement counts for a specific flood/monsoon event or date
- tracking cumulative season-to-date damage totals (houses, livestock, infrastructure)
- identifying which districts/provinces are currently or were affected by a specific event
- checking relief camp counts, persons sheltered, or rescue operation figures
- confirming whether NDMA is still actively issuing SITREPs for an event (i.e., whether the emergency is ongoing)

## When Not to Use This Skill

- For steady-state daily reservoir levels, inflows, or discharges — use `irsa-reservoir-data` instead; IRSA data is routine operational reporting, not emergency response.
- For the underlying rainfall observations that trigger flood events — use `pmd-weather-climate-data` instead; NDMA sitreps report disaster impact, not meteorological measurements.
- For annual water-resources policy narrative or climate/disaster-risk commentary — use `pes-infrastructure-digital-and-climate` instead.
- For long-term disaster-risk reduction planning or policy documents rather than a specific event's real-time figures.

## Routing Rules

- Use this skill only for event-driven, numbered SITREPs tied to an active or recently concluded disaster.
- Do not confuse this skill's casualty/damage figures with IRSA's daily reservoir/flow data; a flood event may reference both sources, but IRSA covers hydrology while NDMA covers human/infrastructure impact.
- If the question is about the season overall after SITREPs have stopped (e.g., "the 2025 monsoon"), treat the last-issued SITREP's cumulative total as the season's final tally unless NDMA later issues a consolidated after-action report.

## Extraction Workflow

1. Identify the specific event (e.g., "2025 monsoon floods") and the SITREP number or date needed.
2. Locate the matching SITREP PDF under the NDMA SITREPs section, filtered by month/event.
3. Distinguish single-day figures (this SITREP's new occurrences) from cumulative season-to-date totals — SITREPs typically report both.
4. Preserve the exact reporting date and SITREP number alongside any cited figure.
5. If a figure is later revised in a subsequent SITREP, prefer the most recent SITREP's cumulative figure and note the revision.

## Technical Rules

- Fatality, injury, and damage figures are provisional and subject to revision as verification continues; do not treat an early SITREP's figures as final without checking for a later update.
- Keep single-day (incremental) figures separate from cumulative season-to-date figures — SITREPs present both and conflating them overstates or understates the true picture.
- Province/district-level figures should sum toward the national cumulative total; investigate large discrepancies as a reporting-lag issue rather than assuming an error.
- SITREP numbering resets or restarts across distinct disaster seasons/years; do not compare "SITREP-51" across two different years as if they were the same point in the season.

## Validation Checklist

- Confirm the SITREP number and issue date for any cited figure.
- Verify whether a figure is a single-day increment or a cumulative season-to-date total.
- Check whether NDMA has issued a more recent SITREP that revises the figure being cited.
- Confirm which event/season the SITREP belongs to before comparing across years.

## Common Pitfalls

- Citing an early SITREP's casualty count as final when later SITREPs revised it upward or downward.
- Confusing incremental daily figures with cumulative totals when reporting a season's impact.
- Treating NDMA SITREP figures as equivalent to IRSA's operational hydrological data, which serves a different purpose.
- Continuing to reference SITREPs as "ongoing" after NDMA has formally discontinued daily issuance for a concluded event.

## Reference

- See [NDMA SITREPs Reference](references/ndma-flood-sitreps.md) for source structure and extraction notes.
