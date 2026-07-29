# PTA Numbering & Licensing Framework Reference

## Source

- Pakistan Telecommunication Authority: `https://www.pta.gov.pk`
- Pakistan Telecommunication (Re-organization) Act, 1996 (and amendments) — available via PTA's laws/regulations section: `https://www.pta.gov.pk`
- PTA Numbering Regulations and National Numbering Plan documents: `https://www.pta.gov.pk` (Licensing/Numbering sections)
- DIRBS consumer portal: `https://dirbs.pta.gov.pk`
- NADRA: `https://www.nadra.gov.pk`

## Legal Foundation: Pakistan Telecommunication (Re-organization) Act, 1996

The 1996 Act restructured Pakistan's telecom sector by breaking up the former state monopoly, Pakistan Telecommunication Corporation, into distinct entities: Pakistan Telecommunication Company Limited (PTCL) as the corporatized (and later partly privatized) incumbent operator, the Pakistan Telecommunication Authority (PTA) as the sector regulator, the Frequency Allocation Board (FAB) as the spectrum-allocation authority, and the National Telecommunication Corporation (NTC) to continue serving government telecom needs. The Act (as amended over time) is PTA's founding statute and the legal basis for its licensing, numbering, tariff, and consumer-protection powers over telecom service providers.

## License Categories

- **Long Distance and International (LDI)**: authorizes carriage of long-distance domestic and international voice/data traffic, including operation of international gateway exchanges connecting Pakistan's network to international carriers. LDI licensees interconnect with local/mobile networks to terminate and originate long-distance and international calls.
- **Local Loop (LL)**: authorizes provision of local (last-mile) fixed telecommunication service to end users. **Wireless Local Loop (WLL)** is a technology variant of local loop service delivered via wireless rather than copper/fiber access, licensed under the local-loop category framework but using radio spectrum for the access link.
- **Cellular Mobile**: authorizes nationwide mobile network operation (the license category held by Pakistan's mobile network operators), bundled with associated spectrum assignments obtained through PTA/FAB-administered auction or allocation processes.
- **Other categories**: PTA also issues narrower or lower-tier licenses/authorizations for services such as value-added services, data/internet service provision, and other class-license categories that carry lighter eligibility and compliance requirements than the major infrastructure-based categories above. The exact current taxonomy of minor license classes should be confirmed against PTA's current licensing framework, as categories have been consolidated/revised over time.

Each license category carries its own eligibility criteria, rollout/coverage obligations, license fee structure (including annual regulatory fees and, where relevant, spectrum fees), and term length — a license in one category does not confer rights associated with another category.

## National Numbering Plan

PTA administers Pakistan's numbering resources under its Numbering Regulations, allocating number blocks (mobile network prefixes/codes, geographic area codes for fixed-line numbers, short codes for value-added/SMS services, and special-service numbers) to licensed operators. Numbering resources are a finite public resource administered by PTA, not permanently owned by any operator — allocations can be reclaimed or reorganized under PTA's numbering policy.

**Mobile Number Portability (MNP)** allows a mobile subscriber to switch between operators while retaining their existing mobile number, administered through a porting-database mechanism coordinated among PTA-licensed operators. MNP is a subscriber-facing portability right layered on top of the underlying numbering-block allocation to operators — the two should not be conflated: numbering-block allocation is operator-facing/administrative, while MNP is subscriber-facing/transactional.

## SIM Registration and Biometric Verification

Pakistan requires biometric verification for SIM issuance, implemented through integration with NADRA's biometric identity database: a prospective SIM purchaser's fingerprint is verified against their CNIC biometric record held by NADRA at the point of sale (historically operationalized through retailer-side biometric verification devices connected to the NADRA verification system). This framework was substantially expanded and enforced through a nationwide biometric re-verification exercise requiring existing SIM holders to re-verify previously issued SIMs, driven by security-policy directives (following the National Action Plan era's telecom-security measures). SIMs failing to complete required (re-)verification are subject to blocking by the operator under PTA's regulatory direction.

This SIM-registration/biometric system is administratively distinct from DIRBS (below): SIM registration verifies the **subscriber's identity** tied to a SIM, while DIRBS verifies **device compliance** tied to a handset's IMEI — a compliant, verified SIM can still be blocked from full service if inserted into a non-compliant/blocked device, and vice versa.

## DIRBS (Device Identification, Registration and Blocking System)

DIRBS is PTA's system for registering mobile devices by their unique IMEI and blocking devices that are not properly registered, are reported lost/stolen, or carry duplicate/invalid IMEIs from operating on Pakistani cellular networks. Key structural points:

- Mobile devices brought into Pakistan (by travelers, or imported commercially) are required to be registered with DIRBS — commercial imports go through a customs-linked registration/duty process, while devices brought in by individual travelers (e.g., in checked baggage) can typically be registered through a consumer-facing DIRBS portal/mobile application, subject to a duty/tax payment for non-passport-linked or extended-use registration and time-limited exemptions for short-term use (specific duty amounts, grace-period lengths, and passport/travel-history-linked exemption terms should be verified against PTA's current DIRBS guidance, as these have been revised administratively).
- DIRBS registration/blocking is IMEI-based and device-specific; it operates independent of which SIM/subscriber identity is later inserted into the device.
- The policy objective of DIRBS is to curb use of smuggled, counterfeit, or stolen devices on Pakistani networks and to formalize the mobile-device import/tax base.

## Extraction Notes

- Distinguish license-category questions (LDI/LL-WLL/Cellular Mobile) from numbering-administration questions (block allocation, MNP) from registration-system questions (SIM/biometric vs. DIRBS/IMEI) — these are four separate regulatory sub-functions.
- Do not present SIM registration and DIRBS device registration as the same system; one verifies subscriber identity (NADRA-linked), the other verifies device compliance (IMEI-linked).
- Flag any specific current DIRBS duty amount, SIM re-verification deadline, or numbering-block fee as needing verification against PTA's current notifications rather than citing a fixed remembered figure.
- When discussing spectrum tied to Cellular Mobile or WLL licenses, note that spectrum allocation itself involves the Frequency Allocation Board (FAB) alongside PTA's licensing function.
