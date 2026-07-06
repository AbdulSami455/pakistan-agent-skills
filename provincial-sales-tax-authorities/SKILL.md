---
name: provincial-sales-tax-authorities
description: Provincial sales tax on services skill. Use when a question involves sales tax on SERVICES in Pakistan and which of the four provincial revenue authorities (PRA, SRB, KPRA, BRA) applies, service-sector tax rates, or multi-province service tax registration — as distinct from FBR's federal sales tax on goods, income tax, or customs duty.
---

# Provincial Sales Tax Authorities

## Overview

Use this skill for Pakistan's provincial sales tax on services regime: the four provincial revenue authorities — Punjab Revenue Authority (PRA), Sindh Revenue Board (SRB), Khyber Pakhtunkhwa Revenue Authority (KPRA), and Balochistan Revenue Authority (BRA) — that each independently levy, collect, and administer sales tax on services within their own province. This is the single most common source of AI agent error on Pakistani tax questions: "what is Pakistan's sales tax rate" has no single correct answer without first establishing (a) whether the transaction is a sale of goods or a supply of services, and (b) if services, which province's authority has jurisdiction. This skill exists specifically to force that disambiguation before answering.

## Coverage

- Constitutional basis: the 18th Constitutional Amendment (2010) removed "tax on services" from the Federal Legislative List, confirming/cementing sales tax on services as a provincial subject. Following this, provinces set up (or, in Sindh's case, had already begun setting up) their own dedicated sales-tax-on-services collection authorities rather than relying on FBR.
- Sindh Revenue Board (SRB): established by the Sindh Revenue Board Act, 2010; began collecting Sindh sales tax on services from 2011, making Sindh the first province to operationalize its own sales tax on services collection (predating Punjab's authority).
- Punjab Revenue Authority (PRA): established 2012 under the Punjab Revenue Authority Act, 2012, administering the Punjab Sales Tax on Services Act, 2012.
- Khyber Pakhtunkhwa Revenue Authority (KPRA): established under the KP Finance Act / KPRA Act (~2013), administering the KP Sales Tax on Services Act, 2013.
- Balochistan Revenue Authority (BRA): the last of the four to be operationalized, administering the Balochistan Sales Tax on Services Act, 2015; historically the smallest in collection base and administrative capacity among the four.
- Each authority publishes its own schedule of taxable services, its own standard rate, and sector-specific rates that can differ materially from the general rate (verify current rates against each authority's own notifications/Finance Act for the year in question — these change annually and have differed between provinces at the same point in time).
- Each authority issues its own registration number/certificate for service providers, separate from an FBR NTN and separate from registration with any other province's authority.

## Use This Skill For

- identifying which provincial authority (PRA, SRB, KPRA, or BRA) has jurisdiction over a specific service transaction
- explaining that "Pakistan's sales tax rate" differs depending on goods-vs-services and, for services, by province
- describing the general registration and return-filing obligation a service business faces with a provincial revenue authority
- explaining why a business operating in more than one province may need to register with and file returns to multiple provincial authorities simultaneously
- clarifying that a sector (e.g., telecom, IT/ITeS, franchise services, construction, advertising) may carry a sector-specific rate that differs from a given province's general services rate
- providing historical/structural context on how the 18th Amendment led to four separate provincial regimes instead of one federal one

## When Not to Use This Skill

- For sales tax on goods (still federal, collected by FBR under the Sales Tax Act 1990) — use `fbr-individual-tax-filing` (for individual filing process) or the relevant FBR skill; do not treat this skill as covering goods transactions.
- For federal income tax questions — use `fbr-individual-tax-filing`.
- For customs duty on imported goods — use `fbr-customs-tariff`.
- For aggregate federal tax collection statistics — use `fbr-yearbook`.
- For provincial budget/finance bill narrative beyond the tax-rate mechanics themselves — check `provincial-budget-documents`.

## Routing Rules

- If the question concerns sales tax on **goods**, income tax, or customs duty at the **federal** level, route to `fbr-individual-tax-filing` or `fbr-customs-tariff` as applicable — this skill covers sales tax on **services** at the **provincial** level only.
- If the question is a bare "what is the sales tax rate in Pakistan" with no goods/services distinction stated, do not answer with a single number; first disambiguate goods vs. services, and if services, which province.
- If a service is rendered from one province but consumed/received in another, flag this as a genuinely contested/complex jurisdictional question under each province's sales tax on services act (place-of-supply rules differ and have been litigated); do not assert a confident single answer without noting the ambiguity and recommending verification against the specific provincial act's place-of-supply provisions.
- If the question involves a business with operations/service delivery in multiple provinces, note the realistic possibility of needing multi-authority registration (e.g., SRB + PRA + FBR for a business with both goods and multi-province services activity) rather than assuming one registration suffices.
- For provincial finance bill/budget narrative beyond the rate mechanics, prefer `provincial-budget-documents`.

## Extraction Workflow

1. Determine whether the transaction in question is a supply of **goods** or a supply of **services**. If goods, this skill does not apply — route to the federal FBR skills.
2. If services, determine where the service is rendered/provided from, and where it is consumed/received, since jurisdiction generally follows the province where the service is rendered — but note that each province's Sales Tax on Services Act defines "provision"/"rendering" slightly differently, and cross-province service transactions can trigger disputes or dual-registration exposure.
3. Identify the specific province (Punjab -> PRA, Sindh -> SRB, KP -> KPRA, Balochistan -> BRA) and map to that authority's own governing act.
4. Identify the specific service category involved (e.g., telecom, banking/financial, IT/ITeS, construction, advertising, franchise, courier, consultancy) since rates are frequently sector-specific rather than a single flat rate.
5. Do not assume a rate quoted for one province or one sector applies to another province or another sector; state explicitly that the figure should be verified against the specific authority's current Finance Act notification.
6. If the business operates in multiple provinces, enumerate each authority it may need to register with separately, plus FBR if it also deals in goods.

## Technical Rules

- There is no single "Pakistan sales tax on services rate" — each of the four provincial authorities sets its own general rate and its own sector-specific rates, and these are revised independently via each province's own annual Finance Act, so they can and do diverge from each other and from the federal goods sales tax rate.
- General/standard provincial services rates in recent years have commonly clustered in a mid-to-high-teens percentage range, but sector-specific rates (telecom services in particular have commonly been set noticeably higher than a province's general services rate) can differ substantially — always attach the specific service category and specific province to any rate cited, and treat any specific percentage as needing verification against that authority's current notification rather than presenting it as a fixed, evergreen figure.
- Registration with one province's authority does not confer registration with another province's authority or with FBR; each is a separate registration, filing, and compliance obligation.
- Do not conflate "Sindh was first to establish its own authority" with "Sindh necessarily has the highest or lowest rates" — chronological precedence in establishment is unrelated to current rate levels.
- The 18th Amendment did not create a uniform national services-tax law; it removed the subject from the federal list, which is precisely why four independent provincial regimes exist instead of one.

## Validation Checklist

- Confirm goods vs. services before citing any sales tax rate or authority.
- Confirm which specific province's authority (PRA/SRB/KPRA/BRA) applies before citing a rate or registration requirement.
- Confirm whether the service falls under a sector-specific rate rather than the province's general rate.
- Flag any specific numeric rate as subject to change via that province's most recent Finance Act and recommend verification against the authority's own current notification.
- If the transaction spans provinces, flag the place-of-supply/jurisdiction question as potentially contested rather than asserting a single confident answer.

## Common Pitfalls

- Answering "what is Pakistan's sales tax rate" with a single number without first separating goods (federal, FBR) from services (provincial, four separate authorities).
- Assuming FBR administers sales tax on services — it does not; each province administers its own services tax through its own authority.
- Treating one province's general services rate as applicable to another province or to a different sector within the same province.
- Assuming a multi-province service business only needs to register once; in practice it may need separate registration with each relevant provincial authority (and FBR for any goods activity).
- Presenting Sindh's chronological head start in establishing SRB as evidence about current rate levels or administrative quality relative to the other three authorities.
- Treating a cross-province service delivery's provincial jurisdiction as settled and obvious when it can, in practice, be genuinely contested.

## Reference

- See [Provincial Sales Tax Authorities Reference](references/provincial-sales-tax-authorities.md) for authority-by-authority structural notes.
