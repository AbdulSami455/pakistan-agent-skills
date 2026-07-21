---
name: pakistan-inflation-measurement-methodology
description: Pakistan inflation measurement methodology skill. Use when an analyst needs to explain HOW Pakistan's CPI is constructed (basket, weights, Laspeyres formula, base year, urban/rural coverage), how core inflation (NFNE, trimmed mean) is derived from the headline basket, or why CPI/SPI/WPI series are not comparable across a base-year change — not simply to fetch the latest inflation print.
---

# Pakistan Inflation Measurement Methodology

## Overview

Use this skill for questions about the construction methodology behind Pakistan's price indices — how the CPI basket, weights, and base year are determined; how PBS computes the index formula; how SBP derives core inflation measures (NFNE, trimmed mean) from the same CPI micro-data; and what breaks comparability when the basket, base year, or weighting source changes. This is a methodology layer that sits behind the raw bulletin numbers, for a reader who needs to know why a reported inflation figure means what it means, not just what the figure is.

## Coverage

- **Index formula**: PBS computes CPI using a weighted Laspeyres-type formula (fixed base-period quantities/weights applied to current prices), the standard approach for a monthly consumer price index of this kind — confirm the exact current formula variant against the latest PBS methodology note, since index compilation practice can be refined between base-year revisions.
- **Basket and weight source**: CPI weights are derived from a household budget/expenditure survey (historically the HIES), which also anchors the base year — the survey year and the index base year are the same reference period. The basket is organized under a COICOP-style (Classification of Individual Consumption by Purpose) 12-group structure, with separate urban and rural baskets (different item counts and weights reflecting different consumption patterns), collected across a defined set of cities/markets.
- **Base year**: PBS periodically rebases CPI to a newer household-survey year; the specific current base year and item/weight counts must be confirmed against the latest PBS Price Statistics methodology note, since these are revised periodically and are easy to state incorrectly from memory or stale sources.
- **Core inflation**: SBP computes two core inflation measures from the same CPI item-level data for monetary policy purposes: (1) Non-Food Non-Energy (NFNE) inflation, excluding the food group and specified energy items (e.g., electricity, gas, motor fuels) from the CPI basket; and (2) 20-percent trimmed-mean inflation, which ranks all CPI items by their individual price-change rate and excludes the top and bottom tails (by cumulative weight) before averaging the remainder. Both are designed to strip out volatile/transitory components that the headline CPI does not filter out.
- **SPI and WPI as distinct instruments**: SPI (weekly, sensitive/essential-item basket, income-group and city-level) and WPI (wholesale-level commodity prices) are separate index constructions from CPI, with their own baskets, weights, and (in SPI's case) update frequency; none of the three should be treated as interchangeable proxies for one another.

## Use This Skill For

- explaining how PBS's CPI basket, weights, and base year are derived, and from which survey
- explaining the mechanical difference between headline CPI, NFNE core inflation, and trimmed-mean core inflation
- assessing whether a multi-year inflation comparison spans a CPI base-year/basket revision and is therefore not a clean like-for-like series
- explaining why SPI, CPI, and WPI can show materially different inflation readings for the same period
- describing the Laspeyres fixed-weight index construction and its known limitation (substitution bias) for interpreting long-run CPI trends

## When Not to Use This Skill

- For the latest published CPI/SPI/WPI print, group-level breakdown, or item-level price table — use `pbs-cpi-spi-wpi-bulletins`.
- For the Pakistan Economic Survey's annual inflation narrative — use `pes-macro-and-prices`.
- For SBP's policy-rate rationale referencing an inflation outlook — use `sbp-monetary-policy-statement`; this skill covers how the inflation figures themselves are built, not how the MPC reacts to them.

## Routing Rules

- If the task needs a specific month's or week's inflation number, route to `pbs-cpi-spi-wpi-bulletins` — this skill is for explaining construction methodology and comparability, not for sourcing the print.
- If the task needs the annual fiscal-year inflation average narrative, route to `pes-macro-and-prices`.
- If the discrepancy in question is about GDP deflators or national-accounts price bases rather than CPI, route to `pakistan-gdp-reconciliation-methodology` — GDP and CPI rebasing calendars are independent of each other.
- For cross-domain structural-break handling (rebasing, methodology changes affecting comparability generally), see `pakistan-data-structural-breaks`.

## Extraction Workflow

1. Identify whether the question is about the headline CPI, a core-inflation measure (NFNE or trimmed mean), SPI, or WPI — these are methodologically distinct constructions, not variants of one series.
2. If the question involves comparing inflation across years, check whether the comparison spans a CPI base-year/basket revision; if so, flag that basket composition and weights changed and a "like-for-like" long-run comparison requires PBS's own linked/backward-compatible series where available.
3. For core-inflation questions, confirm which of the two SBP core measures (NFNE vs. trimmed mean) is being referenced, since they can diverge meaningfully in a given month (NFNE excludes an entire category; trimmed mean statistically excludes outlier items regardless of category).
4. Always state the current CPI base year and weight-survey source as "per the latest PBS methodology note as of [date]" rather than asserting a fixed base year as permanent fact, since PBS has revised the base year multiple times historically and has signaled an intent toward a roughly five-year rebasing cycle.
5. When citing basket structure (group count, item count, weights), cite it as sourced from the specific PBS methodology/Price Statistics document, not from general knowledge, since these figures are revised with each rebasing.

## Technical Rules

- Do not describe the CPI as a chained or current-weighted index; it is constructed on a fixed-base (Laspeyres-type) methodology, meaning weights are held constant at base-period levels until the next rebasing — this has a known substitution-bias implication (the index can overstate true cost-of-living inflation as consumers substitute away from goods with above-average price increases).
- Do not conflate NFNE core inflation with trimmed-mean core inflation; they use different exclusion logic (category-based exclusion vs. statistical-outlier trimming by weight) and can differ from each other and from headline CPI in the same month.
- Do not treat SPI as a lower-frequency proxy for CPI or WPI as a leading indicator of CPI without qualification; each has an independent basket and does not mechanically forecast the others.
- Do not state the current CPI base year, item count, or group weights as fixed facts without noting they should be confirmed against the latest PBS methodology note, since these are revised periodically.
- Urban and rural CPI baskets differ in composition (item count and weights) reflecting different consumption patterns; a national headline CPI is a weighted combination of the two, not a simple average.

## Validation Checklist

- Confirm which index (CPI headline, NFNE core, trimmed-mean core, SPI, WPI) is actually being discussed.
- Confirm the base year and weight-survey source being assumed, and flag if it needs verification against the current PBS methodology note.
- Check whether a multi-year inflation comparison crosses a basket/base-year revision.
- Confirm the change basis (MoM, YoY, fiscal-year average) is explicitly stated alongside any percentage.
- For core-inflation figures, confirm whether NFNE or trimmed-mean methodology is being used, since these can print differently in the same period.

## Common Pitfalls

- Asserting a specific CPI base year, item count, or basket weight from memory without flagging it as needing confirmation against the latest PBS release, since these details change with each rebasing.
- Treating the CPI as a cost-of-living index with continuously updated consumption weights, when it is a fixed-weight Laspeyres-type index subject to substitution bias between rebasing events.
- Using NFNE and trimmed-mean core inflation interchangeably as if they were the same measure.
- Comparing CPI inflation across a rebasing year without acknowledging the basket/weight change.
- Treating SPI's weekly essential-item movement as a proxy for the full CPI print.

## Reference

- See [Inflation Measurement Methodology Reference](references/pakistan-inflation-measurement-methodology.md) for index formula detail, core-inflation construction, and sourcing notes.
