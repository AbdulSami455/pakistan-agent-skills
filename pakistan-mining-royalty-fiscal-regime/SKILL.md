---
name: pakistan-mining-royalty-fiscal-regime
description: Pakistan mineral royalty and mining fiscal-regime skill. Use when a task concerns provincial mineral royalty rates, mining lease fiscal terms (royalty, dead-rent, surface rent, provincial mining taxes/cesses), the Reko Diq project's fiscal-terms structure, provincial mining fiscal frameworks (Balochistan, Sindh, Punjab, KP), or the National Mineral Policy's fiscal provisions — rather than the geology of mineral deposits or the licensing/permitting process itself.
---

# Pakistan Mining Royalty and Fiscal Regime

## Overview

Use this skill for questions about the money side of mineral extraction in Pakistan — royalty rates, dead-rent, surface rent, provincial mining cesses/taxes, and the fiscal-terms architecture of specific projects (notably Reko Diq) — as distinct from the geological characterization of deposits and from the licensing/permitting procedure for obtaining a mining concession. Mining is a provincial subject under the Constitution (Fourth Schedule/post-18th Amendment devolution), so fiscal terms are set principally at the provincial level under each province's mining concession rules, with a few nationally significant projects (Reko Diq) governed by dedicated agreements/legislation layered on top of the provincial framework.

## Coverage

- **Constitutional basis**: Mines and minerals (other than oil and natural gas) are a provincial subject; each province administers its own mining concession rules (e.g., Balochistan Mineral Rules, Sindh Mining Concession Rules, Punjab Mineral Rules, Khyber Pakhtunkhwa Mineral Rules) which set out royalty rates, dead-rent, and surface-rent schedules for mineral categories under that province's jurisdiction.
- **Standard fiscal instruments**: Provincial mining fiscal regimes typically layer (a) royalty — a per-tonne or ad valorem charge on mineral extracted/sold, varying by mineral type and province; (b) dead-rent/rent — a fixed periodic payment on the leased area regardless of production, often creditable against royalty; (c) surface rent — compensation to landowners/government for surface use; and (d) other provincial levies (e.g., excise duty on minerals in some provinces, labour/environmental cesses). Exact rates vary by province and mineral category and are revised periodically — treat specific PKR/tonne or percentage figures as needing current verification (verify current figure) rather than stating a fixed number from memory.
- **Reko Diq fiscal structure**: The Reko Diq copper-gold project in Balochistan operates under a distinct legal/fiscal architecture following the 2022 reconstitution agreement among the Government of Balochistan, Government of Pakistan, and Barrick Gold (with GoB/GoP state-owned entities holding an equity stake alongside Barrick), underpinned by dedicated legislative and foreign-investment-protection arrangements (including reconstitution/framework legislation at the federal and provincial level). The precise royalty rate, government equity percentage, profit-sharing mechanics, and any special fiscal stabilization terms for Reko Diq should be treated as project-specific and stated only at a high-level structural description unless a figure can be confidently sourced — hedge on exact percentages and rupee/dollar figures (verify current figure).
- **National Mineral Policy**: Pakistan's National Mineral Policy (administered at the federal level with provincial implementation) sets broad policy objectives — attracting investment, harmonizing provincial mining rules, streamlining licensing, and improving fiscal competitiveness relative to regional mining jurisdictions — and has been a reference point for provincial rule revisions, though it does not itself override provincial constitutional authority over mining fiscal terms.
- **Federal tax overlay**: Beyond provincial royalty/rent, mining companies are also subject to federal income tax (FBR) and may access mineral-sector-specific tax incentives (e.g., exemptions or reduced rates under the Income Tax Ordinance for exploration/mining phases in some cases) layered on top of the provincial royalty regime — these are two distinct fiscal layers and should not be conflated.

## Use This Skill For

- explaining the structure of royalty, dead-rent, and surface-rent instruments in Pakistani provincial mining fiscal regimes
- describing which level of government (provincial vs. federal) sets which fiscal charge on a mining project
- summarizing the high-level fiscal-terms architecture of the Reko Diq project (with appropriate hedging on exact figures)
- explaining the National Mineral Policy's role in fiscal harmonization across provinces
- distinguishing royalty/fiscal-regime questions from mineral geology or licensing-procedure questions

## When Not to Use This Skill

- For the geology, mineral occurrence, or resource-belt characterization of a deposit — use `pakistan-geology-mineral-resources`.
- For the mining lease/license application and permitting procedure itself (application steps, exploration-to-mining-lease conversion process, required approvals) — treat as out of scope for this skill; no dedicated licensing-process skill currently exists in this repository, so flag that gap rather than fabricating licensing-procedure detail here.
- For general provincial development statistics unrelated to mining fiscal terms — use the relevant province's `*-development-statistics` skill.
- For federal income tax rules of general application (not mining-specific royalty) — use `fbr-individual-tax-filing` or related FBR skills as appropriate.

## Routing Rules

- If the question is about what minerals exist where, deposit grades, or geological formations, route to `pakistan-geology-mineral-resources` instead.
- If the question is purely about federal corporate/income tax mechanics with no mining-royalty dimension, route to the relevant FBR skill instead.
- If the question is about a specific province's general development statistics rather than mining fiscal terms, route to that province's development-statistics skill.
- If the question concerns Reko Diq's geology or resource estimate rather than its fiscal/ownership structure, cross-check `pakistan-geology-mineral-resources`.

## Extraction Workflow

1. Identify which province's mining fiscal rules are relevant (Balochistan, Sindh, Punjab, or KP) — provincial mineral rules are not uniform, and a royalty rate from one province should not be assumed to apply in another.
2. Distinguish the fiscal instrument being asked about: royalty (production-linked), dead-rent (area-linked, often creditable against royalty), surface rent (landowner compensation), or a provincial excise/cess.
3. For Reko Diq specifically, describe the structural framework (GoB/GoP state-entity equity alongside Barrick, dedicated reconstitution agreement/legislation) before attempting any specific percentage or dollar figure, and hedge numeric specifics explicitly.
4. Separate provincial royalty/rent obligations from the federal income-tax layer; do not present them as a single combined "tax rate."
5. Flag National Mineral Policy statements as policy-objective/harmonization language, not as a directly binding fiscal rate schedule (rates remain set at the provincial rule level).

## Technical Rules

- Do not quote a specific royalty percentage or PKR/tonne rate for any mineral or province without hedging that current figures should be verified — provincial mineral rules are amended periodically.
- Do not conflate dead-rent (a fixed area-based charge, often adjustable against royalty due) with royalty itself (a production/value-based charge); they are distinct instruments.
- Do not present the Reko Diq fiscal structure with precise equity percentages, royalty rates, or profit-split figures unless confident of the specific sourced number; describe the structure qualitatively and hedge the numbers.
- Do not treat the National Mineral Policy as having superseded provincial constitutional authority over mining fiscal terms; provinces retain the rule-making power for royalty/rent under the post-18th Amendment framework.
- Keep provincial royalty/rent obligations analytically separate from federal income tax treatment of mining companies.

## Validation Checklist

- Confirm which province's mining fiscal rules the question concerns before citing any rate.
- Confirm which fiscal instrument (royalty, dead-rent, surface rent, federal tax) is actually being asked about.
- Flag any specific rate, percentage, or monetary figure — including for Reko Diq — as needing current-source verification.
- Confirm the question is about fiscal terms, not geology (route to `pakistan-geology-mineral-resources`) or general licensing procedure (flag as a coverage gap).

## Common Pitfalls

- Assuming a single national mineral royalty rate exists when rates are set provincially and vary by mineral and jurisdiction.
- Conflating dead-rent with royalty, or provincial royalty with federal income tax, as if they were one combined figure.
- Stating precise Reko Diq equity percentages, royalty rates, or profit-sharing figures without hedging, when these are project-specific negotiated/legislated terms subject to change and verification.
- Treating the National Mineral Policy as a binding, uniform royalty schedule rather than a federal policy-harmonization framework operating alongside provincial rule-making authority.
- Answering a geology or licensing-procedure question with this skill instead of routing to the correct skill or flagging the coverage gap.

## Reference

- See [Pakistan Mining Royalty and Fiscal Regime Reference](references/pakistan-mining-royalty-fiscal-regime.md) for provincial rule citations, Reko Diq structural background, and extraction notes.
