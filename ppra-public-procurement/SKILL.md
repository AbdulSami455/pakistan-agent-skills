---
name: ppra-public-procurement
description: Public Procurement Regulatory Authority (PPRA) skill. Use when explaining federal government procurement rules, procurement methods and thresholds, tender-notice publication, or firm blacklisting under the PPRA Ordinance 2002 and PPRA Rules 2004 — and for distinguishing federal PPRA from the separate provincial procurement authorities (Punjab PPRA, Sindh PPRA, KPPRA, BPPRA, GB PPRA).
---

# PPRA Public Procurement

## Overview

Use this skill for questions about how Pakistan's federal government procures goods, works, and services — the rules, methods, thresholds, and tender-publication requirements set by the Public Procurement Regulatory Authority (PPRA). PPRA is a rule-setting and oversight body: it does not itself buy anything or spend public money. Each procuring agency (a federal ministry, department, or public-sector entity) conducts its own procurement under PPRA's rules. Provinces run their own, separately legislated procurement regimes — this skill covers the federal PPRA framework and flags the provincial split explicitly.

## Coverage

- **Legal basis**: The Public Procurement Regulatory Authority Ordinance, 2002, and the Public Procurement Rules, 2004 (PPRA Rules), issued under the Ordinance, which set out procurement methods, thresholds, and mandatory procedures for federal procuring agencies.
- **Procurement methods**: open competitive bidding (the default method), and specified exceptions such as limited tendering, direct contracting/single-source procurement, and request-for-quotation for low-value purchases — each permitted only under conditions set out in the Rules.
- **Thresholds**: monetary thresholds that determine which procurement method/procedure applies and what publication/advertisement requirements are triggered (e.g., higher-value procurements generally require wider advertisement, including on PPRA's own portal); (verify current Rupee threshold values against PPRA's latest notified rules/SROs, as these are revised periodically and older cached figures go stale).
- **e-Procurement / tender publication**: PPRA operates a public tender-notice portal/e-procurement system where federal procuring agencies are required to advertise tender opportunities; PPRA also historically required advertisement in national newspapers alongside the website, and has moved toward electronic procurement (e-Pak Acquisition and Disposal System / similar platforms — verify current platform name and mandatory-use status).
- **Blacklisting**: PPRA Rules provide a mechanism for procuring agencies/PPRA to blacklist a firm or supplier found to have violated procurement rules (e.g., submitting false documents, non-performance, collusive bidding), barring it from future government contracts for a specified period.
- **Federal-provincial split**: PPRA (federal) rules apply only to federal government procuring agencies. Each province operates its own separate procurement regulatory authority and rules: Punjab Procurement Regulatory Authority (PPRA-Punjab), Sindh Public Procurement Regulatory Authority (SPPRA), Khyber Pakhtunkhwa Public Procurement Regulatory Authority (KPPRA), Balochistan Public Procurement Regulatory Authority (BPPRA), and a Gilgit-Baltistan procurement regime (GB PPRA) — each with its own ordinance/rules and its own tender portal.

## Use This Skill For

- explaining which procurement method applies to a federal government purchase of a given estimated value
- explaining the default rule of open competitive bidding and the conditions under which an exception (limited tendering, direct contracting, request for quotations) is permissible
- explaining where a federal government tender notice would be published and what advertisement requirements apply
- explaining PPRA's blacklisting mechanism and its effect on a firm's eligibility for future contracts
- distinguishing federal PPRA rules from a specific province's procurement authority and rules
- clarifying that PPRA is a rule-setting/oversight body, not a spending or contract-executing agency

## When Not to Use This Skill

- For a specific province's procurement rules or tender notices (e.g., a Punjab government department's tender) — route to that province's own procurement authority (Punjab PPRA / SPPRA / KPPRA / BPPRA / GB PPRA); this skill covers the federal framework only, though it can be used to explain the jurisdictional split itself.
- For federal or provincial budget allocations/spending amounts — use `federal-budget-documents` or `provincial-budget-documents`; PPRA governs the procurement process, not the budget that funds it.
- For development-project execution details (e.g., a specific PSDP-funded project's status) — use `psdp-federal-development-programme`; PPRA governs how a procuring agency buys goods/works/services, not project planning or funding decisions.
- For a company's registration/incorporation status — use `secp-company-registry`; PPRA's blacklisting mechanism is a separate, procurement-specific eligibility bar, not a corporate-registration status.
- For competition-law/antitrust issues in a bid-rigging case (e.g., a cartel colluding on government tenders) — such conduct may also engage `ccp-competition-enforcement` under the Competition Act's prohibited-agreements provisions; use PPRA for the procurement-process/blacklisting angle and CCP for the antitrust angle, and note both can apply to the same underlying facts.

## Routing Rules

- If the question specifies a province (Punjab, Sindh, KP, Balochistan) or Gilgit-Baltistan, and asks about that province's procurement rules or a provincial department's tender — flag that federal PPRA rules do not apply, and that the relevant provincial procurement authority's own rules and portal govern instead.
- If the question is about how much money was budgeted or spent, rather than the procurement method/process used to spend it — route to `federal-budget-documents` or `provincial-budget-documents`.
- If the question is about a specific development project's implementation — route to `psdp-federal-development-programme` for federal development-project tracking; use this skill only for the procurement-process rules governing how that project's contracts were/should be awarded.
- If the question involves suspected bid-rigging/collusion among bidders — note that this may be both a PPRA blacklisting matter and a `ccp-competition-enforcement` antitrust matter; address the procurement-eligibility angle here and route the antitrust/cartel angle to CCP.
- If the question is about a firm's corporate registration status rather than its procurement-eligibility (blacklist) status — route to `secp-company-registry`.

## Extraction Workflow

1. Confirm whether the procuring agency is federal or provincial — this determines whether federal PPRA Rules or a provincial authority's rules apply. Federal ministries, divisions, attached departments, and federal public-sector entities fall under PPRA; provincial departments and provincial public-sector entities fall under their own province's authority.
2. Identify the estimated procurement value to determine which method/threshold tier applies (open competitive bidding vs. a permitted exception) — check PPRA's current Rules/SROs for the applicable Rupee thresholds rather than relying on a possibly outdated remembered figure.
3. Confirm which procurement method was actually used (open competitive bidding, limited tendering, direct contracting, request for quotations) and whether the Rules permit that method for the stated value/circumstances.
4. Check where the tender notice was/should be published — PPRA's website/e-procurement portal, and (historically) national newspapers — and note if publication requirements were not met.
5. For blacklisting questions, confirm which procuring agency initiated the blacklisting action, the stated grounds, the duration/scope of the bar, and whether it was PPRA-confirmed or is under challenge.
6. Always state explicitly whether the matter falls under federal PPRA or a named provincial authority before citing a rule as applicable.

## Technical Rules

- PPRA (federal) rules bind only federal procuring agencies; they do not automatically apply to provincial government procurement, which is governed by that province's own procurement law and rules. Do not cite federal PPRA thresholds/rules for a provincial tender without noting this distinction.
- PPRA is a regulatory/rule-setting and oversight body — it does not itself execute contracts, disburse payments, or act as a purchasing agency. The procuring agency (the actual ministry/department/entity) is the contracting party, not PPRA.
- Open competitive bidding is the default/preferred method under the Rules; other methods (limited tendering, direct contracting/single-source, request for quotations) are permitted only in specified, limited circumstances (e.g., proprietary items, emergencies, very low-value purchases) — do not treat exceptions as routine alternatives.
- Monetary thresholds for method selection and advertisement requirements are set by rule/SRO and are revised periodically — do not present a specific Rupee figure as current without verifying against PPRA's latest notified rules.
- Blacklisting is a procurement-eligibility bar, not a criminal conviction or a corporate-registration status change — a blacklisted firm may still be a validly registered SECP company; the two statuses are independent.

## Validation Checklist

- Confirm whether the procuring agency is federal (PPRA applies) or provincial (the relevant provincial authority applies).
- Confirm the procurement method cited is one of the Rules-recognized methods and matches the value tier claimed.
- Verify any cited monetary threshold against PPRA's current rules rather than an older remembered figure.
- Confirm blacklisting claims specify the procuring agency, grounds, and duration, and whether the action is final or under challenge.
- Confirm the question is not actually a budget/spending question (route those to the budget skills) or a project-implementation question (route to `psdp-federal-development-programme`).

## Common Pitfalls

- Treating PPRA as a spending/executing agency rather than a rule-setting and oversight body.
- Applying federal PPRA thresholds or rules to a provincial government tender without checking which provincial authority actually governs it.
- Treating limited tendering or direct contracting as a routine alternative to open competitive bidding rather than a conditions-gated exception.
- Citing an outdated procurement threshold figure as current.
- Conflating PPRA blacklisting (procurement-eligibility bar) with a company's SECP registration status, a criminal conviction, or a CCP antitrust finding — these are four separate and independent things.
- Assuming a single, unified "PPRA" covers the whole country — federal PPRA and the four provincial authorities plus GB's regime each have their own separate rules and portals.

## Reference

- See [PPRA Public Procurement Reference](references/ppra-public-procurement.md) for procurement methods, threshold structure, the federal-provincial authority directory, and blacklisting mechanics.
