---
name: federal-ombudsman-wafaqi-mohtasib
description: Federal Ombudsman (Wafaqi Mohtasib) skill. Use when explaining how a citizen files a maladministration complaint against a federal government agency under the Establishment of the Office of Wafaqi Mohtasib (Ombudsman) Order 1983, the jurisdiction/exclusions of that process, the President-appeal mechanism, or Pakistan's other specialized ombudsman institutions (Banking Mohtasib, Insurance Ombudsman, Federal Tax Ombudsman, Federal Insurance Ombudsman) — as distinct from criminal-corruption or court-caseload processes.
---

# Federal Ombudsman (Wafaqi Mohtasib)

## Overview

Use this skill for the maladministration-complaint mechanism against federal government agencies in Pakistan: the Wafaqi Mohtasib (Federal Ombudsman) institution, its statutory basis, complaint process, jurisdictional scope and exclusions, appeal route, and its relationship to Pakistan's other specialized ombudsman bodies. This is a citizen-grievance/maladministration-redress skill, not a criminal-accountability or court-litigation skill.

## Coverage

- **Establishment of the Office of Wafaqi Mohtasib (Ombudsman) Order, 1983**: the founding legal instrument (a Presidential Order, later given continued constitutional/legal standing) creating the Office of the Wafaqi Mohtasib as an independent institution empowered to investigate complaints of maladministration by federal government agencies, ministries, divisions, attached departments, and other federal statutory bodies/corporations against members of the public. The Mohtasib is appointed by the President for a fixed term and functions independently of the executive in adjudicating individual complaints, though appointed by the President.
- **Maladministration defined broadly**: the Order's concept of maladministration typically covers decisions, processes, or omissions by a federal agency that are contrary to law, rules, or regulations; perverse, arbitrary, or unreasonable; based on irrelevant grounds; involve corruption, nepotism, or administrative excess/abuse; or amount to unreasonable delay in performing a statutory duty — the framework is designed to catch administrative failure broadly rather than list a narrow closed set of triggering acts.
- **Jurisdiction and exclusions**: the Wafaqi Mohtasib's jurisdiction covers federal agencies (not provincial government matters, which fall to provincial ombudsman institutions where established). Certain matters are excluded from Mohtasib jurisdiction, commonly including matters sub judice before a court/tribunal, personnel/service matters of certain categories of civil servants (subject to specific carve-outs and evolving case law), and matters concerning foreign affairs, national defence, and the armed forces — the precise exclusion list should be checked against the current consolidated text of the Order, since exclusions have been subject to amendment and judicial interpretation over time.
- **Complaint process**: complaints are typically filed free of cost, without mandatory legal representation, directly with the Wafaqi Mohtasib Secretariat (headquartered in Islamabad, with regional offices), and the Mohtasib has powers to investigate, summon records and officials, and issue a recommendation/decision (including directing implementation, and in practice can direct compensation or corrective administrative action) — informality and accessibility relative to court litigation is a core design feature of the institution.
- **Appeal to the President**: a party aggrieved by a Wafaqi Mohtasib decision may file a representation to the President of Pakistan within the prescribed period, making the President the appellate authority over the Mohtasib's findings — this is a distinguishing structural feature versus ordinary court appeals, which run through the judicial hierarchy instead.
- **Specialized ombudsman institutions**: Pakistan has established several sector-specific ombudsman offices operating on a broadly similar maladministration-redress model but with their own enabling instruments and sectoral jurisdiction: the **Banking Mohtasib Pakistan** (banking-sector consumer complaints against banks), the **Insurance Ombudsman** / **Federal Insurance Ombudsman** (insurance-sector complaints), and the **Federal Tax Ombudsman** (established under the Federal Tax Ombudsman Ordinance 2000, for maladministration complaints against tax authorities such as FBR). These are distinct offices from the Wafaqi Mohtasib, each with sector-specific jurisdiction, though conceptually part of the same broader ombudsman-model tradition in Pakistan. Provincial ombudsman (Mohtasib) offices also exist in some provinces for provincial-government maladministration, separate again from the federal institution.

## Use This Skill For

- explaining how an individual files a maladministration complaint against a federal agency with the Wafaqi Mohtasib
- explaining what counts as "maladministration" under the 1983 Order and distinguishing it from ordinary policy disagreement or a matter properly before a court
- identifying jurisdictional exclusions (sub judice matters, certain service matters, defence/foreign-affairs matters) before advising a complaint will be entertained
- explaining the appeal-to-the-President mechanism as the route beyond a Wafaqi Mohtasib decision
- distinguishing the Wafaqi Mohtasib (general federal maladministration) from the Federal Tax Ombudsman, Banking Mohtasib, and Insurance/Federal Insurance Ombudsman (sector-specific complaint bodies)
- clarifying that this is an administrative-grievance mechanism, not a criminal-prosecution or civil-litigation forum

## When Not to Use This Skill

- For NAB's criminal anti-corruption investigation-to-prosecution pipeline (inquiry, investigation, reference, Accountability Court trial), use `nab-accountability-data` instead — maladministration complaints to the Mohtasib are not criminal proceedings and do not by themselves trigger NAB action.
- For court caseload, pendency, and disposal statistics across the judiciary, use `ljcp-judicial-statistics` — the Mohtasib process is an alternative/parallel track to court litigation, not a court itself.
- For an individual banking-service complaint specifically, use `sbp-banking-consumer-protection`, which covers the bank Complaint Management Unit and Banking Mohtasib escalation route in consumer-protection terms.
- For AGP financial/compliance audit findings against government entities, use `agp-audit-reports` — a distinct accountability mechanism (financial audit) from Mohtasib maladministration complaints.

## Routing Rules

- If the complaint is against a federal government agency/ministry/attached department for administrative failure, delay, or unfair treatment, apply the Wafaqi Mohtasib framework.
- If the complaint concerns a bank specifically, route first to `sbp-banking-consumer-protection` framing, noting the Banking Mohtasib is the applicable specialized ombudsman rather than the Wafaqi Mohtasib.
- If the complaint concerns tax administration (FBR) specifically, note the Federal Tax Ombudsman as the applicable specialized forum rather than the general Wafaqi Mohtasib.
- If the underlying conduct involves an allegation of corruption warranting criminal investigation rather than administrative correction, route to `nab-accountability-data` and clarify these are different tracks that can, in principle, run in parallel.
- If the matter is already sub judice before a court, flag the jurisdictional exclusion before describing the Mohtasib complaint process as available.
- If the question is about provincial government maladministration, note that the Wafaqi Mohtasib's jurisdiction is federal, and a provincial ombudsman institution (where established) would be the relevant body instead.

## Extraction Workflow

1. Identify whether the complaint is against a federal agency (Wafaqi Mohtasib jurisdiction) or falls under a sector-specific ombudsman (banking, tax, insurance) or provincial ombudsman instead.
2. Confirm the conduct alleged fits the maladministration concept (unlawful, arbitrary, unreasonable-delay, or abuse-of-process character) rather than a policy dispute or a matter requiring criminal investigation.
3. Check jurisdictional exclusions (sub judice, certain service matters, defence/foreign-affairs) before describing the complaint as clearly within scope.
4. Describe the process: filing with the Secretariat (or regional office), investigation powers, and the Mohtasib's recommendation/decision, noting the process is designed to be free and accessible without mandatory legal representation.
5. If the outcome is contested, note the appeal-to-the-President mechanism and its prescribed time window as the next step, distinguishing it from a judicial appeal.
6. If a sector-specific ombudsman is implicated, name the correct specialized body (Banking Mohtasib, Federal Tax Ombudsman, Insurance/Federal Insurance Ombudsman) rather than defaulting to the Wafaqi Mohtasib.

## Technical Rules

- The Wafaqi Mohtasib is established under the Establishment of the Office of Wafaqi Mohtasib (Ombudsman) Order, 1983 — do not attribute its founding to a different statute or conflate it with the Federal Tax Ombudsman Ordinance 2000, which is a separate, sector-specific instrument.
- Maladministration complaints to the Mohtasib are an administrative-grievance mechanism, not a criminal proceeding; do not describe a Mohtasib finding as a criminal conviction or equate it with a NAB reference/Accountability Court outcome.
- The appellate authority over a Wafaqi Mohtasib decision is the President of Pakistan (via representation), not a court — do not describe this as a normal judicial appeal.
- The Wafaqi Mohtasib's jurisdiction is federal; provincial-government maladministration is outside its jurisdiction where a provincial ombudsman mechanism exists separately.
- Sector-specific ombudsman institutions (Banking Mohtasib, Federal Tax Ombudsman, Insurance/Federal Insurance Ombudsman) are distinct offices with their own enabling instruments and sectoral jurisdiction — do not treat a complaint properly belonging to one of these as automatically within the Wafaqi Mohtasib's general jurisdiction.
- Flag the precise current jurisdictional-exclusion list, filing timelines, and appeal window as needing verification against the current consolidated text of the 1983 Order, since exclusions and procedure have been subject to amendment and judicial interpretation.

## Validation Checklist

- Confirm the complaint is against a federal agency and fits the maladministration concept before describing Wafaqi Mohtasib jurisdiction as applicable.
- Confirm no jurisdictional exclusion (sub judice, certain service matters, defence/foreign affairs) applies.
- Confirm whether a sector-specific ombudsman (Banking Mohtasib, Federal Tax Ombudsman, Insurance/Federal Insurance Ombudsman) is the more appropriate forum before defaulting to the Wafaqi Mohtasib.
- Confirm the appeal route described is representation to the President, not a court appeal.
- Distinguish this administrative-grievance process clearly from NAB's criminal-accountability pipeline and from ordinary court litigation.

## Common Pitfalls

- Confusing the Wafaqi Mohtasib with NAB, treating a maladministration finding as equivalent to a criminal-corruption determination.
- Describing the Mohtasib's decision as appealable to a court rather than by representation to the President.
- Defaulting to the Wafaqi Mohtasib for a banking or tax complaint when the Banking Mohtasib or Federal Tax Ombudsman is the correct sector-specific forum.
- Ignoring the sub judice and service-matter jurisdictional exclusions when describing what the Mohtasib can entertain.
- Treating the 1983 Order and the Federal Tax Ombudsman Ordinance 2000 as the same instrument.

## Reference

- See [Federal Ombudsman (Wafaqi Mohtasib) Reference](references/federal-ombudsman-wafaqi-mohtasib.md) for the founding order, jurisdictional detail, and specialized-ombudsman landscape.
