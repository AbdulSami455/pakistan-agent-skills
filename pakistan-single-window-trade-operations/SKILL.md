---
name: pakistan-single-window-trade-operations
description: Pakistan Single Window trade operations skill. Use when explaining or analyzing Pakistan Single Window (PSW) workflow for import/export clearance, document submission, and cross-agency trade processing, especially for office teams handling customs, shipping, and regulatory compliance.
---

# Pakistan Single Window Trade Operations

## Overview

Use this skill for operational import/export office work through Pakistan Single Window (PSW): document flow, customs-linked processing, and agency coordination around trade clearance. This is the right skill when the task is about how trade documents move through Pakistan's electronic clearance environment rather than what tariff rate applies to an HS code.

## Coverage

- Pakistan Single Window as the electronic trade-facilitation layer for cross-border cargo processing.
- Interaction boundaries between PSW, customs tariff classification, shipping documents, and regulatory approvals.
- Import/export office workflow around declarations, supporting documents, and agency touchpoints.
- Distinction between platform/process questions and product-specific tariff or tax questions.
- High-level understanding of how traders, clearing agents, customs, and other regulatory agencies intersect operationally.

## Use This Skill For

- explaining what PSW does in an import/export office workflow
- distinguishing platform/process questions from duty-rate questions
- helping office teams understand which documents and approvals move through cross-agency clearance flow
- clarifying how PSW relates to customs, shipping, and regulatory compliance
- summarizing why trade operations teams need PSW familiarity beyond simple tariff lookup

## When Not to Use This Skill

- For HS-code duty-rate lookup, use `fbr-customs-tariff` instead.
- For macro trade statistics, use `tdap-trade-reports` or `pes-external-sector` instead.
- For port cargo throughput statistics, use the relevant port-report skill instead.

## Routing Rules

- Use this skill when the main question is operational trade-processing workflow.
- If the question is "what duty applies," route to `fbr-customs-tariff`.
- If the question is "how much trade happened," route to trade-statistics skills instead.
- Keep PSW process logic separate from customs-law classification and separate from port-operations statistics.

## Extraction Workflow

1. Identify whether the issue is import-side, export-side, or a shared platform/process question.
2. Confirm whether the task concerns document submission, agency approval, clearance workflow, or user-role interaction.
3. Preserve the distinction between PSW as a platform/process layer and customs duty/tax as substantive obligations.
4. Note whether customs, quarantine, standards, or another regulatory touchpoint is the relevant operational concern.
5. If shipping/port context is mentioned, separate platform workflow from cargo-volume reporting.

## Technical Rules

- PSW is a process and integration layer, not itself the tariff schedule or the port operator.
- Customs classification, duty calculation, and regulatory approvals remain distinct substantive questions even when submitted through one platform.
- Office workflow should preserve which document or approval belongs to which agency rather than flattening everything into "customs clearance."
- Platform-based process explanations should not be overstated into legal advice on classification or exemption eligibility.

## Validation Checklist

- Confirm the question is about trade operations workflow rather than pure tariff classification.
- Verify whether the issue is import, export, or cross-agency clearance flow.
- Check whether a separate customs-tariff or regulator-specific skill should handle part of the answer.
- Preserve which agency or document layer is being discussed.

## Common Pitfalls

- Treating PSW as if it determines tariff rates by itself.
- Collapsing all trade compliance into one undifferentiated customs step.
- Confusing operational document submission with substantive legal eligibility for concessions or exemptions.
- Mixing PSW workflow with port cargo statistics.

## Reference

- See [Pakistan Single Window Trade Operations Reference](references/pakistan-single-window-trade-operations.md) for source structure and extraction notes.
