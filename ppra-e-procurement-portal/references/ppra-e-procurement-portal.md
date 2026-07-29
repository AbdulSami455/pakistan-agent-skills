# PPRA e-Procurement Portal Reference

## Source

- Public Procurement Regulatory Authority: `https://www.ppra.org.pk`
- PPRA e-procurement portal (tender notices, e-Pak Acquisition and Disposal System / e-PADS — confirm current official platform name and URL against PPRA's own site, as branding and rollout scope have evolved): linked from `https://www.ppra.org.pk`
- Public Procurement Rules, 2004 (as amended) and related PPRA regulations/SROs — published under PPRA's laws/regulations section: `https://www.ppra.org.pk`

## e-Procurement Portal / e-PADS

PPRA has progressively moved federal procurement toward electronic tendering, operating a web-based procurement portal for publishing tender notices and, for participating procuring agencies/categories, supporting electronic bid submission and processing. The platform has been referenced under names including the e-Pak Acquisition and Disposal System (e-PADS) as PPRA has developed and expanded its e-procurement capability; the exact current platform name, its mandatory-use scope (which procuring agencies/procurement categories are required to use it versus still permitted paper-based tendering), and its functional maturity (whether it supports full electronic bid submission or primarily tender-notice publication) should be verified against PPRA's current site rather than assumed fixed, since this has been an evolving rollout.

**Structural point**: regardless of the specific platform branding at any point in time, the functional roles are consistent — procuring agencies use the portal to publish tender notices (a publication requirement under the Rules, historically supplementing newspaper advertisement for higher-value procurements), and prospective bidders use it to view/download tender documents and, where supported, register as suppliers and submit bids.

## Vendor/Supplier Registration

Before bidding on a specific tender, a vendor typically completes a portal-level supplier/vendor registration, distinct from bidding on any individual tender:

- Registration generally requires submitting company identification/registration documents (e.g., SECP incorporation/registration details for a company, or equivalent business-registration documents for other entity types) and tax registration details (NTN), plus creating login credentials for the portal.
- This registration establishes a standing supplier profile that can then be used to bid on multiple tenders over time, rather than being a one-off, tender-specific submission.
- Exact current form fields, document-upload requirements, and any registration fee should be confirmed against the portal's current interface, since these are UI/process-level details subject to change independent of the underlying Rules.

## Bid Security (Bid Bond)

- **Purpose**: PPRA Rules require bidders on most procurements above a de minimis value to submit a bid security alongside their bid, to discourage frivolous, non-serious, or later-withdrawn bids.
- **Form**: typically a bank guarantee, pay order, demand draft, or other instrument acceptable to the procuring agency, usually set as a percentage of the bid value or the procuring agency's estimated cost (the exact percentage and acceptable instrument types are specified in the procuring agency's bidding documents consistent with PPRA Rules, and should be verified against the current Rules/SROs rather than assumed fixed).
- **Release**: bid security for unsuccessful bidders is normally released/returned after the procurement process concludes (contract award to the successful bidder); the successful bidder's bid security is typically retained until it is replaced by a performance guarantee at contract signing.
- **Forfeiture**: bid security can be forfeited if a bidder withdraws or modifies its bid during the bid validity period, or if the successful bidder fails to sign the contract or furnish the required performance guarantee within the specified time — a deterrent mechanism against non-serious or bad-faith bidding.

## Performance Guarantee

- **Purpose and timing**: furnished by the successful bidder upon contract award/signing (a post-award instrument), securing the procuring agency against the contractor's non-performance or default during contract execution — distinct in both purpose and timing from the pre-award bid security.
- **Form and value**: typically a bank guarantee for a specified percentage of the contract value (the exact percentage is set in the bidding documents consistent with PPRA Rules and should be verified currently rather than assumed fixed), held for the duration of the contract (or a defined portion of it, e.g., through a defects-liability/warranty period for works contracts).
- Bid security and performance guarantee should never be treated as the same instrument — one secures the bidding process itself (pre-award), the other secures actual contract performance (post-award).

## Bid Evaluation Sequencing (Two-Envelope Procedure)

PPRA Rules recognize more than one bidding procedure (single-stage/single-envelope, single-stage/two-envelope, and two-stage/two-envelope bidding, applied depending on the nature/complexity of the procurement):

- In a **two-envelope** procedure, bidders submit technical and financial proposals in separate, sealed envelopes simultaneously, but the procuring agency opens and evaluates the **technical envelope first**.
- Only bidders whose technical proposals meet the qualification threshold set in the bidding documents have their **financial envelopes opened**; financial bids of technically non-responsive bidders are returned unopened (or otherwise not considered).
- This sequencing is a safeguard intended to prevent knowledge of a bidder's price from influencing the technical evaluation, and to ensure only technically qualified bids compete on price.
- **Two-stage bidding** (used for complex procurements where the procuring agency may not be able to fully specify requirements upfront) involves an additional preliminary stage of technical dialogue/proposal refinement before final bid submission — a more elaborate procedure than standard two-envelope bidding, used only in specified circumstances under the Rules.

## Grievance Redressal Mechanism

- **First-instance forum**: a bidder aggrieved by a procuring agency's decision (e.g., rejection of its bid, the evaluation outcome, or another procurement-process decision) files a written grievance with the **procuring agency itself**, not directly with PPRA, in the first instance.
- **Grievance redressal committee**: the procuring agency is required under PPRA Rules to constitute a grievance redressal committee (comprising officers not directly involved in the procurement in question) to consider and decide the grievance.
- **Time-bound process**: the Rules specify a window within which a bidder must file its grievance after the relevant procurement decision/notification, and a window within which the committee must respond — specific day-counts should be verified against the current Rules text rather than assumed fixed.
- **Distinction from blacklisting**: the grievance mechanism is a bidder's own complaint route challenging a specific procurement decision; it is entirely separate from PPRA's blacklisting mechanism, which is a sanction a procuring agency/PPRA can impose on a firm for rule violations (covered in `ppra-public-procurement`) — a bidder can file a grievance without any blacklisting being involved, and blacklisting can occur independent of any grievance having been filed.
- **Beyond the procuring agency**: if a grievance is not satisfactorily resolved at the procuring-agency level, further recourse (e.g., to PPRA itself in an oversight capacity, or to courts) may be available depending on the circumstances and the current Rules — this escalation path should be confirmed against PPRA's current Rules text rather than assumed.

## Extraction Notes

- Always distinguish bid security (pre-award, accompanies the bid) from performance guarantee (post-award, secures contract execution).
- Always identify the bidding procedure type (single-envelope, two-envelope, two-stage) before describing evaluation sequencing.
- Always describe the grievance mechanism as procuring-agency-level in the first instance, via a constituted grievance redressal committee, not as a direct PPRA adjudication.
- Flag any specific current bid-security percentage, performance-guarantee percentage, grievance filing deadline, or portal platform name as needing verification against PPRA's current Rules/SROs and official site.
- Do not conflate vendor portal registration (an administrative prerequisite for e-tendering) with SECP corporate registration (a separate legal registration) — the former typically requires evidence of the latter as supporting documentation, but they are not the same registration.
