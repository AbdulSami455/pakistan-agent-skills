---
name: suparco-space-research
description: SUPARCO (Space and Upper Atmosphere Research Commission) skill. Use when explaining Pakistan's national space program — satellite missions, space applications (remote sensing, satellite communications), and SUPARCO's research mandate — as distinct from PTA's telecom regulation or general meteorological data.
---

# SUPARCO Space Research

## Overview

Use this skill for Pakistan's national space agency, the Space and Upper Atmosphere Research Commission (SUPARCO), established as a committee in 1961 and granted commission status in 1981. This is a general reference skill on Pakistan's space program structure and mission history — not a live satellite-tracking service and not a substitute for SUPARCO's own current mission-status pages.

## Coverage

- Mandate: research and development in space science, technology, and applications for peaceful purposes and socio-economic development, spanning satellite communications, remote sensing/earth observation, space science research, and upper-atmosphere research.
- Satellite programs: Pakistan's satellite history spans communications satellites (e.g., the PAKSAT series, operating in geostationary orbit for communications/broadcast relay) and remote-sensing/earth-observation satellites (e.g., the PRSS/Pakistan Remote Sensing Satellite series), each serving different application purposes.
- Applications: remote sensing data supports agriculture monitoring, disaster management, land-use mapping, and resource assessment; satellite communications support broadcast relay and connectivity; SUPARCO also engages in space science research (upper atmosphere, meteorology-adjacent research) and human spaceflight-related cooperation on specific missions.
- Organizational footprint: headquartered in Islamabad with technical facilities/ground stations in multiple cities (Karachi, Lahore, Multan, Quetta, Peshawar, Gilgit).
- International cooperation: SUPARCO has partnered with other national space agencies (e.g., China's space program) on specific satellite launches and, more recently, astronaut/human-spaceflight-related cooperation.

## Use This Skill For

- explaining SUPARCO's general mandate and organizational history
- distinguishing Pakistan's communications satellites from its remote-sensing/earth-observation satellites
- describing general applications of Pakistan's space program (agriculture monitoring, disaster management, connectivity)
- providing background on a specific named Pakistani satellite mission's general purpose
- clarifying SUPARCO's role relative to other Pakistani technical/regulatory bodies (e.g., not a telecom regulator, not a weather-forecasting body)

## When Not to Use This Skill

- For telecom licensing, spectrum, or connectivity statistics — use `pta-telecom-indicators` instead; SUPARCO builds/operates certain communications satellite infrastructure, but telecom-sector regulation itself is PTA's mandate.
- For weather forecasts or meteorological/climate data — use `pmd-weather-climate-data` instead; PMD (Pakistan Meteorological Department) is the operational weather-data body, distinct from SUPARCO's space-research mandate even though both touch atmospheric science.
- For a specific satellite's real-time operational/orbital status — this skill provides general mission background, not live tracking; direct to SUPARCO's official current announcements for that.

## Routing Rules

- Use this skill for general background on SUPARCO's mandate, satellite program history, and space-applications context.
- If the question is about telecom infrastructure/connectivity regulation rather than the space agency itself, route to `pta-telecom-indicators`.
- If the question is about weather forecasting or climate data rather than the space agency's research/satellite mandate, route to `pmd-weather-climate-data`.

## Extraction Workflow

1. Identify whether the question concerns SUPARCO's general mandate, a specific satellite/mission, or a specific application area (remote sensing, communications, research).
2. If a specific satellite is named, identify which program family it belongs to (communications/PAKSAT-type vs. remote-sensing/PRSS-type) since these serve different purposes and should not be conflated.
3. For application-area questions, connect the space-program capability (e.g., remote sensing) to its general use case (e.g., agriculture monitoring, disaster assessment) without asserting specific current operational data unless sourced from SUPARCO directly.
4. Note any international cooperation partner for a specific mission if relevant, rather than presenting a mission as entirely indigenous when it involved a cooperation partner.

## Technical Rules

- Keep communications satellites (broadcast/connectivity relay) and remote-sensing/earth-observation satellites (imagery/data collection) conceptually distinct; they serve different functions despite both being "SUPARCO satellites."
- SUPARCO is a research/space-technology body, not a telecom regulator (PTA) or weather-forecasting agency (PMD); do not describe it as performing those distinct mandates.
- Mission-specific technical details (launch date, orbital parameters, current operational status) should be treated as needing verification against SUPARCO's current official announcements rather than assumed static.

## Validation Checklist

- Confirm whether the question needs general mandate/background information or a specific mission's detail.
- Verify a named satellite's program family (communications vs. remote sensing) before describing its purpose.
- Check that SUPARCO's role is not conflated with PTA's telecom regulation or PMD's weather-forecasting mandate.
- Flag any specific mission's current operational status as needing confirmation against SUPARCO's official source.

## Common Pitfalls

- Confusing SUPARCO's communications satellites with its remote-sensing satellites as if they served the same purpose.
- Treating SUPARCO as a telecom regulator or weather-forecasting agency rather than a space research/technology body.
- Presenting a specific satellite mission's current operational status as certain without flagging the need for verification.
- Omitting an international cooperation partner when describing a jointly developed/launched mission.

## Reference

- See [SUPARCO Reference](references/suparco-space-research.md) for programme structure and extraction notes.
