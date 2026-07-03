---
name: pes-infrastructure-digital-and-climate
description: Pakistan Economic Survey infrastructure, digital, and climate skill. Use when analyzing, summarizing, comparing, or extracting information from the Pakistan Economic Survey on transport, communications, energy, information technology, telecommunication, and climate change, especially for infrastructure indicators, digital transformation, connectivity, and climate-related policy or resilience themes.
---

# PES Infrastructure, Digital, and Climate

## Overview

Use this skill for Pakistan Economic Survey questions about transport, communications, energy, IT, telecommunication, and climate change. This is the right skill when the task is about enabling infrastructure, connectivity, digital-sector development, energy-sector indicators, or climate-response themes.

## Chapter Coverage

- Chapter 13: Transport and Communications: starts at survey page `227`
- Chapter 14: Energy: starts at survey page `243`
- Chapter 15: Information Technology and Telecommunication: starts at survey page `257`
- Chapter 17: Climate Change: starts at survey page `295`

## Use This Skill For

- extracting transport, logistics, or communication indicators
- summarizing energy-sector performance or policy direction
- analyzing digital transformation, IT, or telecom developments
- extracting climate resilience or climate-policy discussion
- connecting infrastructure and digital indicators to broader development themes in the survey

## Routing Rules

- Use Chapter 13 for transport networks, rail, ports, postal, broadcasting, and communication-sector metrics.
- Use Chapter 14 for energy production, energy management, and energy-sector discussion.
- For petroleum and natural gas production, consumption, or regulated pricing detail, prefer `ogra-petroleum-industry-reports`; Chapter 14 summarizes energy at a narrative level covering both power and petroleum.
- For electricity generation, DISCO performance, or power-sector tariffs, prefer `nepra-state-of-industry` or `nepra-tariff-determinations`.
- Use Chapter 15 for IT exports, broadband expansion, digital transformation, telecom, and public digital infrastructure.
- Use Chapter 17 for climate vulnerability, resilience, adaptation, and climate-policy discussion.
- For observed weather, rainfall, temperature, or climate normals, prefer `pmd-weather-climate-data`; Chapter 17 covers climate policy narrative, not station-level meteorological observations.

## Extraction Workflow

1. Identify whether the question is transport, energy, IT or telecom, or climate-related.
2. Route to the relevant chapter rather than relying on summary graphics alone.
3. Preserve indicator units exactly, such as kilometres, million passengers, tonnes, rupees, or percentages.
4. Keep institution names exact where the survey ties performance to agencies or funds.
5. Distinguish hard indicators from policy narrative.

## Technical Rules

- Infographic-style chapter openers are useful for orientation but should be verified against the chapter text before quoting a figure.
- Transport and communications sections may mix physical infrastructure with media or communications institutions; keep those categories separate.
- IT and telecom discussion may include exports, connectivity, institutions, and digital public infrastructure; do not flatten them into one metric.
- Climate sections often combine policy, risk, and resilience narratives; extract the exact claim type before summarizing.

## Validation Checklist

- Verify whether the number comes from a graphic, a paragraph, or a table.
- Check the unit before quoting transport, freight, passenger, or energy indicators.
- Confirm whether the digital-sector claim is about infrastructure, exports, institutions, or policy.
- Keep climate claims tied to the chapter’s stated frame instead of adding outside climate judgments.

## Common Pitfalls

- Quoting infographic headline numbers without checking chapter context.
- Mixing transport network length with throughput or traffic measures.
- Treating digital policy narrative as the same thing as realized digital-sector output.
- Summarizing climate sections in generic terms without the survey’s specific resilience or vulnerability framing.

## Reference

- See [Infrastructure, Digital, and Climate Reference](references/infrastructure-digital-and-climate.md) for chapter routing and indicator-handling notes.
