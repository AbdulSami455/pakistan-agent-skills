---
name: hec-higher-ed-stats
description: HEC Higher Education Data Repository skill. Use when analyzing, summarizing, comparing, or extracting information from the Higher Education Commission (HEC) Pakistan Higher Education Data Repository (HEDR) or HEC Annual Report data tables, especially for university-level enrollment, graduate output, faculty statistics, and university rankings or categories.
---

# HEC Higher Education Stats

## Overview

Use this skill for questions about Pakistan's higher-education system at the university/institution level: enrollment by university, graduate and degree-completion counts, faculty headcounts and qualifications, and university rankings or categorization. This is the right skill when the task needs more granularity than a general statement about "education" — specifically tertiary-level, institution-by-institution detail.

## Coverage

- Source: HEC's Higher Education Data Repository (HEDR) portal (`hedr.hec.gov.pk` / `hec.gov.pk` data section) and tables published in the HEC Annual Report.
- Typical data domains: enrollment by university and by discipline/field of study, enrollment by degree level (BS, MS/MPhil, PhD), graduate output counts, faculty counts by qualification (PhD/non-PhD) and by rank (professor, associate professor, assistant professor, lecturer), public vs. private sector university counts, and HEC university ranking/categorization (e.g. general, agriculture & veterinary, engineering & technology, medical, business education categories).
- HEC also publishes recognized/chartered university lists by province and sector (public/private).
- Reporting is typically annual, aligned to the academic year, though HEDR portal data can be queried for specific snapshot periods.

## Use This Skill For

- extracting enrollment figures for a specific university or discipline
- summarizing PhD output or faculty PhD-qualification ratios
- comparing public vs. private university statistics
- pulling HEC university ranking or category placement
- counting chartered/recognized universities by province or sector

## Routing Rules

- Use this skill for university-level or institution-level higher-education detail: a named university, a degree level, a faculty count, or a ranking.
- For the general national education narrative (overall enrollment trends, literacy, school infrastructure spending), use `pes-social-sectors` (Chapter 10: Education) instead — that chapter gives the high-level summary, this skill gives the university-by-university detail.
- For school-level (primary through higher-secondary) census data such as institution counts, enrollment, and teachers by province, use `pakistan-education-statistics` instead — HEC HEDR covers tertiary/university level only.
- If a question mixes school-level and university-level figures, split the answer and route each part to the correct skill.

## Extraction Workflow

1. Confirm whether the question is about a specific university, a discipline/field of study, or a system-wide tertiary aggregate.
2. Locate the relevant HEDR table or Annual Report data table (enrollment, graduates, faculty, or institution counts).
3. Preserve the degree level (BS/Bachelor, MS/MPhil, PhD) exactly; do not aggregate across levels unless the source table already does so.
4. Note whether a count refers to public-sector or private-sector institutions, or both combined.
5. If citing a ranking or category, state the ranking category name and the year/cycle of the ranking exactly as published.

## Technical Rules

- Do not merge degree-level enrollment (BS vs MS/MPhil vs PhD) into a single "enrollment" figure unless the source does so.
- Faculty counts split by qualification (PhD-holding vs non-PhD) and by rank are separate breakdowns; keep them distinct.
- Public and private university statistics often come from different reporting cycles in HEDR; do not assume the same as-of date unless confirmed.
- University rankings/categories change between cycles; always attach the ranking cycle/year to any category citation.
- Discipline/field-of-study labels in HEDR may differ from informal subject names; preserve the exact label used in the table.

## Validation Checklist

- Confirm whether the figure is for a specific university, a discipline, or a sector-wide aggregate.
- Check the degree level associated with any enrollment or graduate figure.
- Verify whether the count is public-sector, private-sector, or combined.
- Confirm the academic year or as-of date for the cited figure.

## Common Pitfalls

- Treating a single university's enrollment as representative of the whole HEC system.
- Mixing PhD faculty counts with total faculty counts without noting the distinction.
- Citing an outdated ranking cycle as current.
- Confusing HEC's tertiary-level data with AEPAM/NEMIS school-census data covered by `pakistan-education-statistics`.

## Reference

- See [Higher Education Stats Reference](references/higher-education-stats.md) for HEDR structure and extraction notes.
