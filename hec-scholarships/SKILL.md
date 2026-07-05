---
name: hec-scholarships
description: HEC scholarships and financial-aid skill. Use when looking up need-based, merit-based, or overseas scholarship programs administered by Pakistan's Higher Education Commission (HEC), including eligibility criteria, application windows, and coverage (tuition, stipend), especially for students seeking funding for undergraduate, graduate, or PhD study.
---

# HEC Scholarships

## Overview

Use this skill for scholarship and financial-aid programs administered or facilitated by Pakistan's Higher Education Commission (HEC), covering domestic need-based/merit-based schemes and overseas scholarships for graduate/PhD study abroad. This is a funding-opportunity reference skill, not a university-admission or ranking skill.

## Coverage

- Need-Based Scholarships (NBS): for financially disadvantaged students at participating public-sector universities, typically covering tuition and sometimes a stipend.
- Merit- and needs-based programs (e.g., donor-funded schemes such as USAID-supported programs) with specific eligibility and participating-institution lists.
- Overseas scholarships: HEC-administered or co-administered PhD/postgraduate scholarships for study abroad (e.g., regional country-specific PhD scholarship phases, Commonwealth Scholarships facilitated jointly with partner countries).
- Each scheme has its own eligibility criteria (domicile, discipline, income threshold, academic standing), application cycle, and coverage terms (tuition-only vs. tuition+stipend vs. full funding including travel).
- HEC's central Scholarship Portal aggregates active schemes; provincial HECs (e.g., Sindh HEC) may separately administer their own provincial scholarship programs.

## Use This Skill For

- identifying which HEC scholarship programs a student may be eligible for based on level of study (undergraduate, graduate, PhD) and destination (domestic or overseas)
- checking eligibility criteria (income threshold, domicile, academic merit, discipline restrictions) for a specific scheme
- clarifying what a specific scholarship covers (tuition, stipend, travel, books)
- distinguishing federal HEC scholarships from a provincial HEC's own scheme
- finding application windows and required documents for a specific scholarship cycle

## When Not to Use This Skill

- For general university admission merit lists or entry test cutoffs — use `pakistan-university-admissions` instead; scholarship eligibility and admission merit are separate processes.
- For university rankings or accreditation status — use `hec-university-rankings` or `hec-accreditation-councils` instead.
- For a specific foreign government's or foreign university's own scholarship (not HEC-administered/facilitated) — outside this skill's scope unless HEC is a stated partner or co-administrator.

## Routing Rules

- Use this skill for scholarship/financial-aid eligibility and coverage questions specifically tied to HEC or an HEC-facilitated program.
- If the question is really about getting admitted (merit list, entry test) rather than funding, route to `pakistan-university-admissions`.
- If a scholarship is provincial-HEC-specific (e.g., Sindh HEC), note that eligibility and application processes may differ from the federal HEC scheme of a similar name.

## Extraction Workflow

1. Identify the study level (undergraduate, graduate/Master's, PhD) and whether the destination is domestic or overseas.
2. Identify the specific scheme name (e.g., "Need-Based Scholarship," "Overseas Scholarship for PhD," a named donor-funded program) rather than assuming "HEC scholarship" refers to a single unified program — HEC administers multiple distinct schemes concurrently.
3. Confirm eligibility criteria: domicile requirement, household income threshold (for need-based schemes), academic merit requirement, and any discipline restriction.
4. Note what the scholarship actually covers — tuition only, tuition plus stipend, or full funding including travel/settling-in allowance — since this varies significantly by scheme.
5. Confirm the current application cycle/deadline rather than citing a prior cycle's dates as current, since cycles and even scheme availability change year to year.

## Technical Rules

- Do not conflate different HEC scholarship schemes under one generic "HEC scholarship" label; each has distinct eligibility, coverage, and participating institutions.
- Income-threshold criteria for need-based schemes are specific figures that can be revised between cycles; do not assume a previously cited threshold is still current.
- Distinguish scholarships requiring the recipient to study at a specific list of participating institutions from those that are portable across any HEC-recognized institution.
- Federal HEC and provincial HEC (e.g., Sindh HEC) programs are administratively separate even when similarly named; do not assume identical rules.

## Validation Checklist

- Confirm the exact scheme name and whether it is federal HEC or provincial-HEC administered.
- Verify the study level and domestic/overseas scope match the scheme.
- Check whether the cited eligibility criteria (income, domicile, merit) reflect the current cycle.
- Confirm what the scholarship covers before stating it as "fully funded" or "partial."

## Common Pitfalls

- Treating all HEC scholarship programs as a single scheme with uniform eligibility and coverage.
- Citing an outdated income threshold or application deadline as current.
- Confusing a federal HEC scheme with a similarly named provincial HEC scheme.
- Assuming a scholarship covers full funding (including stipend/travel) when it may only cover tuition.

## Reference

- See [HEC Scholarships Reference](references/hec-scholarships.md) for scheme types and extraction notes.
