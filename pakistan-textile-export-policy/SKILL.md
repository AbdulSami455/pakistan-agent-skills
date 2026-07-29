---
name: pakistan-textile-export-policy
description: Pakistan textile sector export policy and incentive framework skill. Use when a task concerns Textile Policy structure, regional/energy-tariff competitiveness for export-oriented textile industry, the Export Facilitation Scheme (EFS) under FBR customs rules, Pakistan's GSP+ beneficiary status with the EU and its conditions, or TDAP's textile-specific export-promotion role — rather than raw trade-volume data or general customs tariff schedules.
---

# Pakistan Textile Export Policy

## Overview

Use this skill for questions about the policy and incentive architecture supporting Pakistan's textile and apparel export sector — the Textile Policy framework, energy-tariff/regional-competitiveness support for export industry, the customs-duty-and-tax exemption mechanics of the Export Facilitation Scheme (EFS), Pakistan's GSP+ trade-preference status with the EU, and TDAP's textile-sector promotion activities. This is the policy/incentive layer specific to textiles, not raw export statistics or the general customs tariff schedule.

## Coverage

- **Textile Policy**: Pakistan's Ministry of Commerce (and historically the Textile Division/Ministry of Textile Industry, since folded into Commerce) has periodically issued Textile Policy documents (e.g., a Textile Policy covering a multi-year window) setting targets and instruments for export growth, value-addition promotion (moving from yarn/greige-cloth exports toward higher-value garments/made-ups), technology-upgradation support, and energy-cost relief for the sector. Always identify which policy vintage/window is being referenced rather than assuming a single perpetually current document — always verify the current operative policy.
- **Regional/energy competitiveness**: A recurring textile-policy instrument is a subsidized or capped energy tariff (electricity and/or RLNG) for export-oriented industry, intended to offset Pakistan's textile sector's energy-cost disadvantage relative to regional competitors (India, Bangladesh, Vietnam). The specific tariff level, eligibility (zero-rated/export-oriented sectors), and whether it is currently in force have been subject to repeated revision, withdrawal, and reinstatement — treat any specific regional tariff rate as needing current verification (verify current figure).
- **Export Facilitation Scheme (EFS)**: Administered by FBR under customs rules, EFS consolidated and replaced several earlier duty/tax-exemption schemes (including prior manufacturing-bond and export-oriented-unit type schemes) to provide duty- and sales-tax-exempt or deferred import of raw materials, intermediate inputs, and machinery for manufacturers who export their output, subject to input-output ratios, bank-guarantee/insurance mechanisms, and utilization/export-realization reporting. Textile manufacturer-exporters are among the largest users of EFS given the sector's reliance on imported cotton, man-made fibers, dyes, and machinery.
- **GSP+ status with the EU**: Pakistan has been a beneficiary of the EU's Generalised Scheme of Preferences Plus (GSP+) arrangement, which grants preferential (largely duty-free) market access for a wide range of exports — textiles being the largest beneficiary category — conditional on ratification and effective implementation of a specified list of international conventions on human rights, labour rights, environment, and governance. GSP+ status is subject to periodic EU review cycles; the specific review outcome, conditions flagged, and renewal timeline in effect at any point should be treated as needing current verification rather than assumed (verify current review cycle and status).
- **TDAP's role**: The Trade Development Authority of Pakistan runs textile-specific export-promotion activities — international trade-fair participation/facilitation, buyer-seller matchmaking, market-access support, and sector-specific export strategy input — distinct from FBR's customs/tax-incentive administration and from the Ministry of Commerce's policy-setting role.

## Use This Skill For

- explaining the structure and objectives of Pakistan's Textile Policy framework
- describing the energy-tariff relief mechanism for export-oriented textile industry and its competitiveness rationale
- explaining EFS eligibility, mechanics, and how it differs from ordinary dutiable imports
- explaining what GSP+ is, why textiles are its largest beneficiary category, and the nature of its conditionality (with hedged specifics on current review status)
- describing TDAP's textile-sector export-promotion activities

## When Not to Use This Skill

- For actual textile export volumes, values, or destination-market trade data — use `tdap-trade-reports` or `pes-external-sector`.
- For the general customs tariff schedule or duty structure not specific to textile export incentives — use `fbr-customs-tariff`.
- For general federal sales-tax mechanics not specific to the EFS export-incentive structure — use `fbr-sales-tax-federal`.
- For textile-sector output/value-addition statistics as reported in national accounts — use `pbs-national-accounts` or `pes-real-sectors`.

## Routing Rules

- If the question is about how much Pakistan exported in textiles/apparel to a given market or period, route to `tdap-trade-reports` or `pes-external-sector` instead.
- If the question is about the general customs duty/tariff rate on a non-textile-specific import, route to `fbr-customs-tariff` instead.
- If the question is about sales tax mechanics generally rather than the EFS exemption specifically, route to `fbr-sales-tax-federal`.
- If the question is about electricity/gas tariff determinations generally (not the export-industry concessional rate specifically), cross-check `nepra-tariff-determinations` or `ogra-petroleum-industry-reports`.

## Extraction Workflow

1. Identify which policy instrument is in question: Textile Policy (strategic framework), energy-tariff relief (cost-competitiveness instrument), EFS (customs/tax exemption mechanism), GSP+ (EU trade-preference), or TDAP (promotion activity) — these are distinct instruments administered by different bodies.
2. For Textile Policy, identify the specific policy document/vintage being referenced rather than treating "the Textile Policy" as a single evergreen document.
3. For energy tariffs, note that concessional/regionally-competitive rates for export industry have a history of being introduced, withdrawn, and reinstated — do not assume a rate is currently in force without verification.
4. For EFS, distinguish it from predecessor schemes (e.g., earlier manufacturing bond/export-oriented-unit schemes) it replaced or consolidated, and note that eligibility is exporter-status- and input-output-ratio-dependent.
5. For GSP+, separate the trade-preference mechanism (duty-free/preferential access) from its conditionality (convention ratification and implementation, subject to periodic EU review) — do not state a specific review outcome or renewal date without hedging.

## Technical Rules

- Do not state a specific current energy tariff rate (PKR/kWh or RLNG price) for export industry without hedging that it is a frequently revised/contested policy parameter (verify current figure).
- Do not conflate EFS with the general customs tariff regime; EFS is an exemption/deferral mechanism specifically for manufacturer-exporters, not a general duty schedule.
- Do not state Pakistan's GSP+ status, review outcome, or renewal date as settled without flagging that EU GSP+ status undergoes periodic review and specific findings/timelines should be verified.
- Distinguish TDAP's promotional-activity role from FBR's tax/customs-incentive administration role and the Ministry of Commerce's policy-setting role; they are three separate institutions.
- Keep "Textile Policy" (a discrete, periodically issued strategy document) distinct from ad hoc energy-tariff or EFS notifications, which can be issued and revised independently of a formal Textile Policy update.

## Validation Checklist

- Confirm which specific instrument (Textile Policy, energy tariff, EFS, GSP+, TDAP promotion) the question concerns.
- Flag any specific energy-tariff rate, EFS threshold, or GSP+ status/date claim as needing current-source verification.
- Confirm the institutional source (Ministry of Commerce, FBR, EU, TDAP) attributed to each claim is correct.
- Confirm whether the question actually needs export trade-volume data (route elsewhere) versus policy/incentive-structure explanation (this skill).

## Common Pitfalls

- Treating "the Textile Policy" as one single perpetually current document rather than a periodically reissued policy framework.
- Quoting a specific concessional energy-tariff rate as currently in force when such rates have repeatedly been introduced, suspended, and reinstated.
- Conflating EFS with the general customs tariff schedule, or treating it as a blanket duty exemption without noting export-obligation and input-output-ratio conditions.
- Stating a definitive, current GSP+ renewal/review outcome without verification, given the EU's periodic review cycle and its conditionality on convention implementation.
- Confusing TDAP's promotional mandate with FBR's fiscal-incentive administration.

## Reference

- See [Pakistan Textile Export Policy Reference](references/pakistan-textile-export-policy.md) for institutional citations, EFS/GSP+ background, and extraction notes.
