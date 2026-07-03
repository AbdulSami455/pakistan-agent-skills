---
name: world-bank-pakistan-indicators
description: World Bank Pakistan indicators skill. Use when analyzing, summarizing, comparing, or extracting information from the World Bank's World Development Indicators, country data portal, or Pakistan-specific World Bank reports, especially for internationally comparable macro, poverty, governance, and development indicators.
---

# World Bank Pakistan Indicators

## Overview

Use this skill for questions about Pakistan's development indicators as published by the World Bank, including the World Development Indicators (WDI) database, the World Bank Data Portal country page for Pakistan, and World Bank country reports (economic updates, poverty assessments, sector reports). This covers internationally standardized metrics — distinct from Pakistan's own official statistics in PBS, PES, or SBP publications.

## Coverage

- World Development Indicators (WDI): the World Bank's flagship database with hundreds of indicators for Pakistan, including GDP, population, poverty, trade, health, education, infrastructure, governance, and environment metrics.
- World Bank Data Portal (Pakistan country page): summary dashboards and downloadable indicator series.
- World Bank Pakistan reports: Pakistan Development Update (PDU), poverty assessments, sector diagnostics, and programmatic documents when they contain indicator tables or analysis.
- Typical indicators: GDP (current US$, growth rate, per capita), GNI, poverty headcount ratio, Gini index, trade openness, FDI, remittances, life expectancy, school enrollment, access to electricity, CO2 emissions, Doing Business indicators (historical), Worldwide Governance Indicators.

## Use This Skill For

- extracting internationally comparable macro or development indicators for Pakistan
- comparing Pakistan's indicators with regional or global benchmarks
- sourcing World Bank poverty estimates or Gini coefficients for Pakistan
- identifying World Bank governance or business-environment indicators
- cross-checking Pakistan's official statistics against World Bank estimates

## Routing Rules

- Use this skill for World Bank-published indicators with international methodology. For Pakistan's own official GDP figures, prefer `pbs-national-accounts` or `pes-macro-and-prices`.
- For IMF program documents and conditionality, prefer `imf-pakistan-documents`.
- For ADB's Pakistan indicators and sector reports, prefer `adb-pakistan-indicators`; World Bank and ADB may cite overlapping indicators with different vintages or methodologies.
- For Pakistan's own fiscal, monetary, or external-sector statistics, prefer the relevant SBP, PBS, or PES skill rather than World Bank secondary compilations.
- World Bank estimates may differ from PBS or Ministry figures due to currency conversion, rebasing, or modeling — do not treat them as identical without checking.

## Extraction Workflow

1. Identify whether the question needs a WDI database indicator, a Data Portal series, or a World Bank country report table.
2. Preserve the reference year and whether the figure is an estimate, projection, or reported value.
3. Note the indicator code and definition from WDI when available.
4. When comparing across years, check whether the World Bank revised historical estimates in a new WDI edition.
5. Distinguish World Bank-modeled estimates from Pakistan government-reported figures cited within World Bank documents.

## Technical Rules

- GDP and GNI figures may be in current US$, constant US$, or local currency; preserve the denomination and price basis.
- Poverty headcount ratios depend on the poverty line used (international $2.15/day PPP line vs. national poverty lines); preserve the line definition.
- World Bank may report fiscal year or calendar year depending on the indicator; confirm the period basis.
- Governance and business-environment indicators (WGI, historical Doing Business) use World Bank methodology distinct from Pakistan domestic measures.

## Validation Checklist

- Confirm the reference year and indicator definition.
- Verify the unit and denomination (US$, percent, ratio, per capita).
- Check whether the figure is a World Bank estimate or a reported national value.
- Note the WDI edition or report vintage if comparing across time.

## Common Pitfalls

- Treating World Bank GDP estimates as identical to PBS national accounts figures.
- Mixing international poverty lines with Pakistan's own national poverty line from PSLM.
- Citing an outdated WDI value when a newer edition revised the series.
- Conflating World Bank indicators with ADB or IMF figures that use different methodologies or vintages.

## Reference

- See [World Bank Pakistan Indicators Reference](references/world-bank-pakistan-indicators.md) for source structure and extraction notes.
