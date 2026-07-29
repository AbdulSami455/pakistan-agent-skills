---
name: secp-futures-commodity-exchange
description: Pakistan Mercantile Exchange (PMEX) and commodity futures regulation skill. Use when a task concerns commodity futures contracts (gold, silver, currency, crude oil, agricultural commodities) traded on PMEX, PMEX's market structure and clearing mechanics, or SECP's regulatory oversight of the futures market under the Futures Market Act 2016 — as distinct from PSX equity trading or SECP company registration.
---

# SECP Futures & Commodity Exchange (PMEX)

## Overview

Use this skill for Pakistan's commodity futures market: the Pakistan Mercantile Exchange (PMEX), the country's only licensed commodity futures exchange, and the Securities and Exchange Commission of Pakistan's (SECP) regulatory oversight of that market under the Futures Market Act, 2016. This is a market-structure and regulatory-framework skill for derivatives on commodities and financial futures — it does not cover PSX equity trading, which is a separate exchange with a separate statute (the Securities Act, 2015) and separate instruments.

## Coverage

- **PMEX as sole commodity futures exchange**: PMEX (Pakistan Mercantile Exchange Limited), incorporated in 2002 and commencing trading in 2007, is Pakistan's only licensed commodity futures and derivatives exchange. It is demutualized and corporatized, distinct in ownership structure, membership model, and product base from PSX (the equities/debt securities exchange formed from the 2016 demutualization merger of the Karachi, Lahore, and Islamabad stock exchanges).
- **Legal basis**: Futures trading in Pakistan is governed by the **Futures Market Act, 2016**, which replaced the earlier Futures Exchanges Ordinance/Corporatization framework for regulating futures exchanges, futures brokers, and futures contracts. SECP is the apex regulator of PMEX and futures brokers under this Act, exercising licensing, inspection, and enforcement powers analogous to (but statutorily separate from) its oversight of PSX under the Securities Act, 2015.
- **Contract types traded on PMEX**: precious metals futures (gold, silver — cash-settled and, for some contracts, deliverable), currency futures (USD/PKR and other pairs), and agricultural commodity futures (e.g., cotton, wheat, rice-linked contracts as introduced from time to time), plus index-linked and other financial futures PMEX has introduced over time. The specific live contract roster changes as PMEX lists/delists products — treat any specific current contract list as needing verification against PMEX's own contract specifications.
- **Clearing and margining**: PMEX operates its own clearing house function for futures contracts, requiring margin deposits (initial and maintenance margin) from members/brokers on open futures positions — a margining and mark-to-market structure fundamentally different from cash-market equity settlement on PSX (T+2 delivery-versus-payment).
- **Membership/brokerage structure**: Trading on PMEX occurs through PMEX-registered brokers (Trading and clearing members), which are separately licensed/registered entities from PSX-facing stockbrokers, even where the same brokerage house holds both categories of registration.

## Use This Skill For

- explaining what PMEX is, when it was established, and its role as Pakistan's sole commodity futures exchange
- describing the Futures Market Act, 2016 and SECP's regulatory relationship to PMEX
- explaining categories of futures contracts traded on PMEX (precious metals, currency, agricultural commodities)
- distinguishing futures/derivatives trading (leveraged, margin-based, expiry-dated contracts) from PSX cash-market equity trading
- explaining PMEX's clearing, margining, and settlement mechanics at a structural level
- clarifying that PMEX brokerage registration is separate from PSX stockbroker registration even if commonly held by the same firm

## When Not to Use This Skill

- For PSX-listed equity tickers, sector classification, or index constituents (KSE-100, KMI-30, etc.) — use `psx-market-discovery`.
- For PSX historical OHLCV price series or the `psxdata` package — use `psx-historical-data`.
- For a specific PSX-listed company's live quote or fundamentals — use `psx-company-snapshots`.
- For PSX debt instruments (TFCs/Sukuks) or margin-eligible scrip lists on the equity exchange — use `psx-debt-and-eligibility`.
- For verifying a company's SECP registration status, incorporation date, or category (unrelated to futures trading) — use `secp-company-registry`.
- For actual spot commodity prices (e.g., gold rates in the local bullion market, or agricultural commodity spot/wholesale prices) rather than PMEX futures contract structure — this skill covers the exchange/regulatory mechanics, not a live price feed.

## Routing Rules

- If the question is about a stock, index, or equity-market structure, route to the relevant `psx-*` skill — PMEX and PSX are entirely separate exchanges under separate statutes.
- If the question is about whether a company (including PMEX itself or a futures brokerage) is validly registered/incorporated with SECP as a corporate entity, route to `secp-company-registry` for the registration-status lookup, and use this skill only for PMEX's market/regulatory role.
- If the question concerns SECP's oversight of non-banking financial companies (NBFCs), insurance, or modarabas rather than the futures exchange, route to the relevant sector-specific SECP skill (e.g., `secp-insurance-industry-statistics`, `secp-modaraba-regulation`) — this skill is scoped narrowly to the futures/commodity exchange function.
- If the question needs a live/current gold, silver, or currency price rather than the futures-contract structure, note that this skill does not provide live price data.

## Extraction Workflow

1. Confirm the question concerns futures/derivatives trading (leveraged, expiry-dated, margin-based contracts) rather than cash-market equity trading, since the two run on entirely separate exchanges, statutes, and clearing systems.
2. Identify the specific contract category involved (precious metals, currency, agricultural commodity, index/financial futures) before describing contract mechanics, since margin requirements and settlement (cash vs. physical delivery) can differ by contract type.
3. When citing SECP's regulatory role, attribute it to the Futures Market Act, 2016 specifically, not the Securities Act, 2015 (which governs PSX, brokers, and the capital-markets side of SECP's mandate).
4. Distinguish PMEX corporate/membership structure (demutualized exchange, its own trading/clearing members) from PSX's separate membership base, even when discussing overlapping brokerage firms.
5. For any specific current contract specification, margin rate, or fee schedule, flag it as needing verification against PMEX's own current contract specifications rather than stating a fixed figure from memory.

## Technical Rules

- PMEX and PSX are legally and operationally distinct exchanges; do not present PMEX as a "commodities division" of PSX or imply shared clearing/settlement infrastructure unless specifically confirmed.
- The Futures Market Act, 2016 is the operative statute for futures exchange regulation; do not cite the Securities Act, 2015 (PSX's governing statute) as PMEX's legal basis.
- Futures contracts are margin-based and mark-to-market daily; do not describe PMEX trading using cash-market settlement logic (e.g., T+2 delivery-versus-payment) that applies to PSX equities.
- Do not state a specific current margin percentage, contract lot size, or fee without flagging it as needing verification, since PMEX revises contract specifications periodically.
- Keep PMEX broker/member registration distinct from PSX stockbroker registration — both are SECP-regulated intermediary categories but under different licensing regimes.

## Validation Checklist

- Confirm the task is about futures/derivatives trading on PMEX, not equity trading on PSX, before applying this skill.
- Confirm which contract category (metals, currency, agricultural) is relevant before describing settlement/delivery mechanics.
- Confirm the statute cited is the Futures Market Act, 2016, not the Securities Act, 2015.
- Flag any specific numeric contract specification (margin %, lot size, expiry cycle) as needing verification against PMEX's current published contract specs.
- Confirm whether the question actually needs a live commodity price (out of scope) versus the exchange/regulatory structure (in scope).

## Common Pitfalls

- Conflating PMEX with PSX as if they were divisions of the same exchange rather than separate entities under separate statutes.
- Citing the Securities Act, 2015 as PMEX's governing law instead of the Futures Market Act, 2016.
- Describing PMEX futures settlement using PSX's T+2 cash-market delivery-versus-payment logic.
- Treating a remembered specific margin rate, contract lot size, or fee schedule as current without verification.
- Assuming a PSX-registered stockbroker is automatically also a PMEX-registered futures broker (the registrations are separate, even if commonly co-held).

## Reference

- See [SECP Futures & Commodity Exchange Reference](references/secp-futures-commodity-exchange.md) for PMEX's history, the Futures Market Act 2016 structure, and contract-category detail.
