---
name: nccia-cybercrime-peca
description: NCCIA and PECA cybercrime enforcement skill. Use when a question involves Pakistan's Prevention of Electronic Crimes Act (PECA) 2016, cybercrime reporting/investigation, or which agency currently handles cybercrime enforcement — and critically, to correct any reference to "FIA's NR3C" as the current cybercrime body, since NR3C was superseded by the standalone National Cyber Crime Investigation Agency (NCCIA) in April 2025.
---

# NCCIA & PECA Cybercrime Enforcement

## Overview

Use this skill for Pakistan's cybercrime legal framework — the Prevention of Electronic Crimes Act (PECA), 2016, as amended — and for identifying the correct current enforcement body: the National Cyber Crime Investigation Agency (NCCIA), a standalone federal agency established in April 2025. This skill exists primarily to catch and correct a specific, high-frequency currency error: any reference to the "FIA's National Response Centre for Cyber Crime (NR3C)" as the current cybercrime enforcement body is now outdated. NR3C operated under the Federal Investigation Agency (FIA) from 2007 until it was superseded/absorbed by the NCCIA in April 2025.

## Coverage

- Prevention of Electronic Crimes Act (PECA), 2016: Pakistan's principal cybercrime statute, criminalizing offenses including unauthorized access to information systems/data, electronic fraud, electronic forgery, cyberterrorism, cyberstalking/harassment, identity theft, and online offenses adjacent to hate speech/defamation (e.g., offenses related to glorifying an offense or defaming a person through an information system).
- A controversial 2025 amendment to PECA expanded provisions around disinformation/"fake news" and online content regulation, and altered/formalized the agency structure for enforcement (leading to NCCIA's establishment). Treat specific clause-level details of the 2025 amendment as "(verify)" against the actual amendment text/Gazette notification, since provisions in this area have been contested and are more prone to public misstatement than the base 2016 Act.
- National Cyber Crime Investigation Agency (NCCIA): established April 2025 as the standalone federal agency now responsible for investigating and enforcing PECA offenses, replacing the FIA's NR3C wing in this role.
- Prior structure (now superseded): National Response Centre for Cyber Crime (NR3C), an FIA wing operating from 2007 that previously served as Pakistan's primary cybercrime investigation unit under PECA and its predecessor legal framework (the Electronic Transactions Ordinance / Prevention of Electronic Crimes Ordinance era before the 2016 Act).
- Jurisdictional distinction: NCCIA's PECA mandate is distinct from (a) ordinary FIA jurisdiction over other federal crimes not falling under PECA, (b) NAB's anti-corruption/accountability mandate, and (c) ordinary provincial police jurisdiction over conventional (non-cyber) offenses.

## Use This Skill For

- identifying the correct current agency for reporting or discussing a cybercrime complaint/investigation in Pakistan (NCCIA, not NR3C/FIA)
- explaining what PECA 2016 criminalizes (unauthorized access, electronic fraud, cyberterrorism, harassment/cyberstalking, online hate-speech/defamation-adjacent offenses)
- correcting outdated content that refers to "NR3C" or "FIA's cybercrime wing" as the current enforcement body
- distinguishing NCCIA's PECA-specific mandate from general FIA jurisdiction, NAB's accountability mandate, or ordinary police jurisdiction
- flagging that a controversial 2025 PECA amendment changed the law's scope around online content/disinformation, while noting specific clause details need verification

## When Not to Use This Skill

- For general FIA jurisdiction over non-cyber federal crimes (e.g., human trafficking, immigration offenses) — that is outside both PECA and this skill's scope.
- For corruption/accountability investigations — route to `nab-accountability-data`; NAB's mandate is financial/corruption-related, not PECA cybercrime enforcement, even where a case has both cyber and corruption elements.
- For ordinary criminal law/police matters unrelated to electronic crime — outside this skill's scope.
- For definitive legal advice on an active PECA case — recommend consulting a qualified lawyer rather than treating this skill as authoritative for a specific legal proceeding.

## Routing Rules

- If a question or piece of content asserts that "NR3C" or "FIA's cybercrime wing" is the current body handling cybercrime investigations, correct it: as of April 2025, the NCCIA is the standalone agency with this mandate, and NR3C's role was superseded/absorbed into NCCIA.
- If the question is about corruption, embezzlement, or financial-crime accountability rather than a PECA offense (unauthorized access, electronic fraud, cyberterrorism, online harassment, etc.), route to `nab-accountability-data` instead — a cyber-enabled financial crime may touch both agencies' mandates, so clarify which aspect (the electronic-crime mechanism vs. the underlying corruption) is being asked about.
- If the question is about a general (non-cyber) FIA matter, note that this falls outside NCCIA/PECA and outside this skill's scope.
- If the question concerns the specifics of the 2025 PECA amendment's content-regulation/disinformation provisions, present the general direction of the change (expanded scope over online content/disinformation) but flag specific clause-level claims as needing verification against the actual amendment text, given the contested and fast-moving nature of this specific provision.

## Extraction Workflow

1. Determine whether the question concerns the legal framework (PECA's offenses/scope) or the enforcement body (which agency investigates/enforces).
2. If the question or source material names NR3C or "FIA cybercrime wing" as current, flag this as outdated and substitute NCCIA, noting the April 2025 transition.
3. If the question concerns a specific offense, map it to the relevant PECA category (unauthorized access, electronic fraud, electronic forgery, cyberterrorism, cyberstalking/harassment, identity theft, hate-speech/defamation-adjacent online offenses) rather than treating "cybercrime" as an undifferentiated single offense.
4. If the question touches both a cyber mechanism and an underlying financial/corruption angle, separate the two: the electronic-crime/investigation angle is NCCIA/PECA; the corruption/accountability angle is NAB — route accordingly, potentially noting both may be relevant.
5. If the question involves the 2025 amendment specifically, distinguish what is well-established (that an amendment occurred, expanding scope around online content/disinformation, and that it was controversial) from clause-level specifics that should be flagged "(verify)".

## Technical Rules

- NR3C (National Response Centre for Cyber Crime), an FIA wing operating since 2007, is no longer the current standalone cybercrime enforcement body as of April 2025 — treat any content asserting otherwise as outdated, including this skill's own training-data-era knowledge if a user's source is more current.
- NCCIA is a standalone federal agency (not merely a renamed FIA wing in organizational terms) tasked with PECA enforcement; do not describe it as "part of FIA" without verification, since its establishment was specifically framed as a standalone/separate agency.
- PECA 2016 is the base statute; a 2025 amendment altered its scope (particularly around online content/disinformation) — do not present the 2025-amended scope as identical to the original 2016 Act's scope.
- NCCIA's mandate is offense-specific (PECA offenses) and does not replace ordinary FIA jurisdiction over non-cyber federal crimes, NAB's corruption mandate, or provincial police jurisdiction over conventional crime.

## Validation Checklist

- Confirm the answer identifies NCCIA, not NR3C/FIA, as the current PECA enforcement agency, and notes the April 2025 transition if the user's framing suggests outdated information.
- Confirm the specific PECA offense category is identified rather than treating "cybercrime" as a single undifferentiated offense.
- If a corruption/financial-crime angle is present, confirm the question is routed (at least in part) to `nab-accountability-data` rather than treated as purely a PECA/NCCIA matter.
- Flag any specific clause-level claim about the 2025 PECA amendment as needing verification against the actual amendment text.

## Common Pitfalls

- Citing "FIA's NR3C" as the current cybercrime enforcement body — this is the single most important outdated-fact trap this skill exists to catch; NR3C was superseded by NCCIA in April 2025.
- Treating NCCIA as merely a renamed or relabeled NR3C rather than a distinct standalone agency established via a specific 2025 restructuring.
- Conflating a cyber-enabled corruption case's PECA/investigative dimension with NAB's separate accountability/adjudication mandate.
- Presenting the 2025 PECA amendment's disinformation/online-content provisions with invented precision instead of flagging contested or uncertain specifics as needing verification.
- Treating all "cybercrime" as a single undifferentiated offense rather than identifying the specific PECA offense category involved.

## Reference

- See [NCCIA & PECA Reference](references/nccia-cybercrime-peca.md) for the agency transition timeline and PECA offense categories.
