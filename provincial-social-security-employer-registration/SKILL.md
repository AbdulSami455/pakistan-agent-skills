---
name: provincial-social-security-employer-registration
description: Provincial social security employer registration skill. Use when explaining employer registration, employee coverage, and contribution obligations under Pakistan's provincial employee social security institutions, especially for HR, payroll, and factory/commercial establishment compliance.
---

# Provincial Social Security Employer Registration

## Overview

Use this skill for employer compliance with provincial employee social security institutions in Pakistan, such as PESSI, SESSI, and equivalent provincial bodies. This is the right skill for office teams handling employee registration, contribution workflow, and institution-specific coverage questions around medical and cash social-security benefits.

## Coverage

- Provincial employee social security institution structure by province.
- Employer registration and employee enrollment for covered establishments.
- Contribution and payroll-linked compliance concepts.
- Distinction between provincial social security and EOBI old-age benefits.
- Province-specific jurisdiction and the practical reality that labour/welfare compliance is not centralized federally.

## Use This Skill For

- identifying which provincial social security institution applies to an employer
- explaining establishment and employee registration workflow at a high level
- distinguishing social security from EOBI and income tax withholding
- guiding HR/payroll teams on the structure of recurring contribution compliance
- clarifying that provincial jurisdiction matters for labour welfare administration

## When Not to Use This Skill

- For EOBI old-age benefit contributions, use `eobi-employer-contributions` instead.
- For salary tax withholding, use the relevant FBR tax skills instead.
- For workers welfare fund or profit participation obligations, use `workers-welfare-fund-profit-participation` instead.

## Routing Rules

- Use this skill when the question concerns provincial employee social security registration and contributions.
- If the issue is retirement/old-age benefits, route to `eobi-employer-contributions`.
- If the issue is a province-specific labour office or establishment regime, keep the applicable province explicit rather than presenting one national rule.
- Do not collapse medical/social-security coverage, old-age benefits, and tax withholding into a single "payroll deduction" concept.

## Extraction Workflow

1. Identify the province and the employer's establishment type.
2. Confirm whether the issue is employer registration, employee enrollment, or contribution/payment compliance.
3. Preserve the distinction between province-specific institution and federal institutions like EOBI.
4. Note whether the question concerns covered employees, benefits-linked documentation, or payroll process.
5. If a multi-province employer is involved, keep each province's institution separate.

## Technical Rules

- Social security institutions are provincially administered and are not interchangeable across provinces.
- Employee registration, contribution payment, and access to benefits are linked but distinct operational steps.
- Social security compliance should not be merged with EOBI or with tax withholding in explanations.
- Coverage rules, wage thresholds, and contribution percentages can vary and should be tied to the relevant province's current institution guidance.

## Validation Checklist

- Confirm the province and applicable institution.
- Verify that the question is about provincial social security rather than EOBI.
- Check whether numeric contribution references are current and province-specific.
- Preserve the difference between employer registration and employee enrollment.

## Common Pitfalls

- Treating Pakistan employee social security as a single federal system.
- Confusing provincial social security with EOBI.
- Generalizing one province's compliance practice to another province.
- Treating employee medical/social coverage contributions as income tax deductions.

## Reference

- See [Provincial Social Security Employer Registration Reference](references/provincial-social-security-employer-registration.md) for institution structure and extraction notes.
