---
name: pakistan-anti-money-laundering-enforcement
description: Pakistan AML/CFT legal enforcement pipeline skill. Use when explaining or analyzing the Anti-Money Laundering Act 2010 (AMLA), the Financial Monitoring Unit (FMU), predicate offences, investigation/prosecution pathway for money laundering, the National AML/CFT Coordination Committee, or Pakistan's FATF grey-list history — as distinct from a bank's internal AML/CFT compliance program.
---

# Pakistan Anti-Money Laundering Enforcement

## Overview

Use this skill for Pakistan's **legal and enforcement** AML/CFT (Anti-Money Laundering / Combating the Financing of Terrorism) pipeline — the statutory framework under the **Anti-Money Laundering Act, 2010 (AMLA)**, the Financial Monitoring Unit's (FMU) role as financial intelligence unit, predicate offences, and the investigation-to-prosecution pathway. This is the legal/institutional enforcement layer, distinct from a bank or financial institution's own internal AML/CFT compliance program (customer due diligence, transaction monitoring policy, internal reporting) which is a supervisory/prudential matter under SBP's regulatory framework. As of this repository's current content, there is no separate skill dedicated to bank-level AML/CFT compliance procedure; if such a skill is added later, route internal-compliance-program questions there and keep this skill focused on the statutory/enforcement pipeline.

## Coverage

- **Legal basis**: The Anti-Money Laundering Act, 2010 (AMLA) is Pakistan's principal money-laundering statute, criminalizing money laundering as a standalone offence tied to "predicate offences" (the underlying criminal activity generating illicit proceeds — e.g., corruption, narcotics trafficking, terrorism financing, fraud, and other scheduled offences listed in the Act's Schedule). AMLA has been amended multiple times, including to expand the predicate-offence list and strengthen enforcement powers, often in response to FATF Mutual Evaluation and Action Plan requirements — treat the exact current predicate-offence list and penalty figures as needing verification against the current consolidated Act text rather than a fixed historical version.
- **Financial Monitoring Unit (FMU)**: Pakistan's Financial Intelligence Unit (FIU), established under AMLA, receives Suspicious Transaction Reports (STRs) and Currency Transaction Reports (CTRs) from reporting entities (banks, DNFBPs — Designated Non-Financial Businesses and Professions — and other obligated persons), analyzes them, and disseminates intelligence to law enforcement/investigation agencies. FMU is the financial-intelligence node, not itself a prosecuting authority.
- **Investigation and prosecution pathway**: Money laundering cases in Pakistan can be investigated by multiple agencies depending on the predicate offence — e.g., the Federal Investigation Agency (FIA) for many financial-crime-linked predicate offences, the National Accountability Bureau (NAB) where corruption is the predicate offence, or provincial/federal police and the Anti-Narcotics Force where relevant — with AMLA-specific money laundering charges typically prosecuted before designated courts. The specific agency and court track depends on which predicate offence and which investigative agency's jurisdiction is engaged; do not assume a single uniform pathway for every case.
- **National AML/CFT Coordination Committee**: A high-level inter-agency coordination body (structure and exact composition should be verified against current notification) established to coordinate Pakistan's national AML/CFT policy response across FMU, regulators (SBP, SECP), law enforcement, and prosecutorial agencies, particularly salient during Pakistan's FATF Action Plan implementation period.
- **FATF grey-list context**: Pakistan was placed on the Financial Action Task Force (FATF) grey list (increased monitoring list) in **June 2018**, required to implement a multi-point Action Plan addressing AML/CFT deficiencies, and was removed from the grey list in **October 2022** following FATF's assessment that the Action Plan items were substantially completed — this sequence (2018 listing, 2022 exit) reflects the well-documented public record; if asked for granular Action Plan item counts or specific technical-compliance ratings, flag those as needing verification against the specific FATF Mutual Evaluation Report/Follow-up Report rather than asserting exact figures from memory.
- **Confiscation/asset forfeiture**: AMLA provides for freezing, seizure, and confiscation of property/proceeds linked to money laundering, operating alongside (and sometimes overlapping procedurally with) asset-recovery provisions under NAB's own ordinance when corruption is the predicate offence.

## Use This Skill For

- explaining AMLA's structure, predicate-offence concept, and how money laundering is charged as a standalone offence layered on an underlying crime
- explaining the Financial Monitoring Unit's role as Pakistan's financial intelligence unit and its STR/CTR intake-and-dissemination function
- describing which agencies typically investigate/prosecute money laundering depending on the predicate offence
- explaining the National AML/CFT Coordination Committee's coordination role
- providing the FATF grey-list timeline context (2018 listing, 2022 exit) for Pakistan's AML/CFT reform trajectory
- explaining AMLA's asset freezing/seizure/confiscation provisions

## When Not to Use This Skill

- For a bank or financial institution's internal AML/CFT compliance program (KYC/CDD policy, internal transaction monitoring thresholds, SBP prudential AML regulations for banks) — this repository currently has no dedicated bank-compliance-program skill; treat such questions as adjacent but outside this skill's enforcement-pipeline scope, and note the gap rather than answering with enforcement-pipeline material.
- For NAB's broader accountability pipeline (inquiry, investigation, reference, plea bargain, recovery figures) where corruption itself — not the laundering of its proceeds — is the focus, use `nab-accountability-data`; this skill should be used specifically for the money-laundering/AMLA angle, cross-referencing NAB only where corruption is the predicate offence for a laundering charge.
- For cybercrime-specific enforcement (PECA offences) even where cyber-enabled fraud generates laundered proceeds — use `nccia-cybercrime-peca` for the cybercrime-specific investigative angle.
- For Shariah governance or Islamic banking compliance structures — use `sbp-shariah-governance-islamic-banking`; unrelated to AML/CFT enforcement.

## Routing Rules

- If the question is about the statutory AMLA framework, FMU's intelligence function, predicate offences, or the investigation/prosecution pathway for money laundering, use this skill.
- If the question is about NAB's own accountability process where corruption is the substantive offence (not specifically the laundering-of-proceeds angle), route primarily to `nab-accountability-data` and use this skill only for the overlapping AMLA/laundering-charge dimension.
- If the question is about a specific PECA cybercrime offence or NCCIA investigation process, route to `nccia-cybercrime-peca`.
- If the question is about a bank's internal compliance obligations rather than the state's enforcement pipeline, note that no dedicated skill currently exists in this repository for that angle; do not stretch this skill to cover it.

## Extraction Workflow

1. Identify whether the question concerns the legal/statutory enforcement pipeline (AMLA, FMU, predicate offences, prosecution) or a financial institution's internal compliance program; only the former is this skill's scope.
2. If a predicate offence is named, identify which investigative agency's jurisdiction is likely engaged (FIA, NAB, ANF, police) based on the nature of that predicate offence, rather than assuming a single agency handles all money-laundering cases.
3. Keep FMU's financial-intelligence function (receiving/analyzing STRs/CTRs, disseminating intelligence) distinct from the investigating agency's law-enforcement function and from the prosecuting authority's court role — these are sequential, separate functions.
4. If FATF grey-list context is relevant, cite the 2018 listing and 2022 exit as the general timeline, and flag any more granular Action Plan item detail as needing verification against the specific FATF report.
5. Distinguish AMLA-based asset confiscation from NAB-based asset recovery when both could apply (corruption-predicate laundering cases).

## Technical Rules

- Do not name a single agency as "the" money-laundering investigation authority in Pakistan; jurisdiction depends on the predicate offence and can involve FIA, NAB, ANF, or other agencies.
- Do not conflate FMU (financial intelligence unit, receives/analyzes reports) with an investigating or prosecuting authority; FMU disseminates intelligence but does not itself prosecute.
- State the FATF grey-list 2018-2022 timeline only at the confidence level of well-documented public record; hedge any more granular technical-compliance-rating or specific Action Plan item count.
- Keep predicate-offence-specific detail (e.g., corruption vs. narcotics vs. fraud) attached to the correct downstream investigative agency rather than generalizing.
- Do not present this skill's enforcement-pipeline material as covering bank-level internal AML/CFT compliance procedure.

## Validation Checklist

- Confirm the question is about the enforcement/legal pipeline, not internal bank compliance procedure.
- Confirm the correct investigative agency is named based on the predicate offence involved, not assumed uniformly.
- Confirm FMU's role is described as financial-intelligence intake/analysis/dissemination, not investigation or prosecution.
- Confirm any FATF grey-list detail beyond the 2018/2022 timeline is flagged as needing verification.
- Confirm NAB-specific accountability process questions are routed primarily to `nab-accountability-data`.

## Common Pitfalls

- Treating FMU as a law-enforcement or prosecuting body rather than a financial intelligence unit.
- Assuming a single agency (e.g., always FIA, or always NAB) investigates every money-laundering case regardless of predicate offence.
- Overstating granular FATF Action Plan technical-compliance detail beyond the well-documented 2018 listing/2022 exit timeline.
- Conflating AMLA enforcement with a bank's internal AML/CFT compliance obligations.
- Confusing NAB's corruption-accountability pipeline with the AMLA money-laundering pipeline when they only partially overlap (corruption as one possible predicate offence among several).

## Reference

- See [Pakistan AML Enforcement Reference](references/pakistan-anti-money-laundering-enforcement.md) for AMLA structure, FMU function, and FATF timeline sourcing notes.
