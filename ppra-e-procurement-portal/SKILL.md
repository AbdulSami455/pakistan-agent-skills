---
name: ppra-e-procurement-portal
description: PPRA e-procurement portal and bid-mechanics skill. Use when a task needs the fine-grained operational process of Pakistan's federal e-procurement system — vendor/supplier registration on the e-Pak Acquisition and Disposal System (e-PADS) portal, bid security/bid bond and performance guarantee mechanics, technical-vs-financial bid evaluation sequencing, and the grievance redressal mechanism under PPRA Rules 2004 — as distinct from the general procurement-methods/thresholds/blacklisting policy already covered by `ppra-public-procurement`.
---

# PPRA e-Procurement Portal & Bid Mechanics

## Overview

Use this skill for the operational, process-level layer of federal public procurement in Pakistan: how a vendor registers and participates on PPRA's e-procurement portal, how bid security/performance guarantee instruments work, how technical and financial bids are sequenced and evaluated, and how a bidder pursues a grievance against a procuring agency's decision. This skill is deliberately scoped narrower than `ppra-public-procurement`, which already covers the governing law, procurement-method selection (open competitive bidding vs. exceptions), monetary thresholds, and the blacklisting mechanism at a policy level. This skill assumes that policy context and goes one layer deeper into the portal/bid/grievance mechanics a vendor or procuring-agency official actually executes.

## Coverage

- **e-Procurement portal / e-PADS**: PPRA has moved federal procurement toward electronic tendering through its e-procurement system (commonly referenced as the e-Pak Acquisition and Disposal System, e-PADS, or PPRA's e-procurement portal — confirm the current official platform name and mandatory-use status against PPRA's own site, since platform branding and rollout scope have evolved). The portal is used by procuring agencies to publish tender notices and by registered vendors/suppliers to view, download bidding documents, and (depending on the procurement and the portal's current functional scope) submit bids electronically.
- **Vendor/supplier registration**: participating in electronic tendering generally requires a vendor to register on the portal (creating a supplier profile, submitting company/registration documents such as SECP/NTN details, and obtaining portal login credentials) as a prerequisite step separate from bidding on any specific tender.
- **Bid security (bid bond)**: procuring agencies require bidders to submit a bid security (a bank guarantee, pay order, or similar instrument, typically a percentage of the bid/estimated contract value) alongside a bid, to deter frivolous or non-serious bids; a losing bidder's bid security is normally released/returned, while a winning bidder's bid security is typically retained until replaced by a performance guarantee upon contract signing.
- **Performance guarantee**: the successful bidder is generally required to furnish a performance guarantee (a bank guarantee for a percentage of the contract value) upon contract award, securing the procuring agency against non-performance during the contract's execution period — a separate instrument from the bid security, issued at a different stage of the procurement cycle.
- **Bid evaluation sequencing**: for procurements using a two-envelope (technical and financial) system, PPRA Rules require technical bids to be evaluated and bidders to meet the technical qualification threshold before financial bids are opened — financial bids of technically non-responsive bidders are generally not opened, a sequencing safeguard meant to prevent price from influencing technical evaluation.
- **Grievance redressal mechanism**: PPRA Rules provide for a bidder to file a written grievance with the procuring agency (not PPRA directly, in the first instance) within a specified time window after a procurement decision, to be addressed by a grievance redressal committee constituted by the procuring agency — a structured, time-bound complaint process distinct from a general legal challenge.

## Use This Skill For

- explaining how a vendor registers on PPRA's e-procurement portal and what documentation that typically requires
- explaining bid security (bid bond) mechanics: when it's required, typical form (bank guarantee/pay order), and release conditions
- explaining performance guarantee mechanics as a separate, post-award instrument from bid security
- walking through two-envelope (technical/financial) bid evaluation sequencing and why financial bids of technically non-responsive bidders are not opened
- explaining the grievance redressal process under PPRA Rules 2004 — where a bidder files a complaint, the applicable time window, and the committee mechanism

## When Not to Use This Skill

- For which procurement method applies to a purchase (open competitive bidding vs. limited tendering vs. direct contracting), monetary thresholds, or the general federal-vs-provincial procurement-authority split — use `ppra-public-procurement`; that skill covers the policy/method-selection layer this skill assumes as background.
- For the blacklisting mechanism itself (grounds, duration, effect on eligibility) — use `ppra-public-procurement`; this skill's grievance-mechanism coverage is about disputing a specific procurement decision, not the separate blacklisting sanction.
- For a company's SECP registration/incorporation status (relevant background for vendor registration documentation, but a separate lookup) — use `secp-company-registry`.
- For budget allocations funding a procurement — use `federal-budget-documents` or `provincial-budget-documents`.
- For antitrust/bid-rigging concerns among bidders — use `ccp-competition-enforcement`.

## Routing Rules

- Start with `ppra-public-procurement` for the governing law, procurement-method selection, and threshold questions; use this skill only once the task is specifically about portal registration, bid-security/performance-guarantee mechanics, evaluation sequencing, or the grievance process.
- If the question is about a firm's blacklisting (grounds/duration/effect), route to `ppra-public-procurement`, not this skill's grievance-mechanism coverage — blacklisting is a sanction imposed on a firm, while the grievance mechanism is a bidder's own complaint route against a procuring agency's decision.
- If the question is about verifying a vendor's underlying corporate registration (as opposed to its portal registration), route to `secp-company-registry` for the SECP-registration angle and use this skill only for the portal-registration process itself.
- If the question involves suspected collusion among bidders rather than a single bidder's grievance against the procuring agency, route to `ccp-competition-enforcement` for the antitrust angle.

## Extraction Workflow

1. Confirm whether the question needs procurement-method/threshold policy (route to `ppra-public-procurement`) or portal/bid/grievance operational mechanics (use this skill).
2. For portal-registration questions, describe the general registration-then-bid sequence (supplier profile creation, document submission, credential issuance, then tender-specific bid submission) rather than asserting exact current form-field requirements, which are portal-UI-level detail subject to change.
3. For bid-security questions, distinguish it clearly from the performance guarantee: bid security accompanies the bid itself (pre-award), while the performance guarantee is furnished after contract award (post-award) — do not use the terms interchangeably.
4. For evaluation-sequencing questions, confirm whether the procurement uses single-stage/single-envelope, single-stage/two-envelope, or two-stage bidding (PPRA Rules recognize more than one bidding procedure), since the technical-before-financial opening sequence specifically applies to two-envelope procedures.
5. For grievance questions, confirm the grievance is filed with the **procuring agency** (via its constituted grievance redressal committee) in the first instance, not directly with PPRA as an appellate body, and note the process is time-bound from the relevant procurement decision.
6. Flag any specific current bid-security percentage, performance-guarantee percentage, or grievance filing deadline as needing verification against PPRA's current Rules/SROs, since these are specified figures subject to revision.

## Technical Rules

- Bid security and performance guarantee are distinct instruments issued at different procurement-cycle stages; do not conflate them or use the terms interchangeably.
- In a two-envelope bidding procedure, financial bids of bidders who fail technical evaluation are not opened — do not describe technical and financial evaluation as happening simultaneously or in a single combined step for two-envelope procurements.
- The grievance redressal mechanism under PPRA Rules is procuring-agency-level in the first instance (a committee constituted by that agency), not a direct complaint to PPRA itself as a first step — do not describe PPRA as the immediate adjudicator of a bidder's grievance.
- Vendor portal registration is a prerequisite, general-purpose step (creating a standing supplier profile) separate from submitting a bid on any specific tender — do not conflate "registering on the portal" with "bidding on a tender."
- Do not state a specific current bid-security percentage, performance-guarantee percentage, or grievance-filing time window as fixed without flagging it as needing verification against PPRA's current Rules/SROs.

## Validation Checklist

- Confirm whether the task needs policy-layer procurement-method/threshold detail (route to `ppra-public-procurement`) or process-layer portal/bid/grievance mechanics (this skill).
- Confirm bid security and performance guarantee are described as separate instruments at separate stages.
- Confirm the bidding-procedure type (single-envelope vs. two-envelope vs. two-stage) is identified before describing evaluation sequencing.
- Confirm the grievance process is described as procuring-agency-level in the first instance.
- Flag any specific percentage or deadline figure as needing current verification.

## Common Pitfalls

- Treating bid security and performance guarantee as the same instrument or interchangeable terms.
- Describing technical and financial bid evaluation as simultaneous when a two-envelope procedure applies, when PPRA Rules require sequential (technical-first) evaluation.
- Describing PPRA itself as the first-instance adjudicator of a bidder's grievance, when the Rules route the initial grievance to the procuring agency's own committee.
- Conflating a vendor's e-procurement portal registration with SECP corporate registration — these are separate registrations for separate purposes.
- Citing a specific current bid-security percentage, performance-guarantee percentage, or grievance deadline as fixed without a verification flag.

## Reference

- See [PPRA e-Procurement Portal Reference](references/ppra-e-procurement-portal.md) for portal/vendor-registration detail, bid-security and performance-guarantee mechanics, and the grievance redressal process.
