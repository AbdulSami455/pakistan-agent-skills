---
name: eobi-employer-contributions
description: EOBI employer contributions skill. Use when explaining or analyzing employer registration, insured-person coverage, and monthly old-age benefit contributions under Pakistan's Employees' Old-Age Benefits Institution (EOBI), especially for payroll and HR compliance work.
---

# EOBI Employer Contributions

## Overview

Use this skill for employer-side compliance with Pakistan's Employees' Old-Age Benefits Institution (EOBI): registration, insured-person coverage, contributions, and payroll-linked recordkeeping. This is the right skill for recurring HR and payroll office work around old-age benefits, not for general labour-market statistics.

## Coverage

- Employer registration under EOBI and the broad logic of establishment coverage.
- Insured-person enrollment and employee coverage concepts.
- Employer and employee contribution structure as applied through payroll.
- Monthly contribution filing/payment workflow and recordkeeping expectations.
- Benefit-link context only to the extent needed to understand why contribution and insurable-wage classification matter.

## Use This Skill For

- explaining whether an employer likely falls into EOBI coverage
- identifying what office/payroll teams must track for EOBI compliance
- distinguishing employee coverage and insured-person registration from other labour registrations
- summarizing how EOBI contributions fit into monthly payroll operations
- clarifying how EOBI differs from provincial social security institutions

## When Not to Use This Skill

- For provincial social security and medical/cash benefit coverage, use `provincial-social-security-employer-registration` instead.
- For income tax withholding on salary, use `fbr-individual-tax-filing` and related tax skills instead.
- For labour-force statistics or employment-rate analysis, use `pbs-labour-force-survey` instead.

## Routing Rules

- Use this skill for old-age benefits and payroll-linked EOBI registration/contribution questions.
- If the question is about medical treatment, employment injury, or province-specific social-security institutions, route to `provincial-social-security-employer-registration`.
- Do not treat EOBI as a generic replacement for all employee-welfare compliance; it is one institution in a broader employer-compliance stack.
- Keep legal coverage logic separate from current contribution amounts where those amounts are revised or administratively updated.

## Extraction Workflow

1. Identify the employer type and whether the question concerns registration, employee coverage, or monthly contributions.
2. Confirm whether the issue is establishment coverage, employee eligibility, or payment/compliance process.
3. Preserve the distinction between employer contribution, employee deduction, and total contribution liability.
4. Note whether the question concerns ongoing payroll practice or dispute/default context.
5. If another institution is mentioned, separate EOBI from provincial social security and from tax withholding.

## Technical Rules

- EOBI coverage and provincial social-security coverage are separate compliance surfaces and should not be merged.
- Payroll deduction logic should be kept distinct from overall employer cost or total compensation.
- Employee registration/coverage status matters because entitlement and contribution records are linked to insured-person treatment.
- Exact contribution rates, wage ceilings, and threshold conditions can change and should be tied to the current EOBI framework rather than assumed timelessly.

## Validation Checklist

- Confirm the question is about EOBI rather than provincial social security.
- Verify whether the issue is employer registration, employee coverage, or contribution payment.
- Check whether any numeric contribution reference is current and attached to the applicable EOBI rules.
- Preserve the distinction between employer share and employee share where the source does.

## Common Pitfalls

- Confusing EOBI with provincial social security institutions.
- Treating old-age benefit contributions as if they were income tax withholding.
- Quoting contribution amounts without checking the current EOBI structure.
- Assuming every employee-welfare question belongs to one unified institution.

## Reference

- See [EOBI Employer Contributions Reference](references/eobi-employer-contributions.md) for source structure and extraction notes.
