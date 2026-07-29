---
name: pakistan-mental-health-substance-abuse
description: Pakistan mental health and substance-abuse policy skill. Use when a task concerns the Mental Health Ordinance 2001 and post-18th-Amendment provincial mental health acts, involuntary/voluntary psychiatric admission procedure, the Anti-Narcotics Force (ANF) mandate under the Control of Narcotics Substances Act 1997, drug scheduling, or drug-treatment/rehabilitation policy framework — as distinct from general health statistics or communicable-disease surveillance.
---

# Pakistan Mental Health and Substance Abuse Framework

## Overview

Use this skill when a task requires explaining Pakistan's legal/institutional framework for mental health care (admission procedures, patient rights, the licensing/oversight structure for psychiatric facilities) or its narcotics-control and drug-treatment framework (ANF's mandate, drug scheduling and offence thresholds, treatment/rehabilitation policy). This is a legal-and-institutional-framework skill, not a statistics skill — it explains what the law and the responsible agencies do, not what current prevalence/caseload figures are.

## Coverage

- **Mental Health Ordinance, 2001**: the original federal framework governing psychiatric care in Pakistan prior to devolution — established Mental Health Authorities/Boards, admission categories (informal/voluntary admission, and involuntary/compulsory admission subject to statutory safeguards and periodic review), and patient-rights protections (e.g., against arbitrary detention in a psychiatric facility). After the 18th Amendment (2010) devolved health legislation to the provinces, mental health became a provincial subject, and provinces have enacted (or are in the process of enacting) their own mental health legislation — treat the 2001 Ordinance as the historical federal baseline and hedge on which provinces have since replaced it with their own act versus continuing to apply the 2001 Ordinance by adaptation.
- **Provincial mental health legislation**: Sindh enacted the Sindh Mental Health Act, 2013; Punjab has considered/enacted its own mental health legislation in the post-devolution period (exact current title/year should be verified rather than assumed, since provincial mental health legislative activity has continued and this skill should hedge on the current in-force provincial statute for Punjab, KP, and Balochistan specifically). Each provincial act, where enacted, generally follows the same broad structure as the 2001 Ordinance: a licensing/oversight authority for psychiatric facilities, defined admission categories, and safeguards (periodic medical review, right to apply for discharge, restrictions on involuntary admission) for compulsorily admitted patients.
- **Involuntary admission safeguards**: mental health legislation in Pakistan (federal 2001 Ordinance and provincial successors) generally requires medical certification by qualified practitioners, time-limited initial admission orders subject to periodic review/renewal, and a route for the patient (or a representative) to apply for discharge or challenge continued detention — reflecting an intent to prevent indefinite or arbitrary confinement, though actual implementation capacity (functioning Mental Health Authorities/Boards, licensed facility oversight) has been a recurring policy concern documented in secondary/NGO reporting, which should be treated as a distinct, generally softer-sourced claim from the statutory text itself.
- **Control of Narcotics Substances Act, 1997 (CNSA)**: the principal federal narcotics-control statute, defining scheduled narcotic/psychotropic substances and controlled precursor chemicals, prescribing offences (possession, trafficking, manufacture, financing of narcotics offences) with penalties that scale with the quantity involved, and establishing the institutional and procedural framework for narcotics enforcement, including special courts for narcotics offences.
- **Anti-Narcotics Force (ANF)**: the federal law-enforcement agency with primary responsibility for narcotics-control enforcement under the CNSA 1997, operating under the Ministry of Narcotics Control — mandate includes interdiction, investigation and prosecution support for narcotics offences, precursor-chemical control, and coordination with international counter-narcotics bodies (e.g., UNODC) given Pakistan's proximity to Afghan opiate-trafficking routes.
- **Drug scheduling and quantity thresholds**: the CNSA 1997 and its schedules classify narcotic drugs, psychotropic substances, and controlled substances, with statutory quantity thresholds distinguishing simple possession from trafficking-level offences and affecting applicable punishment ranges (including capital/life-imprisonment exposure for large trafficked quantities in the statute's original and amended form) — specific threshold quantities and current penalty tiers should be flagged "(verify current schedule)" rather than stated with invented precision, since schedules and thresholds have been subject to amendment.
- **Treatment and rehabilitation framework**: Pakistan's drug-demand-reduction policy generally distinguishes enforcement/interdiction (ANF's core mandate) from treatment/rehabilitation, the latter delivered through a mix of federal/provincial government treatment centers, ANF-run rehabilitation facilities, and NGO/private treatment providers — reflecting an international drug-policy framing (supply reduction vs. demand reduction vs. harm reduction) that Pakistan's narcotics policy documents generally reference, though the balance of resources and current national drug policy document specifics should be verified rather than assumed.

## Use This Skill For

- explaining the mental health admission framework (voluntary vs. involuntary) and patient-rights safeguards under the 2001 Ordinance or an applicable provincial mental health act
- explaining which level of government (federal historical baseline vs. current provincial statute) governs mental health legislation post-18th Amendment, with appropriate hedging on province-specific current statutes
- explaining ANF's institutional mandate and its relationship to the CNSA 1997
- explaining the structure of narcotics offence classification (possession vs. trafficking, quantity-based thresholds) without asserting unverified specific threshold numbers
- explaining the general distinction between narcotics enforcement (ANF) and drug treatment/rehabilitation policy in Pakistan

## When Not to Use This Skill

- For general population health statistics/indicators (life expectancy, disease burden, health workforce) — use `who-pakistan-health-statistics`.
- For communicable-disease outbreak surveillance (dengue, polio, measles, etc.) — use `nih-disease-surveillance`; this skill covers mental health and substance-abuse policy specifically, not infectious-disease reporting.
- For NCCIA/PECA cybercrime matters even where drug trafficking has an online-facilitation dimension — use `nccia-cybercrime-peca` for the cyber-enforcement angle.
- For general criminal procedure (FIR, bail, cognizable offences) applicable to a narcotics case's procedural mechanics beyond the CNSA's own specific framework — use `pakistan-criminal-procedure-fir` for the general CrPC backdrop, since CNSA cases proceed partly through special courts under CNSA-specific procedure and partly through general criminal-procedure concepts.
- For child-specific protective statutes — use `pakistan-child-protection-laws`, even where substance abuse affects a minor.

## Routing Rules

- If the question is about general health indicators/statistics rather than the mental-health legal/institutional framework, route to `who-pakistan-health-statistics`.
- If the question is about an infectious-disease outbreak rather than mental health or substance abuse, route to `nih-disease-surveillance`.
- If the question asks which specific statute currently governs mental health in a named province, hedge explicitly on province-specific current legislation rather than assuming the 2001 federal Ordinance still applies uniformly nationwide, since mental health is now a devolved, provincial subject.
- If the question is about narcotics-case criminal procedure generally (bail, trial court hierarchy) rather than CNSA-specific scheduling/enforcement, cross-reference `pakistan-criminal-procedure-fir` for the general procedural backdrop while keeping CNSA-specific institutional detail (ANF, schedules) in this skill.
- If the question involves a minor's substance abuse or a child-specific treatment/protection angle, cross-reference `pakistan-child-protection-laws`.

## Extraction Workflow

1. Identify whether the question concerns mental health (admission/patient-rights framework) or substance abuse/narcotics (ANF/CNSA enforcement and scheduling) — these are two related but distinct legal domains within this skill's scope.
2. For a mental health question, confirm whether the question is about the historical federal 2001 Ordinance or a specific province's current legislation, and hedge explicitly if the current in-force provincial statute for that province is not confidently known.
3. For a narcotics question, distinguish ANF's enforcement/interdiction role from the treatment/rehabilitation policy layer, and from ordinary CrPC criminal procedure that runs alongside CNSA-specific special-court procedure.
4. Flag any specific quantity threshold, penalty range, or current provincial statute title/year not confidently known as "(verify)" rather than asserting invented precision.
5. When describing involuntary admission safeguards or drug-scheduling thresholds, describe the general statutory structure/intent rather than citing a specific section number unless confident.

## Technical Rules

- Mental health became a provincial legislative subject after the 18th Constitutional Amendment (2010); do not describe the 2001 Ordinance as the current uniform nationwide law without flagging that provinces may have superseded it with their own legislation.
- Involuntary psychiatric admission under Pakistani mental health legislation is intended to be subject to medical certification, time limits, and periodic review — do not describe it as an indefinite or purely administrative confinement power.
- ANF's mandate is federal narcotics-control enforcement under the CNSA 1997; do not conflate ANF with provincial police narcotics units or with NCCIA/FIA, which have separate mandates.
- CNSA 1997 offence severity and penalty exposure scale with the scheduled substance and the quantity involved; do not describe narcotics offences as a single undifferentiated offence category.
- Treatment/rehabilitation and enforcement/interdiction are policy-distinct functions even where the same agency (ANF) is involved in both; keep the distinction explicit when describing Pakistan's overall drug-policy framework.
- Do not state specific current quantity thresholds, penalty ranges, or provincial mental health statute titles/years with unwarranted precision; hedge explicitly where not confident.

## Validation Checklist

- Confirm whether the question is a mental health or a substance-abuse/narcotics question before selecting the applicable statutory framework.
- For mental health questions, confirm whether federal (2001 Ordinance, historical baseline) or a specific province's current statute is relevant, and hedge on the current provincial statute if not confidently known.
- For narcotics questions, confirm ANF's role is described as enforcement/interdiction under the CNSA 1997, distinct from treatment/rehabilitation policy.
- Flag any specific quantity threshold, penalty figure, or provincial statute title/year not confidently known as "(verify)".
- Confirm the question is not actually a general-health-statistics or infectious-disease-surveillance question misrouted to this skill.

## Common Pitfalls

- Describing the Mental Health Ordinance 2001 as the current uniform law in every province without flagging post-18th-Amendment provincial legislative activity.
- Describing involuntary psychiatric admission as unconstrained or indefinite, ignoring statutory review/discharge safeguards.
- Conflating ANF with provincial police, FIA, or NCCIA.
- Treating all narcotics offences as equivalent regardless of substance schedule or quantity involved.
- Stating specific drug-quantity thresholds or penalty ranges from memory with unwarranted precision.
- Conflating narcotics enforcement statistics/framework with general health or infectious-disease statistics better covered by `who-pakistan-health-statistics` or `nih-disease-surveillance`.

## Reference

- See [Pakistan Mental Health and Substance Abuse Reference](references/pakistan-mental-health-substance-abuse.md) for the mental health admission framework, CNSA/ANF structure, and drug-scheduling detail.
