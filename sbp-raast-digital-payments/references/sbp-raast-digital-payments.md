# SBP RAAST and Digital Payments Reference

## Source

- State Bank of Pakistan, RAAST overview: `https://www.sbp.org.pk/RAAST/index.html`
- State Bank of Pakistan, Payment Systems Department regulatory framework and licensing (EMI regulations, PSO/PSP regulations): `https://www.sbp.org.pk/psd/index.html`
- Payment Systems and Electronic Fund Transfers Act, 2007 (Pakistan) — available via Pakistan Code: `http://www.pakistancode.gov.pk`
- SBP Regulations for Electronic Money Institutions: `https://www.sbp.org.pk`
- SBP Roshan Digital Account: `https://www.sbp.org.pk/RDA/index.html`

## Statutory Basis

The Payment Systems and Electronic Fund Transfers Act, 2007 (PSEFTA) gives the State Bank of Pakistan the statutory authority to designate, regulate, and oversee payment systems operating in Pakistan, and gives legal recognition and finality to electronic fund transfer instructions and records. SBP's subsequent regulatory frameworks for EMIs, PSOs, PSPs, and RAAST itself operate under authority derived from this Act, supplemented by SBP's own regulations, prudential rules, and circulars issued from time to time.

## RAAST

- RAAST is SBP's centrally operated instant payment system, letting people make real-time fund transfers between accounts held at different banks and Electronic Money Institutions using a simplified alias (such as a mobile number) mapped to the recipient's actual account/IBAN through a central addressing database, rather than requiring the sender to know full account details.
- Positioned as national digital-payments infrastructure supporting financial inclusion, RAAST's initial rollout emphasized person-to-person (P2P) transfers, with subsequent expansion toward person-to-merchant (P2M) use cases to support retail/merchant digital payment acceptance.
- SBP has promoted standardized, interoperable QR code specifications to support P2M payment acceptance across different banks/EMIs/merchant acquirers, avoiding a fragmented provider-specific QR landscape.
- Specific rollout-phase dates, fee policy, and adoption/volume statistics should be verified against current SBP press releases and the RAAST microsite, as these have evolved since initial launch.

## Licensed Entity Categories

| Category | Role | Key Distinction |
|---|---|---|
| Electronic Money Institution (EMI) | Issues e-money, operates digital wallets, holds customer funds in safeguarded/pooled accounts | Cannot on-lend customer funds like a deposit-taking bank |
| Payment System Operator (PSO) | Operates payment infrastructure — switching, processing, settlement | Infrastructure-layer authorization |
| Payment Service Provider (PSP) | Offers payment services to end users/merchants (e.g., gateways, aggregators) on top of PSO infrastructure | End-user/merchant-facing authorization |

These are separate SBP authorization regimes; an entity's specific license determines its permitted activities, and an entity may hold more than one authorization type if separately licensed for each.

## Roshan Digital Account (Related but Distinct)

Roshan Digital Account (RDA) is a separate SBP initiative allowing non-resident Pakistanis and Pakistani-origin foreign nationals to remotely open and operate Pakistani bank accounts and access investment products (e.g., Naya Pakistan Certificates, equities). RDA is not a RAAST product; it is a distinct account-access/investment initiative. Funds within an RDA-linked domestic account can subsequently move through domestic payment rails including RAAST, but the two should not be described as the same system.

## Extraction Notes

- Keep RAAST (the payment rail) analytically separate from EMI/PSO/PSP (licensed entity categories) at all times.
- Do not describe an EMI as a bank; its defining constraint is safeguarding rather than on-lending customer funds.
- Cite PSEFTA 2007 as the statutory basis for SBP's payment-system regulatory authority.
- Flag specific fee, rollout-date, or volume/adoption figures as needing verification against current SBP publications.
- Do not conflate Roshan Digital Account with RAAST — different purpose, different initiative, though operationally connectable once funds are domestic.
