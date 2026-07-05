---
name: fbr-individual-tax-filing
description: FBR individual income tax filing skill. Use when explaining how an individual (salaried or non-salaried) registers for an NTN, files an annual income tax return, or submits a wealth statement through FBR's IRIS portal, including filer status, active taxpayer list (ATL), and general filing process — as distinct from aggregate tax-collection statistics.
---

# FBR Individual Tax Filing

## Overview

Use this skill for an individual Pakistani taxpayer's process of registering with and filing returns through the Federal Board of Revenue (FBR), via the IRIS online portal. This is a process/how-it-works reference skill for citizens and students entering the tax system, not a tax-collection statistics skill and not a substitute for professional tax advice on a specific complex filing.

## Coverage

- NTN (National Tax Number) registration: how an individual registers for a tax number, typically linked to their CNIC for individuals.
- IRIS portal: FBR's online system for return filing, wealth statement submission, tax payments, and related e-services (the current version is IRIS 2.0).
- Annual income tax return: the general structure — income declaration (salary, business, property, other sources), tax credits/deductions, and computed tax liability or refund.
- Wealth statement: a required annual declaration of assets and liabilities for individuals above certain criteria, filed alongside the income tax return.
- Filer status and the Active Taxpayer List (ATL): being on the ATL (a "filer") generally carries lower withholding tax rates on various transactions compared to a "non-filer."
- e-Payment: FBR's online tax payment channel (via IRIS or associated payment systems) for any tax due.

## Use This Skill For

- explaining the general steps to register for an NTN and access IRIS as an individual
- describing what an annual income tax return and wealth statement generally require
- clarifying the practical difference between "filer" (on the ATL) and "non-filer" status
- explaining the general structure of income tax filing categories (salaried vs. business/other income individuals)
- directing a user to official FBR channels for current tax rates, deadlines, or forms, since these change by tax year (Finance Act amendments)

## When Not to Use This Skill

- For FBR's aggregate tax collection statistics (by tax head, sector) — use `fbr-yearbook` instead; this skill is about an individual's filing process, not national revenue figures.
- For customs duty/tariff schedules on imported goods — use `fbr-customs-tariff` instead.
- For property valuation tables used in tax calculation — use `fbr-property-valuation` instead; this skill explains the filing process, not valuation rates.
- For providing definitive advice on a specific person's complex tax situation — recommend consulting a tax professional or FBR's own helpdesk instead of treating this skill as authoritative for an individual case.

## Routing Rules

- Use this skill for how-to/process questions about NTN registration, IRIS filing, wealth statements, and filer/non-filer status for an individual.
- If the question is about aggregate revenue or collection statistics rather than an individual's own filing, route to `fbr-yearbook`.
- If the question is about customs or property valuation rather than income tax filing, route to `fbr-customs-tariff` or `fbr-property-valuation` respectively.
- Always caveat specific tax rates, slabs, deadlines, and thresholds as subject to change via each year's Finance Act; direct the user to FBR's current official notifications for the applicable tax year.

## Extraction Workflow

1. Identify whether the individual is a first-time registrant (needs NTN registration) or an existing taxpayer needing to file a return for a specific tax year.
2. Identify the income category: salaried individual, business individual/AOP, or a mix (salary plus property/other income) — filing forms and requirements can differ by category.
3. Confirm the specific tax year in question, since tax slabs, rates, and thresholds are revised annually via the Finance Act and should not be assumed constant across years.
4. Distinguish the income tax return itself from the wealth statement — both are typically required annually for return-filers above the applicable threshold, but they capture different information (income/tax vs. assets/liabilities).
5. If the question involves filer/non-filer implications (e.g., withholding tax on a transaction), clarify that being on the current year's Active Taxpayer List is what confers filer status, not merely having an NTN.

## Technical Rules

- Tax year in Pakistan's individual income tax system typically runs July-June, and rates/slabs are set per Finance Act for that year — do not apply one year's slab to another year's income without confirming.
- Having an NTN is necessary but not sufficient for "filer" status — filer status specifically means appearing on the current Active Taxpayer List (ATL), which requires having filed the return for the relevant tax year.
- The wealth statement and income tax return are distinct filings submitted together; do not conflate wealth reconciliation with income computation.
- IRIS 2.0 is the current portal version; older references to "e.fbr.gov.pk" or legacy IRIS may describe superseded interfaces.

## Validation Checklist

- Confirm which tax year the question is about before citing any rate, slab, or deadline.
- Verify whether the individual is asking about registration (NTN), return filing, or wealth statement specifically.
- Check whether "filer status" in the question refers to ATL inclusion rather than simply NTN possession.
- Flag that specific current rates/deadlines should be verified against FBR's official IRIS portal or notifications rather than treated as fixed.

## Common Pitfalls

- Citing a prior tax year's slabs or deadlines as current without checking for Finance Act revisions.
- Treating NTN registration alone as equivalent to "filer" status without confirming ATL inclusion.
- Confusing the wealth statement (assets/liabilities) with the income tax return (income/tax computation).
- Offering definitive advice on a complex individual tax scenario instead of recommending professional or official FBR guidance.

## Reference

- See [FBR Individual Tax Filing Reference](references/fbr-individual-tax-filing.md) for portal structure and extraction notes.
