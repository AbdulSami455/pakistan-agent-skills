---
name: pta-numbering-licensing-framework
description: PTA telecom licensing and numbering framework skill. Use when a task concerns telecom license categories (LDI, LL, Cellular Mobile, WLL) under the Pakistan Telecommunication (Re-organization) Act 1996, the National Numbering Plan, SIM registration/biometric verification requirements, or mobile device (IMEI) registration via DIRBS — as distinct from PTA's published subscriber/teledensity statistics.
---

# PTA Numbering & Licensing Framework

## Overview

Use this skill for the regulatory and administrative machinery behind Pakistan's telecom sector: how telecom licenses are categorized and issued, how the national numbering (phone number) resource is administered, how SIM registration and biometric verification work, and how mobile devices are registered/blocked through DIRBS. This is a licensing/framework/process skill — it does not host subscriber counts, teledensity figures, or operator revenue data, which live in a separate indicator-data skill.

## Coverage

- **Legal basis**: The **Pakistan Telecommunication (Re-organization) Act, 1996** (as amended) is the primary statute establishing the Pakistan Telecommunication Authority (PTA) as regulator, the Frequency Allocation Board (FAB) for spectrum, and the licensing framework for telecom service providers, following the breakup of the former state telecom monopoly (Pakistan Telecommunication Corporation) into PTCL and separate regulatory bodies.
- **License categories**: PTA issues telecom licenses across categories including **Long Distance and International (LDI)** (for international/domestic long-distance voice traffic carriage and international gateway exchange operation), **Local Loop (LL)** (for local/fixed-line service provision, including Wireless Local Loop, WLL, as a technology variant of local loop service), **Cellular Mobile** (for nationwide mobile network operators), and other category-specific licenses (e.g., for value-added services, class-license categories for smaller-scale services). Each category carries distinct eligibility, spectrum-linkage (where applicable), rollout-obligation, and fee terms.
- **Numbering Plan administration**: PTA administers Pakistan's National Numbering Plan — the allocation of telephone number blocks/prefixes to licensed operators (mobile network codes, area codes for fixed-line numbering, short codes, and special-service numbers). Numbering resources are allocated to licensees under PTA's numbering regulations, not owned permanently by any operator, and can be subject to number portability rules (Mobile Number Portability, MNP) allowing a subscriber to retain their number across operators.
- **SIM registration/biometric verification**: Pakistan requires biometric verification of SIM issuance/re-verification, implemented through integration with NADRA's biometric database (fingerprint verification against NADRA's CNIC records at the point of SIM sale, historically operationalized via retailer-side biometric verification devices/systems). This framework was significantly built out following security-driven policy directives requiring re-verification of previously issued SIMs.
- **DIRBS (Device Identification, Registration and Blocking System)**: PTA's system for registering mobile devices by IMEI (International Mobile Equipment Identity) and blocking non-compliant/non-registered devices from operating on Pakistani mobile networks. DIRBS requires imported/brought-in mobile handsets to be registered (historically via a duty/tax-payment and registration process, including a consumer-facing registration mechanism for travelers bringing in personal devices) before they can register on local cellular networks beyond a limited grace period; devices with duplicate, blacklisted, or invalid IMEIs are blocked.

## Use This Skill For

- explaining PTA's telecom license categories (LDI, LL/WLL, Cellular Mobile) and what each authorizes
- explaining the Pakistan Telecommunication (Re-organization) Act, 1996's role in establishing PTA and the licensing regime
- describing how the National Numbering Plan allocates number resources to operators, including Mobile Number Portability
- explaining the SIM registration/biometric verification framework and its NADRA integration
- explaining DIRBS: what it registers (IMEI), what it blocks, and the general process for a traveler/importer to register a device
- distinguishing licensing/numbering/device-registration process questions from subscriber-count or teledensity data questions

## When Not to Use This Skill

- For subscriber counts, teledensity, broadband penetration, or operator-level revenue/market-share figures — use `pta-telecom-indicators` instead; that skill covers PTA's published statistical data, this skill covers the licensing/numbering/registration framework itself.
- For PTA Annual Report narrative on sector performance or regulatory actions in aggregate — use `pta-telecom-indicators`.
- For broadcast content licensing (TV, radio, cable, DTH) — use the relevant PEMRA skill; PTA licenses telecom carriage infrastructure, PEMRA licenses broadcast content distribution, and the two regulators and statutes are separate.
- For NADRA's own identity-services processes (CNIC issuance, verification services generally) beyond the SIM-biometric integration point — use `nadra-identity-services`.

## Routing Rules

- If the question needs a subscriber count, teledensity rate, or operator revenue figure, route to `pta-telecom-indicators`; use this skill only for the licensing/numbering/registration mechanics.
- If the question is about broadcast/media content licensing rather than telecom carriage licensing, route to the relevant PEMRA skill.
- If the question is about NADRA's identity/CNIC verification systems generally, beyond the specific SIM-registration biometric integration, route to `nadra-identity-services`.
- If the question concerns a specific spectrum auction's outcome or proceeds, note that spectrum/frequency allocation involves the Frequency Allocation Board (FAB) alongside PTA licensing, and flag that auction-specific detail (prices, bands, winners) should be verified against PTA's/FAB's own auction-specific releases rather than this skill's general framework description.

## Extraction Workflow

1. Identify whether the question concerns license category/eligibility, numbering administration, SIM/biometric registration, or device (IMEI/DIRBS) registration — these are four distinct regulatory sub-functions within PTA's mandate.
2. For license-category questions, identify which category (LDI, LL/WLL, Cellular Mobile, or a value-added/class license) is relevant, since rollout obligations, fee structures, and spectrum linkage differ by category.
3. For numbering questions, distinguish number-block allocation to operators (administrative/regulatory) from Mobile Number Portability (a subscriber-facing right to retain a number across operators).
4. For SIM registration questions, describe the biometric-verification-against-NADRA mechanism generally rather than asserting a specific current retailer procedure or fee without verification.
5. For DIRBS questions, distinguish the general registration/compliance concept (IMEI must be registered to operate on local networks) from any specific current duty/tax amount or grace-period length, which should be flagged as needing verification against PTA's current DIRBS guidance.

## Technical Rules

- The Pakistan Telecommunication (Re-organization) Act, 1996 is the founding statute for PTA and the licensing regime; do not cite a different or generic "Telecom Act" without this specific title and year.
- Keep LDI, LL/WLL, and Cellular Mobile license categories distinct; each authorizes a different scope of service and carries different regulatory conditions — do not treat them as interchangeable labels for "a telecom license."
- SIM registration/biometric verification is implemented through integration with NADRA's database; do not describe it as a PTA-only biometric system independent of NADRA.
- DIRBS registers and can block devices by IMEI; it is a device-compliance system, not a subscriber/SIM registration system — keep DIRBS (device-level) and SIM registration (subscriber-identity-level) conceptually separate even though both are anti-fraud/security telecom-compliance mechanisms.
- Do not state a specific current duty/tax rate for DIRBS device registration, a specific SIM re-verification deadline, or a specific numbering-block fee without flagging it as needing verification, since these are administratively revised.

## Validation Checklist

- Confirm which of the four sub-functions (licensing category, numbering, SIM/biometric, DIRBS/IMEI) the question concerns before answering.
- Confirm the statute cited is the Pakistan Telecommunication (Re-organization) Act, 1996.
- Confirm license-category claims specify LDI, LL/WLL, Cellular Mobile, or another named category rather than a generic "telecom license."
- Confirm SIM-registration claims correctly attribute the biometric check to NADRA integration.
- Flag any specific current fee, duty rate, or deadline as needing verification against PTA's current notifications.

## Common Pitfalls

- Confusing this licensing/numbering/registration-framework skill with `pta-telecom-indicators`'s subscriber/statistical data — they answer different question types even though both concern PTA.
- Treating LDI, LL/WLL, and Cellular Mobile licenses as equivalent or interchangeable categories.
- Describing SIM biometric verification without noting the NADRA database integration that underpins it.
- Conflating DIRBS (device/IMEI registration) with SIM registration (subscriber identity registration) as if they were the same system.
- Stating a specific current DIRBS duty amount, SIM re-verification deadline, or numbering fee as settled fact without a verification flag.

## Reference

- See [PTA Numbering & Licensing Framework Reference](references/pta-numbering-licensing-framework.md) for license-category detail, numbering plan structure, and DIRBS/SIM registration mechanics.
