---
name: secp-annual-returns-beneficial-ownership
description: SECP annual returns and beneficial ownership skill. Use when explaining or checking Pakistan company secretarial compliance under the Companies Act, 2017, especially for annual return filing, change-of-director/shareholder filings, and beneficial-ownership declarations through SECP eServices.
---

# SECP Annual Returns and Beneficial Ownership

## Overview

Use this skill for recurring post-incorporation compliance under SECP: annual return filing, changes in directors or shareholders, and beneficial-ownership declarations. This is the right skill for company secretarial workflow and compliance framing, not for merely checking whether a company exists in the public registry.

## Coverage

- Annual return obligations for private, public, and single-member companies under the Companies Act, 2017.
- SECP eServices / Business Registration Portal workflow for post-incorporation filings.
- Director, officer, shareholder, registered-office, and share-capital change filings where these updates trigger prescribed forms.
- Beneficial-ownership declaration requirements under the Companies Act and SECP rules/regulations.
- Filing-timeliness and default-risk context for companies that remain registered but become non-compliant.

## Use This Skill For

- explaining what a company must file annually after incorporation
- distinguishing annual return filing from financial-statement filing or tax filing
- identifying when director/shareholder/registered-office changes trigger SECP filings
- clarifying beneficial-owner declaration obligations and why they differ from legal shareholding
- guiding office/compliance teams through the structure of recurring SECP secretarial work

## When Not to Use This Skill

- For simply verifying that a company exists, use `secp-company-registry` instead.
- For tax registration, income tax filing, or sales tax registration, use the relevant FBR or provincial tax skills instead.
- For listed-company market disclosures or PSX trading information, use the relevant PSX skill instead.

## Routing Rules

- Use this skill when the task is about what a company must file with SECP after incorporation.
- If the question is "is this company registered" or "what is its incorporation date," route to `secp-company-registry`.
- Keep SECP corporate filings separate from FBR tax filings; a company may be active at SECP while being separately non-compliant for tax purposes.
- Beneficial ownership should be treated as a compliance concept distinct from the public-facing company-name search.

## Extraction Workflow

1. Identify the company type: private, public, single-member, company limited by guarantee, foreign company, or LLP where relevant.
2. Confirm whether the task concerns recurring annual filing, an event-driven change filing, or beneficial-ownership disclosure.
3. Preserve the distinction between legal shareholder, director/officer, and beneficial owner.
4. Note whether the filing is periodic or triggered by a change event.
5. If compliance status is discussed, distinguish failure to file from strike-off or dissolution.

## Technical Rules

- Annual return, financial statements, and beneficial-ownership declarations are related but distinct compliance surfaces.
- A company can remain registered while being in default or non-filing status; do not equate registry existence with full compliance.
- Beneficial ownership is not always identical to the name appearing as legal shareholder on the register.
- LLPs are governed through a separate legal regime and should not be described as companies unless the source explicitly uses that term.

## Validation Checklist

- Confirm the entity type and whether Companies Act or LLP rules apply.
- Verify whether the filing is annual, event-driven, or beneficial-ownership specific.
- Check whether the compliance question is about SECP only or is being conflated with FBR obligations.
- Preserve the difference between active registration and current filing compliance.

## Common Pitfalls

- Treating annual return filing as the same thing as income tax return filing.
- Assuming a company found in SECP search is automatically fully compliant.
- Confusing legal shareholding with beneficial ownership.
- Folding LLP compliance into company-law language without checking the governing regime.

## Reference

- See [SECP Annual Returns and Beneficial Ownership Reference](references/secp-annual-returns-beneficial-ownership.md) for filing surfaces and extraction notes.
