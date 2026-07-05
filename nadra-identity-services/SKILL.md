---
name: nadra-identity-services
description: NADRA identity documents skill. Use when explaining CNIC, Smart Card, NICOP, POC, CRC, or FRC application processes, required documents, renewal procedures, or eligibility for Pakistan's National Database and Registration Authority services, especially for citizens or overseas Pakistanis navigating identity registration.
---

# NADRA Identity Services

## Overview

Use this skill for Pakistan's National Database and Registration Authority (NADRA) identity-document services: the Computerized National Identity Card (CNIC) and its variants for overseas Pakistanis and family registration. This is a process/eligibility reference skill, not a live application-status tracker — NADRA's own portal is the system of record for any specific application's status.

## Coverage

- CNIC (Computerized National Identity Card): mandatory identity document for Pakistani citizens aged 18+, issued under the NADRA Ordinance, 2000.
- Smart Card CNIC: the chip-based CNIC variant, functionally the same legal document as the standard CNIC but with additional security features.
- NICOP (National Identity Card for Overseas Pakistanis): identity document for Pakistani citizens residing abroad.
- POC (Pakistan Origin Card): for foreign nationals of Pakistani origin who have renounced or hold foreign citizenship, granting certain rights without full citizenship status.
- CRC (Child Registration Certificate) and FRC (Family Registration Certificate): registration documents for minors and family units respectively, often precursors to a future CNIC.
- Application channels: NADRA registration centers (Pakistan and overseas via consulates/designated centers), and NADRA's online application services for certain document types/renewals.

## Use This Skill For

- explaining which NADRA document (CNIC, NICOP, POC, CRC, FRC) applies to a specific person's citizenship/residency situation
- describing the general required-documents checklist for a first-time CNIC, renewal, or modification application
- clarifying the difference between NICOP and POC for overseas Pakistanis or people of Pakistani origin
- explaining the general application process (in-person at a registration center vs. online where available)
- directing a user to confirm current fees, processing times, or document requirements against NADRA's official channels, since these are revised periodically

## When Not to Use This Skill

- For passport application/renewal — passports are issued by the Directorate General of Immigration & Passports / Ministry of Foreign Affairs, a separate agency from NADRA; do not conflate the two even though they are often needed together.
- For tracking a specific individual's live application status — direct the user to NADRA's official tracking channel rather than asserting a status.
- For voter registration specifics — while CNIC is the basis for electoral rolls, voter-list questions belong with the Election Commission of Pakistan, not this skill.

## Routing Rules

- Use this skill to explain identity-document types, eligibility, and general process; do not use it to assert a specific applicant's current status or a specific fee/processing-time figure without flagging it as subject to change.
- If the question is about a passport rather than a CNIC/NICOP/POC, note explicitly that passports are handled by a different agency.
- If the question extends into voter registration or electoral rolls, note that this skill covers identity documents, not electoral-roll processes.

## Extraction Workflow

1. Identify the applicant's situation: resident citizen (CNIC), citizen residing abroad (NICOP), foreign national of Pakistani origin (POC), or minor/family registration (CRC/FRC).
2. Confirm whether the request is a first-time application, renewal, or modification (e.g., name/address change), since document requirements can differ.
3. Describe the general application channel (in-person registration center, overseas center/consulate, or online service where applicable) relevant to the applicant's location.
4. Flag that exact fees, processing times, and document checklists should be confirmed on NADRA's official website or center, since these are revised periodically and vary by service urgency tier (normal/urgent/executive where offered).

## Technical Rules

- CNIC is mandatory only for citizens aged 18+; minors are registered via CRC, which is a distinct document type, not an early CNIC.
- NICOP is for Pakistani citizens abroad; POC is for foreign nationals of Pakistani origin who do not hold Pakistani citizenship — these serve different legal populations and should not be used interchangeably.
- Passport issuance is handled by a separate agency from NADRA; do not describe passport requirements as part of NADRA's own service list.
- Processing tiers (normal, urgent, executive) typically carry different fees and timelines; do not quote one tier's figure as universal.

## Validation Checklist

- Confirm which specific document (CNIC, Smart Card, NICOP, POC, CRC, FRC) matches the applicant's actual citizenship/residency status.
- Verify whether the request is a new application, renewal, or modification.
- Flag that current fees and processing times should be confirmed against NADRA's official source rather than assumed from this skill.
- Confirm passport-related questions are redirected to the correct agency rather than answered as a NADRA service.

## Common Pitfalls

- Confusing NICOP (for citizens abroad) with POC (for foreign nationals of Pakistani origin).
- Treating passport services as part of NADRA's own service offering.
- Citing a specific fee or processing time as current without flagging that these change periodically.
- Assuming a CRC functions as a CNIC for a minor rather than as a distinct registration document.

## Reference

- See [NADRA Reference](references/nadra-identity-services.md) for document types and extraction notes.
