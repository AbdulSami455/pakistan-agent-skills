---
name: pakistan-constitution-governance
description: Pakistan constitution and governance-structure skill. Use when explaining the 1973 Constitution's structure, fundamental rights, the federal/provincial government system, branches of government, or Pakistan's registered political parties, as distinct from live bill-tracking or election-result reporting.
---

# Pakistan Constitution & Governance

## Overview

Use this skill for Pakistan's constitutional and governmental structure: the 1973 Constitution's organization, fundamental rights, the three branches of government, federal-provincial division of powers, and the landscape of registered political parties. This is a civics/reference skill for students and general readers — not a live legislative-tracking or election-result skill, and not a substitute for professional legal interpretation of specific constitutional provisions.

## Coverage

- The Constitution of the Islamic Republic of Pakistan, 1973 (as amended): its Parts/Chapters structure, covering the Preamble/Objectives Resolution, fundamental rights (Part II, Chapter 1), principles of policy, the federation and its structure, the provinces, relations between federation and provinces, the judicature, and amendment procedure.
- Amendment history: the Constitution has been amended numerous times since 1973 (e.g., 18th Amendment reshaping federal-provincial powers, other major amendments); always anchor a provision's current text to the most recent amendment affecting it, since earlier text can be superseded.
- Branches of government: the bicameral federal legislature (National Assembly and Senate), the executive (President as head of state, Prime Minister as head of government, federal cabinet), and the judiciary (Supreme Court, High Courts, subordinate courts, Federal Shariat Court).
- Federal-provincial structure: four provinces (Punjab, Sindh, Khyber Pakhtunkhwa, Balochistan), Islamabad Capital Territory, and the distinct constitutional arrangements for Gilgit-Baltistan and (historically) the former FATA merger into KP.
- Registered political parties: parties enlisted with the Election Commission of Pakistan (ECP), including party symbols and registration status.

## Use This Skill For

- explaining the general structure of the 1973 Constitution (which Part/Chapter covers a given topic)
- describing a specific fundamental right as set out in the Constitution
- explaining how Pakistan's federal government is structured (executive, legislature, judiciary) and how federal-provincial powers are divided
- providing general information on a registered political party (name, symbol, registration status) via ECP's list
- explaining the basic amendment procedure for the Constitution

## When Not to Use This Skill

- For the live status of a specific bill moving through Parliament — use `parliament-legislative-tracker` instead; this skill covers constitutional/structural reference, not real-time legislative process tracking.
- For election results or constituency-level outcomes — use `ecp-election-results` instead.
- For court caseload/judicial statistics — use `ljcp-judicial-statistics` instead; this skill describes the judiciary's constitutional structure, not its caseload performance.
- For a definitive legal interpretation of a specific constitutional provision in a live legal dispute — recommend consulting a qualified legal professional rather than treating this skill as authoritative legal advice.

## Routing Rules

- Use this skill for structural/civics-level questions about the Constitution and government system, not for tracking a specific bill's live status (`parliament-legislative-tracker`) or election outcomes (`ecp-election-results`).
- If a question is about a political party's electoral performance rather than its registration/symbol, route to `ecp-election-results`.
- If a question is about court caseload statistics rather than the judiciary's constitutional role/structure, route to `ljcp-judicial-statistics`.
- Always note that a constitutional provision may have been amended; do not present pre-amendment text as current without checking the latest amendment status.

## Extraction Workflow

1. Identify whether the question needs the Constitution's structural organization (which Part/Chapter/Article covers a topic), a specific fundamental right, or the general government-structure/political-party landscape.
2. If citing a specific Article, confirm whether it has been affected by a subsequent constitutional amendment (e.g., 18th Amendment and others) before presenting its current text.
3. For government-structure questions, clarify which branch/level (federal executive, federal legislature, judiciary, provincial government) the question actually concerns.
4. For political-party questions, confirm whether the question needs registration/symbol information (ECP's registered list) or electoral performance (a distinct question better answered via `ecp-election-results`).

## Technical Rules

- The Constitution has been amended many times since 1973; do not treat original 1973 text as necessarily current without checking amendment history for the relevant provision.
- Fundamental rights (Part II, Chapter 1) are distinct from the Principles of Policy (Part II, Chapter 2) — rights are generally judicially enforceable, while principles of policy are directive/aspirational; do not conflate the two categories.
- Federal and provincial legislative competence is divided via the Constitution's legislative lists framework, substantially reshaped by the 18th Amendment (which abolished the Concurrent Legislative List and devolved several subjects to provinces); do not describe pre-18th-Amendment federal-provincial division as current.
- A political party's ECP registration/enlistment status is distinct from its parliamentary representation or electoral performance; do not conflate "registered" with "currently holding seats."

## Validation Checklist

- Confirm whether a cited constitutional provision reflects the current (post-amendment) text.
- Verify which branch or level of government a structural question actually concerns.
- Check that fundamental rights are not conflated with principles of policy.
- Confirm whether a political-party question needs registration/symbol data or electoral-performance data, and route accordingly.

## Common Pitfalls

- Presenting a constitutional provision's original 1973 text as current without checking for amendments.
- Conflating fundamental rights (enforceable) with principles of policy (directive/aspirational).
- Describing federal-provincial powers using a pre-18th-Amendment framework.
- Treating a political party's ECP registration as equivalent to holding current parliamentary seats.
- Offering the skill's civics-level content as a substitute for professional legal advice on an active legal matter.

## Reference

- See [Pakistan Constitution & Governance Reference](references/pakistan-constitution-governance.md) for document structure and extraction notes.
