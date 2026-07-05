---
name: nts-testing-service
description: NTS (National Testing Service Pakistan) skill. Use when looking up NAT (National Aptitude Test), GAT (Graduate Assessment Test), or NTS's job/recruitment testing services, including test types, registration process, schedules, and how NTS scores are used for university admission or public-sector job eligibility.
---

# NTS Testing Service

## Overview

Use this skill for Pakistan's National Testing Service (NTS), a widely used standardized-testing body whose scores feed into both university graduate-program admissions and public-sector job recruitment shortlisting. This is a test-structure and process reference skill, not a live test-schedule lookup (schedules change frequently and should be confirmed directly on NTS's site) or a university-specific admission skill.

## Coverage

- NAT (National Aptitude Test): used primarily for undergraduate admission eligibility at some institutions; has category variants (e.g., NAT-IM for pre-medical/pre-engineering-adjacent categories, IE/ICS/ICOM by academic background) run multiple times a year.
- GAT (Graduate Assessment Test): used for graduate/Master's and PhD program admission eligibility (HEC often requires a GAT-General or subject GAT score for scholarship or program eligibility); has General and Subject variants.
- HAT (HEC-mandated tests) and other one-off recruitment/screening tests NTS administers on behalf of public-sector organizations for job shortlisting.
- Registration is per-test-cycle via the NTS website or authorized centers, with fees payable through common mobile-wallet/bank channels.
- NTS also conducts custom recruitment tests for specific government departments/organizations advertising a position, distinct from the standardized NAT/GAT cycles.

## Use This Skill For

- clarifying which NTS test (NAT vs. GAT, and which variant) applies to a specific admission or job-eligibility requirement
- explaining the general structure/purpose of NAT or GAT (without asserting a specific, possibly outdated test date)
- distinguishing NTS's standardized recurring tests from a one-off recruitment test NTS is administering for a specific job advertisement
- clarifying that NTS scores are an eligibility/shortlisting input, not the sole admission or hiring decision
- directing a user to the correct current source (NTS's own site) for exact test dates, since these are published per cycle and change frequently

## When Not to Use This Skill

- For a specific university's admission merit list or closing merit — use `pakistan-university-admissions` instead; NTS scores may feed into eligibility, but the merit list itself belongs to the admitting institution.
- For FBISE or provincial-board school-level exams — use `fbise-curriculum-exams` instead; NTS tests are post-secondary/graduate-level and job-recruitment tests, not board exams.
- For citing an exact upcoming test date as fact — always caveat that schedules should be confirmed on NTS's official site, since this skill's structural description can become stale.

## Routing Rules

- Use this skill to explain what a specific NTS test is, its purpose, and its general structure; do not use it as an authoritative source for a specific cycle's exact date without flagging that it should be confirmed with NTS directly.
- If the question is really about a university's own admission decision after the test, route to `pakistan-university-admissions` for the merit-list side of the process.
- If the question is about school-level (Matric/Intermediate) exams rather than post-secondary or job-recruitment testing, route to `fbise-curriculum-exams` or note the relevant provincial board instead.

## Extraction Workflow

1. Identify which test the question concerns: NAT (undergraduate-level aptitude), GAT (graduate-level), or a custom recruitment test for a specific job advertisement.
2. If a variant matters (e.g., GAT-General vs. GAT-Subject, or NAT category), confirm which one the underlying admission/job requirement specifies.
3. For registration or schedule questions, describe the general process (online registration, fee payment channels, roll-number slip download) while directing to NTS's official site for the current cycle's exact dates.
4. Clarify how the score is used downstream — as a minimum eligibility threshold, a weighted component of a composite merit formula, or a shortlisting cutoff — since this varies by the institution or organization using the NTS score.

## Technical Rules

- NAT and GAT are administered on a recurring multi-cycle-per-year basis; do not state a specific date/cycle as still valid without noting it needs reconfirmation.
- GAT-General and GAT-Subject serve different purposes (general graduate eligibility vs. subject-specific assessment); do not conflate them.
- An NTS score is typically one input into a receiving institution's or organization's own eligibility/merit formula — it does not by itself guarantee admission or selection.
- Custom recruitment tests NTS administers for a specific government position are one-off and distinct from the standardized recurring NAT/GAT cycles.

## Validation Checklist

- Confirm which specific test (NAT, GAT-General, GAT-Subject, or a named custom recruitment test) is relevant to the question.
- Flag any specific test date or cycle as needing confirmation against NTS's current official schedule.
- Clarify whether the score is being used for university admission eligibility or public-sector job shortlisting, since the downstream process differs.
- Confirm the score is described as an input to, not a guarantee of, the final admission/selection outcome.

## Common Pitfalls

- Citing a specific past test date/cycle as if it were still upcoming or currently valid.
- Confusing NAT (undergraduate-level) with GAT (graduate-level) test purposes.
- Treating an NTS score as equivalent to a guaranteed admission or job offer rather than an eligibility/shortlisting input.
- Assuming a single "NTS test" when the question may actually concern a custom one-off recruitment test for a specific job posting.

## Reference

- See [NTS Reference](references/nts-testing-service.md) for test types and extraction notes.
