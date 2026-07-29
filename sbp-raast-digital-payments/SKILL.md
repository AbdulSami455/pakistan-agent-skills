---
name: sbp-raast-digital-payments
description: SBP RAAST and digital payments regulation skill. Use when explaining Pakistan's RAAST instant payment system (P2P/P2M rails), Electronic Money Institution (EMI) regulations, the Payment Systems and Electronic Fund Transfers Act 2007, or the Payment System Operator/Payment Service Provider (PSO/PSP) licensing framework administered by the State Bank of Pakistan — as distinct from consumer-complaint handling or SBP's published statistical bulletins.
---

# SBP RAAST and Digital Payments

## Overview

Use this skill for the regulatory and architectural mechanics of Pakistan's digital payments infrastructure: RAAST (SBP's instant payment system), the licensing regimes for non-bank entities offering electronic money and payment services (EMIs, PSOs, PSPs), and the statutory basis for electronic fund transfers in Pakistan. This is an infrastructure/regulation skill, not a source of live transaction volume statistics or a consumer-complaint escalation guide.

## Coverage

- **Payment Systems and Electronic Fund Transfers Act, 2007 (PSEFTA)**: the foundational statute giving the State Bank of Pakistan authority to regulate, oversee, and license payment systems and electronic fund transfers in Pakistan, and giving legal recognition/finality to electronic fund transfer instructions and electronic records. It underpins SBP's supervisory authority over both bank-operated and non-bank payment infrastructure.
- **RAAST**: Pakistan's real-time, instant payment system built and operated by SBP, enabling free-of-cost (for end users, verify current fee policy) instant fund transfers between bank/EMI accounts using a simple alias (e.g., mobile number) instead of full account/IBAN details, via a centralized addressing database. RAAST supports person-to-person (P2P) transfers and has been extended toward person-to-merchant (P2M) use cases to support digital retail payment acceptance, positioned by SBP as core national payments infrastructure analogous to instant-payment rails in other jurisdictions (e.g., India's UPI, Brazil's Pix) — treat specific rollout-phase dates or volume milestones as needing verification against current SBP releases.
- **Electronic Money Institutions (EMIs)**: a category of non-bank entities licensed and regulated by SBP under its EMI regulatory framework to issue e-money, hold customer funds in safeguarded/pooled accounts (not on-lend them like a bank), and provide digital wallet and payment services — distinct from full-service banks and from Payment System Operators/Payment Service Providers, though an entity can hold multiple authorizations.
- **PSO/PSP licensing framework**: SBP separately licenses/authorizes Payment System Operators (PSOs — entities operating the payment system infrastructure/switch, e.g., processing and settlement rails) and Payment Service Providers (PSPs — entities offering payment services to end users/merchants on top of that infrastructure, e.g., payment gateways, aggregators). The PSO/PSP framework and the EMI framework are separate authorization regimes under SBP, and an entity's specific license type determines what activities it may lawfully conduct (e.g., issuing e-money vs. merely switching/processing transactions).
- **QR code standards**: SBP has promoted standardized, interoperable QR code specifications for merchant payment acceptance (to avoid a fragmented, provider-specific QR landscape), aligning with RAAST's P2M push and broader national financial-inclusion/digital-payments strategy — verify the specific technical standard/version in force for current implementation detail.
- **Roshan Digital Account (RDA) linkage**: RDA is a separate SBP initiative allowing non-resident Pakistanis to remotely open and operate Pakistani bank accounts and invest in Pakistani assets; it is not part of RAAST itself, though RDA-linked transfers can move through Pakistan's domestic payment rails once funds are in-country. Do not describe RDA as a RAAST product — they are distinct SBP initiatives with different purposes (non-resident account access vs. domestic instant payments).

## Use This Skill For

- explaining how RAAST enables instant, alias-based fund transfers between accounts at different banks/EMIs
- distinguishing RAAST (instant payment rail) from EMIs, PSOs, and PSPs (licensed entity categories that connect to or operate around such rails)
- explaining the statutory basis (PSEFTA 2007) for SBP's authority to regulate payment systems and give legal effect to electronic fund transfers
- clarifying what an EMI can and cannot do relative to a licensed bank (e.g., safeguarding vs. on-lending customer funds)
- distinguishing PSO (infrastructure/switch operator) from PSP (payment service provider to end users/merchants) licensing
- explaining the P2P vs. P2M distinction within RAAST and the push toward QR-based interoperable merchant payments
- clarifying that Roshan Digital Account is a separate non-resident account initiative, not a RAAST product

## When Not to Use This Skill

- For an individual's dispute over a bank charge or unresolved service complaint and escalation to the Banking Mohtasib, use `sbp-banking-consumer-protection` instead.
- For SBP's published statistical time series (monetary aggregates, exchange rates, reserves, banking-sector balance sheet data), use `sbp-statistics-bulletin` — this skill covers the regulatory/architectural framework, not the underlying data releases.
- For SBP monetary policy rate decisions and rationale, use `sbp-monetary-policy-statement`.
- For remittance inflow tracking specifically, use `pkr-remittances-tracker`.

## Routing Rules

- If the question is about how instant transfers work technically/operationally (alias-based routing, settlement finality, P2P/P2M), apply the RAAST framework.
- If the question is about which entity type may lawfully hold customer e-money, issue wallets, or operate payment infrastructure, apply the EMI/PSO/PSP licensing distinctions.
- If the question is about a consumer's unresolved complaint against a bank or payment provider, route to `sbp-banking-consumer-protection`.
- If the question needs actual transaction volume, value, or adoption statistics for RAAST or digital payments, route to `sbp-statistics-bulletin` or flag that current SBP data releases should be checked, since this skill does not host time-series figures.
- If the question is about non-resident account access or foreign-currency/investment accounts, route to Roshan Digital Account material specifically and do not conflate it with RAAST.

## Extraction Workflow

1. Identify whether the question is about the payment rail itself (RAAST) or about a licensed entity category (EMI, PSO, PSP) that participates in or operates around it.
2. If about RAAST, confirm whether the use case is P2P or P2M, since SBP's rollout and merchant-acceptance tooling (QR standards) apply specifically to the P2M side.
3. If about a licensed entity, confirm which authorization type is at issue (EMI vs. PSO vs. PSP) before describing what the entity may do — these are distinct regulatory categories with different permitted activities.
4. Trace regulatory authority back to PSEFTA 2007 as the statutory basis for SBP's oversight, rather than treating RAAST/EMI/PSO/PSP rules as freestanding.
5. Flag any specific transaction fee, volume statistic, or rollout-phase date as needing verification against current SBP circulars/press releases.
6. If Roshan Digital Account is mentioned, clarify it as a separate non-resident account initiative and only connect it to RAAST if the specific question concerns fund movement after an RDA-linked deposit reaches a domestic account.

## Technical Rules

- RAAST is the payment rail/infrastructure; EMIs, PSOs, and PSPs are licensed entity categories — do not use these terms interchangeably.
- An EMI holds customer funds in safeguarded/pooled accounts and does not on-lend them the way a bank does under its deposit-taking license; do not describe an EMI as functionally equivalent to a bank.
- PSO authorization (operating switch/processing/settlement infrastructure) is distinct from PSP authorization (offering payment services to end users/merchants); an entity's specific license determines its permitted activities, and holding one does not imply the other.
- PSEFTA 2007 is the statutory basis for SBP's payment-system regulatory authority and for the legal recognition of electronic fund transfers — do not attribute RAAST's or EMI regulation's legal force to a source other than SBP's statutory and regulatory authority under this Act (and subordinate SBP regulations/circulars).
- Roshan Digital Account is not a RAAST product; do not describe RDA transactions as "RAAST transactions" without clarifying the distinction.
- Treat any specific fee-free policy claim, rollout date, or adoption/volume figure as needing verification against current SBP publications rather than asserting a fixed number from memory.

## Validation Checklist

- Confirm whether the question is about the RAAST rail or about EMI/PSO/PSP licensing before answering.
- Confirm EMI, PSO, and PSP are not used interchangeably, and that each entity's permitted activities match its actual authorization type.
- Confirm PSEFTA 2007 is cited as the statutory basis where relevant.
- Confirm Roshan Digital Account is not conflated with RAAST.
- Flag any specific fee, date, or volume statistic as needing current verification.

## Common Pitfalls

- Treating RAAST as a company or licensed entity rather than SBP's instant payment infrastructure/rail.
- Describing an EMI as a bank, or assuming it can on-lend customer deposits.
- Conflating PSO and PSP authorizations as a single license type.
- Citing a specific current transaction-fee or volume figure without flagging it as needing verification.
- Describing Roshan Digital Account as part of, or synonymous with, RAAST.

## Reference

- See [SBP RAAST and Digital Payments Reference](references/sbp-raast-digital-payments.md) for statutory basis, entity-licensing distinctions, and extraction notes.
