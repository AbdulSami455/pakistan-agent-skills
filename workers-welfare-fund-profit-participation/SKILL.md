---
name: workers-welfare-fund-profit-participation
description: Workers welfare fund and profit participation skill. Use when explaining employer obligations around Pakistan's Workers Welfare Fund (WWF) and Workers' Profit Participation Fund (WPPF), especially for finance, HR, and payroll/compliance teams handling statutory worker-welfare calculations.
---

# Workers Welfare Fund and Profit Participation

## Overview

Use this skill for employer obligations tied to statutory worker-welfare funding and profit participation in Pakistan, especially WWF and WPPF concepts that recur in finance, audit, HR, and annual-close work. This is the right skill when the question is about labour-linked statutory allocations rather than ordinary salary tax or social-security contributions.

## Coverage

- Workers Welfare Fund compliance concept and its statutory character.
- Workers' Profit Participation Fund concept and employer-side allocation logic.
- Distinction between payroll-period deductions/contributions and year-end profit-linked allocations.
- Office workflow implications for finance, audit, HR, and statutory-compliance teams.
- Interaction boundaries with labour welfare, tax, and corporate reporting.

## Use This Skill For

- explaining the difference between WWF and WPPF
- identifying when a finance or HR team needs to consider these obligations
- distinguishing monthly payroll-type compliance from annual profit-linked calculations
- summarizing why these obligations appear in audit and statutory-compliance discussions
- separating worker-welfare funds from EOBI, provincial social security, and income tax

## When Not to Use This Skill

- For EOBI employer contributions, use `eobi-employer-contributions` instead.
- For provincial employee social security registration, use `provincial-social-security-employer-registration` instead.
- For general corporate income tax filing, use FBR-related skills instead.

## Routing Rules

- Use this skill when the question is specifically about statutory worker-welfare or profit-participation obligations.
- If the issue is ordinary monthly payroll deductions or old-age/social-security registration, route to the EOBI or provincial social security skills instead.
- If the question is about company profits generally rather than worker-linked statutory allocations, do not over-route here.
- Keep accounting treatment and labour-law basis distinct where the source does.

## Extraction Workflow

1. Identify whether the question concerns WWF, WPPF, or both.
2. Confirm whether the issue is legal applicability, calculation logic, or practical office workflow.
3. Preserve the difference between a welfare levy/fund obligation and a profit-sharing allocation.
4. Note whether the context is monthly payroll, annual close, audit, or employee-distribution mechanics.
5. If the source mentions tax treatment separately, keep it distinct from the worker-welfare obligation itself.

## Technical Rules

- WWF and WPPF are not the same obligation and should not be described interchangeably.
- These obligations are conceptually distinct from EOBI and provincial social security contributions.
- Profit-linked allocations should not be misdescribed as flat monthly deductions unless the source explicitly frames a payment schedule that way.
- Applicability thresholds, calculation bases, and exemptions can change and should be anchored to the current governing framework.

## Validation Checklist

- Confirm whether WWF, WPPF, or both are in scope.
- Verify whether the question is about applicability, computation, or payment/distribution workflow.
- Check whether the context is annual-close/audit or recurring payroll compliance.
- Preserve separation from EOBI, social security, and income tax.

## Common Pitfalls

- Treating WWF and WPPF as the same statutory obligation.
- Folding worker-welfare obligations into ordinary payroll taxes.
- Ignoring that WPPF is tied to profit-linked logic rather than simple employee headcount.
- Quoting thresholds or percentages without tying them to the current framework.

## Reference

- See [Workers Welfare Fund and Profit Participation Reference](references/workers-welfare-fund-profit-participation.md) for source structure and extraction notes.
