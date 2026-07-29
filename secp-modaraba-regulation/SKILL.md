---
name: secp-modaraba-regulation
description: SECP Modaraba regulation skill. Use when explaining or analyzing the Modaraba structure (Modaraba Management Company plus Modaraba Fund), the Modaraba Companies and Modaraba (Floatation and Control) Ordinance 1980, the Religious Board for Modarabas, or Modaraba listing/certificate mechanics — as distinct from conventional/Islamic mutual funds or ordinary company incorporation.
---

# SECP Modaraba Regulation

## Overview

Use this skill for **Modarabas** — Pakistan's statutory Islamic profit-and-loss-sharing investment vehicle, regulated by the Securities and Exchange Commission of Pakistan (SECP) under the **Modaraba Companies and Modaraba (Floatation and Control) Ordinance, 1980** and associated Rules/Regulations. A Modaraba is a distinct corporate-cum-trust-like structure — a Modaraba Management Company manages a separately certificated Modaraba Fund on behalf of certificate holders — and is not simply another name for a mutual fund or an ordinary registered company.

## Coverage

- **Legal basis**: The Modaraba Companies and Modaraba (Floatation and Control) Ordinance, 1980, together with the Modaraba Companies and Modaraba Rules, 1981, and SECP's Modaraba-specific regulations, govern formation, floatation (public offering of Modaraba certificates), management, and winding-up of Modarabas in Pakistan.
- **Two-tier structure**: A Modaraba consists of (a) a **Modaraba Management Company (MMC)** — an SECP-registered company that manages the Modaraba's business and is entitled to a management fee/share of profit as the Modaraba's mudarib (managing partner), and (b) the **Modaraba** itself (the fund/business entity) — a separate certificated vehicle whose certificate holders (rabb-ul-maal, i.e., capital providers) share in profit/loss per the Modaraba's prospectus, distinct from the MMC's own corporate shareholders.
- **Religious Board for Modarabas**: A statutory religious/Shariah supervisory board constituted under the Ordinance reviews Modaraba operations and business activities for Shariah compliance — this is a Modaraba-sector-specific body, structurally distinct from an individual Islamic bank's in-house Shariah Board (see `sbp-shariah-governance-islamic-banking` for the banking-sector equivalent) and from the Shariah Advisory Board frameworks used for Islamic mutual funds/Sukuk.
- **Regulator**: SECP regulates Modaraba registration, floatation approval, and ongoing compliance (through its Specialized Companies Division / Modaraba-specific wing), distinct from SECP's separate company-registration function under the Companies Act, 2017 and its separate mutual-fund regulation under the NBFC framework.
- **Modaraba Association of Pakistan (MAP)**: The sector's trade/industry association representing Modaraba Management Companies collectively, involved in sector advocacy and coordination — an industry body, not a regulator.
- **Listing**: Modaraba certificates can be listed and traded on the Pakistan Stock Exchange (PSX), giving certificate holders a secondary-market exit distinct from an open-ended mutual fund's redemption-at-NAV mechanism.
- **Business scope**: Modarabas historically operate across sectors such as leasing/ijarah, trading, manufacturing participation, and other Shariah-compliant business activities specified in their prospectus/memorandum — a Modaraba's permissible activity set is defined at floatation and reviewed for Shariah compliance, not open-ended like a general trading company.

## Use This Skill For

- explaining the two-tier Modaraba Management Company + Modaraba Fund structure
- explaining how a Modaraba differs from a mutual fund (open-end/closed-end) or a REIT in legal form and capital-raising mechanism
- describing the Religious Board for Modarabas' role in Shariah oversight of a Modaraba's operations
- explaining Modaraba certificate floatation, listing on PSX, and certificate-holder rights
- identifying the Modaraba Association of Pakistan's role as an industry body

## When Not to Use This Skill

- For conventional or Islamic **mutual funds** (open-end/closed-end funds under the NBFC Rules, Asset Management Companies) — use `mufap-mutual-funds`; mutual funds are a distinct NBFC-regulated structure with unit/NAV-based redemption, not a Modaraba's certificate structure.
- For ordinary **company incorporation** (private/public limited companies under the Companies Act, 2017) — use `secp-company-registry`; a Modaraba Management Company itself must incorporate as a company under that framework, but the Modaraba (the managed fund entity) is a separate statutory creature this skill covers.
- For bank-sector Shariah governance (Islamic banks' Shariah Boards under SBP) — use `sbp-shariah-governance-islamic-banking`; the Religious Board for Modarabas is a separate, Modaraba-sector-specific body under SECP, not the SBP banking framework.
- For Sukuk issuance mechanics — use `pakistan-sukuk-structuring-issuance`; Sukuk and Modaraba certificates are both Islamic-finance instruments but structurally distinct (Sukuk are typically asset-backed/asset-based certificates tied to a specific issuance, not a perpetual profit-sharing business vehicle).

## Routing Rules

- If the question concerns the Modaraba Management Company + Modaraba Fund two-tier structure, Modaraba certificate floatation, or the Religious Board for Modarabas, use this skill.
- If the question is about mutual fund NAV, unit trusts, or Asset Management Company regulation, route to `mufap-mutual-funds`.
- If the question is about incorporating an ordinary company (including the MMC's own corporate registration), route the incorporation mechanics to `secp-company-registry`, while keeping the Modaraba-specific floatation/certificate layer in this skill.
- If the question is about a bank's internal Shariah Board rather than the Modaraba sector's Religious Board, route to `sbp-shariah-governance-islamic-banking`.
- If the question is about Sukuk structuring rather than Modaraba certificates, route to `pakistan-sukuk-structuring-issuance`.

## Extraction Workflow

1. Confirm the vehicle in question is a Modaraba (certificate-based, MMC-managed) rather than a mutual fund, REIT, or ordinary company before applying this skill.
2. Identify whether the question concerns the MMC (management entity) layer or the Modaraba (fund/certificate) layer — they have different regulatory touchpoints even though they are linked.
3. If Shariah compliance is discussed, confirm it is the Religious Board for Modarabas being referenced, not a bank's Shariah Board or a mutual fund's Shariah Advisory Board.
4. If listing/trading is discussed, confirm whether the question is about PSX-listed certificate trading (secondary market) or floatation (primary issuance) — these are separate stages.
5. Distinguish the Modaraba Association of Pakistan (industry association) from SECP (the actual regulator) when attributing regulatory statements.

## Technical Rules

- Do not describe a Modaraba as simply "an Islamic mutual fund"; it has a distinct two-tier legal structure (MMC as mudarib plus a separately certificated fund) and its own governing Ordinance, separate from the NBFC/mutual-fund regulatory framework.
- Keep the Religious Board for Modarabas distinct from SBP's bank-level Shariah Boards and from Shariah Advisory Boards used in mutual funds/Sukuk structures — each sits under a different regulatory framework.
- Do not conflate the Modaraba Association of Pakistan (industry body) with SECP (statutory regulator) when describing who sets binding rules.
- Preserve the distinction between the MMC's own shareholders (who own the management company) and the Modaraba's certificate holders (who share in the Modaraba's own profit/loss) — these are two different investor classes.

## Validation Checklist

- Confirm the entity discussed is a Modaraba under the 1980 Ordinance, not a mutual fund, REIT, or general company.
- Confirm whether the MMC layer or the Modaraba Fund layer is being addressed.
- Confirm the correct Shariah oversight body (Religious Board for Modarabas) is named, not a banking or mutual-fund Shariah body.
- Confirm the Modaraba Association of Pakistan is treated as an industry association, not a regulator.
- Confirm listing (PSX secondary trading) is not conflated with floatation (primary certificate issuance).

## Common Pitfalls

- Calling a Modaraba an "Islamic mutual fund" without noting its distinct MMC + certificated-fund legal structure and separate governing Ordinance.
- Confusing the Religious Board for Modarabas with a bank's Shariah Board or a mutual fund's Shariah Advisory Board.
- Treating the Modaraba Association of Pakistan as a regulator rather than an industry association.
- Conflating MMC shareholders with Modaraba certificate holders as if they were the same investor class.
- Applying ordinary Companies Act incorporation rules to the Modaraba Fund itself rather than to the Modaraba Management Company.

## Reference

- See [SECP Modaraba Regulation Reference](references/secp-modaraba-regulation.md) for the Ordinance structure, regulatory bodies, and sourcing notes.
