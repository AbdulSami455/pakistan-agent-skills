---
name: ccp-competition-enforcement
description: Competition Commission of Pakistan (CCP) antitrust/competition-enforcement skill. Use when analyzing merger clearance, abuse of dominant position, cartelization/collusion, or deceptive marketing cases and orders issued by CCP under the Competition Act 2010 — as distinct from SECP's securities/corporate-registration mandate or a court judgment.
---

# CCP Competition Enforcement

## Overview

Use this skill when a task concerns Pakistan's competition/antitrust regulator — the Competition Commission of Pakistan (CCP) — and its enforcement activity: merger review, cartel and collusion cases, abuse-of-dominance findings, or deceptive marketing orders. CCP is a quasi-judicial regulatory body, not a court, and its jurisdiction spans every sector of the economy (cement, sugar, poultry, telecom, banking, real estate, etc.), not just listed or securities-regulated companies. This is not a company-registration skill and not a general court-judgment research skill.

## Coverage

- **Legal basis**: The Competition Act, 2010, which replaced the original Competition Ordinance, 2007. CCP was first established under the 2007 Ordinance and continued under the 2010 Act after the Ordinance repeatedly lapsed/was re-promulgated in its early years.
- **Merger control**: pre-merger review and clearance of transactions that meet notified pre-merger notification thresholds (asset/turnover-based tests set out in CCP's Merger Control Regulations); CCP can approve, approve with conditions/remedies, or block a merger.
- **Abuse of dominant position**: Section 3 of the Competition Act — prohibits an undertaking with a dominant position in a relevant market from abusing that position (e.g., predatory pricing, exclusive dealing, tying, limiting production to the prejudice of consumers).
- **Prohibited agreements / cartelization**: Section 4 of the Competition Act — prohibits agreements between competitors that have the object or effect of preventing, restricting, or reducing competition, including price-fixing, market/customer allocation, and bid-rigging cartels.
- **Deceptive marketing practices**: Section 10 of the Competition Act — prohibits false or misleading claims about products/services, including comparative advertising that misleads consumers.
- **Enforcement outputs**: CCP issues show-cause notices, conducts inquiries/investigations, and issues formal Orders (including financial penalties) through its Bench(es); CCP also publishes an Annual Report and its orders/decisions are typically posted on its website.
- **Appeal path**: CCP orders can be appealed to the Competition Appellate Tribunal (CAT), and from there into the ordinary superior court hierarchy (High Court / Supreme Court) on further appeal — (verify the current appellate tribunal's operational status and composition against CCP's own published material, as the tribunal's functioning has seen periods of disruption historically).

## Use This Skill For

- explaining what a specific CCP order found (e.g., cartel, abuse of dominance, deceptive marketing) and what penalty, if any, was imposed
- explaining CCP's merger review process and what pre-merger notification thresholds trigger a filing requirement
- distinguishing CCP's competition/antitrust mandate from SECP's securities-market and company-registration mandate
- explaining the appeal path for a CCP order (Competition Appellate Tribunal, then higher courts)
- identifying which provision of the Competition Act, 2010 (Section 3 abuse of dominance, Section 4 prohibited agreements, Section 10 deceptive marketing) a case falls under
- summarizing sector-level CCP enforcement history (e.g., cement sector cartel cases, sugar sector inquiries, poultry/banking/telecom cases) at a general level

## When Not to Use This Skill

- For a company's registration status, incorporation date, or corporate category — use `secp-company-registry` instead; SECP regulates company incorporation and securities markets, CCP regulates market competition across all sectors.
- For a listed company's financial statements, disclosures, or stock data — use `psx-company-snapshots` or related PSX skills, not this one.
- For the general legislative status of the Competition Act or any amendment bill — use `parliament-legislative-tracker` for bill-tracking; use this skill only for CCP's own enforcement orders and regulatory activity.
- For a definitive legal interpretation of a CCP order under active appeal — a CCP order is not a final court judgment; do not present it as conclusively settled law if it is under appeal, and recommend consulting a qualified legal professional for an active dispute.
- For sector-specific regulatory rules that are NOT competition-related (e.g., NEPRA's electricity tariff rules, PTA's telecom licensing) — those regulators govern sector-specific conduct, while CCP governs competition conduct that can arise in any sector including those.

## Routing Rules

- If the question is about whether a company exists, its incorporation date, or its registration category — route to `secp-company-registry`; CCP does not maintain a company registry.
- If the question is about a company's securities filings, stock price, or listing status — route to the relevant `psx-*` skill.
- If the question is about a merger/acquisition's competition clearance versus its SECP/corporate-law compliance — split the answer: this skill covers CCP's merger clearance, `secp-company-registry` or corporate-law sources cover the SECP-side company-law steps (e.g., share transfer, scheme of arrangement).
- If the question is about the Competition Act's legislative history or a pending amendment bill — route to `parliament-legislative-tracker` for bill status; use this skill only once the Act's provisions are in force and being enforced.
- If a question conflates "CCP" with "SECP" because both are called "commissions" — explicitly disambiguate before answering: CCP = competition/antitrust across all sectors; SECP = securities markets, corporate registration, insurance, and non-bank finance.

## Extraction Workflow

1. Identify which type of CCP matter is being asked about: merger review, abuse of dominance, cartel/prohibited agreement, or deceptive marketing.
2. For merger questions, check whether the transaction meets CCP's notified pre-merger notification thresholds (asset or turnover-based, set in the Merger Control Regulations) — below threshold, no mandatory filing is triggered; (verify current threshold values against CCP's latest Merger Control Regulations, as these are periodically revised).
3. For enforcement questions, identify the specific Order by case/reference number and date, and note which Bench issued it.
4. State the provision engaged (Section 3 abuse of dominance, Section 4 prohibited agreements/cartels, Section 10 deceptive marketing) rather than using "antitrust violation" generically.
5. Note the penalty amount (if any) and whether it has been paid, stayed, or is under appeal — CCP orders are not final if under appeal.
6. Check whether the matter has moved to the Competition Appellate Tribunal or a higher court, and report the most current known status rather than only the original CCP order.
7. If citing sector-wide enforcement history (e.g., cement, sugar, poultry, LPG, banking), attribute each case to its own order and year rather than aggregating outcomes across unrelated cases.

## Technical Rules

- CCP is a regulatory/quasi-judicial body, not an ordinary court; an "Order" from CCP is an administrative/regulatory decision, not a court judgment, even though it can impose significant financial penalties.
- A CCP order under appeal to the Competition Appellate Tribunal or a higher court is not final — do not report a penalty as conclusively payable/paid without checking appeal status.
- CCP's jurisdiction is sector-agnostic: it applies to any "undertaking" engaged in economic activity, regardless of whether that entity is otherwise regulated by SECP, PTA, NEPRA, OGRA, SBP, or another sector regulator. Sector regulation and competition regulation are parallel, not mutually exclusive.
- Pre-merger notification thresholds are periodically revised by CCP regulation — do not assume a previously cited threshold figure is still current without checking the latest Merger Control (Amendment) Regulations.
- Do not use "CCP" and "SECP" interchangeably; they are separate statutory bodies with separate governing laws (Competition Act, 2010 vs. Securities and Exchange Commission of Pakistan Act, 1997).

## Validation Checklist

- Confirm which Competition Act provision (Section 3, 4, or 10) the matter falls under.
- Confirm whether the cited figure is a CCP-imposed penalty, a merger transaction value, or an unrelated financial figure.
- Check whether the order is final, stayed, or under appeal before describing an outcome as settled.
- Confirm the case is attributed to CCP and not mistakenly attributed to SECP, PTA, NEPRA, or another sector regulator.
- Verify pre-merger notification threshold figures against CCP's current regulations rather than an older cited value.

## Common Pitfalls

- Confusing CCP with SECP because both are "commissions regulating companies" — CCP governs competition across all sectors; SECP governs securities markets and corporate registration.
- Treating a CCP order as a final court judgment rather than an appealable regulatory decision.
- Reporting a penalty amount from a CCP order without checking whether it was later reduced, set aside, or upheld on appeal.
- Citing outdated pre-merger notification thresholds as current.
- Attributing a sector regulator's action (e.g., PTA fining a telecom operator for a licensing breach) to CCP, when it is a separate, non-competition regulatory action.

## Reference

- See [CCP Competition Enforcement Reference](references/ccp-competition-enforcement.md) for the Competition Act's structure, merger control mechanics, and sector case-history notes.
