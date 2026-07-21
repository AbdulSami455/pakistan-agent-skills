---
name: pakistan-debt-sustainability-analysis
description: Pakistan fiscal/debt sustainability analysis methodology skill. Use when an analyst needs to apply or interpret IMF-style Debt Sustainability Analysis (DSA) mechanics to Pakistan — debt-to-GDP dynamics, the primary balance required to stabilize debt, gross financing needs, and MAC-DSA risk benchmarks — rather than simply quoting a debt stock or deficit figure.
---

# Pakistan Debt Sustainability Analysis

## Overview

Use this skill when a task requires applying debt-dynamics arithmetic or IMF/Fiscal-authority DSA-style reasoning to Pakistan's public debt — e.g., computing or explaining the debt-stabilizing primary balance, decomposing the change in debt-to-GDP into its primary-balance, interest-growth-differential, and exchange-rate components, or interpreting Pakistan's debt trajectory against Market-Access-Country (MAC) DSA risk benchmarks. This is the analytical-method layer; it does not host the underlying debt stock, deficit, or interest-rate data.

## Coverage

- **Debt dynamics identity**: The standard public-debt-dynamics decomposition expresses the change in the debt-to-GDP ratio as a function of (a) the interest-rate/growth-rate differential applied to the prior period's debt ratio, (b) the primary balance (revenue minus non-interest expenditure, as a share of GDP), and (c) other flows (e.g., exchange-rate depreciation effects on foreign-currency-denominated debt, one-off stock-flow adjustments). This is the standard framework used across IMF DSAs, not a Pakistan-specific formula, and should be applied with Pakistan's actual reported interest rates, growth rates, and debt composition rather than assumed generic values.
- **MAC DSA framework**: Pakistan's debt sustainability is assessed by the IMF (and, in domestic publications, by Pakistan's own Finance Division/Debt Policy Coordination Office) using the Market Access Countries (MAC) DSA framework, given Pakistan's access to international capital markets. The MAC DSA framework references general risk-benchmark thresholds for public debt-to-GDP and gross financing needs (GFN)-to-GDP as flags for closer scrutiny, not as hard sustainability cutoffs; the specific benchmark values in use for a given DSA vintage should be confirmed against the current IMF Country Report/DSA annex, since the framework and benchmark calibration are reviewed periodically.
- **Domestic DSA reporting**: Pakistan's Finance Division/Debt Policy Coordination Office publishes its own periodic Debt Sustainability Report (e.g., covering a forward multi-year window), which projects debt trajectories under a baseline and stress scenarios using inputs such as the federal primary balance and Medium-Term Budget Strategy Paper projections — this is a domestically produced complement to, not a replacement for, IMF Article IV/program DSA annexes.
- **Foreign-currency debt and exchange-rate sensitivity**: A material share of Pakistan's public debt is external/foreign-currency-denominated (or domestic debt with FX-linked terms); a PKR depreciation mechanically raises the debt-to-GDP ratio through the "other flows"/valuation term of the debt-dynamics identity even with no new borrowing — this channel should be reported separately from the primary-balance and interest-growth-differential channels, not folded into either.
- **Gross Financing Needs (GFN)**: DSA analysis distinguishes the debt *stock* ratio from the GFN ratio (amortization due plus the primary deficit plus interest, as a share of GDP in a given year), since a country can have a moderate debt stock but an acute near-term financing/rollover risk if maturities are concentrated — Pakistan's DSA discussions have specifically flagged GFN and rollover risk given its debt-maturity structure.

## Use This Skill For

- computing or explaining the primary balance required to stabilize (or reduce) Pakistan's debt-to-GDP ratio, given assumed/reported interest and growth rates
- decomposing a change in Pakistan's debt-to-GDP ratio into interest-growth differential, primary balance, and exchange-rate/other-flows components
- explaining what the MAC DSA framework is and how its risk benchmarks are used to flag (not conclusively determine) sustainability concerns for Pakistan
- distinguishing debt-stock sustainability from gross-financing-needs/rollover risk
- explaining why PKR depreciation affects Pakistan's debt ratio independent of new fiscal borrowing

## When Not to Use This Skill

- For the actual reported debt stock, deficit, or debt-servicing figures — use `pes-fiscal-financial-and-debt`, `federal-budget-documents`, or `agpr-fiscal-operations`.
- For IMF program conditionality or review-specific commentary not related to debt-dynamics methodology — use `imf-pakistan-documents`.
- For the mechanics of how the federal divisible pool is split with provinces (a determinant of the federal primary balance but a separate methodology) — use `pakistan-nfc-award-methodology`.

## Routing Rules

- If the task needs Pakistan's actual debt stock, fiscal deficit, or debt-servicing cost for a period, route to `pes-fiscal-financial-and-debt` or `federal-budget-documents` first, then apply this skill's dynamics framework to those figures.
- If the task is about IMF program reviews, disbursement schedules, or conditionality narrative rather than the DSA arithmetic itself, route to `imf-pakistan-documents`.
- If the ratio's GDP denominator is in question (e.g., a rebasing event affecting debt/GDP), cross-check `pakistan-gdp-reconciliation-methodology` for the denominator-side caveat.
- If the question concerns exchange-rate levels or REER rather than the debt-valuation channel specifically, route to `pakistan-reer-bop-methodology` for the exchange-rate analysis itself.

## Extraction Workflow

1. Identify what is being asked: the debt-stabilizing primary balance, a decomposition of an observed debt-ratio change, or an assessment against MAC DSA benchmarks.
2. Gather the specific inputs needed — nominal/real GDP growth rate, effective average interest rate on debt (or nominal interest rate and inflation separately), current debt-to-GDP ratio, and (if decomposing an actual change) the primary balance and any known exchange-rate movement — from the relevant data skill (`pes-fiscal-financial-and-debt`, `sbp-statistics-bulletin`) rather than assuming generic values.
3. Apply the standard debt-dynamics identity using Pakistan's actual inputs; show the interest-growth differential term, the primary-balance term, and the residual/other-flows term (including FX valuation effects) separately.
4. If referencing MAC DSA risk benchmarks, cite the specific IMF DSA annex/vintage being used and note that benchmark calibration is reviewed periodically rather than asserting a fixed universal threshold from memory.
5. When citing Pakistan's own Debt Sustainability Report (Finance Division), note it as a domestic, forward-projection complement to IMF DSA analysis, and flag which fiscal-year window and scenario (baseline vs. stress) is being cited.

## Technical Rules

- Do not compute the debt-stabilizing primary balance without both an interest-rate assumption and a growth-rate assumption; the required primary balance is driven by the interest-rate/growth-rate differential applied to the existing debt stock, not by the debt stock alone.
- Do not attribute a debt-to-GDP ratio change entirely to fiscal policy (the primary balance) without checking the exchange-rate/valuation and GDP-rebasing channels, both of which can move the ratio mechanically without any change in borrowing behavior.
- Do not treat MAC DSA benchmark thresholds as fixed, hard sustainability cutoffs; they are risk-flagging reference points in the IMF's framework, and their calibration should be confirmed against the current DSA methodology document rather than stated as immutable numbers.
- Distinguish debt-stock sustainability (debt/GDP trajectory) from liquidity/rollover risk (gross financing needs/GDP, and maturity concentration); a country can face acute financing risk even with a moderate debt-stock ratio.
- Keep domestic-currency and foreign-currency-denominated debt separate when discussing exchange-rate sensitivity, since only the FX-denominated (or FX-linked) portion carries direct valuation risk from PKR movements.

## Validation Checklist

- Confirm which specific DSA question is being addressed (stabilizing primary balance, ratio decomposition, or benchmark comparison) before applying a formula.
- Confirm the growth rate, interest rate, and debt ratio inputs are sourced from an actual data skill/document, not assumed.
- If citing MAC DSA benchmark values, confirm the IMF DSA annex vintage the values are drawn from.
- If a debt ratio change is being explained, confirm whether an exchange-rate movement or a GDP rebasing contributed to the change independent of fiscal policy.
- Distinguish debt-stock ratio findings from gross-financing-needs/rollover-risk findings when both are discussed.

## Common Pitfalls

- Computing a "debt-stabilizing primary balance" using only the current primary balance and ignoring the interest-rate/growth-rate differential that actually drives the required balance.
- Attributing all debt-to-GDP movement to fiscal discipline (or its absence) without checking for exchange-rate valuation effects on FX-denominated debt.
- Citing a MAC DSA risk-benchmark number as a hard pass/fail sustainability line rather than a risk-flagging reference point.
- Conflating Pakistan's own Finance Division Debt Sustainability Report with an IMF DSA annex, when they are separate (though related) documents with potentially different assumptions.
- Ignoring gross financing needs and debt-maturity concentration when assessing sustainability purely from the debt-stock ratio.

## Reference

- See [Debt Sustainability Analysis Reference](references/pakistan-debt-sustainability-analysis.md) for the debt-dynamics identity, MAC DSA framework detail, and sourcing notes.
