---
name: pide-research-reports
description: PIDE research reports skill. Use when analyzing, summarizing, comparing, or extracting information from Pakistan Institute of Development Economics (PIDE) working papers and policy reports, especially for independent think-tank analysis on a specific topic rather than the chapter-routed structure of a government document like the Pakistan Economic Survey.
---

# PIDE Research Reports

## Overview

Use this skill for Pakistan Institute of Development Economics (PIDE) working papers and policy viewpoints/reports. Unlike government documents such as the Pakistan Economic Survey, PIDE output is topic-driven rather than chapter-routed: each paper or report stands on its own, addressing a specific research question, policy proposal, or empirical analysis.

## Coverage

- Working papers: empirical or theoretical research papers on specific economic topics (e.g. productivity, trade policy, urbanization, energy pricing).
- Policy viewpoints/reports: shorter, policy-oriented pieces aimed at influencing public debate or government policy on a current issue.
- Knowledge briefs and discussion papers: condensed analysis on a narrower question, often responding to a current policy debate.
- No fixed chapter structure across documents — each title is its own self-contained unit with its own scope, methodology, and conclusions.

## Use This Skill For

- summarizing a specific PIDE working paper's research question, methodology, and findings
- extracting policy recommendations from a PIDE policy viewpoint
- comparing PIDE's independent analysis of an issue against the government's own framing in the PES or a budget document
- identifying which PIDE paper(s) are relevant to a specific economic policy question
- tracing how PIDE's position on a topic (e.g. energy subsidies, tax policy) has evolved across multiple papers over time

## Routing Rules

- Use this skill whenever the source is explicitly a PIDE paper or report; do not substitute it for official government statistics.
- If the question is about official economic outturns (growth, inflation, fiscal, external sector) rather than independent analysis, prefer the relevant `pes-*` or `sbp-*` skill, and use PIDE material only for added analytical perspective when requested.
- If the question is about IMF's external assessment rather than a domestic think-tank's, prefer `imf-pakistan-documents`.
- Because PIDE output is topic-driven rather than document-structured, route by topic/keyword search within the specific paper rather than by a fixed chapter map.

## Extraction Workflow

1. Identify the specific PIDE paper or report by title, author, or publication year; do not assume a single canonical "PIDE document" the way PES has one canonical survey per year.
2. Read the abstract/executive summary first to confirm the paper's scope matches the question before extracting detail.
3. Distinguish the paper's empirical findings from its policy recommendations; PIDE papers often separate analysis from prescriptive conclusions.
4. Note the paper's data sources and time period covered, since PIDE papers may use different reference periods than the latest PES or SBP releases.
5. When a question spans multiple PIDE papers on related topics, synthesize position-by-position rather than implying a single unified PIDE institutional view unless the source explicitly states one.

## Technical Rules

- Attribute findings and opinions specifically to the paper's author(s), since PIDE working papers are individually authored research, not institutional consensus statements.
- Do not present a working paper's preliminary or illustrative estimates as official statistics.
- Preserve the exact title and publication year of the paper being cited, since PIDE revises and republishes on recurring topics.
- Keep methodology caveats (e.g. model assumptions, data limitations) attached to any cited finding rather than dropping them.

## Validation Checklist

- Confirm the paper's title, author(s), and publication year match the citation.
- Verify whether a number cited is the paper's own estimate or a figure the paper quotes from another source (e.g. PBS, SBP).
- Check whether the paper presents a finding as preliminary/exploratory or as a robust conclusion.
- Confirm policy recommendations are clearly separated from the empirical analysis section.

## Common Pitfalls

- Treating an individual researcher's working paper as an official PIDE institutional position.
- Citing a PIDE estimate as if it were official government or SBP data.
- Conflating findings from different PIDE papers on the same topic written by different authors with different methodologies.
- Losing track of the paper's reference period when its data predates the latest official releases.
