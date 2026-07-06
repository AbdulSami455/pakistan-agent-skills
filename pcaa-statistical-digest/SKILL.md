---
name: pcaa-statistical-digest
description: PCAA Statistical Digest skill. Use when analyzing, summarizing, comparing, or extracting information from the Pakistan Civil Aviation Authority's annual Statistical Digest, especially for airport-wise and airline-wise passenger movement, aircraft movement, and cargo traffic statistics.
---

# PCAA Statistical Digest

## Overview

Use this skill for Pakistan's civil aviation traffic statistics drawn from the Pakistan Civil Aviation Authority's (PCAA) annual "Statistical Digest." This is the right skill for airport- and airline-level passenger, aircraft movement, and cargo statistics, as distinct from the Pakistan Economic Survey's higher-level transport narrative.

## Coverage

- Published annually by PCAA, covering the preceding fiscal year's civil aviation activity.
- Typical structure: airport-wise traffic statistics (passenger numbers, aircraft movements, cargo tonnage) for major airports (Karachi, Lahore, Islamabad, Peshawar, Quetta, and others); airline-wise traffic breakdown (domestic and foreign carriers); international versus domestic traffic splits; cargo and mail tonnage handled; historical multi-year time series in annex tables; sometimes revenue or operational performance indicators for PCAA-managed airports.
- Document is structure-based with statistical tables organized by airport and airline; exact chapter/page layout varies by edition.

## Use This Skill For

- extracting airport-wise passenger or aircraft movement statistics for a specific year
- comparing airline-wise market share in passenger or cargo traffic
- tracking year-over-year growth or decline in domestic versus international air traffic
- sourcing cargo/mail tonnage handled at a specific airport
- building multi-year time series of Pakistan's aviation traffic trends

## Routing Rules

- Use this skill for PCAA's own aviation-specific statistical digest. Use `pes-infrastructure-digital-and-climate` only for the Pakistan Economic Survey's transport and communications chapter narrative, which summarizes aviation at a much higher level and does not carry airport-wise or airline-wise granularity.
- If the question concerns airport infrastructure investment or policy rather than traffic statistics, treat the Statistical Digest as a secondary source and note that policy narrative may sit in PCAA annual reports or PES instead.
- Pakistan's civil aviation sector was restructured in 2024 (Pakistan Airports Authority Act, 2023 and PCAA Act, 2023): airport operations and their traffic statistics moved to the newly created Pakistan Airports Authority (PAA), while PCAA retained regulatory/safety-licensing functions, and aircraft accident investigation moved to a separate Aircraft Accident and Incident Investigation Board. For editions from 2024 onward, confirm whether the "Statistical Digest" (or its successor publication) is now issued by PAA rather than PCAA before citing a source agency.

## Extraction Workflow

1. Identify the fiscal year covered by the digest edition before extracting any figure.
2. Identify whether the question is about a specific airport, a specific airline, or a national aggregate.
3. Distinguish passenger movement (count of passengers) from aircraft movement (count of flights/landings) from cargo tonnage; these are separate metrics.
4. Separate domestic and international traffic figures rather than presenting a combined total unless asked.
5. Preserve airline names exactly, distinguishing Pakistani carriers from foreign carriers operating in Pakistan.

## Technical Rules

- Passenger counts, aircraft movements, and cargo tonnage are independent metrics; do not infer one from another.
- Airport-wise figures should not be summed casually into a "national total" without checking whether the digest already provides that aggregate (to avoid double-counting transit passengers).
- Keep cargo and mail tonnage distinct if the source table separates them.
- Multi-year annex tables may use different airport groupings across editions; verify consistency before building a long time series.

## Validation Checklist

- Confirm the fiscal year before quoting any traffic figure.
- Verify whether a figure is passenger count, aircraft movement, or cargo tonnage.
- Check whether the figure is airport-specific, airline-specific, or a national aggregate.
- Confirm domestic versus international classification before quoting a split.

## Common Pitfalls

- Conflating aircraft movements (a count of flights) with passenger numbers.
- Summing airport-wise passenger figures into a national total without adjusting for transit/connecting passengers.
- Treating a single year's traffic dip (e.g., during a crisis period) as a permanent trend without checking context.
- Mixing PCAA airport-operational statistics with airline financial performance, which is not this digest's subject.

## Reference

- See [PCAA Statistical Digest Reference](references/pcaa-statistical-digest.md) for structure notes and metric definitions.
