---
name: pakistan-credit-rating-methodology
description: Pakistan credit rating methodology skill. Use when analyzing how PACRA or VIS Credit Rating Company assign, scale, and disclose credit ratings for Pakistani issuers/instruments, or how SECP licenses and regulates Credit Rating Companies (CRCs) under the Credit Rating Companies Regulations, 2016 — for analysts and treasury professionals interpreting a rating action or rating-scale notch rather than looking up a specific current rating figure.
---

# Pakistan Credit Rating Methodology

## Overview

Use this skill for how credit ratings are constructed, scaled, and regulated in Pakistan's two-agency domestic market: The Pakistan Credit Rating Agency Limited (PACRA) and VIS Credit Rating Company Limited (VIS, formerly JCR-VIS). This is the right skill for rating-scale interpretation, methodology structure (business risk/financial risk framework), rating-action mechanics (outlook, watch, upgrade/downgrade), and SECP's licensing/oversight regime for Credit Rating Companies (CRCs) — not a skill for pulling a specific company's current rating (which requires a live lookup against PACRA's or VIS's published rating reports) or for PSX-listed debt-instrument data (see `psx-debt-and-eligibility`).

## Coverage

- SECP's Credit Rating Companies Regulations, 2016 (issued under the Securities Act, 2015), covering CRC licensing requirements, restrictions/duties/obligations, and accounting/financial-record obligations — aligned with IOSCO's Code of Conduct Fundamentals for Credit Rating Agencies.
- The two SECP-licensed CRCs currently operating in Pakistan: PACRA (established 1994, Pakistan's first credit rating agency) and VIS Credit Rating Company Ltd.
- Rating-scale structure: long-term entity/instrument rating scales (e.g., AAA down through D, with speculative-grade generally understood as begining below the investment-grade cutoff), short-term rating scales, and specialized scales for fund stability ratings, REIT ratings, and other structured products, each denoted with distinguishing suffixes (e.g., "(f)" for fund ratings) so they are not confused with issuer/instrument ratings.
- Methodology framework: both agencies structure entity ratings around a Business Risk assessment (industry dynamics, competitive position, management quality) and a Financial Risk assessment (capital structure, coverage ratios, liquidity, profitability), synthesized into a forward-looking opinion on relative default likelihood — not a guarantee or audit opinion.
- Rating actions and outlook/watch mechanics: initial rating assignment, periodic surveillance (typically at least semi-annual), rating outlook (direction over a multi-year horizon), and rating watch (a shorter-horizon flag tied to a specific pending event).
- Distinction between an issuer/entity rating and an instrument rating (which can differ from the issuer's own rating based on instrument-specific features such as seniority, security, or structural credit enhancement).

## Use This Skill For

- explaining how PACRA's or VIS's rating scale is structured and what a specific rating notch (e.g., "AA-", "A1+") signifies in relative terms
- describing the Business Risk / Financial Risk methodology framework used to arrive at a rating opinion
- explaining SECP's licensing and regulatory oversight of Credit Rating Companies under the 2016 Regulations
- clarifying the difference between a rating outlook and a rating watch, and between an issuer rating and an instrument rating
- explaining why a specialized rating (fund stability, REIT) uses a different scale/suffix than a standard corporate entity rating

## When Not to Use This Skill

- For a specific company's or instrument's current actual rating figure, this skill provides the interpretive framework only — the current rating itself must be pulled from PACRA's or VIS's live published rating reports/press releases, not fabricated or assumed stable over time.
- For the list of PSX-listed debt instruments (TFCs/Sukuks) or margin-eligible scrips, use `psx-debt-and-eligibility` instead.
- For a corporate issuer's actual debt-issuance process (TFC/Sukuk structuring, trustee mechanics), use `pakistan-corporate-debt-capital-markets` or `pakistan-sukuk-structuring-issuance` instead — credit rating is one input into that process, not the process itself.
- For SBP's own assessment of banking-sector soundness (a supervisory function distinct from private CRC ratings), use `sbp-financial-soundness-indicators` instead.

## Routing Rules

- Use this skill when the question concerns how a rating is derived, scaled, or regulated — the methodology and framework, not a specific live rating value.
- If asked for a specific company's or instrument's current rating, state clearly that this must be verified against PACRA's (`pacra.com`) or VIS's (`vis.com.pk`) current published rating action/report, since ratings change via surveillance actions and any cached figure can be stale.
- If the question is about debt-instrument listing/eligibility data rather than rating methodology, route to `psx-debt-and-eligibility`.
- If the question is about the underlying debt instrument's legal structure (TFC vs. Sukuk) rather than its credit rating, route to `pakistan-corporate-debt-capital-markets` or `pakistan-sukuk-structuring-issuance`.

## Extraction Workflow

1. Identify whether the question is about rating-scale interpretation, methodology framework, or SECP's CRC licensing/oversight regime — these are related but distinct sub-topics.
2. Confirm which agency (PACRA or VIS) and which rating type (long-term entity, short-term, instrument, fund stability, REIT) is in scope, since scales and suffixes differ by rating type.
3. When explaining a rating notch, describe it in relative/ordinal terms (higher within the scale implies lower relative default likelihood) rather than asserting a specific probability-of-default number unless that figure is explicitly published in the agency's own methodology document for that scale.
4. Distinguish a rating outlook (multi-year directional view) from a rating watch (shorter-horizon, event-driven flag) when describing a rating action.
5. If a specific company/instrument rating is requested, flag that the answer requires a live check against the agency's current published rating and cannot be answered from static knowledge, since ratings are revised via ongoing surveillance.

## Technical Rules

- Do not present a credit rating as a guarantee of repayment or as equivalent to an audit opinion; it is a forward-looking, relative opinion on default likelihood based on the agency's published methodology.
- Keep issuer/entity ratings distinct from instrument ratings; an instrument can be rated differently from its issuer due to seniority, collateral, or structural features.
- Do not conflate PACRA's and VIS's rating scales as identical in every technical respect (e.g., specific suffix conventions for specialized products); note the specific agency when citing scale mechanics.
- Do not state a specific current rating for a named company/instrument without sourcing it to a specific, dated rating action from the agency's own website — ratings are revised periodically and a stale rating cited as current is a material misstatement in a finance context.
- Speculative-grade / investment-grade cutoffs and specific notch definitions should be sourced to the agency's own published rating-scale document rather than assumed to exactly mirror international agencies' conventions, even though the broad AAA-to-D structure is similar in spirit.

## Validation Checklist

- Confirm which agency (PACRA or VIS) and which scale type (entity, instrument, short-term, fund, REIT) the question concerns.
- Verify that any specific rating value cited is sourced to a current, dated rating action rather than presented as a static fact.
- Check whether the request is about rating methodology (this skill) versus PSX debt-instrument listing data (`psx-debt-and-eligibility`).
- Confirm outlook vs. watch terminology is used correctly when describing a rating action.

## Common Pitfalls

- Presenting a specific company's credit rating as current without verifying against the agency's live published rating report.
- Treating a credit rating as a guarantee of creditworthiness or a substitute for independent credit analysis.
- Confusing issuer/entity ratings with instrument-specific ratings, which can diverge due to structural features.
- Mixing PACRA and VIS scale conventions as if they were identical without checking the specific agency's own published scale document.
- Describing a rating outlook and a rating watch as the same thing when they signal different time horizons and triggers.

## Reference

- See [Pakistan Credit Rating Methodology Reference](references/pakistan-credit-rating-methodology.md) for scale structure, regulatory citations, and extraction notes.
