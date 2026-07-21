---
name: pakistan-gdp-reconciliation-methodology
description: Pakistan GDP/national accounts reconciliation methodology skill. Use when an analyst needs to reconcile differing GDP growth figures between PBS provisional estimates, the National Accounts Committee's adopted figure, SBP's own growth assessment, or figures spanning a rebasing event, and needs to explain WHY the numbers diverge rather than just quote one of them.
---

# Pakistan GDP Reconciliation Methodology

## Overview

Use this skill when a task requires reconciling or explaining discrepancies between different vintages or sources of Pakistan's GDP figures — PBS provisional estimates vs. National Accounts Committee (NAC)-approved figures, SBP's independent growth assessment vs. PBS's, or GDP levels/growth rates that span a base-year rebasing. This is a methodology layer: it explains the institutional process that produces the "official" GDP number and the specific mechanics (base year changes, SNA vintage, revision cycle) that break comparability across time or across sources. It does not host GDP data itself.

## Coverage

- The institutional process: PBS compiles provisional national accounts estimates; the National Accounts Committee (NAC) — chaired by the Deputy Chairman Planning Commission or Finance Minister, with PBS, Ministry of Finance, SBP and provincial representatives — reviews and formally approves the estimate that becomes Pakistan's "official" GDP growth figure for the fiscal year.
- Known historical discrepancy pattern: SBP's independent, model-based growth assessment (published in its Monetary Policy Statements/Annual Report) has, in specific years, diverged from PBS's working-paper estimate ahead of NAC reconciliation (e.g., FY21: SBP ~3% vs. PBS ~3.94%, with NAC ultimately adopting the PBS-anchored figure).
- Rebasing mechanics: Pakistan has changed its national accounts base year periodically (e.g., 1999-2000 to 2005-06, and 2005-06 to 2015-16 in January 2022), each time adopting an updated System of National Accounts (SNA) vintage and revised sectoral weights derived from fresh benchmark studies. Rebasing is not a simple index re-scaling — it can materially change the *level* of GDP (PBS's 2015-16 rebasing raised nominal GDP by roughly 11%) as well as sectoral shares, because new benchmark surveys change coverage and weights, not just the reference index value.
- Provisional-to-final revision cycle: PBS's first GDP growth estimate for a fiscal year is provisional (based on partial-year data, e.g., July-March large-scale manufacturing) and is revised at least once (often twice) as more complete data (LSM, agriculture output, tax/import data) becomes available; a "final" figure is typically not settled until 1-2 years later.
- Quarterly National Accounts (QNA) "quarterisation" methodology: SBP and PBS have both published research on how annual national accounts are broken into quarterly series using indicator-based interpolation methods, since Pakistan's primary GDP compilation is fundamentally annual, not quarterly, in nature.

## Use This Skill For

- explaining why an SBP-cited growth figure differs from a PBS press release figure for the same fiscal year
- tracing a GDP growth or level figure through the provisional -> NAC-approved -> revised timeline
- assessing whether two GDP figures being compared straddle a rebasing event (different base years) and are therefore not directly comparable
- explaining the mechanics of why a rebasing changes both the GDP level and sectoral value-added shares, not just the index number
- describing how quarterly GDP estimates are derived from PBS's fundamentally annual compilation process

## When Not to Use This Skill

- For the actual published GDP growth/value-added figures themselves (quarterly or annual) — use `pbs-national-accounts`.
- For the Pakistan Economic Survey's narrative-level annual GDP growth commentary — use `pes-macro-and-prices`.
- For SBP's own annual-report GDP commentary as data (not methodology) — use `sbp-annual-report`.

## Routing Rules

- If the task just needs "what was GDP growth in FY24," route to `pbs-national-accounts` or `pes-macro-and-prices` — this skill is for explaining *why* two cited numbers disagree or *whether* they are comparable.
- If the discrepancy involves fiscal or debt aggregates (not GDP itself, though debt-to-GDP ratios are affected by rebasing), also consult `pes-fiscal-financial-and-debt` for the denominator effect of a GDP rebasing on debt/GDP or deficit/GDP ratios.
- If the question is about inflation/price-index base years rather than GDP, route to `pakistan-inflation-measurement-methodology` instead — CPI and GDP have independent, non-synchronized rebasing calendars.
- If the question is about structural breaks in Pakistani time series generally (not GDP specifically), the meta-skill `pakistan-data-structural-breaks` covers the cross-domain pattern; use this skill for GDP-specific mechanics.

## Extraction Workflow

1. Identify the exact figures being compared: source (PBS vs. SBP vs. IMF/WB), vintage (provisional/NAC-approved/revised), fiscal year, and base year.
2. Check whether the two figures span a rebasing event (pre-2022 base 2005-06 vs. post-2022 base 2015-16, or any subsequent rebasing announced since). If so, flag that levels are not directly comparable without an official backward-revised series (PBS publishes backward-revised series when it rebases; use that series for cross-base-year comparison rather than naively chaining growth rates).
3. If the discrepancy is PBS vs. SBP for the same fiscal year, check whether the PBS figure is still provisional (pre-NAC) — SBP's independent estimate and PBS's provisional working-paper figure often diverge before NAC formally reconciles them; the NAC press release is the authoritative resolution.
4. For quarterly figures, confirm whether the source is PBS's own QNA release or a third party's model-based quarterisation, since Pakistan's GDP compilation is fundamentally annual and quarterly splits use indicator-based interpolation that can differ across compilers.
5. State explicitly which figure is being treated as authoritative and why (e.g., "NAC-approved figure as of [date]" vs. "PBS provisional working paper, pre-NAC").

## Technical Rules

- Never chain a growth rate computed on a 2005-06 base year directly against a growth rate computed on a 2015-16 (or later) base year as if they were one continuous series; use PBS's official backward-revised series for the affected years instead.
- A rebasing changes both the price base and often the survey/benchmark methodology (new SNA vintage, updated informal-sector or services-sector coverage); do not assume the level jump is purely a statistical artifact of "the base year changing" — some of it reflects genuine improved coverage.
- Distinguish "provisional" (PBS's first-cut estimate), "NAC-approved" (the reconciled, official figure), and "revised" (subsequent update as more source data arrives) — these are three different release stages, not interchangeable synonyms for "the GDP figure."
- SBP's independent growth assessment (in MPS/Annual Report) is a policy input, not a competing official statistic; Pakistan has one official GDP series, produced by PBS and ratified by the NAC.
- Debt-to-GDP, tax-to-GDP, and deficit-to-GDP ratios all shift mechanically when the GDP denominator is rebased upward; a ratio improvement driven mainly by rebasing should be labeled as such, not read as a change in underlying fiscal performance.

## Validation Checklist

- Confirm both figures being compared use the same GDP base year; if not, note the rebasing and avoid direct comparison.
- Confirm whether each cited figure is provisional, NAC-approved, or revised, and use the NAC press release as the tie-breaker for "the official" figure.
- If SBP and PBS figures diverge, check for a subsequent NAC reconciliation before treating the divergence as unresolved.
- For any ratio-to-GDP figure spanning a rebasing year, check whether the shift is being (mis)attributed to real economic performance rather than the denominator change.
- For quarterly figures, confirm the compiling source (PBS QNA vs. third-party quarterisation) since methods differ.

## Common Pitfalls

- Treating SBP's independent growth estimate as a second "official" GDP series rather than a pre-reconciliation policy assessment.
- Comparing GDP levels or debt/GDP ratios across a rebasing year without adjusting for the new base, producing a spurious jump or drop.
- Citing a provisional PBS growth figure as final without checking for a later NAC-approved or revised figure.
- Assuming a GDP level jump after rebasing is purely definitional noise, when it typically reflects both a new price/weight base and genuinely expanded survey coverage.
- Using ad hoc quarterly GDP splits from third-party sources as if they were PBS's own official quarterly release.

## Reference

- See [GDP Reconciliation Methodology Reference](references/pakistan-gdp-reconciliation-methodology.md) for the NAC process, rebasing history, and quarterisation methodology sources.
