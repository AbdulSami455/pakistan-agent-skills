---
name: ecp-election-results
description: Pakistan election results skill. Use when tracking Election Commission of Pakistan results, constituency details, notification updates, by-elections, or official election status for national, provincial, or local contests.
---

# ECP Election Results

## Overview

Use this skill for Pakistan election-result questions that need the official Election Commission of Pakistan (ECP) record or a careful status check for a constituency, by-election, or notification. This is a results and status-tracking skill, not a legal or political analysis skill.

## Coverage

- National Assembly and provincial assembly constituency results
- By-election results and notifications
- Constituency codes, names, and delimitation references
- Official result forms and gazette-style final result notices when available

## Use This Skill For

- checking who won a specific National Assembly or provincial seat
- tracing the official result status for a constituency or by-election
- extracting votes, margin, and party affiliation from official result pages or notices
- matching a constituency name to its ECP code or current delimitation
- distinguishing provisional results from final announced results

## Routing Rules

- Use this skill for election results, not for general parliamentary bill tracking. For bills, use `parliament-legislative-tracker`.
- If the task is about voter lists, electoral rolls, or candidate nomination details rather than results, stay with the ECP source but report the specific document type.
- If a user asks about a historical result, verify which election year or by-election date applies before quoting the seat outcome.

## Extraction Workflow

1. Identify the exact election or by-election date and the constituency code.
2. Confirm whether the source is a provisional result, consolidated result, or final official result.
3. Preserve the constituency name as published by ECP, including province and seat number.
4. Extract the winning candidate, party, vote total, runner-up vote total, and margin only from the official result source.
5. If a constituency was renumbered or re-delimited, state the mapping explicitly before giving the result.

## Technical Rules

- Do not mix results from different election years or by-election cycles.
- Do not infer a winner from media reports if an official ECP result notice is available.
- Keep provincial and National Assembly seat numbering separate.
- If the source only shows a form or notice image, transcribe the official figures exactly and note the document type.

## Validation Checklist

- Confirm the constituency code and election year.
- Verify the final result status before treating a preliminary result as official.
- Check whether the seat is general, reserved, or a by-election.
- Confirm the vote total and margin from the same source document.

## Common Pitfalls

- Treating unofficial media tallies as final ECP results.
- Confusing a constituency's current delimitation with its pre-delimitation historical seat number.
- Mixing National Assembly, provincial assembly, and local government contests.
- Citing a candidate's party label without checking whether the result source uses an independent or party-affiliated designation.

## Reference

- See [ECP Election Results Reference](references/ecp-election-results.md) for source routing and result-type notes.
