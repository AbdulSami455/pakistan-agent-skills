---
name: pakistan-zakat-ushr-system
description: Pakistan's statutory Zakat and Ushr system skill. Use when explaining or analyzing compulsory Zakat deduction at source under the Zakat and Ushr Ordinance 1980, the Central/Provincial/Local Zakat Council structure, Central Zakat Fund disbursement, nisab-based deduction mechanics, or Ushr on agricultural produce — as distinct from voluntary individual zakat payment or BISP cash-transfer social protection.
---

# Pakistan Zakat and Ushr System

## Overview

Use this skill for Pakistan's **statutory** Zakat and Ushr system established under the **Zakat and Ushr Ordinance, 1980** — the compulsory deduction-at-source mechanism, the Council structure that administers collection and disbursement, and the Ushr levy on agricultural produce. This is a state-administered redistributive institution with its own legal framework, distinct from an individual Muslim's personal, voluntary zakat obligation (which this skill does not adjudicate) and distinct from unrelated federal cash-transfer programs.

## Coverage

- **Legal basis**: The Zakat and Ushr Ordinance, 1980 (and its associated Rules) established compulsory deduction of Zakat at source from specified categories of assets held in Pakistani financial institutions, and a separate Ushr levy on agricultural produce, administered through a hierarchy of statutory Councils rather than left to individual discretion.
- **Deduction at source**: Zakat is deducted automatically on the first day of Ramazan (Ramadan) from specified saving/deposit account balances and specified financial instruments (e.g., savings bank accounts, notice deposits, and certain National Savings Schemes instruments) held by Muslim citizens above the notified nisab threshold, by the holding financial institution acting as a withholding/deducting agent — this is not a voluntary payment process for the accounts and instruments covered.
- **Nisab**: The Ordinance uses a nisab value (a minimum asset threshold below which Zakat is not deductible) that is notified/revised periodically, typically expressed in monetary terms and referenced to the value of a specified quantity of silver — the current rupee nisab figure changes and should be verified for the applicable year rather than assumed (verify current figure).
- **Council structure**: A four-tier (or similar) administrative hierarchy — Central Zakat Council, Provincial Zakat Councils, and District/Local Zakat Committees — governs policy, fund allocation, and last-mile disbursement to eligible mustahiqeen (deserving recipients), with Local Zakat Committees historically playing the front-line role in identifying and disbursing to beneficiaries in their locality.
- **Central Zakat Fund**: Deducted Zakat is pooled into the Central Zakat Fund and disbursed through the Council hierarchy toward categories such as guzara (subsistence) allowances, educational stipends, health support, and support for religious seminaries/deeni madaris, among other permissible heads under the Ordinance.
- **Ushr**: A separate levy under the same Ordinance on agricultural produce above a specified threshold, intended to parallel the classical Islamic ushr obligation on landowners/cultivators; in practice, Ushr collection through the formal statutory machinery has been far less comprehensive nationally than Zakat deduction at source, with significant provincial variation in active administration.
- **Exemption/non-deduction mechanism**: Account holders who are non-Muslim, who are Muslims following a fiqh (e.g., specified Shia jurisprudence practice) that does not recognize state-administered Zakat deduction in this form, or who otherwise wish to self-assess and pay Zakat independently, can file a declaration (commonly referenced as a CZ-50 form or equivalent) with the deducting institution to be exempted from compulsory deduction at source.

## Use This Skill For

- explaining how and when Zakat is compulsorily deducted from a bank account or savings instrument under the Ordinance
- explaining the nisab concept as used in the statutory deduction mechanism
- describing the Central/Provincial/Local Zakat Council hierarchy and its respective roles
- explaining what the Central Zakat Fund is and the broad categories of disbursement it supports
- explaining Ushr as a statutory levy on agricultural produce and how it differs administratively from Zakat deduction
- explaining the exemption/declaration mechanism for account holders not subject to compulsory deduction

## When Not to Use This Skill

- For an individual's personal religious obligation calculation (e.g., computing one's own zakat liability on gold, cash, or trade goods outside the statutory deduction system) — this is a matter of personal fiqh application, not the statutory administrative system this skill covers.
- For BISP cash transfers and beneficiary/disbursement statistics — use `bisp-social-protection-statistics`; BISP is an unrelated, non-Zakat federal social protection program with its own targeting and funding mechanism.
- For general agricultural statistics or crop production data — use `mnfsr-agri-statistics` or `pbs-agriculture-census`; this skill covers Ushr as a fiscal/legal levy, not agricultural output data itself.
- For provincial agricultural income tax (a distinct provincial tax on agricultural income) — use `provincial-revenue-authorities-land-tax`, which is a separate tax base from the Ushr religious levy even though both touch agricultural land.

## Routing Rules

- If the question is about compulsory bank-account Zakat deduction, nisab, the Council hierarchy, or the Central Zakat Fund, use this skill.
- If the question is about BISP beneficiary counts, cash transfer tranches, or BISP program design, route to `bisp-social-protection-statistics` — do not conflate the two; they are administratively and legally separate systems.
- If the question is a personal fiqh calculation of zakat owed (not the statutory deduction mechanism), note that this falls outside the statutory-system scope of this skill.
- If the question concerns agricultural income tax rather than the Ushr religious levy, route to `provincial-revenue-authorities-land-tax`.

## Extraction Workflow

1. Determine whether the question concerns the statutory deduction-at-source system (Zakat Ordinance) or an individual's independent zakat payment; only the former is covered by this skill's administrative detail.
2. Identify which layer of the question applies: deduction mechanics (nisab, timing, covered instruments), Council/administrative structure, Fund disbursement categories, or Ushr.
3. Flag any specific nisab or threshold figure as needing current verification rather than stating a fixed historic number as presently accurate.
4. Keep Zakat (financial-asset deduction) and Ushr (agricultural-produce levy) as clearly separate mechanisms under the same Ordinance, since they have different collection bases and different practical administration intensity.
5. Note the exemption/declaration route (non-Muslims, dissenting fiqh, or self-assessment preference) when the question concerns why a given account was or wasn't deducted.

## Technical Rules

- Do not state a specific current nisab rupee figure as fact without hedging that it is periodically revised and should be verified for the applicable year.
- Do not describe the statutory Zakat deduction system as identical to an individual's voluntary zakat obligation; the Ordinance is a specific state-administered mechanism covering specified asset classes only, not all wealth a person may hold.
- Keep the Central Zakat Fund (statutory, Ordinance-administered) distinct from any informal or NGO-run zakat collection, and distinct from BISP, which is not a zakat fund at all.
- Note that Ushr collection through the formal Council machinery has, in practice, been much less comprehensive than Zakat deduction at source; do not imply uniform national administration.

## Validation Checklist

- Confirm whether the question is about the statutory system (Ordinance) or an individual's personal zakat calculation.
- Confirm any nisab or threshold figure is flagged for current-year verification.
- Confirm Zakat and Ushr are not conflated as a single identical mechanism.
- Confirm BISP and the Central Zakat Fund are not conflated as the same institution.
- Confirm the Council tier (Central/Provincial/Local) referenced matches the administrative function being described.

## Common Pitfalls

- Treating the statutory Ordinance-based deduction as covering all of a Muslim's zakat-eligible wealth, when it only applies to specified account/instrument categories.
- Confusing BISP cash transfers with Zakat Fund disbursements — they are separate programs with separate legal bases and funding sources.
- Stating a fixed nisab rupee value without noting it is periodically revised.
- Assuming Ushr is collected as comprehensively and automatically as bank-account Zakat deduction.
- Omitting the exemption/declaration mechanism when explaining why some account holders are not subject to deduction.

## Reference

- See [Pakistan Zakat and Ushr System Reference](references/pakistan-zakat-ushr-system.md) for the Ordinance structure, Council hierarchy, and extraction notes.
