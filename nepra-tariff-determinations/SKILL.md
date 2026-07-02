---
name: nepra-tariff-determinations
description: NEPRA tariff determination skill. Use when analyzing, summarizing, comparing, or extracting information from NEPRA's tariff determinations or decisions for a specific power generation, transmission, or distribution licensee, especially for the approved tariff rate, tariff structure, and the regulatory rationale behind it.
---

# NEPRA Tariff Determinations

## Overview

Use this skill for the specific tariff rate or decision NEPRA (National Electric Power Regulatory Authority) has awarded to a named power sector licensee — a generation company (IPP), NTDC, a DISCO, or K-Electric. This is the right skill when the question is about one project or company's approved tariff, not sector-wide performance or planning.

## Coverage

- Tariff determinations are issued per licensee/project following a public hearing process under the NEPRA Act, 1997 and the Tariff Standards and Procedure Rules, 1998.
- Typical categories: generation tariffs for IPPs (by technology — thermal, hydel, wind, solar, coal), transmission tariffs (NTDC), distribution/supply tariffs (ex-WAPDA DISCOs and K-Electric), and periodic adjustments (fuel charge adjustments (FCA), quarterly tariff adjustments (QTA), monthly fuel price adjustments (MFPA)).
- A determination document typically includes: the tariff petition summary, NEPRA's cost-of-service or return-on-equity analysis, the approved tariff structure (capacity/energy split for generation, or slab structure for distribution), and the effective date.
- Multi-Year Tariff (MYT) determinations set a tariff framework spanning several years, subject to periodic/annual adjustments within that framework.

## Use This Skill For

- extracting the approved tariff rate for a specific IPP, DISCO, or K-Electric
- identifying the tariff structure (capacity payment vs. energy payment, or consumer slab rates) for a determination
- tracking periodic adjustments (FCA, QTA, MFPA) applied on top of a base tariff
- comparing tariffs across similar-technology generation projects
- confirming the effective date and validity period of a specific determination

## When Not to Use This Skill

- For sector-wide realized generation/distribution performance — use `nepra-state-of-industry` instead.
- For forward-looking indicative cost assumptions used in capacity planning (not yet an actual determination) — use `igcep-capacity-plan` instead; IGCEP's cost inputs are planning assumptions, not approved tariffs.
- For the guidelines/policy framework used to set tariffs generally, rather than a specific project's determination.

## Routing Rules

- Use this skill only once a specific project or company has reached the tariff determination stage; before that, cost assumptions belong to `igcep-capacity-plan` as indicative planning inputs, not actual tariffs.
- Use `nepra-state-of-industry` for aggregate sector performance rather than a single licensee's tariff decision.
- If the question is about a periodic adjustment (FCA/QTA/MFPA) rather than a base/reference tariff, treat it as a distinct, layered figure on top of the base determination, not a replacement for it.

## Extraction Workflow

1. Identify the specific licensee/project and technology (if generation) the determination applies to.
2. Confirm whether the figure needed is the base/reference tariff or a periodic adjustment (FCA, QTA, MFPA) layered on top of it.
3. Locate the matching determination document, noting its case/docket reference and issuance date.
4. Preserve the tariff structure exactly (e.g., capacity payment vs. energy payment components for generation; fixed vs. variable charges for distribution).
5. Note the effective date and, where applicable, the validity period or next scheduled review.

## Technical Rules

- Keep base/reference tariffs distinct from periodic adjustments (FCA, QTA, MFPA); a consumer or project's all-in rate is the base tariff plus applicable adjustments, not the base tariff alone.
- Generation tariffs for IPPs typically separate capacity payments (fixed, tied to availability) from energy payments (variable, tied to output) — preserve this split rather than quoting a single blended rate unless the source does so.
- Multi-Year Tariff (MYT) determinations set a framework; the applicable rate in any given year may differ from the MYT's headline figure due to indexation or adjustment mechanisms.
- Tariff determinations are specific to a licensee and technology; do not apply one IPP's tariff structure to another without confirming comparable technology and vintage.

## Validation Checklist

- Confirm the exact licensee/project name and case/docket reference for the determination being cited.
- Verify whether the figure is a base tariff or includes a periodic adjustment layer.
- Check the effective date and whether the determination has since been revised or superseded.
- Confirm capacity vs. energy payment components are not conflated when citing a generation tariff.

## Common Pitfalls

- Quoting a base tariff without noting that periodic adjustments (FCA/QTA/MFPA) change the effective all-in rate.
- Treating IGCEP's indicative planning cost assumptions as an actual NEPRA-approved tariff.
- Conflating capacity payment and energy payment components into a single misleading "tariff" figure for a generation project.
- Citing an outdated determination that has since been revised by a subsequent NEPRA decision.

## Reference

- See [NEPRA Tariff Determinations Reference](references/nepra-tariff-determinations.md) for document structure and extraction notes.
