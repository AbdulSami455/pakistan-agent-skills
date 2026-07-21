---
name: pakistan-actuarial-valuation-standards
description: Pakistan actuarial valuation standards skill. Use when analyzing insurer/takaful reserving under SECP's Actuarial Valuation Rules and the Insurance Ordinance 2000, the Pakistan Society of Actuaries' professional framework, or IAS 19 employee-benefit (pension/gratuity) actuarial valuation practice for Pakistani employers — for actuaries, auditors, and CFOs assessing reserve adequacy or employee-benefit liability, not general insurance-industry statistics.
---

# Pakistan Actuarial Valuation Standards

## Overview

Use this skill for actuarial valuation practice in Pakistan across two related but distinct domains: (1) insurer/takaful statutory reserving under SECP's Insurance Ordinance, 2000 framework and the Actuarial Valuation Rules, and (2) IAS 19 (and its local carve-outs, if any) employee-benefit actuarial valuation for corporate gratuity/pension/compensated-absence liabilities, as practiced by actuaries and reviewed by auditors during year-end close. This is the right skill for reserving methodology, actuarial function governance, and valuation-assumption discipline — not for aggregate insurer premium/asset statistics (see `secp-insurance-industry-statistics`) or for EOBI/social-security contribution mechanics (see `eobi-employer-contributions`).

## Coverage

- SECP's Actuarial Valuation Rules framework (a 2025 rules modernization was notified for public consultation, developed in consultation with the Pakistan Society of Actuaries and aligned to IAIS Insurance Core Principles), replacing/updating older valuation guidance issued under the Insurance Ordinance, 2000.
- Statutory minimum reserving requirements for life insurers (Sections 35 and 50 of the Insurance Ordinance, 2000) and non-life (general) insurers (Section 34), and how the Actuarial Valuation Rules operationalize these into methodology.
- Gross premium valuation (GPV) methodology for long-term life and family takaful business, replacing or supplementing net premium valuation approaches, plus updated premium/claims reserving methodology for short-term (non-life) insurance and takaful.
- The mandatory "Actuarial Function" that SECP has directed all insurance companies to establish — an internal function (in-house or via Appointed Actuary arrangements) responsible for reserve adequacy, solvency assessment input, and actuarial assumption-setting, scaled to the size/complexity of the insurer's business.
- The Pakistan Society of Actuaries (PSOA): the professional body (founded 2001, registered with SECP as an NPO) for actuaries in Pakistan, which is consulted on regulatory actuarial standards and administers professional development/qualification pathways (often in coordination with international bodies such as the Society of Actuaries, SOA, and the Institute and Faculty of Actuaries).
- IAS 19 (Employee Benefits) actuarial valuation practice for Pakistani employers: defined-benefit gratuity and pension scheme valuation, actuarial assumption-setting (discount rate typically referenced to Pakistan Investment Bond yields, salary growth, mortality/withdrawal tables), and the split between service cost, net interest, and remeasurement (through OCI) required for financial-statement disclosure under Pakistani-adopted IFRS/IAS.

## Use This Skill For

- explaining SECP's actuarial reserving requirements for life, non-life, and takaful insurers, and how the Actuarial Valuation Rules operationalize Insurance Ordinance sections
- distinguishing gross premium valuation from net premium valuation for long-term insurance/takaful liabilities
- describing the mandatory Actuarial Function's role and how it differs from the external/statutory auditor's role
- explaining IAS 19 defined-benefit valuation mechanics for a Pakistani employer's gratuity or pension scheme, including assumption-setting conventions
- clarifying the Pakistan Society of Actuaries' role as a professional body versus SECP's role as prudential regulator

## When Not to Use This Skill

- For insurer-wise or industry-wide premium, asset, or takaful statistics (as opposed to reserving methodology), use `secp-insurance-industry-statistics` instead.
- For EOBI old-age benefit contributions and payroll mechanics, use `eobi-employer-contributions` instead — EOBI is a state social-insurance scheme, not an employer-sponsored defined-benefit plan valued under IAS 19.
- For SECP's Voluntary Pension System (individual/employer voluntary pension funds distinct from EOBI), use `secp-voluntary-pension-system` instead — that skill covers the VPS regulatory/fund-manager framework, not actuarial reserving methodology for insurer liabilities or IAS 19 employee benefits.
- For general financial-reporting/IFRS-adoption questions beyond IAS 19 employee benefits, use `secp-financial-reporting-standards` instead.

## Routing Rules

- Use this skill when the question concerns actuarial reserving methodology, actuarial assumptions, or the actuarial function's governance role — for an insurer/takaful operator or for a corporate employee-benefit scheme.
- If the question is about how much premium or assets an insurer reported for a given year (not methodology), route to `secp-insurance-industry-statistics`.
- If the question is about EOBI payroll contributions, route to `eobi-employer-contributions`; if about SECP-licensed voluntary pension funds, route to `secp-voluntary-pension-system`.
- Treat this skill as describing regulatory/professional framework and valuation mechanics only — it is not a substitute for an engagement-specific actuarial valuation performed by a qualified, licensed actuary (Fellow/Associate of PSOA or an internationally recognized actuarial body) with access to the specific scheme's data.

## Extraction Workflow

1. Identify whether the question is about insurer/takaful statutory reserving (Insurance Ordinance + Actuarial Valuation Rules track) or employer-sponsored benefit-scheme valuation (IAS 19 track) — the governing framework, valuation method, and audience differ.
2. For insurer reserving, confirm the business line (long-term life/family takaful vs. short-term non-life/general takaful), since valuation methodology (gross premium valuation vs. premium/claims reserving) differs by line.
3. For IAS 19 valuations, confirm which actuarial assumptions are in play (discount rate, salary escalation, mortality/withdrawal, retirement age) and whether the valuation is for gratuity, pension, or compensated absences, since these can carry different assumption sets.
4. Distinguish the Actuarial Function's internal governance role from the statutory/external auditor's role in auditing the financial statements that incorporate the actuarial valuation — these are complementary, not interchangeable, control points.
5. Note the effective date of the governing rules — SECP's Actuarial Valuation Rules were undergoing a substantial 2025 modernization (notified for public consultation); confirm whether a description reflects the rules in force at the relevant valuation date or a draft/proposed version.

## Technical Rules

- Do not describe net premium valuation and gross premium valuation as interchangeable; GPV explicitly reserves for expected future expenses and lapses within the liability calculation in a way traditional net premium valuation does not.
- Keep life/family-takaful (long-term) reserving methodology distinct from non-life/general-takaful (short-term) premium and claims reserving; they use different technical bases (e.g., unearned premium reserves and claims reserves for short-term business vs. policy liability projections for long-term business).
- For IAS 19, do not conflate the current service cost, net interest cost, and actuarial gain/loss (remeasurement) components — they are presented differently (profit-or-loss vs. OCI) under IAS 19 as adopted in Pakistan.
- Do not state a specific discount-rate convention, mortality table, or minimum solvency margin as a fixed universal fact; these are assumption choices an appointed actuary makes based on market data (e.g., PIB yields as of the valuation date) and should be sourced to the specific valuation report or current regulatory guidance.
- Always flag that this skill provides regulatory/framework orientation, not a substitute for the judgment of a qualified actuary (PSOA Fellow/Associate or equivalent international designation) conducting an actual valuation engagement.

## Validation Checklist

- Confirm whether the question is insurer/takaful statutory reserving or corporate IAS 19 employee-benefit valuation before answering.
- For insurer reserving, confirm the business line (long-term vs. short-term) and whether gross premium valuation or premium/claims reserving methodology applies.
- For IAS 19, confirm which liability (gratuity, pension, leave encashment) and which assumption set is being discussed.
- Check whether any cited rule reflects the current Actuarial Valuation Rules or an earlier/draft version, given the 2025 modernization process.
- Flag reliance on a qualified actuary's judgment for any engagement-specific figure rather than presenting a generic assumption as authoritative.

## Common Pitfalls

- Treating gross premium valuation and net premium valuation as the same methodology.
- Confusing the SECP-mandated Actuarial Function with the statutory external auditor's role.
- Presenting a specific discount rate or mortality table as a fixed regulatory requirement rather than an actuary's assumption choice grounded in current market/demographic data.
- Conflating EOBI (state social insurance) or SECP's Voluntary Pension System (individually elected pension funds) with employer-sponsored IAS 19 defined-benefit schemes — these are governed by entirely different frameworks.
- Citing the pre-2025 Actuarial Valuation framework as current without checking whether the 2025 Rules have since been finalized and notified.

## Reference

- See [Pakistan Actuarial Valuation Standards Reference](references/pakistan-actuarial-valuation-standards.md) for source documents, reserving-methodology definitions, and extraction notes.
