---
name: pemra-broadcast-licensing-framework
description: PEMRA broadcast licensing mechanics skill. Use when a task needs the specific licensing process detail under the PEMRA Ordinance 2002 — license category eligibility/fee/term structure, landing rights authorization for foreign satellite channels, the formal Code of Conduct penalty escalation sequence with statutory basis, and cable TV/DTH distribution licensing — as distinct from PEMRA's general content-regulation narrative already covered elsewhere.
---

# PEMRA Broadcast Licensing Framework

## Overview

Use this skill for the specific licensing-process and penalty-framework mechanics administered by the Pakistan Electronic Media Regulatory Authority (PEMRA) under the **PEMRA Ordinance, 2002** (formally the Pakistan Electronic Media Regulatory Authority Ordinance, 2002, as amended). This skill is deliberately scoped narrower than `pemra-media-regulation`, which already covers PEMRA's general licensing-category overview, content-regulation framework, and enforcement narrative at a structural level. This skill goes one layer deeper into licensing mechanics: how a license category's eligibility/fee/term structure works, how landing rights for foreign satellite channels are authorized, the statutory penalty-escalation sequence under the Ordinance, and cable TV/DTH distribution-specific licensing conditions.

## Coverage

- **Legal basis**: The PEMRA Ordinance, 2002, as amended (including amendments broadening PEMRA's scope over time), is the founding statute. PEMRA Rules and PEMRA's own regulations (e.g., licensing regulations for specific categories) are issued under the Ordinance's rule-making powers and govern the detailed licensing process.
- **License category mechanics**: Beyond simply naming categories (satellite TV, FM radio, landing rights, cable TV/DTH — already listed at a structural level in `pemra-media-regulation`), this skill covers the eligibility criteria (ownership caps, citizenship/incorporation requirements for licensees), license term length, renewal process, and fee structure that differ by category under PEMRA's licensing regulations.
- **Landing rights authorization**: PEMRA separately authorizes "landing rights" permissions allowing foreign satellite TV channels to be legally retransmitted/distributed within Pakistan via licensed cable/DTH/IPTV operators — a distinct authorization from a domestic broadcast license, since the foreign channel itself is not PEMRA-licensed as a Pakistani broadcaster but is instead cleared for local distribution.
- **Cable TV/DTH distribution licensing**: cable television distribution and Direct-to-Home (DTH) satellite distribution are separately licensed distribution-layer categories (as opposed to content-origination licenses for TV/radio channels), each with their own technical/coverage-area conditions and must-carry-type obligations that can apply to distributors.
- **Penalty/enforcement escalation under the Ordinance**: the PEMRA Ordinance and Code of Conduct rules set out a formal escalation sequence for content/licensing violations — notice/show-cause, monetary fine, suspension of license/transmission, and (as the most severe step) license revocation/cancellation — with procedural steps (show-cause opportunity, Authority/Council hearing) required before the more severe steps under the statutory scheme.

## Use This Skill For

- explaining the eligibility, term, and fee-structure mechanics for a specific PEMRA license category
- explaining what "landing rights" authorization is and how it differs from a domestic broadcast license
- distinguishing cable TV distribution licensing from DTH distribution licensing as separate distribution-layer categories
- walking through the formal statutory penalty-escalation sequence (show-cause, fine, suspension, revocation) under the PEMRA Ordinance
- explaining procedural requirements (e.g., show-cause opportunity) that must precede PEMRA's more severe enforcement actions

## When Not to Use This Skill

- For a general overview of PEMRA's mandate, license-category list at a structural level, or its Code of Conduct content-regulation framework — use `pemra-media-regulation`, which already covers that ground; this skill assumes that context and goes deeper into licensing-process and penalty-statute mechanics specifically.
- For a specific channel's current license or ban status — neither this skill nor `pemra-media-regulation` is a live tracker; direct to PEMRA's official notifications.
- For telecom infrastructure/carriage licensing (LDI, LL/WLL, Cellular Mobile) — use `pta-numbering-licensing-framework`; PEMRA licenses broadcast content/distribution, PTA licenses telecom carriage infrastructure.
- For print/press regulation — outside PEMRA's electronic-media mandate entirely.

## Routing Rules

- Start with `pemra-media-regulation` for general orientation (what PEMRA is, its license-category list, its content-regulation framework at a structural level); use this skill when the task specifically needs eligibility/fee/term mechanics, landing rights specifics, cable/DTH distribution-layer distinctions, or the statutory penalty-escalation sequence with its procedural steps.
- If the question is about telecom carriage licensing rather than broadcast content/distribution licensing, route to `pta-numbering-licensing-framework`.
- If the question is about a live, current enforcement action's status, note that both this skill and `pemra-media-regulation` are structural/background references, not live trackers — direct to PEMRA's official site.

## Extraction Workflow

1. Confirm the question needs licensing-process depth (eligibility, fee, term, landing rights, distribution-layer distinctions, or penalty-statute procedure) rather than general PEMRA orientation — if it's the latter, route to `pemra-media-regulation` first.
2. Identify which license category or authorization type is relevant (broadcast origination license vs. landing rights vs. cable/DTH distribution license), since these are legally distinct authorizations with different eligibility bases.
3. For penalty/enforcement questions, walk through the statutory escalation sequence (notice/show-cause → fine → suspension → revocation) and note the procedural step (show-cause opportunity, hearing) required before the more severe steps, rather than presenting the harshest penalty as an automatic first response.
4. For landing rights questions, keep clear that the foreign channel is being authorized for local distribution/retransmission by a licensed Pakistani distributor, not being issued a Pakistani broadcast license itself.
5. Flag any specific current fee amount, license term length, or ownership-cap percentage as needing verification against PEMRA's current licensing regulations, since these are subject to periodic revision.

## Technical Rules

- Do not conflate a domestic broadcast license (satellite TV/FM radio origination) with landing rights authorization (foreign channel local-distribution clearance) — they are legally distinct instruments.
- Cable TV and DTH are separate distribution-layer license categories; do not treat one as a subset or synonym of the other.
- The statutory penalty framework under the PEMRA Ordinance follows an escalation sequence with procedural safeguards (show-cause/hearing) preceding suspension or revocation; do not present license cancellation as PEMRA's default or immediate response to a first-instance violation.
- Do not state a specific current license fee, term length, or foreign-ownership cap percentage without flagging it as needing verification against PEMRA's current regulations.
- This skill assumes `pemra-media-regulation`'s general PEMRA orientation as background; do not duplicate that skill's structural content here — go directly to the mechanics layer.

## Validation Checklist

- Confirm the task needs licensing-mechanics depth rather than general PEMRA orientation (route the latter to `pemra-media-regulation`).
- Confirm which specific authorization type (broadcast license, landing rights, cable, DTH) is relevant before describing eligibility or conditions.
- Confirm any penalty-escalation description includes the procedural show-cause/hearing step before suspension or revocation.
- Flag specific fee, term, or ownership-cap figures as needing current verification.
- Confirm the question is not actually a telecom-carriage licensing question (route to `pta-numbering-licensing-framework`).

## Common Pitfalls

- Duplicating `pemra-media-regulation`'s general content and license-category overview instead of going to licensing-mechanics depth.
- Treating landing rights as equivalent to a domestic broadcast license for the foreign channel.
- Conflating cable TV and DTH as the same distribution category.
- Presenting license revocation as an automatic or immediate PEMRA response rather than the final step of a statutory escalation sequence with procedural safeguards.
- Citing a specific current fee, term, or ownership-cap figure without a verification flag.

## Reference

- See [PEMRA Broadcast Licensing Framework Reference](references/pemra-broadcast-licensing-framework.md) for license-category eligibility structure, landing rights mechanics, and the statutory penalty-escalation sequence.
