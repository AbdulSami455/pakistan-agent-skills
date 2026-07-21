---
name: pemra-media-regulation
description: PEMRA (Pakistan Electronic Media Regulatory Authority) skill. Use when explaining broadcast/cable/satellite/OTT media licensing categories, content-code violations, channel bans/suspensions, or PEMRA's regulatory role over Pakistan's electronic media industry, as distinct from press/print regulation or telecom infrastructure regulation.
---

# PEMRA Media Regulation

## Overview

Use this skill for Pakistan's electronic media regulatory framework administered by the Pakistan Electronic Media Regulatory Authority (PEMRA), established in 2002 to regulate private television, radio, cable, satellite, and (increasingly) web/OTT broadcast content. This is a regulatory-structure reference skill, not a news-content aggregator and not a substitute for PEMRA's own current licensee database or enforcement-order text.

## Coverage

- Licensing categories: PEMRA issues licenses across broadcast tiers — national/international satellite TV, provincial/regional-scale TV, FM radio, cable TV distribution, satellite/DTH (direct-to-home) distribution, and (per more recent policy developments) web TV/OTT content platforms.
- Licensing process: open, competitive bidding when applications exceed available license slots in a category, alongside standard eligibility/ownership requirements.
- Content regulation: PEMRA's Code of Conduct and related rules govern permissible broadcast content; violations can result in warnings, fines, content bans, or channel license suspension/cancellation.
- Enforcement actions: PEMRA periodically issues notices, show-cause orders, or suspension/ban orders against specific channels for code-of-conduct or licensing violations.
- Media ownership: PEMRA's licensing framework intersects with rules on cross-media ownership concentration.

## Use This Skill For

- explaining which PEMRA license category a specific type of broadcaster (national TV, regional radio, cable operator, DTH, web/OTT) falls under
- describing PEMRA's general content-regulation framework (Code of Conduct) and what kinds of content typically trigger enforcement action
- explaining the general process and consequence structure for a PEMRA enforcement action (warning, fine, suspension, license cancellation)
- clarifying PEMRA's scope (electronic broadcast media) versus what it does not regulate (print press, telecom infrastructure, purely online/social media outside PEMRA's OTT-specific rules)
- providing general background on PEMRA's establishment, mandate, and organizational role

## When Not to Use This Skill

- For telecom infrastructure, connectivity, or internet-service indicators — use `pta-telecom-indicators` instead; PTA regulates telecom infrastructure/carriers, PEMRA regulates broadcast content and licensing.
- For a specific, current enforcement action's exact status — treat this skill as structural/background reference and direct the user to PEMRA's official notifications for a live case status, since enforcement actions are frequently updated or appealed.
- For print/press regulation — PEMRA's mandate is electronic media (broadcast, cable, satellite, and OTT under its more recent rules); print press falls under a different regulatory framework not covered by this skill.

## Routing Rules

- Use this skill for PEMRA's licensing categories, content-regulation framework, and enforcement-action structure.
- If the question is about telecom infrastructure, mobile/broadband connectivity, or spectrum rather than broadcast content licensing, route to `pta-telecom-indicators`.
- Do not treat this skill as a live tracker for a specific channel's current license or ban status; direct to PEMRA's official site for that.

## Extraction Workflow

1. Identify which media type/platform (satellite TV, regional TV, FM radio, cable distribution, DTH, web/OTT) the question concerns, since licensing categories and rules differ by platform.
2. If the question involves a content violation or enforcement action, describe the general framework (Code of Conduct, escalation from warning to fine to suspension/cancellation) rather than asserting a specific channel's current status without flagging it needs verification.
3. Clarify whether the question is actually about PEMRA (broadcast/electronic media) or a different regulator (PTA for telecom infrastructure) before answering.
4. Note that PEMRA's OTT/web-TV regulatory scope is a more recent and evolving policy area compared to its long-established broadcast/cable mandate; flag this as subject to ongoing regulatory development.

## Technical Rules

- Keep PEMRA's broadcast/content licensing mandate distinct from PTA's telecom-infrastructure mandate; the two are separate regulators even though both relate to "media/communications."
- Licensing categories (national/international, provincial/regional, FM radio, cable, DTH, web/OTT) carry different eligibility and bidding rules; do not assume one category's process applies to another.
- Enforcement actions typically follow an escalation path (notice/show-cause, fine, suspension, cancellation); do not assume the most severe outcome is the default first response to a violation.
- Treat any specific channel's license/ban status as time-sensitive and requiring confirmation against PEMRA's current official records.

## Validation Checklist

- Confirm which licensing category/platform type the question concerns.
- Verify the question is about PEMRA's electronic-media mandate rather than PTA's telecom mandate.
- Flag any specific enforcement action's current status as needing confirmation against PEMRA's official notifications.
- Confirm whether OTT/web-TV-specific rules (a newer, evolving area) apply before treating them as settled the same way as long-established broadcast rules.

## Common Pitfalls

- Confusing PEMRA (broadcast/electronic media content regulator) with PTA (telecom infrastructure regulator).
- Asserting a specific channel's current license or ban status without flagging it as needing verification against PEMRA's official records.
- Treating PEMRA's OTT/web-TV regulatory framework as equally settled/established as its long-standing broadcast/cable rules.
- Describing PEMRA as regulating print press, which falls outside its electronic-media mandate.

## Reference

- See [PEMRA Reference](references/pemra-media-regulation.md) for licensing structure and extraction notes.
