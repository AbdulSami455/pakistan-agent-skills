---
name: epi-immunization-schedule
description: EPI (Expanded Programme on Immunization) Pakistan skill. Use when looking up which vaccines are given at which age for children (and pregnant women) under Pakistan's national routine immunization schedule, administered by the Federal Directorate of Immunization, as distinct from immunization coverage-rate statistics.
---

# EPI Immunization Schedule

## Overview

Use this skill for Pakistan's routine childhood (and antenatal) immunization schedule under the Expanded Programme on Immunization (EPI), administered by the Federal Directorate of Immunization (FDI) with provincial EPI programs implementing delivery. This is a practical schedule-reference skill for parents, students, and health workers — not a coverage-statistics or outbreak-surveillance skill.

## Coverage

- The routine schedule: which vaccine(s) are given at birth, and at each subsequent age milestone up to approximately 15 months, covering the target vaccine-preventable diseases (tuberculosis, poliomyelitis, diphtheria, pertussis, tetanus, hepatitis B, Haemophilus influenzae type b, pneumococcal disease, rotavirus diarrhea, measles, rubella, typhoid).
- Vaccine additions over time: EPI's schedule has been expanded incrementally (e.g., hepatitis B added 2002, Hib in 2009, PCV in 2012, inactivated polio vaccine in 2015, rotavirus in 2017, typhoid conjugate vaccine phased in provincially from 2019-2021, measles vaccine replaced by measles-rubella (MR) vaccine in 2021) — schedule content is not static across years.
- Antenatal component: tetanus toxoid/Td vaccination for pregnant women as part of maternal and neonatal tetanus elimination efforts.
- Supplementary immunization activities (e.g., polio campaign rounds) are a distinct, additional layer on top of the routine schedule — not part of the routine age-based calendar itself.
- Provincial EPI programs (Punjab, Sindh, etc.) implement the national schedule with local delivery/administration specifics but should follow the same national antigen schedule set by FDI.

## Use This Skill For

- looking up which vaccine(s) a child should receive at a specific age under Pakistan's EPI schedule
- explaining what disease(s) a specific EPI vaccine protects against
- clarifying which vaccines were added to the schedule and roughly when, for historical/comparative context
- explaining the antenatal tetanus/Td vaccination component for pregnant women
- distinguishing routine EPI immunization from supplementary campaign activities (e.g., polio National Immunization Days)

## When Not to Use This Skill

- For immunization coverage-rate statistics (percent of target population vaccinated) or internationally modeled indicators — use `who-pakistan-health-statistics` instead.
- For outbreak surveillance or disease case counts (e.g., a measles or polio outbreak bulletin) — use `nih-disease-surveillance` instead.
- For child-specific development, nutrition, or broader well-being indicators beyond immunization — use `unicef-pakistan-data` instead.

## Routing Rules

- Use this skill for the practical "what vaccine at what age" schedule question, not for coverage percentages or outbreak case data.
- If the question is about what share of children are actually vaccinated (coverage rate) rather than what the schedule prescribes, route to `who-pakistan-health-statistics`.
- If the question is about a disease outbreak rather than the preventive schedule, route to `nih-disease-surveillance`.
- Always note that the schedule has changed over time; if the question involves a historical period, flag that the schedule then may differ from the current one.

## Extraction Workflow

1. Identify whether the question is about a specific age milestone (what vaccines are due) or a specific vaccine (at what age it is given and what it protects against).
2. Confirm whether the question is about the current schedule or a historical point in time, since antigens have been added to the schedule progressively.
3. If the question involves a pregnant woman rather than a child, route to the antenatal tetanus/Td component rather than the childhood schedule.
4. Distinguish routine EPI schedule vaccination from supplementary campaign rounds (e.g., polio NIDs), which follow separate campaign-specific timing rather than the fixed age-based routine calendar.
5. Note that some vaccines were phased in provincially at different times (e.g., typhoid conjugate vaccine); flag provincial variation where relevant rather than assuming uniform national timing for every addition.

## Technical Rules

- The routine schedule is age-based (birth, 6 weeks, 10 weeks, 14 weeks, 9 months, 15 months are typical milestones, subject to confirmation against the current official schedule); do not assume a fixed universal schedule without checking the current EPI publication, since it is revised as new antigens are added.
- Measles vaccine was replaced by the combined measles-rubella (MR) vaccine in the current schedule; older references to a standalone "measles vaccine" dose may describe a superseded schedule.
- Supplementary immunization activities (polio campaigns) are additional to, not a replacement for, routine EPI doses.
- Some antigens (e.g., typhoid conjugate vaccine) were introduced in some provinces before others; do not assume simultaneous nationwide rollout for every schedule addition.

## Validation Checklist

- Confirm whether the question needs the current schedule or a historical schedule for a specific vaccine's introduction.
- Verify whether the question concerns the routine age-based schedule or a supplementary campaign activity.
- Check whether a cited antigen addition applies nationally or was provincially phased.
- Confirm the question is about the schedule itself, not coverage rates or outbreak data, before answering.

## Common Pitfalls

- Citing an outdated version of the schedule (e.g., referencing standalone measles vaccine after the MR vaccine replacement).
- Conflating routine EPI schedule doses with supplementary campaign doses (e.g., polio NID rounds).
- Assuming uniform national timing for antigen additions that were actually phased in provincially.
- Answering a coverage-rate or outbreak question using this skill instead of routing to the appropriate WHO or NIH skill.

## Reference

- See [EPI Immunization Schedule Reference](references/epi-immunization-schedule.md) for schedule structure and extraction notes.
