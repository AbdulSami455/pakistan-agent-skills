---
name: pakistan-disability-rights-framework
description: Pakistan disability rights and inclusion legal framework skill. Use when a task concerns the ICT Persons with Disabilities Act 2020 and provincial disability acts (Punjab, Sindh, KP), the statutory employment quota for persons with disabilities, Pakistan's ratification of and obligations under the UN Convention on the Rights of Persons with Disabilities (CRPD), or the National/Provincial Council(s) for Rehabilitation of Disabled Persons — as distinct from social-protection cash-transfer programs or school-facility infrastructure data.
---

# Pakistan Disability Rights Framework

## Overview

Use this skill when a task requires explaining Pakistan's legal and institutional framework for disability rights and inclusion — the post-devolution patchwork of federal (ICT) and provincial disability acts, the statutory employment quota, Pakistan's CRPD obligations, and the Council for Rehabilitation of Disabled Persons structure. This is a legal/institutional-framework skill, not a benefits-disbursement or school-facilities-data skill — it explains what the law requires and which body administers it, not BISP payment figures or school-facility survey statistics.

## Coverage

- **Devolution and the resulting legislative patchwork**: disability welfare/rehabilitation, like most social-welfare subjects, became a provincial matter after the 18th Constitutional Amendment (2010), while the original federal Disabled Persons (Employment and Rehabilitation) Ordinance, 1981 had applied nationwide before devolution. Post-devolution, the Islamabad Capital Territory (ICT) and each province have had to legislate or continue applying adapted/extended versions of the 1981 Ordinance framework — resulting in a jurisdiction-by-jurisdiction patchwork that should not be treated as a single uniform national statute.
- **ICT Persons with Disabilities Act, 2020**: applicable within the Islamabad Capital Territory, representing a modernized reworking of the disability-rights framework (moving toward rights-based, CRPD-aligned language such as recognizing legal capacity, accessibility requirements, and non-discrimination, in addition to the earlier welfare/rehabilitation and employment-quota framing) — treat this as the ICT-specific statute, not automatically applicable in the provinces.
- **Provincial disability legislation**: Punjab, Sindh, and Khyber Pakhtunkhwa have each enacted (or continue to apply adapted versions of) their own disability-related legislation post-devolution; exact current statute titles, years, and specific provisions differ by province and should be hedged/verified rather than assumed identical to the ICT Act or to each other — do not assume a single "Persons with Disabilities Act" title/year applies uniformly across all provinces.
- **Employment quota**: Pakistan's disability framework (originating in the 1981 Ordinance and continued in successor federal/provincial legislation) has long included a statutory minimum-employment quota for persons with disabilities in public- and (in some formulations) private-sector establishments above a specified employee threshold — commonly cited around a 2% quota historically, though the exact current percentage, covered-employer threshold, and enforcement mechanism can vary by jurisdiction and has been subject to proposed upward revision in various reform discussions; state the quota with an explicit "(verify current jurisdiction-specific percentage)" hedge rather than asserting one fixed nationwide figure as current.
- **CRPD ratification context**: Pakistan ratified the UN Convention on the Rights of Persons with Disabilities (CRPD); ratification creates international-law obligations to progressively align domestic law and policy with the Convention's rights-based approach (moving away from a purely medical/welfare model toward accessibility, legal capacity, inclusive education, and non-discrimination) — domestic implementing legislation (like the ICT 2020 Act) is often framed as responsive to CRPD obligations, though the pace and completeness of alignment varies by jurisdiction within Pakistan and should not be overstated as fully achieved.
- **Council for Rehabilitation of Disabled Persons**: a statutory body (historically established at the national level under the 1981 Ordinance framework, with provincial-level counterparts) responsible for registration of persons with disabilities (disability certification/assessment), oversight of rehabilitation institutions and special-education facilities, and administration of quota-compliance and related welfare functions — the exact current name and institutional status (national vs. only provincial-level bodies post-devolution) should be verified rather than assumed unchanged since 1981.

## Use This Skill For

- explaining the post-devolution legal landscape for disability rights (ICT Act 2020 vs. provincial acts) and why a single uniform national statute should not be assumed
- explaining the statutory employment-quota framework for persons with disabilities, with appropriate hedging on the current exact percentage/threshold by jurisdiction
- explaining Pakistan's CRPD ratification and its general implications for domestic disability policy direction
- explaining the role of the (National/Provincial) Council for Rehabilitation of Disabled Persons in registration, certification, and quota oversight
- distinguishing a rights-based/CRPD-aligned framing from an older welfare/rehabilitation-only framing when describing how Pakistani disability law has evolved

## When Not to Use This Skill

- For BISP cash-transfer program details, including any disability-linked social-protection payments — use `bisp-social-protection-statistics`; this skill covers the disability-rights legal/institutional framework, not cash-transfer program administration or disbursement figures.
- For school-facility infrastructure indicators (accessibility features as a facility-survey data point) — use `pakistan-school-infrastructure-wash` for the facilities-data angle; this skill covers the legal inclusion/education-rights framing, not facility survey statistics.
- For general education statistics or curriculum structure — use `pakistan-education-statistics` or `pakistan-national-curriculum-textbooks` as applicable; this skill touches inclusive-education obligations only at the legal-framework level.
- For general labour-force statistics — use `pbs-labour-force-survey`; this skill covers the employment-quota legal obligation, not labour-market outcome data for persons with disabilities.

## Routing Rules

- If the question needs a specific cash-benefit amount or beneficiary count tied to disability, route to `bisp-social-protection-statistics`.
- If the question needs a school-facility accessibility statistic (e.g., percentage of schools with ramps), route to `pakistan-school-infrastructure-wash`.
- If the question is about which specific provincial statute currently governs disability rights in a named province, hedge explicitly and note the province-specific statute should be verified rather than assumed identical to the ICT 2020 Act.
- If the question is about general employment/labour statistics rather than the quota's legal framework, route to `pbs-labour-force-survey` for outcome data while keeping quota mechanics in this skill.
- If the question concerns general CRPD/international human-rights treaty mechanics rather than Pakistan-specific implementation, keep the answer general and flag that treaty-body reporting/review cycle specifics should be verified against the CRPD Committee's current record.

## Extraction Workflow

1. Identify the jurisdiction at issue (ICT/federal vs. a specific province) before citing a specific statute, since disability legislation is not uniform post-devolution.
2. If the question concerns the employment quota, confirm which jurisdiction's quota percentage and covered-employer threshold is being asked about, and hedge the specific current percentage rather than asserting one fixed number as universally current.
3. If the question concerns CRPD, distinguish Pakistan's ratification/international-obligation layer from actual domestic implementing legislation, and avoid overstating the completeness of domestic alignment.
4. If the question concerns registration/certification of disability status, attribute this function to the (National/Provincial) Council for Rehabilitation of Disabled Persons or equivalent current body, hedging on the exact current institutional name/structure.
5. Note explicitly when a claim is a legal/statutory requirement versus an aspirational policy statement, since disability-rights legislation in Pakistan (as elsewhere) has historically faced an implementation gap between statutory rights and practical enforcement.

## Technical Rules

- Disability welfare/rehabilitation legislation is a provincial subject post-18th Amendment; do not describe the ICT Persons with Disabilities Act 2020 as automatically applicable in Punjab, Sindh, KP, or Balochistan.
- The employment quota is a statutory minimum threshold requiring covered employers to reserve a specified percentage of positions for persons with disabilities; do not state a single fixed percentage as the current nationwide figure without an explicit "(verify current jurisdiction-specific percentage)" hedge, since the quota percentage and covered-employer threshold vary by jurisdiction/era and have been subject to proposed revision.
- CRPD ratification obligates Pakistan to progressively align domestic law/policy with the Convention; ratification itself does not automatically make CRPD provisions directly enforceable domestic law absent implementing legislation — do not conflate ratification with automatic domestic legal effect.
- Distinguish the older welfare/rehabilitation-model framing (1981 Ordinance era) from the newer rights-based/CRPD-aligned framing (ICT 2020 Act and similar reforms) when describing the evolution of Pakistani disability law.
- The Council for Rehabilitation of Disabled Persons (national and/or provincial) is the body historically responsible for disability registration/certification and quota-compliance oversight; do not attribute this function to BISP or an education department without verification.

## Validation Checklist

- Confirm the jurisdiction (ICT/federal vs. specific province) before citing a specific disability statute.
- Confirm the employment-quota percentage/threshold is hedged as jurisdiction- and vintage-specific rather than stated as one universal current figure.
- Confirm CRPD ratification is described as an international obligation requiring domestic implementation, not as automatically self-executing domestic law.
- Confirm registration/certification and quota-oversight functions are attributed to the Council for Rehabilitation of Disabled Persons (or verified current equivalent), not conflated with BISP or school-administration bodies.
- Confirm the answer is not actually a request for cash-transfer figures or school-facility statistics better routed elsewhere.

## Common Pitfalls

- Treating the ICT Persons with Disabilities Act 2020 as a uniform national statute applicable in all provinces.
- Stating a single fixed employment-quota percentage as the current universal figure without hedging jurisdiction/vintage variation.
- Conflating CRPD ratification with automatic, self-executing domestic legal enforceability.
- Presenting the older 1981-Ordinance welfare/rehabilitation model and the newer rights-based/CRPD-aligned model as identical rather than noting the framing shift.
- Conflating this skill's legal-framework scope with BISP disability-linked payment data or school-facility accessibility statistics.
- Overstating the practical implementation/enforcement of quota and accessibility requirements as fully realized rather than noting the commonly documented gap between statutory rights and enforcement capacity.

## Reference

- See [Pakistan Disability Rights Framework Reference](references/pakistan-disability-rights-framework.md) for the devolution-era legislative landscape, quota mechanics, and CRPD/Council structure detail.
