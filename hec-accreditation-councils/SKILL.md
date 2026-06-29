---
name: hec-accreditation-councils
description: HEC professional accreditation council skill. Use when checking whether a Pakistani university program is accredited by a professional council — PEC (engineering), PMC/PMDC (medical/dental), NCEAC (computing), NBEAC (business), PBC (pharmacy), PEC (architecture), NCTE (teacher education), or PVMC (veterinary) — especially for program-level accreditation status, accreditation validity periods, and council-recognized institution lists.
---

# HEC Accreditation Councils

## Overview

Use this skill when the task is about whether a specific university program in Pakistan is accredited by its corresponding professional council, or when looking up the list of council-accredited institutions. This is an accreditation-status skill, not a ranking, enrollment, or admission skill.

## Coverage

Pakistan's professional accreditation councils operate under HEC oversight. This skill covers:

1. **PEC** — Pakistan Engineering Council — accredits engineering programs (BE, BS Engineering)
2. **PMC** — Pakistan Medical Commission (successor to PMDC) — accredits medical and dental colleges/programs (MBBS, BDS)
3. **NCEAC** — National Computing Education Accreditation Council — accredits computing/IT programs (BS CS, BS SE, BS IT)
4. **NBEAC** — National Business Education Accreditation Council — accredits business programs (BBA, MBA, MS Business)
5. **PBC** — Pharmacy Council of Pakistan — accredits pharmacy programs (Pharm-D)
6. **PCATP** — Pakistan Council of Architects and Town Planners — accredits architecture and town planning programs
7. **NCTE** — National Council for Teacher Education — accredits teacher education programs (B.Ed, M.Ed)
8. **PVMC** — Pakistan Veterinary Medical Council — accredits veterinary programs (DVM)

## Use This Skill For

- checking whether a specific university's program is accredited by its professional council
- looking up the list of accredited institutions for a specific council
- identifying the accreditation status (accredited, provisional, denied, expired) of a program
- determining which council accredits a given program type
- checking the validity period of a program's accreditation

## Use This Skill For — Not

- For university enrollment or faculty statistics — use `hec-higher-ed-stats` instead.
- For university ranking positions — use `hec-university-rankings` instead.
- For admission merit lists or entry test cutoffs — use `pakistan-university-admissions` instead.
- For HEC's own university categorization — use `hec-higher-ed-stats` instead.
- For school-level education statistics — use `pakistan-education-statistics` instead.

## Routing Rules

- Use this skill when the question is about program accreditation status or council-recognized institution lists.
- If the question is about a university's overall enrollment or faculty — route to `hec-higher-ed-stats`.
- If the question is about a university's rank — route to `hec-university-rankings`.
- If the question is about admission to an accredited program — use `pakistan-university-admissions` for the admission data, and this skill only for the accreditation status.
- If the question mixes accreditation with ranking — split: use this skill for accreditation, `hec-university-rankings` for ranking.

## Extraction Workflow

1. Identify the program type (engineering, medical, computing, business, pharmacy, etc.) to determine which council applies.
2. Identify the specific university and campus — accreditation is program- and campus-specific, not university-wide.
3. Check the relevant council's official website or HEC's accreditation portal for the current accredited-institution list.
4. Note the accreditation status: fully accredited, provisionally accredited, accredited with conditions, or not listed.
5. If the accreditation has a validity period, note the expiry date — accreditation is not permanent.
6. For PMC/PMDC: confirm whether the medical/dental college is recognized for teaching (not just registered) — these are different statuses.

## Technical Rules

- Accreditation is program-specific, not university-wide — a university may have its engineering program accredited but its business program not accredited.
- Council names must be preserved exactly: PEC, PMC, NCEAC, NBEAC, PBC, PCATP, NCTE, PVMC.
- PMC replaced PMDC in 2020 — older records may reference PMDC; current records use PMC.
- Accreditation status can change — always check the latest list on the council's website, not a cached copy.
- Provisional accreditation is not the same as full accreditation — preserve the distinction.
- Some councils publish accreditation with a validity period (e.g., "accredited until 2026") — note the expiry.

## Validation Checklist

- Confirm the correct council for the program type.
- Confirm the specific university and campus match the accreditation list entry.
- Verify the accreditation status (full, provisional, conditional, expired, not listed).
- Check the accreditation validity period if stated.
- Confirm the information is from the latest published list, not an outdated source.

## Common Pitfalls

- Confusing PMDC (old name) with PMC (current name) — use PMC for current queries.
- Treating a university as "accredited" when only one of its programs is accredited.
- Confusing HEC recognition (institutional) with professional council accreditation (program-level) — these are separate.
- Citing an expired accreditation as current.
- Mixing up councils — e.g., asking NBEAC about an engineering program (that is PEC's domain).

## Reference

- See [Accreditation Councils Reference](references/accreditation-councils.md) for council definitions, websites, and program-council mapping.
