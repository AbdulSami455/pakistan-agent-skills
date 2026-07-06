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
- Use `sbp-financial-soundness-indicators` for bank-wise NPL, CAR, or profitability ratios.
- Use `sbp-financial-stability-review` for systemic risk narrative on banks, NBFIs, or insurance.
- Use `ecp-election-results` for official ECP election results, by-elections, and constituency lookup.
- Use `kp-development-statistics` or `balochistan-development-statistics` for province-specific socioeconomic indicators in those provinces.
- Use `karachi-port-cargo-reports` for Karachi Port vessel and cargo throughput; use `port-qasim-cargo-reports` for Port Qasim.
- Use `ogra-petroleum-industry-reports` for oil/gas production, consumption, and regulated petroleum pricing.
- Use `pbs-national-accounts` for quarterly GDP growth or sectoral value-added from PBS.
- Use `psdp-federal-development-programme` for federal development project allocations and expenditure.
- Use `bisp-social-protection-statistics` for BISP/Benazir beneficiary counts and cash transfer disbursements.
- Use `gwadar-port-cargo-reports` for Gwadar Port vessel and cargo throughput.
- Use `ajk-development-statistics` or `gb-development-statistics` for territory-specific socioeconomic indicators.
- Use `who-pakistan-health-statistics` or `unicef-pakistan-data` for internationally standardized health and child indicators.
- Use `pmd-weather-climate-data` for weather observations, climate normals, or seasonal forecasts.
- Use `world-bank-pakistan-indicators` or `adb-pakistan-indicators` for multilateral development indicators with cross-country comparability.
- Use `ccp-competition-enforcement` for antitrust/competition matters (mergers, cartels, abuse of dominance) — distinct from `secp-company-registry`'s securities/registration mandate.
- Use `provincial-sales-tax-authorities` for sales tax on services (PRA/SRB/KPRA/BRA) — distinct from `fbr-individual-tax-filing` and `fbr-customs-tariff`, which cover federal taxes on goods/income/customs.
- Use `ppra-public-procurement` for government tender/procurement rules and processes, federal or provincial.
- Use `agp-audit-reports` for Auditor General financial/compliance audit findings ("audit paras") — distinct from `nab-accountability-data`, which covers criminal corruption investigations and prosecutions.
- Use `nab-accountability-data` for NAB's accountability pipeline (inquiry, investigation, reference, plea bargain, recovery figures).
- Use `nccia-cybercrime-peca` for PECA cybercrime enforcement questions — note NCCIA (est. April 2025) superseded FIA's NR3C; treat "NR3C" as outdated if encountered.

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
