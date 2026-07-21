---
name: pakistan-sukuk-structuring-issuance
description: Pakistan Sukuk structuring and issuance skill. Use when analyzing how corporate Sukuk are structured and issued under SECP's Sukuk regulatory framework, or how Government of Pakistan Ijara Sukuk (GIS) are auctioned by SBP — covering structure types (Ijarah, Diminishing Musharakah, Bai Muajjal, Wakala), the issuer/trustee/investor mechanics, and issuance workflow, for treasury, DCM, and Islamic-finance practitioners.
---

# Pakistan Sukuk Structuring and Issuance

## Overview

Use this skill for how Sukuk are structured and brought to market in Pakistan across two distinct tracks: (1) corporate/privately-placed or listed Sukuk under SECP's securities regulations, and (2) sovereign GoP Ijara Sukuk (GIS) issued by the Ministry of Finance and auctioned through SBP as a government domestic-debt instrument. This is a structuring/issuance-mechanics skill, not a Shariah-governance-apparatus skill (see `sbp-shariah-governance-islamic-banking` for how Shariah Boards approve structures) and not a general corporate-debt skill (see `pakistan-corporate-debt-capital-markets` for TFCs and conventional debt securities regulation, which share procedural ground with Sukuk but differ structurally).

## Coverage

- Corporate Sukuk issuance under SECP's securities law framework: the Sukuk-specific regulations (originally the Issue of Sukuk Regulations, 2015, since amended/consolidated within SECP's broader debt-securities regulatory framework) governing public offer and privately placed Sukuk.
- Common Sukuk structures used in Pakistan: Ijarah (sale-and-leaseback of an underlying asset), Diminishing Musharakah (declining co-ownership with lease/purchase undertaking), Musharakah/Mudarabah (partnership-based, profit-and-loss sharing), Murabaha-based short-term structures, Wakala (agency-based investment), and Bai Muajjal (deferred-payment sale) structures — each with a different asset-backing/asset-based character and risk profile.
- The GoP Ijara Sukuk (GIS) program: sovereign Sukuk issued since 2008 by the Government of Pakistan against underlying government assets (e.g., motorways, land), auctioned periodically by SBP on behalf of the Ministry of Finance, in both Fixed Rental Rate (FRR) and Variable Rental Rate (VRR) variants, and sometimes transacted via Bai Muajjal (deferred-payment purchase) auctions.
- The role of the Special Purpose Vehicle (SPV) / Sukuk-issuing entity that holds or has beneficial rights to the underlying asset and issues Sukuk certificates representing undivided ownership/beneficial interest to Sukuk-holders.
- Trustee/registrar mechanics distinct from conventional TFC trustees where Sukuk-specific asset-holding or asset-servicing arrangements apply.
- Distinction between asset-backed Sukuk (true sale of underlying asset, recourse limited to the asset) and asset-based Sukuk (asset used as a Shariah-compliance vehicle but with a purchase undertaking that restores conventional-debt-like recourse to the originator) — a structural distinction with real credit and Shariah implications.

## Use This Skill For

- explaining how a corporate Sukuk is structured (Ijarah vs. Diminishing Musharakah vs. Wakala, etc.) and what SECP regulation governs its issuance
- distinguishing GoP Ijara Sukuk auctions (FRR vs. VRR, outright purchase vs. Bai Muajjal) from corporate Sukuk issuance
- explaining the difference between asset-backed and asset-based Sukuk structures and why that distinction matters for investor recourse
- walking through the SPV/trustee/underlying-asset mechanics of a Sukuk issuance
- clarifying how a Sukuk differs structurally from a TFC even where both are used for similar fixed-income fundraising purposes

## When Not to Use This Skill

- For the Shariah Board approval process and Shariah-governance apparatus that certifies a Sukuk structure as compliant, use `sbp-shariah-governance-islamic-banking` instead.
- For conventional Term Finance Certificates (TFCs), Privately Placed TFCs, and the general PSX debt-market listing/trading mechanics, use `pakistan-corporate-debt-capital-markets` instead — use this skill only for Sukuk-specific structural questions.
- For a quick lookup of which debt instruments (TFCs, Sukuks) are currently listed/traded on PSX or margin-eligible, use `psx-debt-and-eligibility` instead — that skill is for retrieving current listed-instrument data, not structuring mechanics.
- For SBP's monetary policy stance or general domestic-debt auction calendar mechanics beyond Sukuk specifically, use `sbp-monetary-policy-statement` instead.

## Routing Rules

- Use this skill for how a Sukuk is structured, what asset underlies it, and how it is issued/auctioned — whether corporate or sovereign.
- If the question is really about a TFC or conventional bond mechanics, route to `pakistan-corporate-debt-capital-markets`, noting the Sukuk/TFC structural distinction if relevant.
- If the question is about whether a specific structure has been Shariah-certified or how a Shariah Board reviewed it, route to `sbp-shariah-governance-islamic-banking`.
- If the question is simply "what Sukuk are currently listed on PSX," route to `psx-debt-and-eligibility` for the data lookup, using this skill only to explain structural terms encountered in that data.

## Extraction Workflow

1. Identify whether the Sukuk in question is corporate (SECP-regulated, private placement or public offer) or sovereign (GoP Ijara Sukuk auctioned via SBP) — the regulatory framework, auction/issuance mechanics, and typical investor base differ.
2. Identify the specific structure type (Ijarah, Diminishing Musharakah, Musharakah, Wakala, Murabaha, Bai Muajjal) before describing risk or return mechanics, since each has a different legal/contractual basis.
3. For GoP Ijara Sukuk, confirm whether the instrument is Fixed Rental Rate (FRR) or Variable Rental Rate (VRR), and whether the transaction is a primary auction, an outright-purchase auction, or a Bai Muajjal (deferred-payment) auction — these are reported and priced differently.
4. For corporate Sukuk, confirm whether the underlying asset arrangement makes the structure asset-backed (true sale, limited recourse to the asset) or asset-based (purchase undertaking restores originator recourse) before characterizing investor risk.
5. Note the as-of date of any auction result, regulation version, or issuance size, since SECP's Sukuk regulations have been amended over time and GIS auction results are point-in-time.

## Technical Rules

- Do not describe a Sukuk as "an Islamic bond" without qualification — a Sukuk certificate represents an undivided beneficial/ownership interest in an underlying asset, business, or project, not a debt obligation of the issuer in the conventional sense, even though asset-based structures can approximate debt-like cash flows.
- Keep asset-backed and asset-based Sukuk structurally distinct; conflating them misstates investor recourse in a default/impairment scenario.
- Do not state specific current profit/rental rates, auction sizes, or regulatory thresholds as fact without sourcing them to a specific dated SBP auction result or SECP notification, since these change with each auction/amendment.
- GoP Ijara Sukuk rental payments are semi-annual and tied to the rental rate mechanism (fixed or variable, often referenced to a benchmark for VRR); do not describe them as "coupon interest" — the underlying legal characterization is a lease rental.
- SPV/trustee arrangements in Sukuk issuances exist specifically to hold or evidence the underlying asset arrangement; do not describe the SPV as a mere administrative formality equivalent to a conventional bond trustee.

## Validation Checklist

- Confirm whether the Sukuk is corporate or sovereign before describing its regulatory or auction framework.
- Verify the specific structure (Ijarah, Diminishing Musharakah, Wakala, etc.) rather than defaulting to a generic "Islamic bond" description.
- For GoP Ijara Sukuk, confirm FRR vs. VRR and the auction mechanism (primary, outright purchase, Bai Muajjal) before citing a rate or amount.
- Check whether the structure is asset-backed or asset-based before making any statement about investor recourse.
- Confirm the source date for any rate, auction result, or regulatory citation.

## Common Pitfalls

- Describing a Sukuk as functionally and legally identical to a conventional bond or a TFC without noting the underlying-asset and ownership-interest distinction.
- Confusing asset-backed with asset-based Sukuk, which have materially different recourse implications.
- Treating GoP Ijara Sukuk rental payments as "interest" rather than lease-rental income under the Ijarah structure.
- Citing a Sukuk auction rate or issuance size without a specific date, given how frequently GIS auctions occur.
- Assuming the 2015 Issue of Sukuk Regulations remain unamended — SECP has revised/consolidated this framework over time; always check for the current regulation text.

## Reference

- See [Pakistan Sukuk Structuring and Issuance Reference](references/pakistan-sukuk-structuring-issuance.md) for structure definitions, source documents, and extraction notes.
