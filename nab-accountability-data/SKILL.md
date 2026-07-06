---
name: nab-accountability-data
description: National Accountability Bureau (NAB) skill. Use when explaining NAB's anti-corruption investigation-to-prosecution pipeline (inquiry, investigation, reference, Accountability Court trial), plea bargain/voluntary return, or NAB recovery-figure announcements under the National Accountability Ordinance 1999 — and for distinguishing NAB from an AGP audit finding, from FIA, and from ordinary police/courts.
---

# NAB Accountability Data

## Overview

Use this skill when a task concerns Pakistan's National Accountability Bureau (NAB) — its legal mandate, its case pipeline from inquiry through prosecution in Accountability Courts, its plea-bargain/voluntary-return mechanism, or its periodic recovery-figure announcements. This is a criminal-accountability-process skill. It is explicitly not an audit-findings skill: an Auditor-General of Pakistan (AGP) report flagging financial irregularities is a different kind of document from a NAB reference alleging a criminal offense, and the two are frequently and incorrectly conflated in secondary reporting.

## Coverage

- **Legal basis**: The National Accountability Ordinance, 1999 (NAO 1999), as amended multiple times. Amendments over the years have adjusted NAB's jurisdictional scope, monetary thresholds for cognizable cases, and procedural rules — describe amendment effects generally and flag specific amendment years/provisions as "(verify)" unless you are confident of the exact year and text, since this area has changed more than once and sources disagree on some details.
- **Case pipeline**: complaint verification → inquiry (fact-finding, can summon records/individuals) → investigation (formal, can lead to arrest) → reference (formal charge document filed in an Accountability Court) → trial before an Accountability Court (a special court distinct from ordinary criminal courts) → appeal (to the relevant High Court and onward).
- **Plea bargain / voluntary return**: a distinctive NAB mechanism under the NAO 1999 allowing an accused to return allegedly ill-gotten assets/gains (in part or full) in exchange for the closure of the case against them (plea bargain typically involves an admission and court approval; voluntary return can occur at an earlier stage before a reference is filed). This mechanism is a recurring subject of public and legal controversy because it allows case closure without a full criminal trial or conviction.
- **Recovery announcements**: NAB periodically announces cumulative "recovery" figures (amounts recovered through convictions, plea bargains, and voluntary returns). A significant share of reported recoveries in NAB's own historical disclosures has been in the form of non-cash assets (land, property, shares, other assets) valued at an assessed figure, rather than cash actually deposited into the government treasury — this distinction matters for accurate reporting and should be flagged whenever a recovery figure is cited.
- **Accountability Courts**: special courts established under the NAO 1999 to try NAB references, operating under a distinct procedure from ordinary Sessions/Magistrate criminal courts.

## Use This Skill For

- explaining NAB's case pipeline: inquiry, investigation, reference, and trial before an Accountability Court
- explaining the plea bargain / voluntary return mechanism and how it differs from a criminal conviction
- contextualizing a NAB recovery-figure announcement, including the cash-vs-non-cash-asset composition question
- distinguishing a NAB reference/investigation from an AGP audit report's findings
- distinguishing NAB's jurisdiction and mandate from FIA's and from ordinary police
- explaining, at a general level, how NAB amendments have changed NAB's scope over time (without asserting a specific unverified figure/date as fact)

## When Not to Use This Skill

- For Auditor-General of Pakistan (AGP) audit findings, financial/compliance irregularities in government accounts, or Public Accounts Committee (PAC) review of audit paras — these belong to a hypothetical/companion AGP-audit skill, not this one. Do not use NAB accountability data to answer a question that is actually about an AGP audit report; the two describe fundamentally different kinds of findings (audit irregularity vs. criminal allegation).
- For FIA (Federal Investigation Agency) cases — cybercrime, human trafficking, passport/immigration fraud, and other federal offenses outside NAB's corruption-specific mandate — FIA is a separate agency with separate jurisdiction; do not describe an FIA case as a NAB case or vice versa.
- For ordinary police/criminal court cases unrelated to corruption by a public office-holder — NAB's mandate is specifically corruption and corruption-related offenses as defined in the NAO 1999, not general criminal law.
- For court caseload/pendency statistics generally — use `ljcp-judicial-statistics`; that skill covers aggregate court statistics across the judiciary, while this skill covers NAB's own case-pipeline and institutional data specifically.
- For the constitutional/structural description of the judiciary — use `pakistan-constitution-governance`; this skill covers NAB as an investigative/prosecutorial body, not the judiciary's constitutional design (Accountability Courts are statutory special courts, not part of the constitutionally described ordinary court hierarchy described in that skill).
- For legislative status of a NAB (Amendment) Bill working through Parliament — use `parliament-legislative-tracker` for the bill's live status; use this skill once an amendment is enacted and in force.

## Routing Rules

- If a source says "AGP found irregularities/misuse of Rs. X" — do not restate this as "NAB found corruption of Rs. X" or "Rs. X was stolen." An AGP audit objection is a compliance/financial-irregularity finding reviewed by the Public Accounts Committee, not a judicial or NAB determination of corruption; flag this distinction explicitly and note that AGP-audit-specific data belongs in a separate audit-focused skill, not this one.
- If the question is about a cybercrime, trafficking, or immigration-fraud case — route to FIA's mandate conceptually (this repo may not have a dedicated FIA skill; if not, state clearly that the case is outside NAB's mandate rather than answering as if NAB were the relevant agency).
- If the question is about general court backlog/disposal statistics rather than a NAB-specific case or the Accountability Court system specifically — route to `ljcp-judicial-statistics`.
- If the question is about the judiciary's constitutional structure rather than NAB's statutory investigative/prosecutorial process — route to `pakistan-constitution-governance`.
- If the question is about a NAB amendment bill still moving through Parliament rather than a NAB amendment already in force — route to `parliament-legislative-tracker` for the bill's status.

## Extraction Workflow

1. Identify which stage of the NAB pipeline the question concerns: inquiry, investigation, reference filed, trial ongoing, verdict/conviction, or appeal — these are distinct stages and a case at an early stage (e.g., "under inquiry") should not be described as if a reference has been filed or a conviction has occurred.
2. If a recovery figure is cited, determine whether it is described as cash recovered, an assessed value of non-cash assets (land/property/shares), or a mixed total — and state this composition explicitly rather than presenting the headline total as if it were all cash.
3. If a plea bargain or voluntary return is involved, note that this results in case closure/asset return, not a criminal conviction — do not describe a plea-bargain outcome as "convicted of corruption."
4. If the source data originates from an AGP audit report rather than a NAB reference or court record, explicitly relabel it as an audit finding, not a NAB case, and note it would need Public Accounts Committee review, not Accountability Court prosecution, to proceed further.
5. Confirm which agency (NAB, FIA, ordinary police) actually has jurisdiction over the described conduct before attributing a case to NAB.
6. For any specific amendment year, threshold, or numeric claim about NAB's current scope that you are not fully confident of, state it with an explicit "(verify)" flag rather than presenting it as settled.

## Technical Rules

- NAB investigates and prosecutes offenses under the NAO 1999 (corruption and corruption-related practices by, typically, public office-holders and in some cases private individuals/entities involved in such practices) through a dedicated pipeline: inquiry → investigation → reference → Accountability Court trial → appeal.
- Accountability Courts are special courts created under the NAO 1999, distinct from ordinary Sessions Courts/Magistrate Courts; do not describe a NAB reference as being tried in an "ordinary criminal court."
- A plea bargain/voluntary return is legally distinct from a conviction: it typically involves the accused returning assets and the court/NAB closing the case without a finding of guilt in the same sense as a full trial verdict — do not equate "recovered via plea bargain" with "convicted."
- NAB's own reported cumulative "recovery" figures have historically included a large non-cash component (land, property, other assets, valued at an assessed figure) alongside actual cash — do not report a NAB recovery headline figure as if it were entirely cash recovered into the treasury without checking the cash/non-cash breakdown.
- An AGP audit report's "irregularity," "misappropriation," or "loss to the exchequer" figure is an audit finding subject to management response and Public Accounts Committee review — it is not, by itself, a judicial or prosecutorial finding of corruption, and does not automatically become a NAB case. Only a subset of audit-flagged matters, if at all, are separately investigated and pursued by NAB (or other agencies) as criminal matters.
- FIA and NAB are separate federal agencies with separate governing laws and separate case types; do not use one agency's data to answer a question about the other's caseload.
- NAB's jurisdictional scope and procedural rules have been amended multiple times; describe amendment effects in general terms and flag specific years/thresholds you are not confident of as "(verify)" rather than stating them as settled fact.

## Validation Checklist

- Confirm which pipeline stage (inquiry, investigation, reference, trial, conviction, appeal) the claim actually describes.
- If a recovery figure is cited, confirm whether it is cash, non-cash-asset value, or a combined total, and state this explicitly.
- Confirm the source data is actually a NAB record and not an AGP audit report being mislabeled as a NAB corruption finding.
- Confirm the case is actually within NAB's mandate and not an FIA or ordinary-police matter.
- Flag any NAB amendment year, threshold, or scope claim you are not fully confident of as "(verify)" rather than presenting invented precision.

## Common Pitfalls

- Restating an AGP audit "irregularity" figure as "NAB found corruption of Rs. X" — these are different institutions producing different kinds of findings; the AGP figure requires PAC review, not automatic NAB prosecution.
- Describing a plea bargain or voluntary return as a criminal "conviction."
- Reporting a NAB cumulative recovery figure as pure cash without noting that a substantial share has historically been non-cash assets valued at an assessed figure.
- Confusing NAB with FIA (different agency, different jurisdiction — cybercrime, trafficking, immigration fraud fall under FIA, not NAB) or with ordinary police.
- Treating "under NAB inquiry" as equivalent to "charged" or "convicted" — an inquiry is the earliest, most preliminary stage and may never progress to a reference.
- Presenting a specific NAB amendment year or monetary threshold from memory as certain fact without flagging uncertainty, given that NAB's governing law has been amended multiple times with details that are easy to misstate.

## Reference

- See [NAB Accountability Data Reference](references/nab-accountability-data.md) for the case-pipeline structure, plea-bargain mechanics, recovery-figure composition notes, and the NAB/AGP/FIA disambiguation table.
