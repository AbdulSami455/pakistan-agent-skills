---
name: pmd-weather-climate-data
description: PMD weather and climate data skill. Use when analyzing, summarizing, comparing, or extracting information from the Pakistan Meteorological Department's weather observations, climate summaries, seasonal forecasts, or extreme-event reports, especially for temperature, rainfall, humidity, and climate normals for Pakistani cities and regions.
---

# PMD Weather and Climate Data

## Overview

Use this skill for questions about Pakistan's official weather observations, climate summaries, and meteorological forecasts as published by the Pakistan Meteorological Department (PMD). This covers station-level and city-level weather data, monthly/annual climate normals, seasonal forecasts, and extreme-event reports — distinct from climate-policy narrative in the Pakistan Economic Survey or disaster situational reports from NDMA.

## Coverage

- Daily and monthly weather observations: temperature (maximum, minimum, mean), rainfall, humidity, wind speed/direction, recorded at PMD weather stations across Pakistan.
- Climate normals: long-term average values for temperature and rainfall by station/month, used as baselines for anomaly reporting.
- Seasonal forecasts: PMD's monsoon, winter, and other seasonal outlooks for Pakistan.
- Extreme-event reports: heatwave, cold wave, heavy rainfall, flood-triggering rainfall, or drought-related meteorological bulletins issued by PMD.
- Historical climate data archives: station-wise time series accessible through PMD's website or data services.

## Use This Skill For

- extracting temperature or rainfall observations for a specific city, station, or period
- identifying monthly or annual climate normals for a location
- sourcing PMD seasonal forecast outlooks (monsoon, winter)
- comparing observed weather against climate normals (anomaly analysis)
- identifying PMD extreme-event bulletins for heatwaves, cold spells, or heavy rainfall

## Routing Rules

- Use this skill for PMD weather observations, climate normals, and meteorological forecasts. For climate-change policy narrative in the annual economic survey, prefer `pes-infrastructure-digital-and-climate` (Chapter 17: Climate Change).
- For flood emergency situational reports (damages, affected population, relief operations), prefer `ndma-flood-sitreps`; PMD provides the meteorological trigger (rainfall amounts, forecast) while NDMA reports the disaster response impact.
- For reservoir inflows and dam operational levels driven by rainfall, prefer `irsa-reservoir-data` for the water-management side and this skill for the underlying rainfall observations.
- PMD climate normals and PES climate chapter narratives serve different purposes; do not conflate a station rainfall total with a national climate-policy statistic.

## Extraction Workflow

1. Identify the weather station or city, the variable (temperature, rainfall, humidity, etc.), and the time period.
2. Preserve whether the figure is an observed value, a climate normal (long-term average), or a forecast.
3. Note the unit (degrees Celsius, millimeters of rainfall, percent humidity) exactly as reported.
4. For seasonal forecasts, preserve the forecast period and confidence language rather than treating outlooks as realized outcomes.
5. For extreme-event bulletins, distinguish the meteorological measurement from downstream disaster impact reported by other agencies.

## Technical Rules

- Temperature may be reported as maximum, minimum, or mean daily/monthly values; preserve the type.
- Rainfall is typically in millimeters (mm); do not confuse with inches unless the source explicitly uses imperial units.
- Climate normals are long-term averages (typically 30-year baselines); observed values should be compared against the correct normal period.
- Seasonal forecasts are probabilistic outlooks, not deterministic predictions; preserve the forecast framing.
- Station names may differ from city or district administrative names; confirm the station location before joining to other datasets.

## Validation Checklist

- Confirm the station/city, variable, and time period.
- Verify whether the figure is observed, a climate normal, or a forecast.
- Check the unit before quoting.
- For anomaly analysis, confirm the normal baseline period used.

## Common Pitfalls

- Treating a seasonal forecast as a realized weather outcome.
- Mixing maximum and mean temperature without labeling which type.
- Citing a single station's rainfall as representative of a whole province or river basin.
- Conflating PMD meteorological measurements with NDMA disaster impact statistics.

## Reference

- See [PMD Weather and Climate Reference](references/pmd-weather-climate-data.md) for source structure and extraction notes.
