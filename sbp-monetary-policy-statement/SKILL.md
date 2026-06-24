---
name: sbp-monetary-policy-statement
description: SBP Monetary Policy Statement skill. Use when analyzing, summarizing, comparing, or extracting information from a State Bank of Pakistan Monetary Policy Statement, especially for the policy rate decision, Monetary Policy Committee (MPC) rationale, and the inflation outlook discussion behind a specific MPC meeting.
---

# SBP Monetary Policy Statement

## Overview

Use this skill for questions about a specific State Bank of Pakistan (SBP) Monetary Policy Statement (MPS). SBP's Monetary Policy Committee issues these statements roughly six times a year, each announcing whether the policy rate is held, cut, or raised, along with the reasoning. This is the right skill when the task is about a single MPC decision and its stated rationale, not a full-year narrative.

## Coverage

- Each MPS covers one MPC meeting and is dated to that meeting (e.g. the statement following the January, March, or June meeting).
- Statements typically include: the policy rate decision, a short summary of the MPC's assessment of inflation and growth, real sector and external sector context, and forward guidance language.
- Source: SBP's monetary policy page on `https://www.sbp.org.pk` under Monetary Policy / MPC decisions, including the press release and the longer "Monetary Policy Statement" document where published.

## Use This Skill For

- extracting the policy rate decision (held, cut, raised) and the size of any change in basis points
- summarizing the MPC's stated rationale for a specific meeting
- comparing the policy rate decision and tone across consecutive MPC meetings
- extracting the MPC's inflation outlook or inflation range for the statement period
- identifying forward guidance language (e.g. "data-dependent," "further monetary easing")

## Routing Rules

- Use this skill for a single MPC meeting's decision and reasoning, not the full-year monetary narrative.
- If the question is about a broader, full-year monetary and credit narrative across a fiscal year, prefer `pes-fiscal-financial-and-debt` (its Money and Credit chapter) or `sbp-annual-report` for SBP's own framing.
- If the question is about systemic financial stability or bank soundness rather than the rate decision itself, use `sbp-financial-stability-review` or `sbp-financial-soundness-indicators` instead.
- If the question is about external reserves or balance of payments backdrop cited in the statement, use `sbp-balance-of-payments-bulletin` for the underlying data and this skill only for how the MPC framed it.

## Extraction Workflow

1. Identify the exact MPC meeting date the statement belongs to.
2. Locate the policy rate decision, usually stated in the opening paragraphs of the press release.
3. Read the rationale section for the inflation outlook, growth assessment, and external account commentary the MPC cites as drivers.
4. Preserve the exact basis-point change and the resulting policy rate level.
5. Note any forward guidance or conditionality language exactly as written.
6. If comparing across meetings, align statements by meeting date, not calendar quarter, since MPC meeting cadence is irregular.

## Technical Rules

- Always state the policy rate as a level (e.g. "X percent") together with the change from the prior meeting, not just the change.
- Do not infer a future rate path; only report forward guidance language the MPC actually used.
- Distinguish between the MPC's inflation outlook (forward-looking) and historical inflation outturns it cites as context.
- Keep meeting-specific language separate from boilerplate MPS sections that repeat across statements.

## Validation Checklist

- Confirm the policy rate figure and the direction of change match the stated decision.
- Verify the meeting date and statement date are not confused with the next scheduled meeting date.
- Check whether the statement distinguishes real, nominal, or risk-adjusted commentary.
- Confirm whether cited inflation figures are realized (past) or projected (outlook).

## Common Pitfalls

- Quoting the policy rate level without noting whether it changed from the previous meeting.
- Treating routine boilerplate risk language as a new forward-guidance signal.
- Confusing the MPC's projected inflation range with the latest realized CPI figure.
- Mixing up consecutive meetings when comparing tone across a tightening or easing cycle.

## Reference

- See [Monetary Policy Statement Reference](references/monetary-policy-statement.md) for statement structure and extraction notes.
