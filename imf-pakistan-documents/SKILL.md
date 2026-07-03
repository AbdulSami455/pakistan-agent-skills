---
name: imf-pakistan-documents
description: IMF Pakistan documents skill. Use when analyzing, summarizing, comparing, or extracting information from IMF Article IV consultation reports or EFF/SBA staff reports for Pakistan, especially for program targets, structural benchmarks, and IMF staff assessments, which present an external, IMF-framed view distinct from the government's own Pakistan Economic Survey narrative.
---

# IMF Pakistan Documents

## Overview

Use this skill for IMF documents specific to Pakistan: Article IV consultation reports and program (Extended Fund Facility/Stand-By Arrangement) staff reports. These documents present the IMF's own independent assessment, program conditionality, and structural benchmarks — a framing distinct from the Ministry of Finance's Pakistan Economic Survey or SBP's own publications.

## Coverage

- Article IV consultation reports: the IMF's periodic, programme-independent assessment of Pakistan's economic policies and outlook, including staff appraisal and selected issues papers.
- Program staff reports (EFF, SBA, or other facilities): published at each review, covering program performance, quantitative performance criteria, structural benchmarks, and the staff's policy assessment.
- Letters of Intent / Memorandum of Economic and Financial Policies (MEFP), often annexed to staff reports, stating the government's own commitments to the IMF.
- Press releases accompanying Executive Board decisions on reviews or new arrangements.

## Use This Skill For

- extracting specific program targets (e.g. primary balance target, net international reserves floor) from a staff report
- identifying structural benchmarks and their due dates from a program review
- summarizing the IMF staff's assessment of risks to the program or the macroeconomic outlook
- comparing the IMF's projections (growth, inflation, fiscal) with the government's own PES figures for the same period
- tracing whether a specific structural benchmark was met, missed, or rephased across consecutive reviews

## When Not to Use This Skill

- For the government's own narrative or outturns for the same period — prefer the relevant `pes-*` skill.
- For SBP's own monetary or external-sector narrative — prefer `sbp-annual-report` or `sbp-monetary-policy-statement`.
- For the federal budget text itself — use `federal-budget-documents`; use this skill only for the program target the budget is meant to satisfy.
- For Pakistan's debt or fiscal position from the government's own perspective — use `pes-fiscal-financial-and-debt` instead.
- For World Bank or ADB development indicators with cross-country comparability, prefer `world-bank-pakistan-indicators` or `adb-pakistan-indicators`; IMF documents focus on program conditionality rather than broad development indicator databases.

## Routing Rules

- Use this skill when the question specifically needs the IMF's own assessment, program conditionality, or IMF staff projections.
- If the question is about the government's own narrative or outturns for the same period, prefer the relevant `pes-*` skill, and use this skill to provide the contrasting external view if the task calls for comparison.
- If the question is about SBP's own monetary or external-sector narrative, prefer `sbp-annual-report` or `sbp-monetary-policy-statement`; cross-reference IMF documents only where the program directly addresses monetary or exchange-rate policy commitments.
- If the question is about federal budget documents reflecting commitments made under an IMF program, use `federal-budget-documents` for the budget text itself and this skill for the program target it is meant to satisfy.

## Extraction Workflow

1. Identify which specific document type is needed: Article IV (independent assessment) vs. a program review staff report (conditionality-focused).
2. Identify the exact review (e.g. "first review," "fifth review") or consultation year, since targets and benchmarks are revised at each review.
3. Locate quantitative performance criteria and structural benchmarks in their dedicated tables/annexes rather than the narrative text alone.
4. Distinguish performance criteria (binding) from indicative targets and structural benchmarks (often softer, with due dates) when describing program conditionality.
5. Preserve whether a benchmark was reported as met, missed, met with a delay, or rephased to a later date.
6. When comparing IMF and government figures for the same indicator, keep both figures and their sources distinct rather than presenting one as more authoritative without context.

## Technical Rules

- Always specify the review number or consultation year for any cited target, since program conditionality evolves across reviews.
- Do not conflate quantitative performance criteria with structural benchmarks; they have different legal weight within the program.
- Keep IMF staff projections labeled as IMF projections, not as official government figures, even when discussed in the same answer.
- Preserve the exact wording of staff risk assessments (e.g. "risks are tilted to the downside") rather than paraphrasing into a different register.

## Validation Checklist

- Confirm which review or consultation cycle the cited target or assessment belongs to.
- Verify whether a benchmark is a performance criterion, indicative target, or structural benchmark.
- Check the stated status (met/missed/rephased) against the specific review document, not an inferred status.
- Confirm IMF projections are not misattributed to the Ministry of Finance or SBP.

## Common Pitfalls

- Treating an Article IV assessment as program conditionality when no program is in place.
- Confusing structural benchmarks (often qualitative/policy actions) with quantitative performance criteria (numeric targets).
- Citing an outdated review's targets when a more recent review has revised them.
- Presenting IMF growth/inflation projections as the government's own forecasts.

## Reference

- See [IMF Pakistan Documents Reference](references/imf-pakistan-documents.md) for document structure and extraction notes.
