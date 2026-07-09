---
name: ipo-pakistan-trademarks
description: IPO Pakistan trademarks skill. Use when explaining trademark search, filing, opposition, renewal, and classification workflow under IPO Pakistan, especially for businesses handling brand-name clearance and office-level intellectual property administration.
---

# IPO Pakistan Trademarks

## Overview

Use this skill for trademark workflow in Pakistan through the Intellectual Property Organization of Pakistan (IPO Pakistan): brand-name clearance, class selection, filing, publication, opposition, and renewal. This is the right skill for practical business and legal-office work around protecting names, logos, and marks, not for generic branding advice.

## Coverage

- Trademark search and brand-clearance logic.
- Filing workflow under IPO Pakistan and broad goods/services class structure.
- Publication, examination, objection, opposition, registration, and renewal stages.
- Distinction between a business/company name and a registered trademark right.
- Office-side workflow for maintaining mark status, renewal cycle, and class coverage.

## Use This Skill For

- explaining how to check whether a proposed brand may conflict with an existing mark
- distinguishing trademark registration from SECP company registration
- guiding office/legal teams on class-based filing logic
- clarifying objection/opposition stages in the trademark process
- explaining renewal and ongoing maintenance at a high level

## When Not to Use This Skill

- For SECP company incorporation or company-name registry checks, use `secp-company-registry` instead.
- For deceptive-marketing competition cases after commercial conduct occurs, `ccp-competition-enforcement` may be relevant for the competition-law side.
- For patents or designs, this skill does not apply unless IPO Pakistan trademark material explicitly cross-references them.

## Routing Rules

- Use this skill for trademarks and brand-right workflow under IPO Pakistan.
- If the task is only to verify a company's legal existence, route to `secp-company-registry`.
- Do not treat SECP name approval or incorporation as creating trademark rights.
- Keep classification and filing-stage logic explicit because trademark rights are class-specific and process-driven.

## Extraction Workflow

1. Identify whether the issue is pre-filing search, fresh filing, objection/opposition, registration, or renewal.
2. Confirm whether the mark is a word mark, logo/device mark, or combined mark if the source makes that distinction.
3. Preserve the relevant class or classes and whether the mark covers goods or services.
4. Note whether the question is about procedural stage or substantive conflict risk.
5. Separate trademark registration status from general business-use or company-registration status.

## Technical Rules

- A company name registered with SECP is not the same as a registered trademark.
- Trademark rights are class-specific; one registration does not automatically cover every product or service category.
- Publication and opposition are distinct stages; publication does not itself guarantee registration.
- Renewal and ongoing maintenance matter because trademark rights are not a one-time office task.

## Validation Checklist

- Confirm the issue is trademark-specific rather than company-registration specific.
- Verify whether the question concerns search, filing, opposition, registration, or renewal.
- Check whether the relevant class coverage is preserved.
- Distinguish mark type and filing stage if the source does.

## Common Pitfalls

- Assuming SECP incorporation protects a brand as a trademark.
- Ignoring class selection and treating a trademark as universally protective.
- Treating publication as final registration.
- Confusing office-use of a logo/name with an actual registered right.

## Reference

- See [IPO Pakistan Trademarks Reference](references/ipo-pakistan-trademarks.md) for workflow stages and extraction notes.
