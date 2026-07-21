---
name: secp-corporate-insolvency-rehabilitation
description: Pakistan corporate insolvency, rehabilitation, and winding-up skill. Use when analyzing a distressed company's options under the Corporate Rehabilitation Act 2018 (court-supervised rescue, moratorium, rehabilitation plan) versus winding-up/liquidation under the Companies Act 2017, including insolvency practitioner appointment, creditor ranking, and the practical gap between the statutory rescue framework and its use in practice.
---

# SECP Corporate Insolvency & Rehabilitation

## Overview

Use this skill for advanced/practitioner-level questions on Pakistani corporate insolvency law: whether a distressed company should pursue court-supervised rehabilitation under the Corporate Rehabilitation Act, 2018 (CRA 2018), or is instead headed toward winding-up/liquidation under the Companies Act, 2017; how a moratorium and rehabilitation plan work procedurally; how an insolvency practitioner/administrator is appointed and supervised; and how creditors are ranked and paid out in a liquidation. This is a company-law-insolvency skill, not a personal bankruptcy skill, and not a general company-registration skill.

## Coverage

- **Legal basis for rehabilitation**: The Corporate Rehabilitation Act, 2018 (CRA 2018), enacted following the earlier Corporate Restructuring Companies Act, 2016 (which created a distinct vehicle — corporate restructuring companies — for acquiring and restructuring non-performing loans/distressed assets, and is a different mechanism from CRA 2018's court-supervised rescue of a company itself). The Corporate Rehabilitation Regulations, 2019 (SECP SRO 1415(I)/2019) supplement the Act procedurally.
- **Rehabilitation mechanism**: a company (or its creditors, subject to conditions) may apply to the relevant court for rehabilitation proceedings; on admission, a moratorium/stay of legal proceedings against the company is generally triggered, an administrator/rehabilitation practitioner is appointed or supervises the process, and a rehabilitation plan is formulated for creditor approval and court sanction. Treat the exact procedural sequencing, voting thresholds, and moratorium scope as needing verification against the Act's current text and Regulations rather than asserting precise mechanics from memory, since insolvency procedure is detail-sensitive and errors here have real consequences for a distressed client.
- **Winding-up/liquidation under the Companies Act, 2017**: the separate, older track — voluntary winding-up (members' or creditors') and compulsory/court winding-up (petition to the court, typically on grounds including inability to pay debts), leading to appointment of an Official Liquidator/liquidator, realization and distribution of assets, and eventual dissolution of the company.
- **Insolvency practitioners**: SECP maintains a panel of insolvency experts (established under the CRA 2018 framework) from which administrators/practitioners for rehabilitation cases may be drawn; treat panel composition and qualification criteria as SECP-published and subject to change, verify current panel/list against SECP's own page rather than an outdated cached list.
- **Creditor ranking in liquidation**: general company-law liquidation priority (liquidation costs, certain preferential/statutory dues, secured creditors per their security, unsecured creditors pro rata, and shareholders last) — the precise statutory ranking and any preferential-debt categories (e.g., employee dues, certain government dues) must be verified against the Companies Act 2017's current winding-up provisions rather than assumed from general comparative-insolvency intuition, since exact preferential categories and their order are jurisdiction-specific and have been amended.
- **Practical gap**: Pakistan's corporate rescue culture is young — CRA 2018 was explicitly framed as a shift toward a rescue-oriented regime (modeled conceptually on frameworks like Chapter 11/UK administration), but actual reported use of CRA 2018 rehabilitation proceedings has been limited relative to the number of distressed companies in the economy; SECP has run stakeholder consultations on strengthening the insolvency and debt-enforcement framework, indicating the regime is still evolving. Do not assume CRA 2018 rehabilitation is a well-trodden, high-volume process — flag this as a comparatively new and lightly-used mechanism whose case law is still developing.

## Use This Skill For

- explaining the difference between CRA 2018 court-supervised rehabilitation and Companies Act 2017 winding-up/liquidation, and which a distressed company might pursue
- explaining the general procedural shape of a rehabilitation application: filing, moratorium, administrator appointment, plan formulation, creditor approval, court sanction
- explaining the general procedural shape of voluntary vs. compulsory winding-up under the Companies Act 2017
- describing the role and appointment of an insolvency practitioner/administrator or Official Liquidator
- describing general creditor-ranking logic in a liquidation at a conceptual level, while flagging that exact statutory priority categories need verification
- distinguishing CRA 2018 (company rescue) from the Corporate Restructuring Companies Act 2016 (a distinct NPL-acquisition-vehicle mechanism) — these are frequently confused because both concern "corporate restructuring"

## When Not to Use This Skill

- For an individual's personal bankruptcy/insolvency (a different, and comparatively underdeveloped, area of Pakistani law not covered here) — this skill is company-law-specific.
- For a company's basic registration status, incorporation date, or category — use `secp-company-registry`.
- For a company's annual filings, beneficial-ownership disclosure, or general SECP compliance calendar — use `secp-annual-returns-beneficial-ownership`.
- For a bank's or NBFC's own prudential/capital distress and regulatory intervention by SBP (as opposed to an ordinary company's rehabilitation/winding-up under the Companies Act/CRA 2018) — banking-sector resolution follows a different, SBP-led regulatory framework not detailed in this skill; flag this distinction rather than applying CRA 2018 mechanics to a bank.
- For definitive advice on an active rehabilitation or winding-up petition — recommend a licensed corporate/insolvency lawyer and the applicable court's own rules; this skill is structural/procedural orientation, not case-specific legal advice.

## Routing Rules

- If the question is about whether a company exists or its basic registration details, route to `secp-company-registry`.
- If the question is about annual return filing or beneficial ownership disclosure obligations rather than distress/insolvency, route to `secp-annual-returns-beneficial-ownership`.
- If the question conflates the Corporate Restructuring Companies Act 2016 (NPL-acquisition vehicles) with the Corporate Rehabilitation Act 2018 (company rescue proceedings), disambiguate explicitly before answering — they are separate statutes with separate purposes, both part of the same broader 2016-2018 legislative push but operating differently.
- If the question is about a bank or NBFC specifically, note that SBP-led prudential/resolution mechanisms may apply in addition to or instead of the ordinary Companies Act/CRA 2018 framework, and that this skill's detail is oriented to ordinary (non-financial-sector) companies.
- If the question is about competition-law implications of a distressed-asset sale or merger arising from insolvency, note that CCP merger control may still apply and route the competition-clearance angle to `ccp-competition-enforcement` or `ccp-merger-control-technical`.

## Extraction Workflow

1. Identify whether the question concerns rescue (rehabilitation under CRA 2018) or exit/wind-down (winding-up/liquidation under the Companies Act 2017) — these are different tracks with different triggers, outcomes, and practitioner roles.
2. If rehabilitation, identify which procedural stage is at issue: application/admission, moratorium, administrator appointment, plan formulation, creditor voting, or court sanction — do not assume a later stage has occurred without confirmation.
3. If winding-up, identify whether it is voluntary (members'/creditors') or compulsory (court-ordered), since the initiating process, control over the liquidator, and creditor involvement differ materially between the two.
4. For any creditor-ranking or priority-of-payment question, state the general conceptual order (costs of liquidation, preferential/statutory dues, secured creditors, unsecured creditors, shareholders) but flag the precise statutory categories and their exact order as needing verification against the Companies Act 2017's current winding-up provisions.
5. For an insolvency-practitioner/administrator question, note that SECP maintains a panel framework under the CRA 2018 and direct the user to SECP's own published panel/list for current, named practitioners rather than asserting specific names or numbers.
6. Always note that CRA 2018 rehabilitation is a comparatively new and lightly-used mechanism in practice — do not imply a large, mature body of Pakistani rehabilitation case law exists unless specifically verified for the case in question.
7. Flag that this is a structural/procedural overview, not legal advice for an active proceeding, and recommend a licensed insolvency/corporate lawyer for case-specific application.

## Technical Rules

- CRA 2018 (rehabilitation/rescue) and the Companies Act 2017 (winding-up/liquidation) are two distinct legal tracks with different objectives — rehabilitation aims to rescue a viable but distressed company as a going concern; winding-up aims to realize and distribute assets and dissolve the company. Do not describe a company as "in insolvency proceedings" without specifying which track.
- The Corporate Restructuring Companies Act, 2016 is not the same statute as the Corporate Rehabilitation Act, 2018 — the 2016 Act enables specialized companies to acquire and restructure non-performing loans/distressed assets from financial institutions; the 2018 Act provides the court-supervised rescue mechanism for a distressed company itself. Do not use these names interchangeably.
- A moratorium/stay triggered by admission into rehabilitation proceedings generally restrains creditor enforcement action against the company for the duration of the proceedings — but the exact scope (which creditors, which types of claims, any carve-outs such as secured-creditor rights) must be verified against the Act's current text rather than assumed to be absolute.
- An insolvency practitioner/administrator role in rehabilitation is distinct from an Official Liquidator's role in winding-up — the former is oriented to rescue and plan formulation, the latter to asset realization and distribution; do not use the titles interchangeably.
- Creditor priority in liquidation is not "first come, first served" — it follows a statutory ranking (liquidation costs, certain preferential dues, secured creditors per their security, unsecured creditors pro rata, shareholders last), and the precise categories/order must be confirmed against the Companies Act 2017's current text for any case-specific claim.
- CRA 2018's practical uptake has been limited; do not present it as a heavily litigated, well-precedented regime — note explicitly that reported rehabilitation case volume is low relative to the size of Pakistan's distressed-company population, and that SECP has itself acknowledged the need to strengthen the insolvency/debt-enforcement framework through stakeholder consultation.

## Validation Checklist

- Confirm whether the question is about rehabilitation (CRA 2018) or winding-up/liquidation (Companies Act 2017) before answering.
- Confirm the Corporate Restructuring Companies Act 2016 is not being confused with the Corporate Rehabilitation Act 2018.
- Confirm any creditor-ranking claim is flagged as needing verification against the Companies Act 2017's current winding-up provisions rather than stated as settled fact with invented category names or order.
- Confirm the procedural stage (application, moratorium, administrator appointment, plan, court sanction / voluntary vs. compulsory winding-up) is correctly identified rather than assumed.
- Confirm the answer does not overstate CRA 2018's practical case volume or maturity of precedent.
- Confirm the answer recommends a licensed insolvency/corporate lawyer for an active, case-specific matter.

## Common Pitfalls

- Confusing the Corporate Restructuring Companies Act 2016 (NPL-acquisition vehicles) with the Corporate Rehabilitation Act 2018 (company rescue proceedings) — they sound similar but do different things.
- Treating CRA 2018 rehabilitation as a mature, high-volume, well-precedented process comparable to Chapter 11 practice in the US — Pakistan's rescue culture under this Act is still young and lightly used.
- Asserting a specific, invented statutory creditor-priority order or preferential-debt category without flagging it as needing verification against the Companies Act 2017's current text.
- Treating "insolvency practitioner" and "Official Liquidator" as interchangeable titles when they serve different functions in rehabilitation versus winding-up.
- Applying ordinary-company CRA 2018/Companies Act 2017 mechanics to a bank or NBFC without flagging that SBP-led prudential/resolution frameworks may separately or instead apply.
- Presenting this skill's structural overview as sufficient legal advice for an active rehabilitation or winding-up petition.

## Reference

- See [SECP Corporate Insolvency & Rehabilitation Reference](references/secp-corporate-insolvency-rehabilitation.md) for the statutory framework, procedural stage structure, and source list.
