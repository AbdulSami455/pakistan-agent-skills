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
