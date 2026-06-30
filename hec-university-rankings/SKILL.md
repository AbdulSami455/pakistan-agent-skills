---
name: hec-university-rankings
description: HEC and international university ranking skill. Use when looking up, comparing, or tracking Pakistani university positions in ranking systems — specifically HEC's own university categorization/ranking, QS World University Rankings (Asia/general), and Times Higher Education (THE) rankings for Pakistan — especially for year-over-year position changes, discipline-level ranking, or cross-system comparison.
---

# HEC University Rankings

## Overview

Use this skill when the task is about where a Pakistani university stands in a ranking system — HEC's own ranking/categorization, QS World University Rankings, or Times Higher Education (THE). This is a ranking-position skill, not an enrollment or faculty-statistics skill; for those, use `hec-higher-ed-stats` instead.

## Coverage

Three ranking systems are in scope:

1. **HEC University Ranking / Categorization** — published by HEC Pakistan, grouping universities into categories (general, agriculture & veterinary, engineering & technology, medical, business education) and ranking within categories. Updated in cycles; not annual.
2. **QS World University Rankings** — published annually by Quacquarelli Symonds; includes a QS Asia ranking and a global ranking where a small number of Pakistani universities appear. Also publishes QS by Subject for Pakistani institutions.
3. **Times Higher Education (THE) World University Rankings** — published annually; includes a THE Asia ranking and THE Impact ranking where Pakistani universities sometimes feature.

## Use This Skill For

- looking up a specific Pakistani university's position in QS, THE, or HEC ranking for a given year
- comparing a university's ranking position year-over-year within the same system
- comparing a university's position across two different ranking systems (e.g., QS vs THE) for the same year
- identifying which Pakistani universities appear in a given ranking and at what position
- extracting discipline/subject-level ranking for a Pakistani university

## Use This Skill For — Not

- For university enrollment, graduate output, or faculty statistics — use `hec-higher-ed-stats` instead.
- For admission merit lists, entry test scores, or admission cutoffs — use `pakistan-university-admissions` instead.
- For whether a program is accredited by a professional council (PEC, PMDC, NCEAC) — use `hec-accreditation-councils` instead.
- For school-level education statistics — use `pakistan-education-statistics` instead.

## Routing Rules

- Use this skill when the question is about a university's rank or position in a named ranking system (QS, THE, or HEC ranking).
- If the question is about enrollment, faculty, or graduate numbers — route to `hec-higher-ed-stats`.
- If the question is about HEC's university **categorization** (general, engineering, medical, etc.) as part of a broader enrollment/faculty query — use `hec-higher-ed-stats` for that context; use this skill only when the categorization/ranking is the primary focus.
- If the question is about whether a university is recognized/chartered by HEC — that is a recognition question, not a ranking question; use `hec-higher-ed-stats` (which covers recognized university lists).
- If the question mixes ranking with admission cutoffs — split: use this skill for the ranking part, `pakistan-university-admissions` for the admission part.

## Extraction Workflow

1. Identify which ranking system is being asked about: HEC, QS, or THE. Do not mix systems in a single comparison without labeling each.
2. Identify the ranking year/edition — rankings are published annually and positions change year to year; always anchor a position to its specific edition.
3. Identify whether the question asks for an overall university rank or a subject/discipline-level rank — these are different tables.
4. For QS: note whether the position is from the global ranking or the Asia ranking — Pakistani universities often appear in Asia but not globally.
5. For THE: note whether the position is from the World ranking, Asia ranking, or Impact ranking — each is a separate table.
6. For HEC: note the ranking category (general, engineering, medical, etc.) — a university's position is category-specific.

## Technical Rules

- Always state the ranking system, the edition/year, and the category (if applicable) alongside any rank number.
- QS and THE use different methodology; a university can be ranked #5 by QS and #12 by THE in the same year — never average or merge across systems.
- HEC ranking positions are within-category, not national overall — a university ranked #1 in "engineering & technology" is not necessarily the top university nationally.
- Subject/discipline rankings are separate from overall university rankings — do not present a subject rank as the university's overall rank.
- Pakistani universities may appear in QS Asia but not QS Global — clarify which list a position comes from.

## Validation Checklist

- Confirm the ranking system (HEC, QS, or THE) matches what the question asks.
- Confirm the ranking edition/year — do not cite a 2023 position when the question asks for the latest.
- Verify whether the rank is overall or subject/discipline-specific.
- For QS/THE: verify whether the rank is global or Asia-level.
- For HEC: verify the ranking category.

## Common Pitfalls

- Citing a QS Asia rank as if it were a QS World rank.
- Mixing HEC category rankings with QS/THE global rankings in a single comparison without noting the different scales.
- Treating a subject-level rank as the university's overall position.
- Citing an outdated ranking edition as current — these update annually.
- Confusing HEC's ranking (a domestic categorization) with international rankings.

## Reference

- See [University Rankings Reference](references/university-rankings.md) for ranking system definitions and Pakistani university coverage notes.
