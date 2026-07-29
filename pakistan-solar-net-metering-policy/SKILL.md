---
name: pakistan-solar-net-metering-policy
description: Pakistan distributed/rooftop solar net-metering regulatory framework skill. Use when a task concerns NEPRA's Alternative and Renewable Energy (Net-Metering) Regulations, the net-metering vs. gross-metering distinction, DISCO-level interconnection/application process for rooftop solar, buy-back tariff mechanics, or AEDB's role in renewable-energy policy — rather than utility-scale generation tariffs or system-wide capacity planning.
---

# Pakistan Solar Net-Metering Policy

## Overview

Use this skill for questions about Pakistan's regulatory framework for small, distributed/rooftop solar (and other distributed renewable) generation connected to the distribution grid — the net-metering regime administered by NEPRA and implemented at the DISCO (distribution company) level, with AEDB (Alternative Energy Development Board) as the federal renewable-policy body. This is the consumer/prosumer-facing interconnection and buy-back layer, not utility-scale IPP tariff-setting or long-term capacity planning.

## Coverage

- **Legal basis**: NEPRA's Alternative and Renewable Energy (Net-Metering) Regulations (first notified 2015, subsequently amended) govern net-metering for consumers generating electricity from renewable sources (primarily solar PV, also small wind/hydro/biogas) up to a specified capacity threshold, for self-consumption with export of surplus to the grid.
- **Net-metering vs. gross-metering**: Net-metering nets a consumer's exported and imported units within a billing cycle, crediting/billing only the difference; gross-metering (introduced/discussed in later regulatory amendments and DISCO practice) instead measures and settles all generated (exported) units and all consumed (imported) units separately, typically at different rates — a materially different economic mechanism. Always identify which regime a source is describing before quoting a buy-back rate.
- **Interconnection process**: A consumer applies to their DISCO (or K-Electric in its franchise area) for a net-metering connection; the process typically involves technical feasibility/load study, installation of a bi-directional meter, an interconnection agreement, and inspection/commissioning sign-off before export is permitted. Capacity eligibility and required documentation are set by the NEPRA regulations and DISCO-specific implementation procedures (SOPs), which can vary somewhat by DISCO.
- **Buy-back tariff mechanics**: The rate at which exported units are credited/paid has been a recurring point of regulatory revision; NEPRA periodically determines or revises the net-metering buy-back rate (sometimes referenced against the DISCO's average purchase price or a specific approved rate). Do not assert a specific current buy-back rate without verification — this is a frequently revised figure (verify current figure).
- **AEDB's role**: AEDB (Alternative Energy Development Board), under the Ministry of Energy (Power Division), is Pakistan's federal focal body for renewable-energy policy promotion, project facilitation, and technical guidance (e.g., solar PV installation standards, technology certification), distinct from NEPRA's regulatory/licensing role and DISCOs' operational interconnection role.
- **Recent tariff-revision controversy context**: There has been public and industry debate in recent years over proposals to reduce the net-metering buy-back rate and/or shift consumers toward gross-metering, driven by DISCO/regulator concerns about revenue impact from rising rooftop-solar uptake; the specific status, rate levels, and implementation timeline of any such revision should be treated as fluid and verified against the current NEPRA notification rather than stated definitively (verify current status).

## Use This Skill For

- explaining the net-metering application/interconnection process at the DISCO level
- distinguishing net-metering from gross-metering and their different economic effects on a rooftop-solar consumer
- explaining NEPRA's and AEDB's respective roles in the distributed-solar regulatory ecosystem
- framing the buy-back tariff mechanism and why the specific rate needs current verification
- summarizing the policy debate around net-metering tariff revisions (with appropriate hedging on current status)

## When Not to Use This Skill

- For utility-scale IPP/solar-park generation tariff determinations — use `nepra-tariff-determinations`.
- For system-wide, multi-year generation capacity expansion planning (including utility-scale renewables in the future generation mix) — use `igcep-capacity-plan`.
- For realized, historical power-sector generation and capacity statistics — use `nepra-state-of-industry`.
- For general energy-sector narrative in the Pakistan Economic Survey — use `pes-infrastructure-digital-and-climate`.

## Routing Rules

- If the question is about a specific IPP's or solar park's power purchase tariff, route to `nepra-tariff-determinations` instead.
- If the question is about how much solar capacity is planned or forecast in the national generation mix, route to `igcep-capacity-plan` instead.
- If the question is about historical/realized generation output or DISCO-level loss/recovery performance broadly (not net-metering specifically), route to `nepra-state-of-industry`.
- If the question concerns environmental/climate policy framing around renewables rather than the regulatory mechanics, cross-check `pakistan-environment-climate-policy`.

## Extraction Workflow

1. Identify whether the question is about net-metering (netted billing) or gross-metering (separately settled import/export) — do not assume net-metering by default if the source specifies gross-metering.
2. Identify which entity's action is being described: NEPRA (regulation/rate approval), AEDB (policy/technical facilitation), or the DISCO (application processing/interconnection).
3. Note the capacity threshold and consumer category (residential/commercial/industrial) referenced, since eligibility criteria in the NEPRA regulations are capacity- and category-bound.
4. For any buy-back rate or tariff figure, flag it as subject to change and note the notification date/source rather than presenting it as a permanent number.
5. If describing the controversy around tariff revision, present it as a live/evolving policy debate, not a settled outcome, unless a specific NEPRA notification is being cited with its date.

## Technical Rules

- Do not use "net-metering" and "gross-metering" interchangeably; they have different billing mechanics and different implications for a consumer's economics.
- Do not state a specific current buy-back rate (PKR/kWh) without hedging — this figure is periodically revised by NEPRA (verify current figure).
- Distinguish NEPRA's regulatory/rate-setting role from AEDB's policy-facilitation role and the DISCO's operational interconnection role; they are three separate institutions with distinct mandates.
- Note that interconnection procedures and turnaround times can vary by DISCO even under a single national NEPRA regulation.

## Validation Checklist

- Confirm whether net-metering or gross-metering is the regime under discussion.
- Confirm which institution (NEPRA, AEDB, or DISCO) is the source of the specific claim being made.
- Flag any buy-back rate or capacity threshold as needing current verification against the latest NEPRA notification.
- Confirm the consumer category and capacity band the rule applies to.

## Common Pitfalls

- Treating net-metering and gross-metering as synonyms when they are economically distinct billing mechanisms.
- Quoting a specific buy-back tariff rate as fixed/permanent when it is a periodically revised regulatory parameter.
- Conflating AEDB's renewable-policy facilitation role with NEPRA's licensing/tariff-regulation authority.
- Presenting the net-metering tariff-revision debate as a finalized policy change without checking the current notification status.
- Confusing this distributed/rooftop-consumer framework with utility-scale IPP solar tariff determinations.

## Reference

- See [Pakistan Solar Net-Metering Policy Reference](references/pakistan-solar-net-metering-policy.md) for regulatory citations and extraction notes.
