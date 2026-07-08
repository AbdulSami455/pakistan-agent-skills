---
name: pakistan-earthquake-seismic-hazard
description: Pakistan earthquake and seismic hazard skill. Use when analyzing, summarizing, comparing, or extracting information from Pakistan's earthquake bulletins, seismic event catalogs, and hazard-zonation references, especially for epicenter, magnitude, depth, aftershocks, and regional seismic-risk context.
---

# Pakistan Earthquake and Seismic Hazard

## Overview

Use this skill for earthquake events and seismic-risk context in Pakistan: event magnitude, depth, epicenter, aftershock sequences, and regional hazard framing. This is the right skill when the task is about seismic observations or hazard interpretation, not about general geography or disaster-loss reporting.

## Coverage

- PMD seismic monitoring bulletins and earthquake event notices.
- Geological Survey of Pakistan hazard and geoscience references where they provide fault, tectonic, or hazard-zone context.
- NDMA or engineering-hazard material only insofar as it references seismic exposure and preparedness zones rather than post-disaster relief.
- Event-level details such as origin time, latitude/longitude, depth, magnitude, and felt-region summaries.
- Regional seismic context for northern Pakistan, Balochistan, the Chaman fault system, Hindukush deep events, and Kashmir-region seismicity.

## Use This Skill For

- extracting event details for a named earthquake
- summarizing an aftershock sequence or repeated tremors in a region
- distinguishing shallow crustal events from deep Hindukush events
- describing seismic hazard context for a province or district
- identifying whether an item is an observed event bulletin or a static hazard-zonation reference

## When Not to Use This Skill

- For disaster casualty counts, damaged buildings, or relief operations after an earthquake, use NDMA or relevant disaster-response sources instead.
- For topographic or tourism descriptions of mountain regions, use `pakistan-tourism-heritage` instead.
- For geology and mineral occurrence, use `pakistan-geology-mineral-resources` instead.

## Routing Rules

- Use this skill for earthquake observations, seismic catalogs, and hazard context.
- If the question asks what happened after the quake in humanitarian terms, separate the seismic event from the disaster-impact report.
- If the task is about a fault zone, tectonic setting, or seismic hazard map interpretation, this skill is correct even if no recent earthquake bulletin is involved.
- If the task is about mining geology rather than seismicity, route to `pakistan-geology-mineral-resources`.

## Extraction Workflow

1. Identify whether the question is about an individual event, a sequence, or a hazard-zone reference.
2. Preserve event parameters exactly: magnitude scale if specified, depth, origin time, and epicenter area.
3. Note whether the source is reporting an observed event, a felt report, or a hazard map / explanatory document.
4. If multiple events are involved, keep them ordered by date and time.
5. Distinguish hazard-zone narrative from actual observed earthquake counts.

## Technical Rules

- Magnitude, intensity, and damage are different concepts; do not substitute one for another.
- Deep Hindukush earthquakes can be widely felt with less local surface damage than shallow events; preserve depth context.
- A seismic hazard map is a long-horizon planning tool, not a record of recent earthquakes.
- Aftershock sequences should not be merged into a single count unless the source does so explicitly.
- Epicenter labels are approximate location descriptions layered over coordinates; preserve both when available.

## Validation Checklist

- Confirm the event date and local/UTC time basis if the source specifies it.
- Verify the magnitude and depth before quoting.
- Check whether the source is a live event bulletin or a static hazard reference.
- Confirm the region naming, especially where a cross-border or offshore event is still felt in Pakistan.

## Common Pitfalls

- Confusing magnitude with intensity or damage severity.
- Treating a hazard-zone map as evidence of a recent earthquake event.
- Ignoring event depth when interpreting felt impact.
- Folding separate aftershocks into one unqualified earthquake total.

## Reference

- See [Pakistan Earthquake and Seismic Hazard Reference](references/pakistan-earthquake-seismic-hazard.md) for source structure, event fields, and hazard-context notes.
