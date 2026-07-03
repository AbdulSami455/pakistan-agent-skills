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

## Extraction Notes

- Always anchor a figure to its station/city, variable type, time period, and data category (observed/normal/forecast).
- For anomaly analysis, use the normal baseline period stated in the source rather than assuming a default.
