---
name: pakistan-national-curriculum-textbooks
description: Pakistan national curriculum and textbooks skill. Use when analyzing, summarizing, comparing, or extracting information from Pakistan's national curriculum documents, textbook-board materials, and subject/class mappings, especially for grade-wise learning content, textbook alignment, and board-specific curriculum scope.
---

# Pakistan National Curriculum and Textbooks

## Overview

Use this skill for Pakistan's curriculum and textbook structure from early grades through higher secondary where official curriculum frameworks, textbook-board mappings, and subject-scope documents are involved. This is the right skill when the task is about what should be taught and in which class or board context, not about exam schedules or national enrollment statistics.

## Coverage

- National Curriculum of Pakistan documents and curriculum-framework material.
- Federal and provincial textbook-board subject/class listings and approved textbook mappings.
- Subject-wise scope, sequence, competencies, and learning-outcome structure by class.
- Differences between national curriculum guidance and board-specific textbook implementation.
- Curriculum framing for core school subjects such as English, Urdu, Mathematics, Science, Islamiat, Pakistan Studies, Social Studies, Computer Science, and elective streams where applicable.

## Use This Skill For

- identifying which topics belong to a specific subject and grade
- mapping a class/subject to the relevant curriculum or textbook board document
- distinguishing national curriculum guidance from board-issued textbook implementation
- comparing subject coverage across grades
- answering curriculum-structure questions for school planning or educational content design

## When Not to Use This Skill

- For Federal Board exam papers, date sheets, or marks schemes, use `fbise-curriculum-exams` instead.
- For school enrollment, teacher counts, or institution statistics, use `pakistan-education-statistics` instead.
- For university admissions or entry tests, use `pakistan-university-admissions` instead.

## Routing Rules

- Use this skill when the task is "what is in the curriculum" or "which textbook/curriculum document applies."
- If the user asks about exam format or past papers, route to `fbise-curriculum-exams` or a board-result skill instead.
- If a provincial textbook board implements the national curriculum differently in packaging or textbook titles, preserve both the national and board-specific layers instead of assuming one replaces the other.
- Distinguish curriculum content from pedagogy advice unless the source explicitly includes pedagogical standards.

## Extraction Workflow

1. Identify the grade/class, subject, and board or jurisdiction.
2. Confirm whether the question is about curriculum scope, learning outcomes, textbook mapping, or approved titles.
3. Preserve the exact class band and subject label.
4. If the source is board-specific, keep that board attached to the answer rather than generalizing to all Pakistan schools.
5. Separate compulsory subjects from elective or stream-specific subjects.

## Technical Rules

- Curriculum frameworks and textbooks are related but not identical; do not treat a textbook title as the curriculum itself.
- Provincial textbook boards may differ in title, edition, or implementation while still claiming alignment with national curriculum.
- Grade bands matter; do not merge primary, middle, SSC, and HSSC subject structures into one flat syllabus.
- Learning outcomes, content strands, and assessment guidance are separate elements when the source distinguishes them.

## Validation Checklist

- Confirm the class/grade and subject.
- Verify whether the answer is national-curriculum level or board-specific textbook level.
- Check whether the board/jurisdiction is explicit.
- Preserve edition or revision year where the curriculum was updated.

## Common Pitfalls

- Treating one board's textbook list as universal across Pakistan.
- Confusing curriculum outcomes with exam paper format.
- Mixing grade levels when summarizing subject content.
- Referring to a textbook as if it were the legal curriculum framework.

## Reference

- See [Pakistan National Curriculum and Textbooks Reference](references/pakistan-national-curriculum-textbooks.md) for source structure and extraction notes.
