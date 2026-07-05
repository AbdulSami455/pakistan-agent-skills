---
name: nih-disease-surveillance
description: NIH Pakistan disease surveillance skill. Use when analyzing, summarizing, or extracting information from the National Institutes of Health Islamabad's outbreak alerts, disease surveillance bulletins, or public health guidelines for epidemic-prone diseases (dengue, polio, measles, etc.) in Pakistan, as distinct from WHO's internationally modeled health indicators.
---

# NIH Disease Surveillance

## Overview

Use this skill for Pakistan's own disease-surveillance and outbreak-response publications from the National Institutes of Health (NIH), Islamabad — an autonomous body under the Ministry of National Health Services, Regulation and Coordination. This is the right skill for domestically reported outbreak alerts, case-definition guidelines, and disease-specific advisories — not for internationally standardized/modeled indicators (use WHO) or routine immunization scheduling (use the EPI schedule skill).

## Coverage

- Field Epidemiology and Disease Surveillance Division bulletins: case counts and trend updates for epidemic-prone diseases (e.g., dengue, Crimean-Congo hemorrhagic fever, measles, polio, cholera/acute watery diarrhea).
- Surveillance case definitions: NIH's standardized definitions for reporting communicable/infectious diseases, used to determine what counts as a "confirmed" or "suspected" case.
- Outbreak-specific guidelines and advisories: prevention and control guidance issued during specific outbreak events (e.g., post-monsoon disease risk advisories, dengue control guidelines).
- Public Health Emergency Preparedness and Response materials, including national action plans issued during major health emergencies (e.g., past pandemic response plans).
- NIH's role spans both surveillance/reporting and vaccine-related research/production, but this skill focuses on the surveillance and outbreak-communication side.

## Use This Skill For

- extracting current or recent outbreak case counts/trends for a specific disease from NIH bulletins
- looking up NIH's surveillance case definition for a specific communicable disease
- finding outbreak prevention/control guidance issued by NIH for a specific disease or event
- distinguishing NIH's domestically reported case data from WHO's internationally modeled disease-burden estimates
- identifying which disease surveillance center within NIH (e.g., Center for Infectious Diseases Prevention and Control) issued a specific bulletin

## When Not to Use This Skill

- For internationally standardized/modeled health indicators (life expectancy, mortality rates, WHO-modeled disease burden) — use `who-pakistan-health-statistics` instead.
- For the routine childhood immunization schedule (which vaccine at which age) — use `epi-immunization-schedule` instead; NIH covers outbreak surveillance, EPI covers the routine vaccination calendar.
- For event-driven flood/disaster casualty and relief figures — use `ndma-flood-sitreps` instead, even where a flood event triggers a related disease outbreak covered here.
- For child-specific development/nutrition indicators — use `unicef-pakistan-data` instead.

## Routing Rules

- Use this skill for NIH's own domestically reported surveillance bulletins, case definitions, and outbreak guidance.
- If the question needs an internationally comparable/modeled indicator rather than a domestic case count, route to `who-pakistan-health-statistics`.
- If the question is about the routine vaccination schedule rather than outbreak surveillance, route to `epi-immunization-schedule`.
- If a disease outbreak is linked to a flood/disaster event, this skill covers the disease-surveillance angle while `ndma-flood-sitreps` covers the disaster-impact angle — keep the two distinct.

## Extraction Workflow

1. Identify the specific disease and reporting period the question concerns.
2. Confirm whether the question needs a case count/trend (surveillance bulletin), a case definition (used for classification), or prevention/control guidance (advisory document).
3. Note which NIH center or division issued the material, if specified, since NIH covers multiple public-health domains beyond surveillance (e.g., vaccine production, non-communicable disease control).
4. Preserve the exact reporting period and whether figures are provisional (during an active outbreak) or a finalized summary.
5. If comparing to WHO figures for the same disease, flag that NIH's domestically reported case counts and WHO's modeled estimates can differ due to underreporting, case-definition differences, or estimation methodology.

## Technical Rules

- NIH case counts are based on Pakistan's own surveillance case definitions, which may differ from WHO's international case-definition standards; do not treat the two as automatically equivalent.
- Outbreak bulletins are time-bound to a specific reporting period; do not treat an early-outbreak figure as the final total without checking for a later update.
- NIH's mandate spans surveillance, vaccine research/production, and public health emergency response — confirm which function a specific document belongs to before characterizing its purpose.
- Distinguish "confirmed" cases from "suspected" cases where the source makes that distinction; conflating them overstates confirmed disease burden.

## Validation Checklist

- Confirm the specific disease and reporting period for any cited figure.
- Verify whether the source is a surveillance bulletin, case definition document, or outbreak guideline.
- Check whether case counts are confirmed, suspected, or a combined figure.
- Confirm this skill's domestic case data is not being conflated with WHO's separately modeled estimates for the same disease.

## Common Pitfalls

- Treating NIH's domestic case counts as identical to WHO's internationally modeled estimates for the same disease.
- Citing an early-outbreak case count as final without checking for a later, revised bulletin.
- Confusing NIH's outbreak surveillance role with EPI's separate routine-immunization scheduling role.
- Blending confirmed and suspected case counts into a single unqualified "cases" figure.

## Reference

- See [NIH Disease Surveillance Reference](references/nih-disease-surveillance.md) for source structure and extraction notes.
