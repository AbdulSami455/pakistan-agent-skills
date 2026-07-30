---
name: pakistan-defense-budget-framework
description: Pakistan defense budget presentation framework skill. Use when a task needs the unclassified, public-facing structure of how defense expenditure appears in Pakistan's Federal Budget documents — the Demand for Grants structure, Ministry of Defence vs. Ministry of Defence Production split, current vs. development defense spending, and historical defense-spending-as-%-of-GDP/budget context with hedged figures — as distinct from the general federal budget skill or classified/operational military matters, which this skill does not and cannot address.
---

# Pakistan Defense Budget Framework

## Overview

Use this skill for how Pakistan's defense expenditure is **presented in public federal budget documents** — the Demand for Grants structure, the split between the Ministry of Defence and Ministry of Defence Production, and the current-versus-development expenditure classification, all as unclassified budget-presentation mechanics. This skill covers only publicly disclosed, unclassified budget-document structure. It does not, and cannot, provide classified operational, procurement-contract, or force-structure detail — no such detail is publicly disclosed in Pakistan's budget documents, and this skill must not speculate about it.

## Coverage

- **Where defense spending appears**: Pakistan's federal Demand for Grants and Appropriations document presents defense expenditure through specific Grant numbers/heads corresponding to the Ministry of Defence and the Ministry of Defence Production (and related defense-services grants for the Army, Navy, and Air Force presented as separate heads within the broader defense services grant structure). The Budget in Brief similarly shows a defense-services aggregate line as part of current expenditure.
- **Ministry of Defence vs. Ministry of Defence Production**: these are two **separate federal ministries** in Pakistan's budget/administrative structure. The Ministry of Defence oversees the armed forces' administrative and services functions (and reports the defense-services current expenditure grant); the Ministry of Defence Production oversees defense production organizations/entities (state-owned defense-production enterprises) and is budgeted separately, with its own, much smaller, Demand for Grants allocation. Reports that cite "the defense budget" as a single figure are typically referring to the Ministry of Defence's defense-services allocation, not a combined total inclusive of Defence Production — always check which is being cited.
- **Current vs. development defense spending**: like other ministries, defense-related expenditure is split between **current expenditure** (recurring costs — pay and allowances, stores, maintenance — presented in the Demand for Grants/current budget) and **development expenditure** (defense-related development projects that may appear within the Public Sector Development Programme, PSDP, under a defense-services development head, distinct from the much larger current defense-services grant). The current-expenditure defense-services grant is, by long-standing structure, substantially larger than any defense-related development-budget component.
- **Historical defense-spending-as-share context**: Pakistan's defense expenditure as a share of GDP and as a share of total federal current expenditure has been a long-running fiscal feature, generally described in public commentary as a large share of federal current (non-development, non-debt-servicing) expenditure alongside debt servicing — but any specific percentage-of-GDP or percentage-of-budget figure for a given year should be treated as needing verification against that year's actual Budget in Brief/PES figures rather than stated from memory, since the ratio moves with both nominal defense allocation growth and GDP/budget-size changes (including the effect of GDP rebasing).

## Use This Skill For

- explaining where and how defense expenditure is presented in Pakistan's federal Demand for Grants and Budget in Brief documents
- distinguishing the Ministry of Defence's budget from the Ministry of Defence Production's separate, smaller budget
- explaining the current vs. development split for defense-related expenditure, including how a defense-services PSDP component (if any) differs from the main current-expenditure defense grant
- framing historical defense-spending-as-share-of-GDP or -of-budget trends with appropriately hedged, verify-current-figure language
- clarifying what is and is not publicly disclosed in Pakistan's defense budget presentation (line-item granularity is limited by design; classified/operational detail is not published)

## When Not to Use This Skill

- For the general federal budget process, Budget Speech, Finance Bill, or non-defense ministry allocations — use `federal-budget-documents`; this skill is the defense-specific slice of that same annual budget-document set.
- For realized/actual fiscal outturns (as opposed to budgeted defense allocations) — use `pes-fiscal-financial-and-debt` or `agpr-fiscal-operations` for actual expenditure figures once reported.
- For federal development-project tracking generally (beyond noting that a defense-services development head can appear in the PSDP) — use `psdp-federal-development-programme`.
- For any classified, operational, procurement-contract-specific, or force-structure detail — this skill does not have access to and must not speculate about non-public defense information; state plainly that such detail is not disclosed in public budget documents rather than guessing.

## Routing Rules

- If the question is about the general budget cycle, other ministries' allocations, or the Finance Bill's tax measures, route to `federal-budget-documents` and use this skill only for the defense-specific presentation layer within those same documents.
- If the question is about actual/realized defense expenditure outturns for a completed period rather than the budgeted allocation, route to `pes-fiscal-financial-and-debt` or `agpr-fiscal-operations`.
- If the question asks for classified, operational-readiness, procurement-contract-value, or force-structure detail, decline to speculate and state that Pakistan's public budget documents do not disclose that level of detail — do not fill the gap with invented figures.
- If the question is about a defense-related development project specifically within the PSDP, cross-reference `psdp-federal-development-programme` for that document's project-level structure.

## Extraction Workflow

1. Confirm whether the question needs the Ministry of Defence's defense-services allocation, the Ministry of Defence Production allocation, or both — these are separate grants/ministries and should not be silently combined into one "defense budget" figure without saying so.
2. Identify whether current or development expenditure is being asked about; report the current-expenditure defense-services grant as the primary, much larger figure, and separately note any defense-related PSDP/development component if relevant.
3. For any specific rupee amount or percentage-of-GDP/budget figure, source it to a specific fiscal year's actual Budget in Brief/Demand for Grants, and hedge explicitly ("verify current figure against the FY[year] Budget in Brief") rather than stating a fixed number from general knowledge.
4. When asked for a historical trend, describe the qualitative pattern (defense spending has long been a large share of current federal expenditure alongside debt servicing) without asserting precise year-by-year percentages unless sourced to a specific document.
5. If a question probes toward classified or operationally sensitive detail (force levels, specific weapons-system costs, procurement-contract terms), redirect to what is publicly disclosed (aggregate grant totals only) and explicitly state that granular/classified detail is not part of the public budget disclosure.

## Technical Rules

- Always distinguish the Ministry of Defence's defense-services grant from the Ministry of Defence Production's separate, smaller grant; do not report one figure as "the total defense budget" without clarifying scope.
- Defense-services line items in the Demand for Grants are aggregated at a high level (grant/major-head totals) rather than broken into granular operational sub-items; do not imply the public document discloses procurement-contract-level or unit-level detail it does not contain.
- Treat any specific percentage-of-GDP, percentage-of-total-budget, or year-over-year growth figure for defense spending as requiring sourcing to a specific year's actual budget document; do not state a precise figure from memory as current.
- Never speculate about or fabricate classified, operational, or force-structure information; state plainly that such information is outside the scope of public budget disclosure.
- Note that GDP rebasing (a periodic statistical exercise) can itself move a "defense spending as % of GDP" ratio independent of any change in the nominal defense allocation — flag this when discussing the ratio's trend.

## Validation Checklist

- Confirm whether the figure requested is the Ministry of Defence grant, Ministry of Defence Production grant, or a combined total, and label accordingly.
- Confirm whether current or development expenditure is being discussed, and do not merge the two without saying so.
- Confirm any specific rupee or percentage figure is attributed to a specific fiscal year's budget document, with a "verify current figure" hedge if not freshly sourced.
- Confirm the response does not include any invented classified, operational, or procurement-contract-specific detail.
- Confirm any GDP-share trend discussion notes the possible confounding effect of GDP rebasing.

## Common Pitfalls

- Reporting the Ministry of Defence Production's allocation as if it were part of, or the same as, the Ministry of Defence's main defense-services grant.
- Presenting a specific defense-spending-as-%-of-GDP figure from memory as current without sourcing it to an actual budget-year document.
- Implying that Pakistan's public budget documents disclose classified, unit-level, or procurement-contract-specific defense detail — they do not, by design.
- Treating a change in defense-spending-as-%-of-GDP as necessarily reflecting a change in nominal defense allocation, without checking for a GDP-rebasing effect.
- Conflating current defense-services expenditure with any defense-related PSDP/development-budget component, which is a separate and much smaller allocation.

## Reference

- See [Pakistan Defense Budget Framework Reference](references/pakistan-defense-budget-framework.md) for the Demand for Grants structure, the Ministry of Defence/Defence Production split, and sourcing notes.
