---
name: fbise-curriculum-exams
description: FBISE (Federal Board of Intermediate and Secondary Education) skill. Use when looking up SSC/HSSC syllabus, scheme of studies, model question papers, past papers, date sheets, or exam structure for Pakistan's Federal Board, especially for students preparing for Matric (SSC) or Intermediate (HSSC) exams.
---

# FBISE Curriculum & Exams

## Overview

Use this skill for Pakistan's Federal Board of Intermediate and Secondary Education (FBISE) — the board covering Islamabad and federally administered institutions — for SSC (Matric, grades 9-10) and HSSC (Intermediate, grades 11-12) exam structure, syllabus, and past papers. This is a student-facing reference skill for exam preparation, not a national education-statistics skill.

## Coverage

- Scheme of Studies: subject lists and credit-hour/marks distribution per grade and stream (Science, Humanities/Arts, Commerce).
- Syllabus and Student Learning Outcomes (SLOs): subject-wise curriculum content, aligned to the National Curriculum of Pakistan where applicable.
- Model Question Papers: SLO-based sample papers illustrating question format and marks distribution for each subject.
- Past Papers / Old Question Papers: previous years' actual exam papers, useful for exam preparation.
- Date Sheets and Notifications: exam schedules, registration deadlines, and result announcements.
- Note: FBISE sets curriculum/exams for Islamabad and federal institutions; provincial boards (Lahore, Karachi, Peshawar, Quetta boards, etc.) each run separate, independently administered SSC/HSSC systems with their own syllabi and papers — do not assume FBISE's syllabus applies to a provincial board student.

## Use This Skill For

- looking up which subjects and marks distribution apply to a specific SSC or HSSC grade/stream under FBISE
- finding a specific subject's syllabus or Student Learning Outcomes for Federal Board exams
- locating model question papers or past papers for exam preparation
- checking FBISE exam date sheets or registration timelines
- clarifying the difference between FBISE and a specific provincial board's requirements

## When Not to Use This Skill

- For a provincial board's (Lahore, Karachi, Peshawar, Quetta, etc.) own syllabus or past papers — those boards are administratively separate from FBISE and publish independently; this skill does not cover their content.
- For university admission merit lists or entry tests — use `pakistan-university-admissions` instead.
- For national school enrollment/institution statistics — use `pakistan-education-statistics` instead.
- For HEC university-level accreditation or rankings — use `hec-accreditation-councils` or `hec-university-rankings` instead.

## Routing Rules

- Use this skill only for Federal Board (FBISE)-specific curriculum, syllabus, or exam-paper content; for a student under a provincial board, note explicitly that FBISE's content may not match their board's syllabus.
- If the question is about progressing from HSSC results into university admission (merit lists, entry tests), hand off to `pakistan-university-admissions`.
- If the question needs aggregate national pass-rate or enrollment statistics rather than an individual student's exam content, prefer `pakistan-education-statistics`.

## Extraction Workflow

1. Identify the exact level (SSC-I/SSC-II i.e. grade 9/10, or HSSC-I/HSSC-II i.e. grade 11/12) and stream (Science, Humanities, Commerce) the question refers to.
2. Confirm the subject and whether the question needs Scheme of Studies (marks distribution), full syllabus/SLOs, or a model/past paper.
3. Note the specific examination year for past papers or date sheets, since content and format can change between years (e.g., SLO-based reform years).
4. If the question could apply to a provincial board student, flag that FBISE content is specific to Islamabad/federal institutions and may differ from their board.

## Technical Rules

- SSC and HSSC are each split into Part-I and Part-II (grades 9/10 and 11/12 respectively); a "Matric" or "Intermediate" result combines both parts' marks — do not treat a single part's paper as the full-level result.
- Preserve exact subject and paper names (e.g., "Pakistan Studies," "Compulsory English") since similarly named subjects can have different syllabi across streams.
- Model question papers illustrate format/SLO alignment; they are not guaranteed to match the exact content of a future actual exam.
- Marks distribution (theory vs. practical, MCQs vs. subjective) is subject-specific; do not assume a uniform structure across all subjects.

## Validation Checklist

- Confirm whether the question is about FBISE specifically or could be conflated with a provincial board.
- Verify the grade level (SSC/HSSC, Part-I/Part-II) and stream match what is being asked.
- Check the examination year for any past paper or date sheet reference.
- Confirm subject name matches exactly, since names can be similar across streams.

## Common Pitfalls

- Treating FBISE's syllabus or past papers as applicable to a provincial board student without flagging the distinction.
- Confusing SSC (Matric) with HSSC (Intermediate) date sheets or syllabi.
- Citing a model question paper as if it guarantees the exact content of a future exam.
- Mixing Part-I and Part-II subject lists or marks distributions for the same level.

## Reference

- See [FBISE Reference](references/fbise-curriculum-exams.md) for document structure and extraction notes.
