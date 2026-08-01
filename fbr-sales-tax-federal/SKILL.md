---
name: fbr-sales-tax-federal
description: Federal Sales Tax on goods skill. Use when explaining or analyzing sales tax registration, the standard sales tax rate, zero-rating/exemptions, input/output tax adjustment, or Sales Tax Return (STR) filing under the Sales Tax Act 1990 as administered by FBR through IRIS/e-FBR — as distinct from provincial sales tax on services, federal income tax, or customs duty.
---

# FBR Federal Sales Tax (Goods)

## Overview

Use this skill for Pakistan's federal Sales Tax on **goods**, levied and administered by the Federal Board of Revenue (FBR) under the **Sales Tax Act, 1990**. This covers registration thresholds, the standard rate, the input/output tax credit mechanism, and the Sales Tax Return (STR) filing cycle through FBR's IRIS/e-FBR portal. It is a transaction/consumption tax on the supply of goods, structurally and administratively separate from provincial sales tax on services and from FBR's own income tax and customs regimes.

## Coverage

- **Legal basis**: The Sales Tax Act, 1990, and its Rules, govern sales tax on the supply of taxable goods and on goods imported into Pakistan (import-stage sales tax is collected alongside customs duty at import but under the Sales Tax Act's charging provisions). FBR's Inland Revenue wing administers domestic-supply sales tax; import-stage sales tax collection is operationally handled at the customs stage via WeBOC/PSW but the underlying levy is a Sales Tax Act liability, not a customs duty.
- **Registration**: Persons/entities making taxable supplies above prescribed thresholds (or falling into specified categories such as manufacturers, importers, wholesalers, distributors, and certain retailers) are required to register for sales tax and obtain a Sales Tax Registration Number (STRN) — thresholds and categorical triggers are periodically revised by FBR/Finance Act amendments and should be verified for the applicable tax period rather than assumed fixed (verify current figure).
- **Standard rate**: The Sales Tax Act specifies a standard ad valorem rate applied to the value of taxable supplies, with the exact percentage subject to change via Finance Act amendments — always verify the currently applicable standard rate rather than citing a remembered historical figure (verify current rate).
- **Zero-rating and exemptions**: Certain supplies (e.g., specified exports, and categories notified under the Act's Schedules) are zero-rated (taxed at 0% with input tax still refundable/adjustable), while others are wholly exempt (no output tax charged, and corresponding input tax is generally not adjustable) — zero-rating and exemption are legally distinct treatments with different input-tax consequences, and the specific goods/sectors covered are listed in the Act's Schedules, which are amended periodically.
- **Input/output tax mechanism**: A registered person charges output tax on taxable supplies made and can adjust/claim credit for input tax paid on purchases used in making taxable supplies, remitting only the net difference; input tax attributable to exempt supplies is generally not adjustable, requiring apportionment where a registered person makes both taxable and exempt supplies.
- **Return filing**: Registered persons file a monthly Sales Tax Return (STR), commonly referenced as the STR-7 or via FBR's current e-filing form nomenclature, through the IRIS/e-FBR portal, declaring output tax, input tax, and net payable/refundable position for the tax period — filing and payment deadlines are set by FBR and should be verified for the current period rather than assumed unchanging.
- **Sales Tax Special Procedures/Withholding**: FBR also operates Sales Tax Special Procedures Rules and a sales tax withholding regime for specified categories of buyers/withholding agents, which modify the standard charge/collect mechanism for particular sectors — treat these as sector-specific overlays on the general Act rather than the default rule.

## Use This Skill For

- explaining who must register for federal sales tax and the general registration trigger logic
- explaining the standard sales tax rate concept and where zero-rating/exemption differs from it
- explaining the input/output tax adjustment mechanism and net payable/refundable computation
- describing the monthly Sales Tax Return filing cycle through IRIS/e-FBR
- distinguishing sales tax on goods from provincial sales tax on services and from customs duty at import
- explaining the difference between zero-rated and exempt supplies for input-tax-credit purposes

## When Not to Use This Skill

- For sales tax on **services** (e.g., restaurants, telecom, professional services) administered by provincial revenue authorities — use `provincial-sales-tax-authorities` (PRA/SRB/KPRA/BRA); services sales tax sits under provincial statutes, not the federal Sales Tax Act, 1990.
- For federal **income tax** filing, withholding on salary/business income, or return-of-income obligations — use `fbr-individual-tax-filing`.
- For **customs duty** and tariff classification on imports — use `fbr-customs-tariff`; note that import-stage sales tax is collected alongside customs duty operationally, but the underlying legal basis and this skill's scope is the Sales Tax Act charge, not the customs tariff schedule itself.
- For FBR's aggregate revenue collection statistics/yearbook figures rather than the mechanics of the tax itself — use `fbr-yearbook`.

## Routing Rules

- If the transaction involves a supply of goods (manufacture, import, wholesale, distribution, retail of tangible goods), use this skill.
- If the transaction involves a service (even if invoiced alongside goods), route the services portion to `provincial-sales-tax-authorities` and identify the correct provincial authority (PRA for Punjab, SRB for Sindh, KPRA for Khyber Pakhtunkhwa, BRA for Balochistan; Islamabad Capital Territory services fall under a federal ICT sales tax regime — verify current administering body).
- If the question is about income tax withholding obligations layered on the same transaction, route the income-tax angle to `fbr-individual-tax-filing`.
- If the question is about the customs duty/tariff classification of an imported good rather than the import-stage sales tax charge, route to `fbr-customs-tariff`.

## Extraction Workflow

1. Confirm the supply in question is of goods (not services) before applying this skill; mixed transactions may require routing parts to different skills.
2. Identify whether the question concerns registration obligation, rate/exemption status, input/output adjustment, or return filing mechanics.
3. Flag any specific registration threshold, standard rate percentage, or filing deadline as needing current-period verification rather than stating a remembered figure as presently accurate.
4. Distinguish zero-rated supplies (0% rate, input tax still adjustable/refundable) from exempt supplies (no output tax, input tax generally not adjustable) — do not use the terms interchangeably.
5. If a withholding or special-procedure regime is implicated (e.g., a specified withholding agent buyer), note that it modifies the general charge/collect default rather than assume the standard mechanism applies unmodified.

## Technical Rules

- Do not state a specific standard sales tax rate or registration threshold as a fixed, timeless figure — these are amended through Finance Acts and SROs and must be verified for the applicable tax period.
- Keep zero-rating and exemption analytically separate; conflating them produces wrong input-tax-credit conclusions.
- Do not describe provincial services sales tax as part of the Sales Tax Act, 1990 framework — it is governed by separate provincial statutes with separate administering authorities.
- Treat import-stage sales tax as a Sales Tax Act liability collected via the customs process, not as a component of the customs duty/tariff rate itself.
- Preserve the distinction between a registered person's output tax liability and their net payable/refundable position after input tax adjustment.

## Validation Checklist

- Confirm the transaction is a supply of goods, not services, before applying this skill.
- Confirm any rate, threshold, or deadline cited is flagged for current-period verification.
- Confirm zero-rated vs. exempt classification is correctly applied for input-tax-credit purposes.
- Confirm services-sales-tax questions are routed to the correct provincial authority skill, not answered here.
- Confirm customs-duty/tariff-classification questions are routed to `fbr-customs-tariff`.

## Common Pitfalls

- Treating provincial sales tax on services as governed by the Sales Tax Act, 1990, when it is a separate provincial-statute regime.
- Conflating zero-rated and exempt supplies, leading to incorrect input-tax-credit conclusions.
- Citing a fixed standard rate or registration threshold without noting it is subject to Finance Act revision.
- Confusing the Sales Tax Return (STR) filing cycle with the federal income tax return filing cycle, which has separate forms and deadlines.
- Treating import-stage sales tax collection as equivalent to, or part of, customs duty rather than a distinct Sales Tax Act charge collected at the same border-clearance stage.

## Reference

- See [FBR Federal Sales Tax Reference](references/fbr-sales-tax-federal.md) for the Act's structure, registration/return mechanics, and sourcing notes.
