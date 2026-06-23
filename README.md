# Pakistan Agent Skills

Pakistan Agent Skills is a repository of reusable skills for AI agents working with the `psxdata` Python package. The repository is intentionally narrow: it focuses on package usage for Pakistan Stock Exchange data, not web APIs or unrelated Pakistan-domain work.

## Scope

This repository currently organizes `psxdata` into focused skills so an agent can use the right package workflow for the task at hand.

- historical OHLCV data
- market discovery data such as tickers, indices, and sectors
- company-level quote and fundamentals workflows
- debt market and margin-eligibility workflows

## Current Skills

| Skill | Purpose |
| --- | --- |
| `psx-historical-data` | Use `psxdata.stocks()` for historical OHLCV workflows. |
| `psx-market-discovery` | Use `psxdata.tickers()`, `psxdata.indices()`, and `psxdata.sectors()` for market structure and discovery tasks. |
| `psx-company-snapshots` | Use `psxdata.quote()` and `psxdata.fundamentals()` for company-level data retrieval. |
| `psx-debt-and-eligibility` | Use `psxdata.debt_market()` and `psxdata.eligible_scrips()` for debt and margin-eligibility tasks. |

## Repository Structure

```text
skills/
  psx-historical-data/
    SKILL.md
  psx-market-discovery/
    SKILL.md
  psx-company-snapshots/
    SKILL.md
  psx-debt-and-eligibility/
    SKILL.md
```

Each skill should remain self-contained inside its own folder.

Required:

- `SKILL.md`

Optional:

- `references/` for package notes or usage examples
- `scripts/` for deterministic helpers
- `assets/` for templates used by outputs

## Contribution Guide

Contributions should improve how agents use the `psxdata` package.

Good contributions include:

- adding a new package-focused PSX skill
- improving an existing skill’s package usage guidance
- tightening examples around specific `psxdata` functions
- adding short package references where they reduce ambiguity

Avoid:

- adding API-layer documentation
- mixing unrelated domains into a single skill
- copying large product documentation into references
- adding files that do not directly improve package usage

## Skill Standards

When authoring or reviewing a skill:

- keep the skill tied to concrete package functions
- explain when to use the skill in terms of user tasks
- use realistic PSX examples such as ticker symbols and date ranges
- keep instructions actionable and concise
- avoid generic finance guidance that is not specific to `psxdata`

## Review Checklist

- the skill scope is narrow and clear
- `SKILL.md` explains when the skill should be used
- examples map to actual `psxdata` package functions
- the skill does not drift into API or framework documentation
- the contribution improves package usage in a concrete way

