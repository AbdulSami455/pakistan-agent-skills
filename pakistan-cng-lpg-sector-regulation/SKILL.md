---
name: pakistan-cng-lpg-sector-regulation
description: Pakistan CNG and LPG sector regulation skill. Use when a task concerns OGRA's CNG station licensing, LPG marketing company licensing, CNG price-fixing/pricing-formula mechanics, gas load-shedding/curtailment policy affecting the CNG sector, or the natural-gas-versus-LPG regulatory distinction — rather than broader OGRA petroleum industry statistics or upstream oil/gas production data.
---

# Pakistan CNG and LPG Sector Regulation

## Overview

Use this skill for questions about the regulatory mechanics specific to Compressed Natural Gas (CNG) and Liquefied Petroleum Gas (LPG) as retail/consumer fuel sectors in Pakistan — station and marketing-company licensing, pricing mechanisms, and gas-curtailment policy affecting CNG — as distinct from OGRA's broader petroleum-industry statistical reporting (production/consumption/infrastructure) and from natural gas transmission/distribution utility regulation generally.

## Coverage

- **Regulatory authority**: OGRA (Oil and Gas Regulatory Authority), under the OGRA Ordinance, 2002, regulates midstream/downstream petroleum activities including CNG station licensing and LPG marketing/storage/distribution licensing, alongside its broader natural-gas tariff and petroleum-pricing mandate.
- **Natural gas (piped) vs. LPG (cylinder-based) distinction**: Natural gas reaches CNG stations and piped domestic/commercial/industrial consumers via the two state-run gas utilities' transmission and distribution networks — SNGPL (Sui Northern Gas Pipelines Limited, serving Punjab/KP/Islamabad) and SSGC (Sui Southern Gas Company, serving Sindh/Balochistan) — under their own OGRA-regulated gas tariffs and gas-allocation policy. LPG, by contrast, is not pipeline-distributed at consumer scale in most of Pakistan; it is produced domestically (as a by-product of gas processing/refining) and imported, then marketed in cylinders (or, for some commercial/industrial use, bulk/auto-gas) by licensed LPG marketing companies, largely outside the SNGPL/SSGC piped network. Always keep these two supply chains and their separate regulatory tracks distinct.
- **CNG station licensing**: OGRA licenses CNG stations (dealer/retail outlet licenses) and administers technical/safety standards for CNG dispensing, storage, and cylinder-testing at the retail level, in addition to sanctioning gas supply/connection to a station from the relevant gas utility (SNGPL/SSGC).
- **LPG marketing company licensing**: OGRA licenses LPG marketing companies (LPGMCs), covering production/import sourcing, storage/bottling-plant operation, and distribution/marketing of cylinder LPG, with separate licensing tracks for LPG production/extraction (at gas-processing facilities) versus marketing/distribution.
- **CNG price-fixing mechanism history**: For a substantial period, CNG retail prices were administratively fixed/notified by OGRA (often referenced against a formula linked to petrol/HSD prices or gas cost-of-service), a practice that has evolved over time toward greater price deregulation for CNG in some respects; the current pricing mechanism (fully deregulated vs. formula-administered) should be verified rather than assumed static, given the sector's regulatory history of shifting approaches (verify current mechanism).
- **Gas load-shedding/curtailment policy for CNG**: Because CNG competes with higher-priority consumers (domestic, power, fertilizer, industry) for a constrained indigenous natural gas supply, government/OGRA gas-load-management policy has historically subjected the CNG sector to seasonal curtailment (e.g., reduced supply days or hours, particularly in winter when domestic heating demand peaks), governed by a gas-allocation priority order set by the government (historically domestic and export-industry/fertilizer given higher priority than CNG). Specific current curtailment schedules or priority-order rules should be treated as subject to seasonal/policy revision (verify current schedule).

## Use This Skill For

- explaining OGRA's CNG station licensing and safety/technical regulatory role
- explaining LPG marketing company licensing structure (production/import, storage, marketing tracks)
- describing the history and structure of CNG price-fixing/deregulation mechanisms
- explaining gas load-shedding/curtailment policy as it affects the CNG sector specifically
- distinguishing the piped-natural-gas regulatory track (SNGPL/SSGC) from the cylinder-based LPG regulatory track

## When Not to Use This Skill

- For broader OGRA petroleum-industry statistics (crude/gas production volumes, refinery throughput, general product consumption tables) — use `ogra-petroleum-industry-reports`.
- For NEPRA-regulated electricity tariffs or power-sector matters — use `nepra-tariff-determinations` or `nepra-state-of-industry`.
- For upstream oil/gas exploration and production licensing (E&P concessions) — treat as outside this skill's downstream/retail-sector scope; no dedicated E&P licensing skill currently exists in this repository.
- For customs duty/import-tariff treatment of LPG imports specifically (as opposed to OGRA's marketing-license regulation) — use `fbr-customs-tariff`.

## Routing Rules

- If the question needs production, consumption, or infrastructure statistics for the broader petroleum sector rather than CNG/LPG-specific licensing or pricing mechanics, route to `ogra-petroleum-industry-reports`.
- If the question is about natural gas tariff determinations for SNGPL/SSGC generally (not the CNG-station-specific angle), note that as adjacent OGRA tariff activity but keep this skill's focus on the CNG/LPG retail-regulatory mechanics.
- If the question is about electricity load-shedding rather than gas curtailment, route to `nepra-state-of-industry` instead.
- If the question is purely about customs/import duty rates on LPG cargoes, route to `fbr-customs-tariff`.

## Extraction Workflow

1. Identify whether the question concerns CNG (piped-gas-fed, vehicle dispensing) or LPG (cylinder/bulk, off-pipeline) — the regulatory and supply-chain mechanics differ substantially.
2. For CNG, identify whether the question is about station licensing/safety regulation, pricing mechanism, or supply curtailment — these are three distinct regulatory threads.
3. For LPG, identify whether the question concerns the production/import-sourcing license, the storage/bottling-plant license, or the marketing/distribution license, since OGRA's LPG licensing has separate tracks for each stage.
4. When discussing gas curtailment, identify the priority-order context (domestic vs. CNG vs. industry vs. power/fertilizer) rather than presenting CNG curtailment as an isolated, unexplained restriction.
5. Flag current pricing-mechanism status (administered vs. deregulated) and current curtailment schedules as needing verification given their history of policy revision.

## Technical Rules

- Do not conflate CNG (compressed natural gas, drawn from the piped SNGPL/SSGC network) with LPG (liquefied petroleum gas, cylinder/bulk-distributed, largely off-pipeline); they are chemically, logistically, and regulatorily distinct fuels.
- Do not attribute LPG cylinder supply/pricing issues to SNGPL/SSGC network curtailment; LPG marketing companies operate largely independent of the piped-gas utilities' allocation constraints.
- Do not state a specific current CNG price or pricing formula without hedging, given the sector's history of shifting between administered pricing and deregulation.
- Do not present a specific current gas-curtailment schedule for CNG as fixed/permanent; curtailment is typically a seasonal and policy-reviewed measure.
- Keep OGRA's CNG-station-level licensing/safety role distinct from SNGPL/SSGC's gas-supply/allocation role; a CNG station requires both an OGRA license and a gas connection/allocation from the relevant utility.

## Validation Checklist

- Confirm whether the question is about CNG or LPG before answering; do not default to one when the source specifies the other.
- Confirm which regulatory thread (licensing, pricing, curtailment) is actually being asked about.
- Flag any specific current price, pricing formula, or curtailment schedule as needing current-source verification.
- Confirm OGRA (licensing/pricing/safety) versus SNGPL/SSGC (supply/allocation) attribution is correct for the specific claim being made.

## Common Pitfalls

- Treating CNG and LPG as interchangeable terms or regulatory regimes when they have distinct supply chains and licensing tracks.
- Attributing LPG cylinder shortages to natural-gas pipeline curtailment, when LPG largely operates outside the SNGPL/SSGC network.
- Stating a specific CNG price or LPG cylinder price as current without noting the sector's history of administered-versus-deregulated pricing shifts.
- Presenting winter CNG curtailment as an isolated CNG-sector issue without noting the underlying gas-allocation priority order across domestic, industrial, fertilizer, and power sectors.
- Using this skill for general petroleum production/consumption statistics that belong in `ogra-petroleum-industry-reports`.

## Reference

- See [Pakistan CNG and LPG Sector Regulation Reference](references/pakistan-cng-lpg-sector-regulation.md) for institutional citations, licensing-track detail, and extraction notes.
