# Pakistan Agent Skills

Pakistan Agent Skills is a repository of reusable skills for AI agents working on Pakistan-specific data, research, and analysis tasks. The repository currently covers two focused areas:

- `psxdata` package workflows for Pakistan Stock Exchange data
- Pakistan Economic Survey 2025-26 document analysis derived from the survey PDF

## Current Skills

| Skill | Purpose |
| --- | --- |
| `psx-historical-data` | Use `psxdata.stocks()` for historical OHLCV workflows. |
| `psx-market-discovery` | Use `psxdata.tickers()`, `psxdata.indices()`, and `psxdata.sectors()` for market structure and discovery tasks. |
| `psx-company-snapshots` | Use `psxdata.quote()` and `psxdata.fundamentals()` for company-level data retrieval. |
| `psx-debt-and-eligibility` | Use `psxdata.debt_market()` and `psxdata.eligible_scrips()` for debt and margin-eligibility tasks. |
| `pes-macro-and-prices` | Use the Pakistan Economic Survey for macro overview, growth, investment, and inflation questions. |
| `pes-real-sectors` | Use the survey for agriculture, manufacturing, and mining analysis. |
| `pes-fiscal-financial-and-debt` | Use the survey for fiscal development, money, capital markets, and public debt analysis. |
| `pes-external-sector` | Use the survey for trade, remittances, reserves, and external-sector analysis. |
| `pes-social-sectors` | Use the survey for education, health, labour, population, and social protection analysis. |
| `pes-infrastructure-digital-and-climate` | Use the survey for transport, communications, energy, IT, telecom, and climate analysis. |

## Repository Structure

```text
skills/
  psx-historical-data/
  psx-market-discovery/
  psx-company-snapshots/
  psx-debt-and-eligibility/
  pes-macro-and-prices/
  pes-real-sectors/
  pes-fiscal-financial-and-debt/
  pes-external-sector/
  pes-social-sectors/
  pes-infrastructure-digital-and-climate/
```

Each skill remains self-contained inside its own folder.

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

## Contribution Guide

Contributions should improve one of the repository’s active domains:

- package-focused PSX workflows
- Pakistan Economic Survey analysis workflows

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
