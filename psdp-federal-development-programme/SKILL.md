---
name: psdp-federal-development-programme
description: PSDP federal development programme skill. Use when analyzing, summarizing, comparing, or extracting information from Pakistan's Public Sector Development Programme (PSDP) documents published by the Ministry of Planning, Development & Special Initiatives, especially for ministry-wise or project-wise development allocations, releases, and expenditure against the federal development budget.
---

# PSDP Federal Development Programme

## Overview

Use this skill for questions about Pakistan's Public Sector Development Programme (PSDP), the federal government's annual development spending plan administered by the Ministry of Planning, Development & Special Initiatives (MoPD&SI). This covers PSDP books, project-wise allocation tables, and periodic release/expenditure reports — distinct from the current (non-development) expenditure covered in the Demand for Grants or from provincial ADP/PSDP equivalents.

## Coverage

- Published annually as part of the federal budget cycle, typically alongside or shortly after the federal budget documents.
- Typical content: total PSDP size for the upcoming fiscal year; ministry/division-wise allocation breakdown; project-wise detail (project name, executing agency, estimated cost, allocation for the year, cumulative expenditure to date); sector-wise aggregates (infrastructure, social sectors, production sectors); foreign-aided vs. locally funded project splits; releases and expenditure reports issued periodically during the fiscal year.
- PSDP is forward-looking at budget time (proposed allocations) and backward-looking during the year (actual releases and expenditure against allocations).
- Provincial governments maintain their own Annual Development Programmes (ADPs); this skill covers the federal PSDP only.

## Use This Skill For

- extracting total federal PSDP size for a fiscal year
- identifying ministry-wise or sector-wise development allocations
- looking up a specific project's allocation, estimated cost, or cumulative expenditure
- comparing budgeted PSDP allocations with actual releases/expenditure during the year
- distinguishing development expenditure from current (recurrent) expenditure in federal spending analysis

## Routing Rules

- Use this skill for federal development spending (PSDP). For federal current/recurrent expenditure and overall budget aggregates, prefer `federal-budget-documents`.
- For realized fiscal outturns across all expenditure (development and current), prefer `pes-fiscal-financial-and-debt` once the fiscal year is complete.
- For provincial development budgets (Punjab ADP, Sindh ADP, etc.), this skill does not apply; note the provincial ADP as a separate source.
- If the question is about IMF program conditionality on development spending, cross-reference with `imf-pakistan-documents` for program targets and this skill for the actual PSDP allocation detail.

## Extraction Workflow

1. Identify whether the question needs budgeted allocations (at budget time) or actual releases/expenditure (during or after the fiscal year).
2. Confirm the fiscal year the PSDP covers.
3. For project-specific questions, locate the project in the project-wise detail table rather than relying on ministry-level aggregates.
4. Preserve the executing agency, estimated total cost, allocation for the year, and cumulative expenditure as separate fields.
5. Distinguish foreign-aided projects from locally funded projects when the table provides this breakdown.

## Technical Rules

- PSDP allocations are budget estimates; actual releases may lag allocations, and expenditure may lag releases — do not treat allocation as equivalent to spent amount.
- Project estimated costs and annual allocations are different concepts; a project's total estimated cost can span multiple fiscal years.
- Ministry/division names and project listings can change between PSDP editions due to reorganizations or project completion; confirm the edition year.
- Foreign-aided project figures may be denominated in foreign currency for the aid component; preserve the currency and conversion basis if stated.

## Validation Checklist

- Confirm the fiscal year and whether the figure is a budget allocation, release, or expenditure.
- Verify whether the figure is federal PSDP or a provincial ADP before quoting.
- Check whether a project-wise figure matches the ministry aggregate it belongs to.
- Note whether foreign-aided and locally funded components are being combined or kept separate.

## Common Pitfalls

- Treating PSDP budget allocations as realized expenditure.
- Conflating federal PSDP with provincial ADP figures.
- Quoting a project's annual allocation as its total estimated cost.
- Mixing development and current expenditure when reading federal spending totals.

## Reference

- See [PSDP Reference](references/psdp-federal-development-programme.md) for document structure and extraction notes.
