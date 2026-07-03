---
name: adb-pakistan-indicators
description: ADB Pakistan indicators skill. Use when analyzing, summarizing, comparing, or extracting information from the Asian Development Bank's Key Indicators, Basic Statistics, country reports, or sector assessments for Pakistan, especially for Asia-Pacific comparable macro, poverty, infrastructure, and sector development indicators.
---

# ADB Pakistan Indicators

## Overview

Use this skill for questions about Pakistan's development indicators as published by the Asian Development Bank (ADB), including the Key Indicators for Asia and the Pacific, Basic Statistics, ADB country reports (Pakistan economic updates, sector assessments), and ADB Data Library series for Pakistan. This covers ADB's Asia-Pacific standardized metrics — distinct from Pakistan's own official statistics and from World Bank or IMF compilations.

## Coverage

- Key Indicators for Asia and the Pacific: ADB's annual statistical publication with Pakistan-specific rows for macro, social, infrastructure, and trade indicators.
- Basic Statistics: ADB's compact statistical reference with cross-country comparability across developing Asia.
- ADB Pakistan country reports: Pakistan economic updates, country partnership strategy progress reports, and sector diagnostics (energy, transport, water, education, health) when they contain indicator tables.
- ADB Data Library: downloadable indicator series for Pakistan covering GDP, inflation, trade, poverty, social indicators, and infrastructure access.
- Typical indicators: GDP growth, inflation, fiscal balance, current account, poverty rate, Gini coefficient, trade shares, FDI, remittances, access to electricity, road density, school enrollment, health expenditure.

## Use This Skill For

- extracting ADB-published development indicators for Pakistan with Asia-Pacific comparability
- comparing Pakistan's indicators with other developing Asian economies cited in ADB reports
- sourcing ADB poverty or inequality estimates for Pakistan
- identifying ADB sector-specific indicators (energy access, transport infrastructure, water supply)
- cross-checking Pakistan's official statistics against ADB estimates

## Routing Rules

- Use this skill for ADB-published indicators with Asia-Pacific methodology. For World Bank WDI indicators, prefer `world-bank-pakistan-indicators`.
- For IMF program documents and conditionality, prefer `imf-pakistan-documents`.
- For Pakistan's own official GDP figures, prefer `pbs-national-accounts` or `pes-macro-and-prices`.
- For Pakistan's own fiscal, monetary, or external-sector statistics, prefer the relevant SBP, PBS, or PES skill rather than ADB secondary compilations.
- ADB estimates may differ from PBS, World Bank, or Ministry figures due to currency conversion, rebasing, or modeling — do not treat them as identical without checking.

## Extraction Workflow

1. Identify whether the question needs a Key Indicators table row, an ADB Data Library series, or an ADB country report table.
2. Preserve the reference year and whether the figure is an estimate, projection, or reported value.
3. Note the indicator definition and whether it uses ADB's Asia-Pacific comparability framework.
4. When comparing across years, check whether ADB revised historical estimates in a new edition.
5. Distinguish ADB-modeled estimates from Pakistan government-reported figures cited within ADB documents.

## Technical Rules

- GDP and related macro figures may be in current US$, constant US$, or local currency; preserve the denomination and price basis.
- Poverty rates depend on the poverty line used; preserve the line definition (ADB may use national or international lines depending on the publication).
- ADB fiscal year conventions for Pakistan may align with Pakistan's July–June fiscal year for some indicators but use calendar year for others; confirm the period basis.
- Sector indicators (energy access, road density) use ADB definitions that may differ from Pakistan domestic agency definitions.

## Validation Checklist

- Confirm the reference year and indicator definition.
- Verify the unit and denomination (US$, percent, ratio, per capita).
- Check whether the figure is an ADB estimate or a reported national value.
- Note the publication edition or data vintage if comparing across time.

## Common Pitfalls

- Treating ADB GDP estimates as identical to PBS national accounts figures.
- Conflating ADB indicators with World Bank WDI values that use different vintages or methodologies.
- Citing an outdated Key Indicators edition when a newer release revised the series.
- Mixing ADB poverty estimates with Pakistan's own national poverty line from PSLM without noting the definitional difference.

## Reference

- See [ADB Pakistan Indicators Reference](references/adb-pakistan-indicators.md) for source structure and extraction notes.
