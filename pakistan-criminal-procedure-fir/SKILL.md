---
name: pakistan-criminal-procedure-fir
description: Pakistan general criminal procedure skill. Use when a task concerns First Information Report (FIR) registration under the Code of Criminal Procedure 1898, the cognizable vs. non-cognizable offence distinction, pre-arrest/post-arrest bail framework, police investigation stages leading to a challan/charge-sheet, or the organizational structure of the Pakistan Penal Code 1860 — as distinct from NAB's corruption-specific pipeline or PECA cybercrime enforcement.
---

# Pakistan Criminal Procedure and FIR

## Overview

Use this skill when a task requires explaining how Pakistan's general criminal-justice process works at the police/trial-court level — how an FIR is registered, what cognizable and non-cognizable offences mean procedurally, how bail (pre-arrest and post-arrest) operates, and how a police investigation proceeds toward a challan (charge-sheet) and trial. This is the general CrPC 1898 procedural layer, applicable to ordinary criminal offences under the Pakistan Penal Code 1860 and other criminal statutes tried in ordinary Magistrate/Sessions courts — not the specialized institutional pipelines of NAB (corruption) or NCCIA (cybercrime under PECA), which layer their own procedures on top of or instead of parts of this general framework.

## Coverage

- **Code of Criminal Procedure, 1898 (CrPC)**: the principal procedural statute governing FIR registration, arrest, investigation, bail, and trial procedure in criminal cases in Pakistan (amended repeatedly; some provinces have made procedural amendments post-18th Amendment). Governs Magistrate and Sessions Court criminal procedure generally.
- **FIR (First Information Report)**: the written record of information about the commission of a cognizable offence, recorded by an officer in charge of a police station under CrPC Section 154, which sets the criminal investigative process in motion. An FIR is not itself a finding of guilt; it is the formal starting document.
- **Cognizable vs. non-cognizable offences**: a cognizable offence is one for which police may arrest without a warrant and investigate without prior magistrate authorization; a non-cognizable offence requires a magistrate's permission for police to investigate and does not carry a general power of warrantless arrest — this classification (set out in the First Schedule to the CrPC alongside PPC offences) governs how a complaint proceeds procedurally.
- **Bail framework**: pre-arrest (anticipatory) bail, sought before arrest to prevent apprehended arrest in a case, and post-arrest bail, sought after arrest/custody, are governed by distinct CrPC provisions (commonly discussed as Section 497 for post-arrest bail in non-bailable offences and Section 498 for bail generally/pre-arrest bail) with different tests — bailable vs. non-bailable offence classification (also set out in the First Schedule) determines whether bail is a matter of right or judicial discretion.
- **Investigation stages**: FIR registration → initial site/scene investigation → recording of statements (including under Section 161 CrPC, not given on oath, and Section 164 CrPC, recorded before a magistrate) → collection of evidence/forensics → arrest (if warranted) → completion of investigation → submission of the police report (challan/charge-sheet) under Section 173 CrPC to the trial court, recommending prosecution or, in some cases, cancellation of the FIR ("cancellation report"/"C-report") where no offence is made out.
- **Pakistan Penal Code, 1860 (PPC)**: the substantive criminal code defining offences and punishments, organized into chapters by subject matter (e.g., offences against the state, offences relating to the armed forces, offences against public tranquility, offences affecting the human body — including Qisas and Diyat provisions introduced via the Criminal Law (Amendment) Ordinance 1990 for offences like murder/hurt, offences against property, offences relating to marriage, defamation, criminal intimidation). This skill covers the PPC's organizational structure and how it interacts with CrPC procedure — not a section-by-section restatement of penal provisions.
- **Trial-court hierarchy for criminal matters**: Magistrates (various classes, with differing sentencing powers) and Sessions Courts try criminal cases depending on offence severity, with the High Court exercising appellate and revisional jurisdiction.

## Use This Skill For

- explaining how an FIR is registered, what information it must contain, and what happens if police refuse to register one (including the remedy of approaching a magistrate/High Court)
- explaining the cognizable vs. non-cognizable distinction and its procedural consequences for arrest and investigation
- explaining the pre-arrest vs. post-arrest bail distinction and the general tests courts apply
- explaining the stages of a police investigation from FIR to challan/charge-sheet
- explaining the organizational structure of the Pakistan Penal Code 1860 (chapters/categories of offences) without restating specific penal provisions as settled without hedging
- explaining the general Magistrate/Sessions Court hierarchy for criminal trials

## When Not to Use This Skill

- For NAB's corruption-specific inquiry/investigation/reference pipeline under the National Accountability Ordinance 1999 — use `nab-accountability-data`; NAB has its own distinct procedural pipeline that does not follow ordinary CrPC FIR/challan steps in the same way.
- For PECA cybercrime enforcement and NCCIA's investigative role — use `nccia-cybercrime-peca`; cybercrime offences under PECA 2016 follow specialized procedure and a dedicated agency, not an ordinary police-station FIR process in the same form.
- For court pendency/disposal/caseload statistics — use `ljcp-judicial-statistics`.
- For family-law matters (even where a criminal complaint like domestic violence intersects with a family dispute) — use `pakistan-family-law-courts` for the civil/family-court side.
- For child-specific protective statutes (juvenile justice procedure specifically, child marriage, missing-children alerts) — use `pakistan-child-protection-laws`; general CrPC bail/FIR framework applies as a backdrop, but juvenile-specific procedural modifications belong to that skill.

## Routing Rules

- If the question is specifically about NAB's own case pipeline (inquiry, investigation, reference, Accountability Court), route to `nab-accountability-data` rather than describing it as an ordinary FIR/challan process.
- If the offence is a PECA cybercrime matter or concerns NCCIA's jurisdiction, route to `nccia-cybercrime-peca`.
- If the question is about a juvenile accused, note that the Juvenile Justice System Act 2018 modifies ordinary CrPC procedure (e.g., separate juvenile courts, restrictions on detention) — cross-reference `pakistan-child-protection-laws` for the juvenile-specific procedural layer rather than presenting adult CrPC procedure as directly applicable without modification.
- If the question needs caseload/pendency statistics rather than an explanation of the procedural framework, route to `ljcp-judicial-statistics`.
- If the question is about a family-law civil suit rather than a criminal complaint, route to `pakistan-family-law-courts`.

## Extraction Workflow

1. Identify what stage of the criminal process the question concerns: FIR registration, cognizable/non-cognizable classification, bail, investigation, or challan/trial referral — these are distinct stages with distinct legal tests.
2. Confirm whether the offence in question is classified as cognizable or non-cognizable (and, separately, bailable or non-bailable) before describing arrest or bail procedure, since these classifications (not the offence's perceived seriousness alone) drive the procedural pathway.
3. For a bail question, confirm whether pre-arrest or post-arrest bail is at issue, since these are sought at different stages, before different fora in some formulations, and assessed under different tests.
4. For an investigation-stage question, walk through the actual CrPC sequence (FIR → investigation → statements under Sections 161/164 → arrest if warranted → Section 173 police report/challan) rather than compressing it into an undifferentiated "police investigate and then there's a trial."
5. When referencing PPC structure, describe it by chapter/category (offences against the state, the body, property, etc.) rather than citing specific section numbers and punishments from memory unless confident; hedge specific section numbers and punishment ranges as "(verify current PPC text)" given the PPC has been amended (including by special/amendment laws) multiple times.
6. Flag if the matter actually falls under a specialized pipeline (NAB, PECA/NCCIA, juvenile justice) rather than ordinary CrPC procedure, and route accordingly instead of answering as if general CrPC procedure applies unmodified.

## Technical Rules

- An FIR (Section 154 CrPC) can only be formally "registered" by an officer in charge of a police station for a cognizable offence; for a non-cognizable offence, the complainant's recourse is generally a complaint to a magistrate rather than direct police FIR registration, and police need magistrate permission to investigate.
- Registration of an FIR is not evidence of guilt and is not itself a judicial finding; it is the triggering document for investigation.
- Bail in a bailable offence is ordinarily a matter of right; bail in a non-bailable offence is a matter of judicial discretion assessed against the specific facts and the applicable CrPC provision — do not describe bail as automatic for a non-bailable offence.
- Pre-arrest (anticipatory) bail and post-arrest bail are procedurally and doctrinally distinct; do not use the terms interchangeably.
- The police investigation culminates in a report under Section 173 CrPC (commonly called a "challan" in Pakistani practice), which is submitted to the trial court and can recommend either prosecution (charge-sheet) or that no case is made out (cancellation/C-report) — do not assume every FIR automatically results in a challan recommending prosecution.
- The Pakistan Penal Code 1860 is the substantive offence-defining code; the CrPC 1898 is the procedural code — do not conflate the two when a question asks about "the criminal law" generally.
- Specific PPC section numbers, punishment ranges, and CrPC provision numbers should be flagged "(verify current text)" unless you are confident of them, since amendments (including through special ordinances) have altered numbering and content over time.

## Validation Checklist

- Confirm which procedural stage (FIR, cognizability classification, bail, investigation, challan/trial) the question actually concerns.
- Confirm cognizable/non-cognizable and bailable/non-bailable classifications are addressed as distinct, offence-specific classifications rather than assumed from offence severity alone.
- Confirm pre-arrest vs. post-arrest bail is correctly distinguished if a bail question is involved.
- Confirm the matter is not actually a NAB, PECA/NCCIA, or juvenile-justice matter requiring a different specialized skill.
- Flag specific PPC/CrPC section numbers or punishment ranges not confidently known as "(verify)".

## Common Pitfalls

- Describing FIR registration as itself a determination of guilt or wrongdoing.
- Treating non-cognizable offences as if police can freely arrest and investigate without magistrate involvement.
- Conflating pre-arrest and post-arrest bail, or treating post-arrest bail in a non-bailable offence as automatic.
- Assuming every FIR leads to a challan recommending prosecution, ignoring the possibility of a cancellation/C-report.
- Applying ordinary adult CrPC procedure to a juvenile accused without flagging the Juvenile Justice System Act 2018's procedural modifications.
- Describing a NAB or PECA/NCCIA matter using ordinary FIR/challan terminology instead of routing to the specialized skill for that pipeline.
- Citing specific PPC section numbers or sentencing ranges from memory with unwarranted precision.

## Reference

- See [Pakistan Criminal Procedure Reference](references/pakistan-criminal-procedure-fir.md) for the FIR/investigation sequence, bail framework detail, and PPC chapter structure.
