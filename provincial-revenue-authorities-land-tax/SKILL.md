---
name: provincial-revenue-authorities-land-tax
description: Provincial land revenue and agricultural income tax administration skill. Use when explaining or analyzing Board of Revenue structures, land record management, agricultural income tax as a provincial subject, or stamp duty on property transactions — as distinct from FBR's federal property valuation tables for withholding tax.
---

# Provincial Revenue Authorities and Land Tax

## Overview

Use this skill for the **provincial** revenue-administration stack governing land: each province's Board of Revenue structure, land record maintenance/digitization, **agricultural income tax** (a provincial subject under the Constitution, separate from federal income tax on non-agricultural income), and **stamp duty** on property transactions. This is provincial fiscal/land-administration territory, distinct from FBR's federal valuation tables used for federal withholding/capital gains tax purposes.

## Coverage

- **Board of Revenue (BoR) structure**: Each province maintains its own Board of Revenue (e.g., Punjab, Sindh, Khyber Pakhtunkhwa, Balochistan each have their own BoR under provincial revenue legislation), which oversees land administration, revenue collection related to land, and the provincial land-record hierarchy (historically Patwari/Tehsildar/Assistant Commissioner (Revenue)/Deputy Commissioner tiers, though titles and structure vary somewhat by province and have been modified by digitization reforms).
- **Land record digitization**: Several provinces have undertaken computerization of land records, replacing or supplementing the traditional manual patwari-register system with digital records and computerized issuance of Fard (record-of-rights extract) — Punjab's effort in this space has been associated with the Punjab Land Records Authority (PLRA) and the Arazi Record Management Information System (ARMIS)/Land Records Management and Information Systems infrastructure; other provinces have their own parallel digitization initiatives with different institutional names and rollout status — verify the current institutional name and coverage status for a specific province/district rather than assuming uniform nationwide digitization.
- **Agricultural income tax**: Agricultural income is a **provincial** tax subject under the Constitution (per the Federal Legislative List/Fourth Schedule allocation), meaning each province levies and collects tax on agricultural income under its own provincial Agricultural Income Tax Act, administered through the provincial Board of Revenue — this is legally and administratively separate from FBR's federal Income Tax Ordinance, 2001, which generally excludes agricultural income from the federal tax base specifically because it is constitutionally a provincial subject.
- **Stamp duty**: Provincial stamp duty (under provincial Stamp Act legislation, historically derived from the Stamp Act, 1899 as adapted provincially) is charged on registration of property-transaction instruments (sale deeds, gift deeds, etc.), typically calculated against the provincial Deputy Commissioner (DC) valuation rate or a notified valuation table for the area — a separate valuation and tax base from FBR's own federal property valuation tables.
- **Registration**: Property transfer instruments are registered under the (provincially adapted) Registration Act, 1908 framework, with the registration/sub-registrar office function often integrated with or adjacent to the BoR/land-record hierarchy at district level.

## Use This Skill For

- explaining the Board of Revenue structure and land-administration hierarchy in a given province
- describing land record digitization initiatives (e.g., Punjab's PLRA/ARMIS) and their general purpose
- explaining agricultural income tax as a provincial tax subject, distinct from federal income tax
- explaining provincial stamp duty on property transactions and its relationship to DC valuation rates
- clarifying which level of government (provincial vs. federal) administers a given land-related levy

## When Not to Use This Skill

- For FBR's own notified property valuation tables used for federal withholding tax/capital gains tax purposes — use `fbr-property-valuation`; that skill covers the federal SRO-based valuation tables, which are a separate, typically higher, valuation from provincial DC rates used for stamp duty.
- For federal income tax on non-agricultural income — use `fbr-individual-tax-filing`; agricultural income is specifically carved out of the federal tax base and taxed provincially instead.
- For general provincial budget allocations/expenditure — use `provincial-budget-documents`; this skill covers the land-tax/land-administration function specifically, not overall provincial fiscal operations.
- For agricultural production/output statistics — use `mnfsr-agri-statistics` or `pbs-agriculture-census`; this skill covers the tax/administrative layer on agricultural land, not crop output data.
- For the Zakat Ushr religious levy on agricultural produce — use `pakistan-zakat-ushr-system`; Ushr is a distinct religious levy under the Zakat and Ushr Ordinance, 1980, administered through Zakat Councils, not the same as provincial agricultural income tax administered through the Board of Revenue.

## Routing Rules

- If the question concerns provincial land administration, Board of Revenue structure, land records, agricultural income tax, or stamp duty, use this skill.
- If the question concerns FBR's federal property valuation SRO tables (used for withholding/capital gains tax on property sale), route to `fbr-property-valuation` and note that provincial DC rates (this skill) and FBR notified values are separate valuation systems for separate tax purposes.
- If the question concerns federal, non-agricultural income tax, route to `fbr-individual-tax-filing`.
- If the question concerns the Ushr levy specifically (a religious/Zakat-system levy rather than the provincial agricultural income tax), route to `pakistan-zakat-ushr-system`.
- If the question is about provincial development/socioeconomic statistics rather than land-tax administration, route to the relevant province-specific statistics skill (e.g., `punjab-development-statistics`, `sindh-development-statistics`).

## Extraction Workflow

1. Identify which province is in question, since Board of Revenue structure, land-record digitization program names, and agricultural income tax statutes are each provincially specific (Punjab, Sindh, KP, Balochistan each have their own legislation and institutional names).
2. Determine whether the question concerns land administration/records, agricultural income tax, or stamp duty — these are related but distinct functions within the same provincial revenue apparatus.
3. If FBR valuation is mentioned alongside provincial DC rates, keep the two systems explicitly separate and note which one applies to the tax being discussed (federal withholding/CGT vs. provincial stamp duty).
4. Flag any specific digitization-program name (e.g., PLRA/ARMIS) as province-specific and not necessarily replicated identically in other provinces; verify current program name/status if citing an initiative outside Punjab.
5. Note that agricultural income tax collection has historically been a comparatively small share of provincial own-source revenue relative to its assessed potential; avoid implying uniform robust enforcement across all provinces without verification.

## Technical Rules

- Do not conflate provincial DC valuation rates (used for stamp duty) with FBR's federal notified property valuation tables (used for withholding/capital gains tax); they are separate systems, separate rates, and often produce different values for the same property.
- Do not describe agricultural income tax as part of the federal Income Tax Ordinance, 2001; it is constitutionally a provincial subject taxed under separate provincial statutes.
- Attribute land-record digitization program names (e.g., PLRA/ARMIS) specifically to the province in question; do not assume the same program name or rollout status applies nationally.
- Keep Ushr (a Zakat Ordinance religious levy) analytically separate from agricultural income tax (a provincial fiscal levy), even though both apply to agricultural land/produce.
- Treat provincial Board of Revenue nomenclature and tier structure (Patwari/Tehsildar/etc.) as broadly similar but not identical across provinces; verify province-specific terminology before asserting a specific title applies universally.

## Validation Checklist

- Confirm which specific province's Board of Revenue/legislation is being discussed.
- Confirm FBR federal valuation and provincial DC/stamp-duty valuation are not conflated.
- Confirm agricultural income tax is correctly attributed to provincial (not federal) jurisdiction.
- Confirm any land-record digitization program name cited is attributed to the correct province and flagged for current-status verification.
- Confirm Ushr and agricultural income tax are treated as distinct levies with different administering bodies.

## Common Pitfalls

- Treating FBR's federal property valuation tables as the same thing as provincial DC rates used for stamp duty.
- Describing agricultural income tax as a federal tax, when it is constitutionally and administratively a provincial subject.
- Assuming Punjab's PLRA/ARMIS digitization model and branding applies identically in other provinces.
- Conflating Ushr (Zakat Ordinance religious levy) with provincial agricultural income tax (a separate fiscal levy on the same general land base).
- Assuming uniform, robust agricultural income tax enforcement across all provinces without verification; actual collection performance has historically varied and lagged assessed potential.

## Reference

- See [Provincial Revenue Authorities and Land Tax Reference](references/provincial-revenue-authorities-land-tax.md) for Board of Revenue structure, agricultural income tax basis, and sourcing notes.
