---
name: pakistan-education-statistics
description: Pakistan Education Statistics (AEPAM/NEMIS Annual School Census) skill. Use when analyzing, summarizing, comparing, or extracting information from the AEPAM/NEMIS "Pakistan Education Statistics" annual report, especially for school-level institution counts, enrollment, and teacher numbers by province and education level (primary, middle, secondary, higher secondary).
---

# Pakistan Education Statistics

## Overview

Use this skill for questions about Pakistan's Annual School Census (ASC) data as compiled by AEPAM (Academy of Educational Planning and Management) and NEMIS (National Education Management Information System) in the "Pakistan Education Statistics" annual report. This is the authoritative school-census-level document for institution counts, enrollment, and teacher numbers — the right skill whenever the task needs province-by-province, level-by-level school statistics rather than a single national education summary line.

## Coverage

- Published annually by AEPAM under the Ministry of Federal Education and Professional Training, drawing on NEMIS's Annual School Census data collected from provincial/area education departments.
- Typical structure: a national summary chapter (total institutions, enrollment, teachers), followed by detailed statistical tables broken down by education level (primary, middle, secondary, higher secondary/intermediate) and by province/area (Punjab, Sindh, KP, Balochistan, ICT, AJK, Gilgit-Baltistan, and sometimes merged former FATA districts).
- Tables typically cover: number of institutions (by level, by gender, by public/private sector, by rural/urban location), enrollment (by level, gender, sector), and number of teachers (by level, gender, sector, and sometimes qualification).
- Some editions include school facility indicators (electricity, drinking water, boundary wall, toilets) and student-teacher ratios.

## Use This Skill For

- extracting the number of schools/institutions at a given level in a given province
- pulling enrollment figures by education level, gender, or sector (public/private)
- extracting teacher counts or student-teacher ratios by level or province
- comparing school census indicators across provinces or survey years
- identifying rural/urban or public/private splits in institution, enrollment, or teacher counts

## Routing Rules

- Use this skill for school-census-level detail: institution counts, enrollment, and teachers broken down by province and education level (primary through higher secondary).
- For the general national education narrative in the annual economic survey (overall progress indicators, literacy rate, attendance, brief enrollment trend), use `pes-social-sectors` (Chapter 10: Education) instead — that chapter is a higher-level summary, this report is the underlying census.
- For university/tertiary-level statistics (enrollment by university, faculty, rankings), use `hec-higher-ed-stats` instead — this report does not cover higher education.
- If a question needs both the headline national trend and the province-level breakdown, use `pes-social-sectors` for the trend statement and this skill for the underlying province/level detail.

## Extraction Workflow

1. Identify the education level (primary, middle, secondary, higher secondary) and the geography (national, provincial, or area) the question needs.
2. Locate the matching statistical table; ASC tables are typically organized first by level, then by province, then by gender/sector splits within each.
3. Preserve whether a figure is institutions, enrollment, or teachers — these are reported in separate tables, not combined.
4. Note the survey/census year explicitly; ASC editions are dated to a specific academic year (e.g. "2023-24").
5. If the question needs a public/private or rural/urban split, confirm the table provides that breakdown rather than inferring it from the national total.

## Technical Rules

- Do not combine institution counts across levels (primary + middle + secondary) unless the source table already provides that aggregate.
- Keep gender splits (boys/girls/co-education institutions) distinct from enrollment gender splits.
- Public-sector and private-sector counts are tracked separately; do not assume a national total is public-sector only.
- Student-teacher ratio is a derived indicator; confirm whether the source computed it or whether it needs computing from enrollment and teacher counts separately.
- ICT, AJK, and Gilgit-Baltistan are sometimes reported separately from the four provinces; do not silently fold them into a "national" total without checking the table's scope.

## Validation Checklist

- Confirm the education level matches what was asked (primary vs middle vs secondary vs higher secondary).
- Verify the geography (province, area, or national) matches the table cited.
- Check the academic/census year of the data.
- Confirm whether the figure is institutions, enrollment, or teachers, and whether a gender or sector split applies.

## Common Pitfalls

- Reporting a provincial figure as a national total or vice versa.
- Mixing enrollment counts with institution counts when answering "how many schools" questions.
- Treating AEPAM/NEMIS school-census figures as interchangeable with HEC's tertiary-level statistics.
- Citing a census year inconsistently when comparing two years' tables.

## Reference

- See [Pakistan Education Statistics Reference](references/education-statistics.md) for ASC report structure and extraction notes.
