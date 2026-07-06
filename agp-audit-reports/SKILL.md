---
name: agp-audit-reports
description: Auditor General of Pakistan (AGP) audit reports skill. Use when a question involves AGP's constitutional audit function (Articles 168-171), audit reports on federal or provincial government accounts, "audit paras"/irregularity findings, or Public Accounts Committee (PAC) review of those paras — and critically, to correct any conflation of an AGP irregularity figure with a proven corruption or theft figure.
---

# AGP Audit Reports

## Overview

Use this skill for the Auditor General of Pakistan (AGP) — Pakistan's Supreme Audit Institution under Articles 168-171 of the Constitution — and its audit reports on federal and provincial government accounts. This skill's most important job is disambiguation: an AGP "audit para" is a flagged financial or procedural irregularity, not a proven finding of corruption, theft, or embezzlement. Media and secondary reporting very commonly conflate "AGP found irregularities of Rs. X billion" with "Rs. X billion was stolen," and this skill exists specifically to catch and correct that framing before it propagates.

## Coverage

- Constitutional basis: Articles 168-171 of the Constitution of Pakistan, 1973, establish the office of the Auditor-General of Pakistan, prescribe the manner of audit and the form of accounts, and require audit reports relating to the accounts of the Federation to be submitted to the President for laying before the National Assembly and Senate, and reports relating to a Province to be submitted to the Governor for laying before the Provincial Assembly.
- AGP's mandate: financial audit (verifying accounts are accurate and complete) and compliance audit (verifying expenditure complied with applicable rules, sanctions, and authorizations) of federal government accounts, and — through the constitutionally provided arrangement — of provincial government accounts as well, carried out operationally through Field Audit Offices (e.g., Director General Audit offices covering specific provinces/sectors such as Federal Government Audit, Provincial Audit for each province, Defence Services Audit, Revenue Audit, Works Audit, and similar specialized wings; verify exact current wing names/structure against AGP's own published organogram).
- Audit cycle: field audit conducted against departmental accounts and records -> draft observations issued to the audited entity for response (Departmental Accounts Committee / management response stage) -> audit report finalized -> report submitted to the President (for federal accounts) or Governor (for provincial accounts) -> report laid before the National Assembly/Senate or the relevant Provincial Assembly -> the Public Accounts Committee (PAC) of the relevant assembly examines the report's individual "audit paras."
- Audit para: a specific flagged item in an audit report — e.g., an unreconciled expenditure, a procurement rule violation, a missing document/record, an overpayment, an unauthorized expenditure, or a recovery pointed out as due to government. An audit para spans a wide severity range, from a documentation/technical compliance gap to a more serious irregularity that may (but does not automatically) warrant further investigation.
- PAC review and disposition: PAC summons the relevant Principal Accounting Officer (typically the federal/provincial secretary of the concerned ministry/department) to examine each para, can direct recovery, can direct disciplinary/departmental action, and can "settle" a para (treat it as resolved/closed) once satisfied with the explanation or corrective action, or keep it pending, or in some cases recommend referral to another body (e.g., NAB or FIA) if the facts suggest a criminal offense beyond a mere procedural/financial irregularity.
- AGP's independence: the Auditor-General's appointment, terms of service, and removal are constitutionally insulated from ordinary executive control (broadly analogous in spirit, though not in specific mechanism, to the security of tenure protecting superior court judges), intended to preserve the impartiality of the audit function from the executive branch whose accounts it audits. (Verify the exact current tenure length, removal procedure, and appointment mechanism against the current constitutional text and any amendments, since these details are precise and easy to misstate.)

## Use This Skill For

- explaining what an AGP audit report is, how it is produced, and the cycle from field audit to PAC review
- explaining what an "audit para" is and is not — specifically, that it is an irregularity finding, not a criminal or corruption finding
- distinguishing an audit para that is still pending PAC review from one that PAC has "settled"/cleared
- explaining AGP's constitutional basis (Articles 168-171) and its audit of both federal and provincial accounts via Field Audit Offices
- explaining AGP's constitutionally protected independence and why that independence matters for audit credibility
- correcting a claim that restates an AGP irregularity/loss figure as a proven theft, embezzlement, or corruption figure

## When Not to Use This Skill

- For actual criminal-accountability proceedings — corruption investigation, NAB references, Accountability Court trials, plea bargains, or NAB recovery-figure announcements — use `nab-accountability-data` instead; AGP does not investigate or adjudicate criminal guilt.
- For general court caseload/pendency statistics — use `ljcp-judicial-statistics`; PAC is a parliamentary committee, not a court, and this skill does not cover judicial caseload data.
- For the live legislative status of a bill (e.g., an amendment to the Auditor-General's (Functions, Powers and Terms and Conditions of Service) Ordinance) — use `parliament-legislative-tracker` for the bill's status; use this skill for AGP's function once any such change is in force.
- For the constitutional/structural description of Parliament or provincial assemblies generally, beyond their role in receiving and reviewing audit reports — use `pakistan-constitution-governance`.
- For federal or provincial budget documents themselves (allocations, expenditures as planned) rather than the audit of actual spending against those allocations — use `federal-budget-documents` or `provincial-budget-documents`.

## Routing Rules

- If a question or source states an AGP-reported irregularity/loss/misappropriation figure and frames it as money that "was stolen" or "corruption of Rs. X," correct the framing: this is an audit finding of irregularity, pending PAC review, not a judicial or investigative finding of corruption or theft. Note that only a subset of audit paras, if any, are ever referred onward for criminal investigation.
- If the question is actually about a criminal-accountability process — an inquiry, investigation, reference, Accountability Court trial, plea bargain, or recovery announcement — route to `nab-accountability-data`, since that is a separate institution (NAB) and a separate legal process from AGP's audit function.
- If the question is about PAC's committee proceedings themselves (summoning officials, recommending action) rather than the underlying audit content, keep the answer within this skill but clarify that PAC is a parliamentary oversight body, not a prosecutorial or judicial one.
- If the question concerns budget allocations/planned expenditure rather than the audit of actual spending, route to `federal-budget-documents` or `provincial-budget-documents` as applicable.
- If the question concerns a bill amending AGP's governing law that is still moving through Parliament, route to `parliament-legislative-tracker` for the bill's live status.

## Extraction Workflow

1. Identify whether the question concerns AGP's audit function/report content, or a subsequent criminal-accountability question — if the latter, route to `nab-accountability-data` rather than answering from AGP audit content alone.
2. If an audit para or irregularity figure is cited, identify which stage of the cycle it is at: freshly reported in the audit report, pending PAC review, or already reviewed and settled/kept-pending/referred-onward by PAC. Do not describe a freshly reported para as if it were a PAC-settled conclusion, or vice versa.
3. Determine whether the accounts in question are federal or provincial, since the audit is the same AGP function operationally executed through Field Audit Offices, but the report is laid before a different legislative body (National Assembly/Senate for federal accounts; the relevant Provincial Assembly for provincial accounts).
4. If the source language uses terms like "misappropriation," "loss to the exchequer," "irregularity," or "recoverable," preserve that exact audit terminology rather than substituting a stronger word like "theft," "embezzlement," or "fraud" unless a subsequent criminal proceeding has actually established that finding.
5. If the question asks about AGP's independence, address the constitutional tenure/removal protections rather than describing AGP as an ordinary executive department, but flag specific tenure-length or removal-mechanism details as "(verify)" if not fully certain.

## Technical Rules

- An "audit para" is AGP's/the audit report's flagged observation of a financial or compliance irregularity. It is not a criminal charge, not a conviction, and not, by itself, proof that funds were stolen or embezzled — do not use those stronger terms unless a separate criminal investigation/adjudication (a NAB reference and Accountability Court proceeding, an FIA case, or an ordinary court judgment) has actually reached that conclusion.
- AGP audits accounts and compliance; it does not investigate intent or prosecute individuals. Any recommendation that a matter be referred for criminal investigation is a distinct, subsequent step, typically arising from PAC review or a separate referral, not from the audit report itself rendering a guilt finding.
- PAC can "settle" an audit para (treat it as resolved, e.g., after a satisfactory explanation, corrective action, or recovery of an overpayment), keep it pending for further departmental action or information, or in some cases refer facts suggesting a criminal offense onward to an investigative agency — these are three distinct outcomes and should not be conflated. A para that has not yet been reviewed by PAC is neither settled nor dismissed; it is simply pending.
- AGP's audit reports cover federal government accounts and, via the constitutional arrangement, provincial government accounts as well (operationally through Field Audit Offices); do not describe AGP as auditing federal accounts only.
- AGP's appointment and service conditions are constitutionally protected to preserve independence from the executive branch being audited; do not describe the Auditor-General as removable at the executive's discretion in the manner of an ordinary civil servant.
- A large aggregate irregularity figure reported in an audit report typically represents the sum of many individual paras across many entities and years, not necessarily a single incident — do not present an aggregate figure as if it reflects one discrete loss event unless the source specifically describes it that way.

## Validation Checklist

- Confirm the claim is being described as an audit/irregularity finding, not restated as a proven corruption, theft, or embezzlement figure, unless a separate criminal proceeding has actually made that finding.
- Confirm which stage of the audit-to-PAC cycle the cited para is at (freshly reported, pending PAC review, settled, referred onward).
- Confirm whether the accounts in question are federal or provincial, and which legislative body the report was laid before.
- If independence/tenure claims are made about the Auditor-General, flag specific tenure-length or removal-mechanism details as "(verify)" unless fully confident.
- If the underlying question is actually about a criminal-accountability process, confirm it has been routed to `nab-accountability-data` rather than answered solely from AGP audit content.

## Common Pitfalls

- Restating "AGP found irregularities of Rs. X billion" as "Rs. X billion was stolen/embezzled" — this is the single most important framing error this skill exists to correct; an audit para is an irregularity finding, not a criminal or judicial determination.
- Treating every audit para as equally serious, when in fact paras range from minor documentation/compliance gaps to more serious flagged irregularities.
- Describing a freshly issued audit para as already "settled" by PAC, or conversely treating a PAC-settled para as if it remains an open, unresolved allegation.
- Describing AGP as investigating or prosecuting wrongdoing, rather than auditing accounts and compliance and reporting findings for parliamentary/PAC review.
- Treating AGP as auditing only federal accounts and omitting its role in provincial government audit via Field Audit Offices.
- Presenting a specific tenure length, removal procedure, or appointment mechanism for the Auditor-General with unverified precision instead of flagging it for verification.
- Conflating this skill's audit-irregularity content with `nab-accountability-data`'s criminal-accountability content — the two describe fundamentally different institutions and different kinds of findings.

## Reference

- See [AGP Audit Reports Reference](references/agp-audit-reports.md) for the audit cycle structure, audit-para terminology, and the AGP/PAC/NAB disambiguation notes.
