---
name: pakistan-environment-climate-policy
description: Pakistan environmental regulation and climate policy skill. Use when explaining Pak-EPA's environmental protection mandate (permits, Environmental Impact Assessments, pollution enforcement) or the Ministry of Climate Change's national climate policy role, as distinct from the Pakistan Economic Survey's climate narrative chapter or NDMA's disaster-response function.
---

# Pakistan Environment & Climate Policy

## Overview

Use this skill for Pakistan's environmental regulatory and climate-policy institutions: the Pakistan Environmental Protection Agency (Pak-EPA) and the Ministry of Climate Change and Environmental Coordination. This is a regulatory-structure and policy-framework reference skill — not a live pollution-monitoring data feed, and not the same as the Pakistan Economic Survey's narrative climate chapter.

## Coverage

- Pak-EPA: the federal executive environmental regulator (operational since 1997 under enabling legislation), responsible for environmental protection enforcement — including Environmental Impact Assessment (EIA) and Initial Environmental Examination (IEE) review/approval for projects, pollution-control standards (air, water, industrial effluent), and enforcement actions against violations.
- Provincial EPAs: environmental protection is a devolved subject post-18th Amendment, so each province (and Gilgit-Baltistan/AJK) generally operates its own provincial EPA with its own EIA/IEE review process for projects within its jurisdiction — do not assume Pak-EPA (federal) has jurisdiction over a provincial-level project.
- Ministry of Climate Change and Environmental Coordination: the federal policy ministry responsible for national climate policy, international climate commitments/negotiations (e.g., Pakistan's Nationally Determined Contributions under the Paris Agreement), and climate-adaptation/mitigation policy frameworks.
- EIA/IEE process: project proponents (for specified categories of development projects) must submit an EIA or IEE for regulatory review before proceeding; the review determines environmental conditions or project modifications required for approval.

## Use This Skill For

- explaining Pak-EPA's or a provincial EPA's general regulatory role and enforcement mechanisms
- describing the general EIA/IEE process and when it applies to a project
- explaining the Ministry of Climate Change's policy role, including Pakistan's international climate commitments
- clarifying which level of government (federal Pak-EPA vs. provincial EPA) has jurisdiction over a specific type of project
- distinguishing environmental regulatory/policy institutions from disaster-response bodies

## When Not to Use This Skill

- For the Pakistan Economic Survey's narrative-level climate chapter — use `pes-infrastructure-digital-and-climate` instead; that skill covers the annual survey's climate-policy narrative and indicators, while this skill covers the regulatory/institutional structure itself.
- For event-driven flood/disaster casualty and relief figures — use `ndma-flood-sitreps` instead; environmental regulation and disaster response are distinct government functions even when a climate-linked event (e.g., a flood) connects them.
- For meteorological/weather data — use `pmd-weather-climate-data` instead.
- For forest cover or protected-area/biodiversity data specifically — check whether a dedicated skill for that already exists before defaulting to this one, since this skill covers regulatory/policy structure rather than environmental-monitoring datasets.

## Routing Rules

- Use this skill for Pak-EPA/provincial-EPA regulatory structure, the EIA/IEE process, and Ministry of Climate Change policy questions.
- If the question needs the Economic Survey's narrative climate-chapter content, route to `pes-infrastructure-digital-and-climate`.
- If the question is about a specific flood/disaster event's impact, route to `ndma-flood-sitreps`; this skill covers policy/regulatory structure, not event response.
- If a project's jurisdiction is ambiguous, clarify federal (Pak-EPA) versus provincial EPA jurisdiction before answering, since environmental regulation is largely devolved.

## Extraction Workflow

1. Identify whether the question concerns Pak-EPA/provincial-EPA regulatory enforcement, the EIA/IEE process for a specific project type, or the Ministry of Climate Change's policy/international-commitment role.
2. If a specific project or jurisdiction is named, determine whether federal Pak-EPA or the relevant provincial EPA has jurisdiction, since environmental regulation is a devolved subject.
3. For EIA/IEE questions, clarify which of the two applies (IEE for lower-impact projects, EIA for higher-impact projects, per the applicable schedule of project categories) rather than treating them as interchangeable.
4. For climate-policy questions, distinguish domestic policy/regulatory content from Pakistan's international climate commitments (e.g., NDCs), since these are related but distinct policy tracks.

## Technical Rules

- Environmental regulation is a devolved (largely provincial) subject post-18th Amendment; do not assume federal Pak-EPA jurisdiction over a project without confirming it falls under federal purview specifically.
- EIA and IEE are distinct review tracks tied to a project's expected environmental impact category; do not use them interchangeably.
- Keep the Ministry of Climate Change's policy/international-commitment role distinct from Pak-EPA's project-level regulatory/enforcement role — they are related but structurally different functions.
- Keep this skill's regulatory/policy-structure focus distinct from the Economic Survey's narrative climate-chapter content and from NDMA's disaster-response function.

## Validation Checklist

- Confirm whether federal Pak-EPA or a provincial EPA has jurisdiction over the specific project/question at hand.
- Verify whether an EIA or IEE (not used interchangeably) applies to the project category in question.
- Check whether the question needs regulatory/policy-structure content (this skill) or narrative-survey content (`pes-infrastructure-digital-and-climate`).
- Confirm disaster-response questions are routed to `ndma-flood-sitreps` rather than answered from this skill.

## Common Pitfalls

- Assuming federal Pak-EPA has jurisdiction over a project actually under provincial EPA jurisdiction.
- Using "EIA" and "IEE" interchangeably when they are distinct review tracks for different impact categories.
- Conflating this skill's regulatory/policy-structure content with the Economic Survey's narrative climate chapter.
- Treating environmental regulation and disaster response (NDMA) as the same government function.

## Reference

- See [Pakistan Environment & Climate Policy Reference](references/pakistan-environment-climate-policy.md) for institutional structure and extraction notes.
