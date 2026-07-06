# PMD Weather and Climate Data Reference

## Source

- Pakistan Meteorological Department (PMD)
- Official website: `https://www.pmd.gov.pk`
- Weather observations and forecasts: check "Weather" or "Forecast" sections
- Climate data and normals: check "Climate" or "Climate Data Processing Centre" sections
- Seasonal forecasts: published as monsoon/winter outlook bulletins on the PMD website

## Typical Data Types

- Daily/monthly temperature (max, min, mean) in degrees Celsius
- Daily/monthly rainfall in millimeters (mm)
- Humidity, wind speed/direction, sunshine hours
- Climate normals (long-term averages, typically 30-year baselines)
- Seasonal forecasts (monsoon, winter outlooks)
- Extreme-event bulletins (heatwave, cold wave, heavy rainfall)

## Station Notes

- PMD operates weather stations across Pakistan; station names may not match administrative district names exactly.
- Confirm station location before joining to district-level statistics from other sources.

## Major Observation Stations/Cities

PMD's observation network includes stations at all major Pakistani cities, commonly cited in weather bulletins and climate summaries. Well-known major stations include:

- **Karachi** (coastal Sindh — hot, humid coastal climate regime)
- **Lahore** (Punjab plains)
- **Islamabad** (Islamabad/Rawalpindi area, Potohar plateau — also the location of PMD's head office)
- **Peshawar** (Khyber Pakhtunkhwa)
- **Quetta** (Balochistan — high-altitude, arid/semi-arid regime with cold winters, distinct from lowland stations)
- **Multan** (southern Punjab)
- **Faisalabad** (central Punjab)
- Other stations frequently cited in PMD reporting include Sialkot, Jacobabad, Sibi, Chitral, Gilgit, Skardu, and Muzaffarabad — Jacobabad and Sibi are often referenced for extreme summer heat records, while Skardu, Gilgit, and Chitral are referenced for northern/high-altitude cold extremes. Confirm exact station name/network membership before citing a less-common station (verify).

## Climate Normal Baseline Convention

- Meteorological "climate normals" are conventionally calculated over 30-year reference periods, per World Meteorological Organization (WMO) convention (commonly cited 30-year periods internationally include 1981–2010 and 1991–2020).
- PMD's currently published baseline period should be confirmed from the specific PMD climate publication being read rather than assumed by default — WMO-recommended normal periods are updated roughly every decade, and PMD's adopted baseline for a given product may lag or differ from the latest WMO-recommended period (verify current PMD baseline period in use).

## Flood Forecasting Division

- PMD maintains a **Flood Forecasting Division (FFD)**, based in Lahore, as a functional unit distinct from PMD's general weather-forecasting operations. The FFD focuses specifically on riverine flood forecasting — monitoring rainfall and river-flow data to issue flood forecasts/warnings for Pakistan's major rivers (the Indus system and its tributaries, e.g. Jhelum, Chenab, Ravi, Sutlej) — a different work stream from routine daily/city weather forecasts and seasonal outlooks.
- When a question concerns flood forecasting/warning specifically (as opposed to general rainfall observation or forecasting), attribute it to the Flood Forecasting Division rather than treating it as generic PMD weather forecasting. Downstream flood-disaster response reporting sits with NDMA (`ndma-flood-sitreps`); FFD's own output is the meteorological/hydrological forecast itself, not the disaster-impact report.

## Extraction Notes

- Always anchor a figure to its station/city, variable type, time period, and data category (observed/normal/forecast).
- For anomaly analysis, use the normal baseline period stated in the source rather than assuming a default.
