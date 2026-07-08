---
name: pakistan-learning-assessments
description: Pakistan learning assessments skill. Use when analyzing, summarizing, comparing, or extracting information from Pakistan's learning-assessment reports, especially for literacy, numeracy, grade-level competencies, school-type gaps, and province-wise learning outcomes.
---

# Pakistan Learning Assessments

## Overview

Use this skill for reports measuring what students in Pakistan can actually read, understand, or solve, rather than how many are enrolled in school. This is the right skill for ASER-style learning outcomes, provincial assessment studies, and official competency reporting across literacy, numeracy, and grade-level achievement.

## Coverage

- ASER Pakistan assessment reports and district/province-level learning snapshots.
- Provincial assessment systems and official student-achievement reports where they publish comparable competency results.
- PIE/AEPAM or ministry-supported assessment studies where learning outcomes are measured directly.
- Literacy, numeracy, and foundational-learning indicators by grade, gender, school type, rural/urban split, and province where available.
- Benchmark-style indicators such as reading at a lower-grade level, arithmetic competency, or subject achievement bands.

## Use This Skill For

- extracting literacy or numeracy outcome percentages by grade or province
- comparing public vs private school performance in assessment reports
- summarizing changes in learning outcomes across survey rounds
- distinguishing enrollment access from actual learning achievement
- identifying how an assessment defines a competency benchmark

## When Not to Use This Skill

- For school counts, enrollment, or teacher totals, use `pakistan-education-statistics` instead.
- For curriculum scope or textbook mapping, use `pakistan-national-curriculum-textbooks` instead.
- For university rankings or tertiary statistics, use `hec-higher-ed-stats` instead.

## Routing Rules

- Use this skill when the task is about learning quality or competency outcomes rather than participation in schooling.
- If the question needs both access and achievement, split the answer between this skill and `pakistan-education-statistics`.
- Keep sample-based assessments distinct from census-based education statistics.
- If an assessment is not nationally representative, preserve its geography and methodology limits instead of generalizing.

## Extraction Workflow

1. Identify the assessment source, grade level, subject domain, and geography.
2. Confirm whether the result is a percentage meeting a benchmark, an average score, or a categorical achievement band.
3. Preserve the exact competency definition used by the report.
4. Note whether the comparison is by gender, school type, rural/urban status, or province.
5. If comparing years, confirm the indicator and survey design are comparable.

## Technical Rules

- Assessment reports are often sample-based; do not treat them as full-population counts.
- "Can read a sentence/story" and "is enrolled in grade X" are different constructs and must not be merged.
- Benchmarks may be grade-below-grade expectations rather than full grade-level mastery; preserve the exact framing.
- Public/private comparisons can reflect sample composition differences; do not convert them into causal claims unless the report does so.

## Validation Checklist

- Confirm the assessment source and year.
- Verify the grade, subject domain, and competency definition.
- Check whether the figure is a percent, score, or category.
- Preserve whether the result is national, provincial, district, or subgroup-specific.

## Common Pitfalls

- Treating learning-assessment figures as if they were school-census totals.
- Ignoring the benchmark definition behind a literacy/numeracy percentage.
- Comparing non-equivalent rounds as if they used the same methodology.
- Turning descriptive public/private gaps into causal claims without support.

## Reference

- See [Pakistan Learning Assessments Reference](references/pakistan-learning-assessments.md) for source structure and extraction notes.
