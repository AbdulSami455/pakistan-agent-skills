---
name: pakistan-university-admissions
description: Pakistan university admission skill. Use when looking up or comparing admission merit lists, entry test scores, closing merits, or admission cutoffs for Pakistani universities and professional colleges (medical, engineering, business), especially for HEC-affiliated institutions, provincial public universities, and major private universities.
---

# Pakistan University Admissions

## Overview

Use this skill when the task is about university admission outcomes in Pakistan: merit lists, closing merit percentages, entry test score cutoffs, admission criteria, or seat allocation for undergraduate and postgraduate programs. This is an admission-results skill, not a ranking or enrollment-statistics skill.

## Coverage

This skill covers admission data from multiple source types:

1. **Public sector university merit lists** — published by individual universities (e.g., PU, UET Lahore, KU, DUHS, Sindh University) on their official websites and admission portals after each admission cycle.
2. **Provincial centralized admission systems** — where a provincial board or consortium manages admissions for multiple universities (e.g., Punjab's centralized engineering/medical admission, Sindh's centralized MBBS/BDS admission).
3. **Professional college admissions** — MBBS/BDS through PMDC-recognized medical colleges (using MDCAT), engineering through PEC-recognized universities (using ECAT/NET), and other professional programs.
4. **Private university admissions** — merit lists and cutoffs published by major private universities (LUMS, NUST, FAST, IoBM, etc.) on their own portals.
5. **HEC entry test requirements** — HEC's policy on mandatory entry tests (NET, MDCAT, ECAT, etc.) for university admission eligibility.

## Use This Skill For

- looking up the closing merit percentage for a specific program at a specific university in a given admission year
- comparing closing merits across universities for the same program (e.g., MBBS closing merit at different medical colleges)
- identifying the entry test required for a specific program (MDCAT for MBBS, ECAT/NET for engineering, etc.)
- extracting seat allocation numbers by category (open merit, quota, reserved seats)
- tracing how closing merits have changed year-over-year for a specific program

## Use This Skill For — Not

- For university enrollment totals or faculty statistics — use `hec-higher-ed-stats` instead.
- For university ranking positions — use `hec-university-rankings` instead.
- For whether a program is accredited by a professional council — use `hec-accreditation-councils` instead.
- For school-level education statistics — use `pakistan-education-statistics` instead.
- For HEC's own university categorization — use `hec-higher-ed-stats` instead.

## Routing Rules

- Use this skill when the question is about admission cutoffs, merit lists, entry test scores, or seat allocation.
- If the question is about total enrollment at a university — route to `hec-higher-ed-stats`.
- If the question is about a university's rank — route to `hec-university-rankings`.
- If the question is about whether a program is accredited — route to `hec-accreditation-councils`.
- If the question mixes admission data with ranking — split: use this skill for admission, `hec-university-rankings` for ranking.

## Extraction Workflow

1. Identify the specific university, program, and admission year/cycle the question asks about.
2. Identify whether the program is undergraduate or postgraduate — closing merits and entry test requirements differ by level.
3. Identify the admission category if relevant: open merit, quota (provincial, federal, overseas, disabled, sports, etc.) — closing merits differ by category.
4. For medical programs: confirm the entry test is MDCAT (a single national test; "NMDCAT" is the same test under a since-reverted regulator-era name, not a separate exam) and note the test year and which regulator (PMDC or, for the 2019-2023 period, PMC) was administering it that year.
5. For engineering programs: confirm whether the entry test is ECAT (Punjab), NET (NUST), or another university-specific test.
6. Extract the closing merit figure exactly as published — note whether it is a percentage, an aggregate score, or a test score threshold.
7. Note the program duration if relevant (e.g., 5-year MBBS vs 4-year BS) — this affects merit comparisons.

## Technical Rules

- Always state the admission year/cycle alongside any closing merit figure — merits change annually.
- Distinguish "closing merit" (the last admitted student's score) from "minimum eligibility" (the threshold to apply) — these are different figures.
- Entry test names must be preserved exactly: MDCAT, ECAT, NET, HAT-HEC, etc. — do not abbreviate inconsistently, and do not treat "NMDCAT" as a test distinct from MDCAT (it is the same exam under a former regulator-era name).
- Seat counts by category (open merit, quota, reserved) should be reported separately, not summed into a single total unless the source does so.
- Provincial quota systems differ — a Punjab-domiciled student's closing merit may differ from a Sindh-domiciled student's for the same program at a federal university.
- Private university admission criteria may include their own entry tests or accept HEC's HAT — confirm which test applies.

## Validation Checklist

- Confirm the university name and program match the source being cited.
- Confirm the admission year/cycle — do not cite a 2023 closing merit for a 2025 question.
- Verify whether the figure is a closing merit, minimum eligibility, or entry test cutoff.
- Check the admission category (open merit vs quota) if the question specifies one.
- Confirm the entry test name and year for professional programs.

## Common Pitfalls

- Citing a closing merit from one admission year as if it applies to the next year.
- Confusing minimum eligibility criteria with the actual closing merit (the closing merit is almost always higher).
- Mixing up entry test names — MDCAT (medical) vs ECAT (engineering) vs NET (NUST) vs HAT (HEC general).
- Reporting a quota-category closing merit as if it were the open-merit figure.
- Treating a private university's admission criteria as equivalent to a public university's.

## Reference

- See [University Admissions Reference](references/university-admissions.md) for admission system structure and entry test definitions.
