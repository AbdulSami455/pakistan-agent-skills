---
name: ecp-election-results
description: Pakistan election results skill. Use when tracking Election Commission of Pakistan (ECP) results for National Assembly, provincial assembly, Senate, or local government contests — including Form 45/47/49 result documents, reserved-seats (women/minority) allocation, delimitation, and by-elections — as distinct from parliamentary bill-tracking or political/legal analysis.
---

# ECP Election Results

## Overview

Use this skill for Pakistan election-result questions that need the official Election Commission of Pakistan (ECP) record or a careful status check for a constituency, by-election, reserved seat, or notification. ECP is the constitutional body (Article 218) responsible for organizing and conducting elections to the National Assembly, provincial assemblies, the Senate, and local governments, and for household tasks like delimitation of constituencies. This is a results and status-tracking skill, not a legal or political analysis skill.

## Coverage

- **General elections**: National Assembly (NA) and provincial assembly (PA) constituency results, most recently the **2024 general election** (held 8 February 2024), and prior general elections (2018, 2013, 2008, etc.).
- **Delimitation**: constituency boundaries are redrawn after each census. The constituencies used in the 2024 general election were based on the **2023 delimitation exercise**, which itself was carried out using the results of the **2023 digital census** (a shift from the previously used 2017 census-based delimitation). This delimitation changed constituency numbers, boundaries, and in some cases seat counts per province/district compared to 2018.
- **Senate elections**: indirect elections held periodically (roughly every three years for a rotating set of seats, since Senate members serve six-year terms with partial rotation) where sitting members of the National Assembly and provincial assemblies act as the electoral college; Senate results are a structurally different exercise from direct NA/PA general elections and should not be conflated with them.
- **By-elections**: results and notifications for individual seats vacated after the general election (death, resignation, disqualification, dual-seat vacation, etc.).
- **Reserved seats**: allocation of women's and non-Muslim/minority reserved seats in the National Assembly and provincial assemblies, which are not directly contested but allocated to parties proportionally.
- **Local government (LG) elections**: a structurally separate dataset covering mayors/chairmen, councillors, union council/tehsil/district-level seats — conducted under provincial LG laws and a different electoral framework than national/provincial assembly elections.
- **Result forms**: the specific ECP-prescribed forms that document results at each stage (see Technical Rules below) — Form 45, Form 47, and Form 49 — which are frequently central to real election disputes, recounts, and litigation in Pakistan.
- Constituency codes, names, and delimitation references (e.g., NA-1 through NA-266 post-2023 delimitation; provincial assembly seats coded PP/PS/PK/PB by province).

## Use This Skill For

- checking who won a specific National Assembly, provincial assembly, or Senate seat
- tracing the official result status for a constituency or by-election
- extracting votes, margin, and party affiliation from official result forms (Form 45/47/49) or notices
- matching a constituency name to its ECP code or current (post-2023) delimitation
- distinguishing provisional (polling-station-level) results from final consolidated/notified results
- explaining how reserved seats (women/minorities) are allocated to parties after a general election
- explaining the difference between National Assembly/provincial assembly elections and local government elections

## When Not to Use This Skill

- For general parliamentary bill tracking, legislative sessions, or law-making activity — use `parliament-legislative-tracker` instead.
- For voter-list/electoral-roll counts or constituency population statistics not tied to a specific result — treat as a data-lookup task using ECP's own rolls rather than this skill's result-tracking framing, and flag if it's really a `pakistan-census-bulletins` question.
- For deep legal/constitutional analysis of an election dispute (e.g., interpreting Article 62/63 disqualification case law) — this skill only tracks the factual result record, not legal reasoning; route conceptual constitutional questions to `pakistan-constitution-governance`.

## Routing Rules

- Use this skill for election results, not for general parliamentary bill tracking. For bills, use `parliament-legislative-tracker`.
- If the question is about local government (LG) election results (mayors, councillors, union council/tehsil/district seats), treat it as a distinct dataset from NA/PA general elections — LG elections run on separate provincial timelines and separate result-reporting formats; do not merge LG turnout/seat figures into general-election tallies.
- If the question is about Senate seats, note this is an indirect election by sitting NA/PA members, not a direct popular vote — do not describe Senate results using popular-vote-margin framing appropriate to NA/PA seats.
- If a user asks about a historical result, verify which election year or by-election date applies, and which delimitation (pre- or post-2023) the constituency numbering reflects, before quoting the seat outcome.
- If the task is about voter lists, electoral rolls, or candidate nomination details rather than results, stay with the ECP source but report the specific document type rather than treating it as a "result."

## Extraction Workflow

1. Identify the exact election or by-election date and the constituency code, and confirm which delimitation (pre-2023 or post-2023) that code corresponds to.
2. Confirm whether the source is a **Form 45** (polling-station-level provisional result), a **Form 47** (constituency-level consolidated result), a **Form 49** (declaration of the returned candidate), or a later official gazette notification — these represent successive stages, not interchangeable documents.
3. Preserve the constituency name as published by ECP, including province and seat number/prefix (NA-, PP-, PS-, PK-, PB-).
4. Extract the winning candidate, party, vote total, runner-up vote total, and margin only from the official result source, and note which form-stage the figures come from.
5. If a constituency was renumbered or re-delimited (e.g., comparing a 2018 NA seat to its 2024 post-delimitation equivalent), state the mapping explicitly before giving the result.
6. For reserved-seat questions, extract the general-seat tally each party won first, then apply/report the proportional allocation ECP notified for women's and minority reserved seats — do not treat reserved seats as directly contested.
7. For Senate questions, confirm which segment/tranche of seats was up for election (Senate seats rotate; not all seats are contested in the same year) before citing a result.

## Technical Rules

- **Form 45** — "Result of the Count," prepared and signed by the Presiding Officer at each individual polling station immediately after counting; it is the first, most granular official record and is frequently the reference point in recount disputes since it's the closest document to the actual ballot count.
- **Form 47** — "Consolidated Statement of the Results of the Count," prepared by the Returning Officer for the whole constituency by consolidating all polling stations' Form 45s; discrepancies between Form 45 totals and Form 47 consolidated totals are a common and legally significant type of election dispute in Pakistan.
- **Form 49** — the Returning Officer's formal declaration naming the returned (winning) candidate for the constituency, issued after consolidation; this is the document that legally establishes who won the seat, ahead of the ECP's own gazette notification.
- Reserved seats (women and non-Muslim/minority) are allocated to political parties **proportionally to the number of general seats each party won** in that assembly (National Assembly or a given provincial assembly), based on party lists submitted before the election — they are not separately voted on by the public.
- Do not mix results from different election years, by-election cycles, or pre-/post-2023-delimitation constituency numbering without explicitly flagging the mapping.
- Do not infer a winner from media reports if an official ECP Form 47/49 or gazette notification is available.
- Keep National Assembly, provincial assembly, Senate, and local government seat numbering and result formats separate — they are not interchangeable systems.
- If the source only shows a form or notice image, transcribe the official figures exactly and note the document type (Form 45 vs. 47 vs. 49) rather than presenting a transcription as an ECP-verified final result if it is only a polling-station-level document.

## Validation Checklist

- Confirm the constituency code, election year, and which delimitation (pre-2023 vs. post-2023) applies.
- Verify the final result status (Form 47/49 or gazette notification) before treating a Form 45 or preliminary result as official/final.
- Check whether the seat is a general seat, a reserved seat, a Senate seat, or a local government seat — each has a different result-determination process.
- Confirm the vote total and margin come from the same source document (do not mix a Form 45 subtotal with a Form 47 constituency total).
- For reserved-seat claims, confirm the underlying general-seat tally used for the proportional allocation.

## Common Pitfalls

- Treating unofficial media tallies or Form 45 polling-station figures as final ECP constituency results (that status belongs to Form 47/49 and gazette notification).
- Confusing a constituency's current (post-2023 delimitation) numbering with its pre-delimitation historical seat number.
- Mixing National Assembly, provincial assembly, Senate, and local government contests as if they were one dataset.
- Describing reserved seats as directly contested by voters rather than proportionally allocated based on general-seat tallies.
- Citing a candidate's party label without checking whether the result source uses an independent or party-affiliated designation (notably relevant given post-2024-election disputes over independent candidates and party affiliation for reserved-seat purposes).
- Treating Senate elections as if they used the same direct-popular-vote result format as NA/PA elections.

## Reference

- See [ECP Election Results Reference](references/ecp-election-results.md) for source routing, result-form detail, delimitation history, and result-type notes.
