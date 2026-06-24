# Pakistan Agent Skills

Pakistan Agent Skills is a repository of reusable skills for AI agents working on Pakistan-specific data, research, and analysis tasks.

Skills are organized as self-contained folders at the repository root. Each skill should include a `SKILL.md`, and may optionally include `references/`, `scripts/`, and `assets/` subfolders.

Required:

- `SKILL.md`

Optional:

- `references/` for source-specific notes, chapter maps, or extraction guidance
- `scripts/` for deterministic helpers
- `assets/` for templates used by outputs

## Using These Skills With Different Models

These skills are plain-text, model-agnostic assets. They are not tied to one framework. The general pattern is the same across Claude, OpenAI models, Hermes, and OpenClaw:

1. load the relevant `SKILL.md`
2. optionally load the linked `references/` file if the task needs more detail
3. tell the model which skill to use
4. give the model the actual task, source file, and output requirement

The most reliable setup is to pass the skill text as context and keep the user task separate.

### General Prompt Pattern

Use a wrapper like this with any model:

```text
You are working with a domain skill.

Skill name: <skill-name>
Skill instructions:
<paste SKILL.md here>

Optional references:
<paste only the needed reference file here>

Task:
<actual user task>

Requirements:
- follow the skill exactly
- preserve dates, units, labels, and source distinctions
- if the skill defines routing or validation rules, apply them before answering
```

### Claude

Claude works well when the skill is presented as operating instructions before the task.

Recommended pattern:

```text
Use this skill as your operating guide:
<paste SKILL.md>

If needed, use this supporting reference:
<paste selected reference>

Now complete this task:
<task>
```

Notes:

- Keep the skill ahead of the task in the prompt.
- Pass only the one relevant reference file instead of all references.
- For large-document work such as PES, ask Claude to first identify the correct chapter or subsection before extracting figures.

### OpenAI Models

OpenAI models work best when the skill is placed in the system or developer-style instruction layer, with the task in the user layer.

Recommended pattern:

```text
System or developer instruction:
Follow this skill exactly:
<paste SKILL.md>

Reference material if needed:
<paste selected reference>

User task:
<task>
```

Notes:

- Put the skill in the higher-priority instruction layer when possible.
- Keep references selective to control context size.
- For PSX package tasks, include the exact function or dataset the model should work on.

### Hermes

Hermes-style local models usually do better with explicit structure and shorter context blocks.

Recommended pattern:

```text
[ROLE]
Follow the skill below.

[SKILL]
<paste SKILL.md>

[REFERENCE]
<paste only if needed>

[TASK]
<task>

[OUTPUT RULES]
- preserve units and dates
- do not invent missing figures
- follow the skill workflow
```

Notes:

- Prefer one skill at a time.
- Break complex tasks into two passes if needed:
  - first select the right section or function
  - then extract or analyze
- Avoid pasting multiple long references into a smaller local model context window.

### OpenClaw

OpenClaw or similar open local agents benefit from strongly bounded instructions and explicit routing.

Recommended pattern:

```text
Instruction:
Use the following skill as the operating procedure.

Skill:
<paste SKILL.md>

Reference:
<paste selected reference if required>

Task:
<task>

Before answering:
1. identify the relevant section of the skill
2. identify the source section or function
3. extract the answer
4. verify units, labels, and years
```

Notes:

- Add step-by-step verification explicitly.
- Prefer narrower skills such as `pes-external-sector` instead of broad multi-domain context.
- For local agent pipelines, store each skill and reference as separate retrievable chunks.

## Skill Selection Examples

- Use `psx-historical-data` for `psxdata.stocks()` tasks.
- Use `psx-market-discovery` for `tickers`, `indices`, or `sectors`.
- Use `psx-company-snapshots` for `quote` or `fundamentals`.
- Use `psx-debt-and-eligibility` for `debt_market` or `eligible_scrips`.
- Use `pes-macro-and-prices` for GDP growth, macro overview, or inflation.
- Use `pes-real-sectors` for agriculture, manufacturing, or mining.
- Use `pes-fiscal-financial-and-debt` for deficits, policy rates, markets, or debt.
- Use `pes-external-sector` for exports, imports, remittances, reserves, or current account.
- Use `pes-social-sectors` for education, health, labour, population, poverty, or inequality.
- Use `pes-infrastructure-digital-and-climate` for transport, energy, IT, telecom, or climate.
- Use `sbp-monetary-policy-statement` for a specific MPC meeting's policy rate decision or rationale.
- Use `sbp-annual-report` for SBP's own State of the Economy narrative or statistical annexes.
- Use `sbp-balance-of-payments-bulletin` for monthly/quarterly current account, reserves, or debt servicing.
- Use `sbp-financial-soundness-indicators` for bank-wise NPL, CAR, or profitability ratios.
- Use `sbp-financial-stability-review` for systemic risk narrative on banks, NBFIs, or insurance.
- Use `federal-budget-documents` for Budget in Brief, Budget Speech, Finance Bill, or Demand for Grants figures.
- Use `fbr-yearbook` for tax collection by tax head, sector, or withholding category.
- Use `fbr-customs-tariff` for HS-code duty rates or tariff-change analysis.
- Use `fbr-property-valuation` for city-wise notified property valuation rates.
- Use `imf-pakistan-documents` for IMF Article IV or EFF/SBA program targets and benchmarks.
- Use `pide-research-reports` for independent PIDE working papers or policy viewpoints.
- Use `provincial-budget-documents` for Punjab, Sindh, KP, or Balochistan budget allocations and ADP.
- Use `mufap-mutual-funds` for mutual fund NAVs, categories, or performance.
- Use `pkr-remittances-tracker` for monthly remittances by sending country/corridor.
- Use `secp-insurance-industry-statistics` for insurer-wise premiums, assets, or takaful data.
- Use `nih-disease-surveillance` for weekly outbreak alerts or disease case counts by district.
- Use `hec-higher-ed-stats` for university enrollment, graduate output, or faculty statistics.
- Use `pakistan-education-statistics` for school-level institution, enrollment, or teacher counts.
- Use `mnfsr-agri-statistics` for crop area, production, or yield by crop and district.
- Use `pbs-agriculture-census` for farm size, land tenure, irrigation, or livestock counts.
- Use `pbs-labour-force-survey` for granular employment, unemployment, or informal-sector statistics.
- Use `pbs-pslm` for poverty rates or household consumption at district/provincial level.
- Use `pbs-cpi-spi-wpi-bulletins` for item-level CPI, SPI, or WPI price detail.
- Use `pakistan-census-bulletins` for population or household counts by administrative unit.
- Use `secp-company-registry` for a company's registration status, incorporation date, or category.
- Use `parliament-legislative-tracker` for a bill's status through the National Assembly or Senate.
- Use `ndma-flood-sitreps` for rainfall, river flow, casualty, or relief-operation data during floods.
- Use `pta-telecom-indicators` for subscriber, teledensity, or operator-level telecom revenue data.
- Use `pakistan-unesco-heritage-sites` for Pakistan's World Heritage or Tentative List sites.
- Use `pakistan-admin-boundaries` for province/division/district/tehsil names and codes.
- Use `unhcr-pakistan-refugee-data` for registered Afghan refugee or PoR population trends.
- Use `ljcp-judicial-statistics` for case pendency, disposal rates, or judge strength by court level.
- Use `beoe-labour-migration-report` for overseas worker deployment by destination or occupation.
- Use `nepra-state-of-industry` for generation capacity, fuel mix, tariffs, or T&D losses.
- Use `nepra-tariff-determinations` for a specific DISCO or generation company tariff order.
- Use `igcep-capacity-plan` for long-term generation capacity expansion forecasts.
- Use `ogra-petroleum-industry-report` for refining, marketing, or POL consumption statistics.
- Use `ogra-pol-price-notifications` for fortnightly petrol/diesel/kerosene price buildup.
- Use `irsa-reservoir-data` for Tarbela/Mangla/Chashma reservoir levels, inflows, or discharges.
- Use `tdap-trade-reports` for granular monthly export-import detail by product and market.
- Use `punjab-development-statistics` for Punjab-specific socioeconomic indicators.
- Use `sindh-development-statistics` for Sindh-specific socioeconomic indicators.
- Use `kp-open-data` for discovering or downloading KP government open datasets.
- Use `pcaa-statistical-digest` for airport- or airline-wise passenger and cargo traffic.
- Use `pakistan-railways-yearbook` for passenger/freight volumes or financial performance.
- Use `port-qasim-cargo-reports` for vessel arrivals or cargo throughput by commodity type.
- Use `i2i-startup-ecosystem-report` for startup funding trends or ecosystem player mapping.
- Use `sbp-ict-exports-special-section` for IT/ICT export deep-dive analysis.

## Contribution Guide

Contributions should improve one of the repository’s active domains:

- package-focused PSX workflows
- Pakistan Economic Survey analysis workflows

Stricter contribution rules:

- keep each PR limited to one clear change set
- do not mix documentation cleanup, refactors, and new skill content in the same PR unless they are tightly coupled
- add or update `SKILL.md` only when the change improves task execution quality in a measurable way
- include a short rationale for any new reference file, rule, or validation step
- preserve existing scope boundaries; a skill should stay narrow and domain-specific
- prefer small, reviewable edits over broad rewrites
- never copy large source documents verbatim into `references/`
- do not introduce framework-specific material unless the skill explicitly needs it

Good contributions include:

- adding a narrowly scoped new skill
- tightening extraction or validation guidance
- adding short references that reduce ambiguity
- improving figure-handling, chapter-routing, or dataset-specific instructions

Avoid:

- mixing unrelated domains into a single skill
- copying large source documents verbatim into references
- adding framework or product material that is outside the skill’s scope
- adding files that do not directly improve execution quality
- submitting changes without verifying the target source or workflow
- expanding a skill beyond the data source or function it is meant to cover

## Skill Standards

When authoring or reviewing a skill:

- tie the skill to concrete tasks, sources, or functions
- make trigger conditions explicit in the description
- keep instructions actionable and concise
- preserve exact dates, units, year labels, and source distinctions
- move long supporting detail into `references/` instead of bloating `SKILL.md`

## Review Checklist

- the skill scope is narrow and clear
- `SKILL.md` clearly explains when the skill should be used
- examples or references map to the underlying source material
- extraction rules protect against label, unit, or year misreads
- the contribution improves execution quality in a concrete way

## Protecting `main`

This repository cannot enforce branch restrictions by itself. Set the rule in your git host.

If you want only your account to be able to push directly to `main`:

1. Open the repository settings in your host platform.
2. Add a branch protection rule or ruleset for `main`.
3. Require pull requests for all changes.
4. Restrict direct pushes to `main` so only your account is allowed.
5. Keep admin bypass disabled unless you explicitly need it.

GitHub path:

- `Settings` -> `Branches` -> `Add branch protection rule`
- Target branch: `main`
- Enable `Require a pull request before merging`
- Under `Restrict who can push to matching branches`, add only your GitHub account

If your host supports rulesets, use the equivalent `main` branch ruleset and add only your account to the allowed push or bypass list.
