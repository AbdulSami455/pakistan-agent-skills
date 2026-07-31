---
name: pakistan-child-protection-laws
description: Pakistan child protection legal framework skill. Use when a task concerns the Juvenile Justice System Act 2018, child-marriage restraint laws (Child Marriage Restraint Act 1929 and Sindh's higher minimum-age provincial law), the Zainab Alert, Response and Recovery Act 2020, or the National Commission on the Rights of Child Act 2017 — as distinct from child statistics/data or general adult criminal procedure.
---

# Pakistan Child Protection Laws

## Overview

Use this skill when a task requires explaining Pakistan's child-specific protective legal framework — how juvenile offenders are processed differently from adults, what the minimum marriage age is (and how it varies by province), how the Zainab Alert system operates for missing/abducted/trafficked children, and what the National Commission on the Rights of Child does. This is a child-specific legal/institutional-framework skill, not a statistics skill and not a general adult criminal-procedure skill — it explains the protective legal architecture, not child mortality/nutrition/education indicators or ordinary FIR/bail mechanics for adult accused.

## Coverage

- **Juvenile Justice System Act, 2018 (JJSA)**: the federal statute governing the treatment of children (defined by a specified age threshold — commonly a person under 18 years — verify exact statutory age definition and any offence-category exceptions) in conflict with the law. Establishes Juvenile Courts, restricts joint trial of a child with an adult co-accused, restricts and regulates detention (including a general presumption favoring bail and alternatives to detention, subject to hedging on offence-severity exceptions), requires probation and social-welfare-officer involvement, and provides for diversion (resolving certain matters outside formal trial, e.g., through reconciliation) for less serious offences — superseded the earlier Juvenile Justice System Ordinance, 2000.
- **Child Marriage Restraint Act, 1929 (as amended)**: the historical federal-origin statute (pre-partition, continued in force and amended over time) setting a minimum marriage age and penalizing solemnization of, or participation in, an underage marriage. Post-devolution, provinces have legislative competence to set their own minimum marriage age; Sindh enacted the Sindh Child Marriage Restraint Act, 2013, raising the minimum marriage age for both boys and girls to 18 years in that province — other provinces have, at various points, considered but not uniformly enacted an equivalent 18-year threshold, and the nationally applicable minimum age outside Sindh (commonly cited historically as 16 years for females and 18 for males under the 1929 Act's original terms) should be verified rather than assumed, given ongoing legislative reform efforts and proposed federal/provincial bills to raise the age. Do not state a single uniform minimum marriage age for all of Pakistan without flagging Sindh's distinct, higher threshold.
- **Zainab Alert, Response and Recovery Act, 2020**: enacted following high-profile child abduction/murder cases, establishes a rapid-alert mechanism and institutional response framework (a dedicated agency/response mechanism, commonly referenced as the Zainab Alert, Response and Recovery Agency, coordinating with police) for missing, abducted, or trafficked children, intended to trigger an immediate, coordinated search-and-recovery response analogous in concept to international "Amber Alert"-style systems, adapted to Pakistan's institutional context.
- **National Commission on the Rights of Child Act, 2017**: establishes the National Commission on the Rights of Child (NCRC) as an independent statutory body mandated to monitor implementation of child-rights law and policy in Pakistan (including Pakistan's obligations under the UN Convention on the Rights of the Child), review laws for consistency with child-rights standards, receive and inquire into complaints of child-rights violations, and recommend policy/legal reform — a monitoring/advisory and complaints-review body, not itself a prosecutorial or law-enforcement agency.
- **Provincial child protection institutions**: provinces have separately established child protection bureaus/authorities (e.g., Punjab's child protection institutional framework) handling child-welfare casework (removal from abusive situations, institutional care placement) distinct from both the juvenile-justice (offender-focused) and NCRC (monitoring/advisory) functions — flag this as a third, casework-focused institutional layer when relevant.

## Use This Skill For

- explaining how the Juvenile Justice System Act 2018 modifies ordinary criminal procedure for a child accused (separate courts, bail presumption, detention restrictions, diversion)
- explaining the minimum marriage age framework, explicitly distinguishing Sindh's 18-year threshold from the position in other provinces, with appropriate hedging on the current age outside Sindh
- explaining the Zainab Alert, Response and Recovery Act 2020's rapid-response mechanism for missing/abducted/trafficked children
- explaining the National Commission on the Rights of Child's monitoring/advisory/complaints mandate and distinguishing it from a prosecutorial or law-enforcement role
- distinguishing juvenile-offender protective law from child-victim protective law (marriage restraint, missing-child response) within this skill's combined scope

## When Not to Use This Skill

- For child statistics/data — mortality, nutrition, immunization, WASH, education access indicators — use `unicef-pakistan-data`; this skill covers the legal/institutional protective framework, not indicator data.
- For general adult criminal procedure (FIR registration, bail for adult accused, CrPC investigation stages) — use `pakistan-criminal-procedure-fir` for the general framework that the Juvenile Justice System Act 2018 modifies for child accused; this skill covers the juvenile-specific modifications, not the baseline adult procedure itself.
- For family-law custody/guardianship disputes between parents — use `pakistan-family-law-courts`; this skill covers child-protection statutes (juvenile justice, marriage-age restraint, missing-child response), not ordinary civil custody litigation.
- For general education statistics or curriculum — use `pakistan-education-statistics` or `pakistan-national-curriculum-textbooks`.

## Routing Rules

- If the question needs a statistic (child mortality rate, out-of-school children count, nutrition indicator) rather than a legal-framework explanation, route to `unicef-pakistan-data`.
- If the question is about ordinary adult criminal procedure and only incidentally involves a child witness/victim rather than a child accused or child-protection statute, route to `pakistan-criminal-procedure-fir` and note the JJSA modifications only if a juvenile accused is actually involved.
- If the question is about custody/guardianship between parents rather than a child-protection/juvenile-justice/marriage-age matter, route to `pakistan-family-law-courts`.
- If the question asks for the minimum marriage age without specifying a province, answer with explicit province-differentiated hedging (Sindh's 18-year threshold vs. the position elsewhere) rather than stating one number as if uniformly nationwide.
- If the question is about NCRC's role, keep its monitoring/advisory/complaints-review function distinct from law enforcement or prosecutorial action — do not describe NCRC as capable of directly prosecuting a child-rights violation.

## Extraction Workflow

1. Identify which child-protection domain the question concerns: juvenile offenders (JJSA 2018), child marriage (restraint laws), missing/abducted children (Zainab Alert Act), or rights monitoring/advisory (NCRC Act) — these are distinct statutes with distinct institutional mechanisms.
2. For a juvenile-justice question, confirm the statutory age threshold and any offence-category exceptions to the general bail-presumption/detention-restriction rules before answering, and hedge specifics not confidently known.
3. For a marriage-age question, always specify which province/jurisdiction is being discussed and flag Sindh's distinct 18-year minimum explicitly rather than giving a single blended national answer.
4. For a missing/abducted-child question, describe the Zainab Alert Act's rapid-response/coordination mechanism and note it operates alongside, not instead of, ordinary FIR/police-investigation processes for the underlying criminal offense.
5. For an NCRC question, describe its monitoring, law-review, and complaints-inquiry mandate, and explicitly note it is not a prosecutorial or law-enforcement body.
6. Flag any specific age threshold, penalty range, or provincial statute detail not confidently known as "(verify)" rather than asserting invented precision.

## Technical Rules

- The Juvenile Justice System Act 2018 modifies, rather than replaces, general CrPC criminal procedure for child accused — a child in conflict with the law is still subject to the underlying substantive offence definitions (PPC or other law) but proceeds through juvenile-specific procedural safeguards (separate trial, restricted detention, diversion options, probation-officer involvement).
- Do not state a single nationwide minimum marriage age without flagging Sindh's distinct, higher (18-year) threshold under its own provincial Child Marriage Restraint Act 2013 — this is a genuine, legally significant provincial variation, not a minor detail.
- The Zainab Alert, Response and Recovery Act 2020's rapid-alert mechanism is a coordination/response-triggering framework; it operates alongside, not as a replacement for, the underlying criminal investigation (FIR, police investigation) into an abduction/trafficking offense.
- NCRC is a monitoring, advisory, and complaints-review statutory body under the National Commission on the Rights of Child Act 2017 — it is not a court, prosecutor, or police agency, and does not itself convict or prosecute anyone for a child-rights violation.
- Distinguish juvenile-offender protective law (JJSA, protecting a child accused of an offence) from child-victim protective law (marriage-age restraint, Zainab Alert) — both fall within this skill's scope but serve different protective purposes and should not be conflated in an answer.

## Validation Checklist

- Confirm which child-protection statute/domain (JJSA, marriage-age restraint, Zainab Alert, NCRC) the question actually concerns.
- If a marriage-age question, confirm the answer differentiates Sindh's 18-year threshold from the position in other provinces rather than giving one blended figure.
- If a juvenile-justice question, confirm the answer describes JJSA as modifying, not replacing, general CrPC procedure.
- If an NCRC question, confirm the answer describes a monitoring/advisory/complaints role, not a prosecutorial one.
- Flag any specific age threshold, penalty, or provincial statute detail not confidently known as "(verify)".

## Common Pitfalls

- Stating a single nationwide minimum marriage age without flagging Sindh's distinct, higher threshold.
- Describing the Juvenile Justice System Act 2018 as an entirely separate/parallel criminal code rather than a set of procedural modifications layered on general CrPC/PPC.
- Treating the Zainab Alert Act as replacing, rather than supplementing, ordinary FIR/police-investigation processes for the underlying offense.
- Describing NCRC as able to prosecute or convict, rather than monitor, review, and refer/recommend.
- Conflating child-protection legal-framework questions with `unicef-pakistan-data`'s statistical scope.
- Conflating this skill's juvenile-offender and marriage-age/missing-child scope with ordinary parental custody disputes under `pakistan-family-law-courts`.

## Reference

- See [Pakistan Child Protection Laws Reference](references/pakistan-child-protection-laws.md) for JJSA procedural detail, the marriage-age provincial variation, and the Zainab Alert/NCRC institutional structure.
