---
name: pakistan-board-exam-results
description: Pakistan board exam results skill. Use when analyzing, summarizing, comparing, or extracting information from Pakistani board exam result gazettes, pass-rate summaries, and board notifications, especially for SSC/HSSC results, pass percentages, position holders, and board-wise performance comparisons.
---

# Pakistan Board Exam Results

## Overview

Use this skill for board-issued SSC and HSSC result publications in Pakistan: result gazettes, pass percentages, top-position summaries, subject-group performance, and board-specific result notifications. This is the right skill when the task is about outcomes of school-board examinations rather than curriculum scope, exam format, or university admission.

## Coverage

- Federal and provincial board result gazettes and official result notifications.
- SSC and HSSC annual and supplementary result summaries where boards publish pass percentages or candidate counts.
- Board-wise performance tables, top-position announcements, and stream/group-specific result breakdowns where available.
- Differences across boards such as FBISE, Lahore, Gujranwala, Rawalpindi, Karachi, Hyderabad, Peshawar, Abbottabad, Quetta, and others, depending on the source set used.
- Examination-cycle context such as annual exam, second annual/supplementary exam, or revised result notices.

## Use This Skill For

- extracting pass percentages or candidate counts for a specific board and year
- summarizing result performance by SSC/HSSC level and part
- distinguishing annual from supplementary or second annual result cycles
- identifying board toppers or position holders from official notices
- comparing broad board-level outcome summaries when the underlying board sources are official and comparable

## When Not to Use This Skill

- For Federal Board syllabus, model papers, or date sheets, use `fbise-curriculum-exams` instead.
- For university merit lists or entry-test cutoffs, use `pakistan-university-admissions` instead.
- For curriculum mapping, use `pakistan-national-curriculum-textbooks` instead.

## Routing Rules

- Use this skill only for officially published results, gazettes, and result notices from examination boards.
- Keep board-specific result frameworks separate; one board's annual/supplementary terminology may differ from another's.
- If the question asks why performance is high or low, keep the answer descriptive unless an official board or assessment source provides analysis.
- Distinguish result publication from exam schedule or paper format.

## Extraction Workflow

1. Identify the board, level (SSC/HSSC), part, and exam cycle.
2. Confirm whether the source is a gazette, press release, result summary, or revised notification.
3. Preserve whether the metric is pass percentage, total appeared, total passed, top positions, or subject-group breakdown.
4. Note the result year and cycle exactly.
5. If comparing boards, confirm the measures and cycles are truly comparable.

## Technical Rules

- SSC/HSSC Part-I and Part-II results should not be merged unless the source provides a combined figure.
- Annual, supplementary, and second annual examinations are different cycles; preserve the board's exact label.
- A result gazette may contain candidate-level data while a press release gives only headline summaries; do not claim one provides the other.
- Position-holder lists are ceremonial summaries, not substitutes for overall pass-rate statistics.

## Validation Checklist

- Confirm the board name and exam cycle.
- Verify the year and whether the result is annual or supplementary/second annual.
- Check whether the cited figure is a count or percentage.
- Preserve level and part labels exactly.

## Common Pitfalls

- Mixing result cycles across boards.
- Treating a topper announcement as if it summarizes board-wide performance.
- Confusing exam date sheets with published result notices.
- Combining Part-I and Part-II outcomes without a source-provided aggregate.

## Reference

- See [Pakistan Board Exam Results Reference](references/pakistan-board-exam-results.md) for source structure and extraction notes.
