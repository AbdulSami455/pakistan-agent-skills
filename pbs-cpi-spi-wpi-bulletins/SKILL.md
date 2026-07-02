---
name: pbs-cpi-spi-wpi-bulletins
description: PBS CPI/SPI/WPI price bulletins skill. Use when analyzing, summarizing, comparing, or extracting information from the Pakistan Bureau of Statistics (PBS) monthly Consumer Price Index (CPI) press release, weekly Sensitive Price Indicator (SPI) bulletin, or Wholesale Price Index (WPI) bulletin, especially for item- or commodity-level price detail at monthly or weekly frequency.
---

# PBS CPI / SPI / WPI Bulletins

## Overview

Use this skill for questions about Pakistan's high-frequency price statistics published by the Pakistan Bureau of Statistics (PBS): the monthly CPI press release, the weekly SPI bulletin, and the WPI bulletin. This is the right skill when the task needs item-level or commodity-level price detail at monthly or weekly granularity, not an annual inflation narrative.

## Coverage

- CPI (Consumer Price Index): published monthly by PBS; reports headline year-on-year and month-on-month inflation, along with group-wise indices (food, housing/utilities, transport, clothing, etc.) and urban/rural splits.
- SPI (Sensitive Price Indicator): published weekly by PBS; tracks prices of a fixed basket of essential/sensitive items (mostly food and daily-use commodities) across income groups and cities, intended as a fast-turnaround affordability gauge between monthly CPI releases.
- WPI (Wholesale Price Index): published monthly (sometimes with weekly detail) by PBS; tracks wholesale-level prices for commodity groups distinct from the retail-level CPI basket.
- Each bulletin typically includes: the headline index value and percentage change (period-on-period and year-on-year), a commodity/item-level price table, and group/sub-group index breakdowns.
- CPI and WPI use a fixed base year for index calculation; SPI uses a fixed basket of items reported by city/market.

## Use This Skill For

- extracting the latest monthly CPI inflation rate (headline, food, core) or a specific group's index change
- pulling weekly SPI movement for specific items or income groups
- extracting WPI movement for specific commodity groups
- comparing item-level or commodity-level price changes across weeks or months
- distinguishing urban versus rural or income-group-specific price movement

## Routing Rules

- Use this skill for monthly (CPI/WPI) or weekly (SPI) item/commodity-level price detail.
- For the annual inflation narrative (full fiscal-year average inflation, broad commentary on price drivers), use `pes-macro-and-prices` instead — that chapter summarizes the year, these bulletins are the underlying high-frequency releases.
- If a question asks "what was inflation last week" or "how did the price of a specific item move this month," use this skill; if it asks for the full fiscal-year inflation average, use `pes-macro-and-prices`.
- CPI, SPI, and WPI are three distinct indices with different baskets and frequencies; do not treat a movement in one as automatically implying the same movement in another.

## Extraction Workflow

1. Identify which index the question needs: CPI (retail, monthly), SPI (weekly, sensitive-item basket), or WPI (wholesale, monthly).
2. Locate the headline index table for the exact period (month or week) referenced.
3. If the question is item- or group-specific, locate the corresponding commodity/group row in the detailed table rather than relying on the headline figure.
4. Preserve whether a percentage change is month-on-month, year-on-year, or week-on-week — bulletins typically report more than one basis side by side.
5. Note the base year used for index calculation when citing an index level rather than a percentage change.

## Technical Rules

- Do not mix CPI, SPI, and WPI figures as if they were the same index; each has a distinct basket, weighting, and frequency.
- Always specify the change basis (MoM, YoY, WoW) alongside any percentage figure.
- SPI is reported by income group and/or city in many bulletins; do not present a city- or group-specific figure as the national average without checking.
- CPI group indices (food, housing, transport, etc.) are weighted sub-components; a single group's movement does not represent headline inflation.
- WPI commodity groups differ from CPI consumption groups; do not assume the same classification applies to both.

## Validation Checklist

- Confirm which index (CPI, SPI, or WPI) the question is actually asking about.
- Verify the exact period (week or month) and the change basis (MoM, YoY, WoW) of the cited figure.
- Check whether the figure is a headline index, a group-level sub-index, or an item-level price.
- Confirm the base year if an index level (not a percentage change) is being quoted.

## Common Pitfalls

- Treating SPI's weekly sensitive-item movement as equivalent to the full CPI basket's monthly movement.
- Quoting a CPI group sub-index change as the headline inflation rate.
- Mixing month-on-month and year-on-year changes without labeling which basis is being cited.
- Citing WPI commodity movements as if they reflect retail/consumer prices.

## Reference

- See [Price Bulletins Reference](references/price-bulletins.md) for bulletin structure and extraction notes.
