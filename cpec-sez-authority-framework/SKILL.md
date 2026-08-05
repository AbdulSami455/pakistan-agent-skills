---
name: cpec-sez-authority-framework
description: CPEC and Special Economic Zones institutional/legal framework skill. Use when explaining the China-Pakistan Economic Corridor's governance structure under the CPEC Authority Act 2022, the Special Economic Zones Act 2012, one-window facilitation, SEZ fiscal-incentive structure, major SEZ projects, or the Joint Cooperation Committee — as distinct from port operations data or general federal development-spending figures.
---

# CPEC and SEZ Authority Framework

## Overview

Use this skill for the institutional and legal architecture behind the China-Pakistan Economic Corridor (CPEC) and Pakistan's Special Economic Zones (SEZ) regime: which body governs CPEC decision-making, how an SEZ is legally established and incentivized, and how the two frameworks (CPEC as a bilateral cooperation umbrella, SEZs as a domestic industrial-zone legal category) relate to and reinforce each other. This is a framework/governance skill, not a source of live cargo-throughput or development-budget figures.

## Coverage

- **CPEC as bilateral framework**: CPEC is a long-term bilateral economic cooperation framework between Pakistan and China, encompassing energy, infrastructure (including road/rail corridors and Gwadar Port development), and industrial cooperation (including SEZs), guided at the government-to-government level by a **Joint Cooperation Committee (JCC)** — the apex bilateral coordination body co-chaired by senior officials from both countries (on the Pakistani side, historically the Ministry of Planning, Development & Special Initiatives), supported by sector-specific Joint Working Groups (JWGs) covering areas such as energy, transport infrastructure, Gwadar, and industrial cooperation/SEZs.
- **CPEC Authority Act, 2022**: an Act of the Parliament of Pakistan placing the CPEC Authority (originally created by executive/ordinance action and subsequently given statutory backing) on a firmer legal footing, with a mandate to coordinate, plan, and facilitate implementation of CPEC projects across federal ministries, provincial governments, and the private sector — treat the precise institutional history (ordinance-to-Act transition, any subsequent restructuring of the Authority's status or reporting line) as needing verification against the current Gazette text, since CPEC institutional arrangements have been adjusted more than once.
- **Special Economic Zones Act, 2012**: the principal domestic legal framework for establishing SEZs in Pakistan, letting federal and provincial governments jointly declare an area an SEZ, and establishing SEZ Authorities (with both federal and provincial-level SEZ Authority/board structures) responsible for zone development, developer/enterprise approval, and regulatory facilitation within a zone. The Act empowers "one-window facilitation" — a single-point regulatory interface intended to reduce the number of separate approvals a zone developer or zone enterprise must otherwise obtain from multiple federal/provincial agencies.
- **SEZ fiscal incentives**: SEZ developers and zone enterprises are typically eligible for a package of fiscal incentives under the SEZ Act framework and associated tax-law provisions — commonly including exemptions from customs duties and taxes on capital goods/machinery imported for zone development or set-up, and income-tax holidays/exemptions for a specified initial period for both zone developers and zone enterprises — but the precise current exemption periods, eligible categories, and any sunset/rollback of specific incentives should be verified against the current Income Tax Ordinance provisions and SEZ Act rules in force, since SEZ fiscal incentives have been subject to periodic review, phase-out debate, and IMF-programme-linked scrutiny.
- **Major SEZ examples**: several SEZs have been publicly associated with the CPEC industrial-cooperation pillar, commonly cited examples include Rashakai Special Economic Zone (Khyber Pakhtunkhwa, along the M-1 motorway corridor), Dhabeji Special Economic Zone (Sindh, near Karachi/Thatta), and Allama Iqbal Industrial City (Faisalabad, Punjab) — these are the most frequently referenced "early harvest"/priority SEZs in CPEC industrial-cooperation material; treat the current development/operational status of any specific zone (which enterprises have actually moved in, occupancy levels, completion of infrastructure) as needing verification against current reporting, since these projects have experienced delays and phased progress relative to original announcements.
- **CPEC phases**: CPEC is commonly described in Pakistani and Chinese official communication as having moved from an initial phase emphasizing energy and infrastructure projects toward a subsequent phase emphasizing industrial cooperation, SEZs, agriculture, and socioeconomic development — treat specific phase-naming and dating as a general framing rather than a precise, universally fixed periodization.

## Use This Skill For

- explaining the CPEC Authority's statutory mandate under the CPEC Authority Act 2022 and its coordinating role across federal/provincial/private-sector CPEC implementation
- explaining how the Joint Cooperation Committee and its Joint Working Groups structure bilateral CPEC decision-making
- explaining how an SEZ is legally established under the SEZ Act 2012 and what "one-window facilitation" means in practice
- describing the general structure of SEZ fiscal incentives (customs/tax exemptions for developers and zone enterprises) while flagging precise current rates/periods for verification
- identifying commonly cited CPEC-linked SEZs (Rashakai, Dhabeji, Allama Iqbal Industrial City) while flagging current operational status as needing verification
- distinguishing CPEC (bilateral cooperation umbrella, broader than SEZs) from the SEZ Act framework (a general domestic legal tool usable for any SEZ, not exclusively CPEC-linked zones)

## When Not to Use This Skill

- For Gwadar Port vessel arrival/berthing and cargo-throughput data, use `gwadar-port-cargo-reports` — this skill covers CPEC/SEZ institutional and legal framework, not port operations statistics.
- For general federal development-project allocations and expenditure (PSDP), use `psdp-federal-development-programme` — CPEC projects may appear within PSDP figures, but this skill does not itself host budget/expenditure data.
- For SECP company incorporation of an enterprise setting up within an SEZ, use `secp-company-registry`.
- For FBR customs-duty schedules generally (beyond SEZ-specific exemptions), use `fbr-customs-tariff`.

## Routing Rules

- If the question is about CPEC's bilateral governance/coordination structure, apply the Joint Cooperation Committee/CPEC Authority Act 2022 framework.
- If the question is about how a zone becomes a legally recognized SEZ, or what incentives a zone enterprise receives, apply the SEZ Act 2012 framework — note that SEZs are a general legal category usable beyond CPEC-linked zones specifically, even though CPEC industrial cooperation is a major driver of SEZ policy attention.
- If the question needs actual cargo/vessel throughput at Gwadar, route to `gwadar-port-cargo-reports`.
- If the question needs actual PSDP allocation/expenditure figures for a CPEC-linked project, route to `psdp-federal-development-programme`.
- If the question asks about a specific SEZ's current occupancy, completion status, or investment figures, flag this as needing current verification rather than restating an early-announcement figure as current fact.
- If the question concerns a specific tax exemption rate or duration for SEZ enterprises, flag for verification against the current Income Tax Ordinance/SEZ Act rules rather than asserting a fixed figure.

## Extraction Workflow

1. Determine whether the question is about CPEC's bilateral governance (JCC/JWG/CPEC Authority) or about the domestic SEZ legal mechanism (SEZ Act 2012) — these are related but distinct layers.
2. If about CPEC Authority, identify its statutory basis (CPEC Authority Act 2022) and its coordinating (not executing) mandate across federal ministries, provinces, and the private sector.
3. If about an SEZ, identify the applicable SEZ Authority (federal or provincial) and confirm whether the question concerns zone-developer incentives or zone-enterprise incentives, since incentive structures can differ between the two.
4. If a specific SEZ (Rashakai, Dhabeji, Allama Iqbal Industrial City, or another) is named, note its general location/province and CPEC-industrial-cooperation association, while flagging current development/operational status as needing verification.
5. If fiscal incentives are discussed, separate customs/duty exemptions on imported capital goods from income-tax holiday provisions, and flag exact current rates/periods for verification.
6. Note which CPEC phase framing (energy/infrastructure-first vs. subsequent industrial-cooperation/SEZ emphasis) is relevant to the question, without asserting a rigid universal date boundary between phases.

## Technical Rules

- CPEC is a bilateral cooperation framework broader than SEZs; the SEZ Act 2012 is a general domestic legal tool that predates and extends beyond CPEC-specific zones — do not describe all Pakistani SEZs as CPEC projects, or CPEC as consisting only of SEZs.
- The CPEC Authority's statutory mandate under the CPEC Authority Act 2022 is coordination and facilitation across federal/provincial/private-sector actors, not direct project execution — do not describe the Authority as itself building or operating individual CPEC projects.
- SEZ fiscal incentives commonly distinguish developer-level incentives (for the entity building zone infrastructure) from enterprise-level incentives (for firms operating within the zone) — do not conflate the two when describing exemption eligibility.
- Do not state a precise, current income-tax holiday duration or customs-exemption scope for SEZs without flagging it as needing verification against the current Income Tax Ordinance and SEZ Act rules, since these have been subject to periodic review and phase-out discussion (including in IMF-programme contexts).
- Do not assert a specific SEZ's current occupancy, completion percentage, or investment inflow as settled fact without flagging it for verification, given documented delays across CPEC-linked SEZ projects relative to original timelines.

## Validation Checklist

- Confirm whether the question is about CPEC bilateral governance or the domestic SEZ legal framework before answering.
- Confirm the CPEC Authority's role is described as coordinating, not executing, projects directly.
- Confirm developer-level and enterprise-level SEZ incentives are not conflated.
- Flag any specific fiscal-incentive rate/duration or SEZ operational-status claim as needing current verification.
- Distinguish this skill's institutional/legal scope from `gwadar-port-cargo-reports` (operations data) and `psdp-federal-development-programme` (budget data).

## Common Pitfalls

- Treating CPEC and the SEZ Act framework as the same thing, rather than a bilateral cooperation umbrella and a general domestic legal tool that intersect but are not coextensive.
- Describing the CPEC Authority as executing projects itself rather than coordinating across implementing ministries/provinces/private parties.
- Citing a specific SEZ's current investment or occupancy status as settled fact without verification, given known delays across these projects.
- Asserting a precise, unhedged tax-holiday duration or customs-exemption scope for SEZs without flagging it for verification against current law.
- Conflating zone-developer incentives with zone-enterprise incentives.

## Reference

- See [CPEC and SEZ Authority Framework Reference](references/cpec-sez-authority-framework.md) for statutory basis, institutional structure, and extraction notes.
