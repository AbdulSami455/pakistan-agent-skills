---
name: fbr-customs-tariff
description: FBR Pakistan Customs Tariff skill. Use when analyzing, summarizing, comparing, or extracting information from the FBR Pakistan Customs Tariff (Fifth Schedule and the broader tariff schedule), especially for HS-code-based duty rate lookups and analysis of tariff changes published with the annual June budget.
---

# FBR Customs Tariff

## Overview

Use this skill for Pakistan's Customs Tariff schedule, published by FBR and updated annually alongside the June budget (commonly referenced by its Fifth Schedule for concessionary rates, plus the main First Schedule for standard tariff lines). This is the right skill for HS-code-level duty lookups and for analyzing what changed in a given year's tariff revision.

## Coverage

- Tariff schedule organized by Harmonized System (HS) code, typically at the 8-digit national tariff line level, grouped into sections and chapters following the HS classification.
- Standard customs duty rates by HS code (First Schedule).
- Concessionary/exemption schemes and conditional rates (Fifth Schedule and SRO-based concessions).
- Annual tariff changes announced with the Finance Bill/Finance Act, including new lines, rate changes, and withdrawn concessions.

## Use This Skill For

- looking up the customs duty rate for a specific HS code or product description
- identifying whether a product qualifies for a concessionary rate under the Fifth Schedule or a specific SRO
- analyzing what tariff rates changed in a given year's budget compared to the prior year
- tracing a tariff line across chapters when a product could plausibly fall under more than one HS heading
- summarizing the net protective effect of a tariff change for a sector (e.g. higher duty on finished goods vs. inputs)

## Routing Rules

- Use this skill for HS-code-specific duty rates and schedule structure.
- If the question is about the broader Finance Bill or overall budget revenue impact rather than a specific tariff line, prefer `federal-budget-documents`.
- If the question is about aggregate customs duty collection statistics rather than the rate schedule itself, prefer `fbr-yearbook`.
- If the question is about trade volumes or import/export values rather than duty rates, prefer `pes-external-sector`.

## Extraction Workflow

1. Identify the specific HS code or product description in question; if only a product name is given, locate its likely HS chapter/heading first.
2. Check whether the standard rate (First Schedule) or a concessionary rate (Fifth Schedule/SRO) applies, and note any conditions attached to the concession (e.g. end-use, sector-specific, import-quota-linked).
3. When comparing tariff changes year-over-year, locate the same HS code in both the current and prior tariff schedule before concluding a rate changed.
4. Note whether a "change" is a duty rate change, a regulatory duty (RD) addition/removal, or an additional customs duty (ACD) change — these are distinct levies that can move independently.
5. Preserve the exact HS code (typically 8-digit at the national level) when citing a rate, since rates can differ between closely related codes.

## Technical Rules

- Do not quote a tariff rate without the specific HS code it attaches to; rates vary materially within the same broad product category.
- Distinguish customs duty (CD), regulatory duty (RD), additional customs duty (ACD), and any other duty layers; do not collapse them into a single "tariff rate" unless the question asks for the combined effective rate.
- Preserve conditional language exactly (e.g. "subject to quota," "for industrial use only") rather than treating a concessionary rate as unconditional.
- When an SRO amends the Fifth Schedule mid-year, treat the SRO as the more current source for that line.

## Validation Checklist

- Confirm the HS code cited matches the product description in the question.
- Verify whether the cited rate is the standard rate or a conditional concessionary rate.
- Check whether regulatory duty or additional customs duty applies on top of the base customs duty.
- Confirm which tariff year's schedule is being used, since rates change with each budget.

## Common Pitfalls

- Quoting a duty rate without specifying the exact HS code, when adjacent codes carry different rates.
- Treating a Fifth Schedule concessionary rate as unconditional when it has end-use or quota conditions.
- Confusing customs duty with the combined effective rate including RD/ACD and other import levies.
- Comparing tariff lines across years without checking whether the HS code itself was restructured or renumbered.

## Reference

- See [Customs Tariff Reference](references/customs-tariff.md) for schedule structure and extraction notes.
