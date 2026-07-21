---
name: sbp-shariah-governance-islamic-banking
description: SBP Shariah governance and Islamic banking compliance skill. Use when analyzing Shariah Governance Framework (SGF) structure, Shariah Board composition, AAOIFI standard adoption, or Shariah non-compliance risk for Islamic Banking Institutions (IBIs) regulated by the State Bank of Pakistan — for actuaries, auditors, or compliance officers assessing an IBI's Shariah governance architecture rather than its financial soundness ratios.
---

# SBP Shariah Governance and Islamic Banking

## Overview

Use this skill for the regulatory architecture that governs Shariah compliance at Islamic Banking Institutions (IBIs) in Pakistan — full-fledged Islamic banks and the Islamic banking windows/branches of conventional banks — as set by the State Bank of Pakistan (SBP). This is the right skill for Shariah Governance Framework (SGF) structure, Shariah Board composition and powers, the Shariah Compliance/Audit/Review functions, AAOIFI standard adoption, and Shariah non-compliance risk mechanics. It is not a skill for bank-wide prudential ratios (CAR, NPLs) or general banking-sector soundness — those belong to `sbp-financial-soundness-indicators`.

## Coverage

- The Shariah Governance Framework (SGF) for Islamic Banking Institutions, issued and periodically revised by SBP's Islamic Finance department (formerly Islamic Banking Department), most recently overhauled via IFPD Circular No. 08 of 2024 (compliance timeline into 2025).
- Shariah Board (SB) structure: minimum scholar composition, fit-and-proper criteria, appointment/removal process, and the SB's binding authority over Shariah matters at the IBI (distinct from the Board of Directors' governance authority).
- Second line of defence: the Shariah Compliance Department and Shariah Review function, which monitor day-to-day product and transaction compliance.
- Third line of defence: internal Shariah Audit, which independently tests the adequacy of the compliance and review functions, feeding into the IBI's overall internal audit structure.
- Adoption of AAOIFI (Accounting and Auditing Organization for Islamic Financial Institutions) Shariah standards in Pakistan — SBP has directed phased adoption of specific AAOIFI Shariah standards as mandatory for IBIs, layered on top of SBP's own SGF and Fatwa/ruling mechanisms.
- Shariah non-compliance risk: the concept that income or a transaction found non-Shariah-compliant after the fact must be purified (typically via charity/Shariah-compliant disposal) rather than recognized as bank income — a risk category distinct from credit, market, or operational risk.
- Product approval workflow: new Islamic banking products/structures (Murabaha, Ijarah, Diminishing Musharakah, Musharakah, Mudarabah, Salam, Istisna variants) require Shariah Board approval before launch, and SBP maintains its own essentials/model agreements for common modes.

## Use This Skill For

- explaining the Shariah Board's composition requirements and its relationship to the Board of Directors
- describing the three-lines-of-defence structure for Shariah compliance (compliance, review, audit) at an IBI
- clarifying which AAOIFI Shariah standards have been mandated for adoption in Pakistan and how SBP layers its own SGF on top
- explaining Shariah non-compliance risk and purification-of-income mechanics
- distinguishing an Islamic banking window/branch of a conventional bank from a full-fledged Islamic bank for governance purposes
- walking through the product-approval process for a new Islamic banking mode of finance

## When Not to Use This Skill

- For an Islamic bank's or conventional bank's capital adequacy, NPL, or profitability ratios, use `sbp-financial-soundness-indicators` instead.
- For narrative systemic-risk discussion of the Islamic banking segment within overall financial stability, use `sbp-financial-stability-review` instead.
- For Sukuk instrument structuring and issuance mechanics (as opposed to the Shariah-governance apparatus that approves such structures), use `pakistan-sukuk-structuring-issuance` instead.
- For a bank customer's consumer-complaint escalation process, use `sbp-banking-consumer-protection` instead — this skill covers institutional Shariah governance, not retail dispute resolution.
- For general banking-sector monetary policy or liquidity operations (including Islamic liquidity/OMO tools), use `sbp-monetary-policy-statement` instead.

## Routing Rules

- Use this skill when the question concerns how Shariah compliance is governed, verified, or audited inside an Islamic Banking Institution.
- If the question is about a specific financial ratio or soundness metric of an Islamic bank, route to `sbp-financial-soundness-indicators` and only use this skill for the Shariah-governance dimension if asked.
- If the question is about a Sukuk (government or corporate) as a capital-markets instrument, route to `pakistan-sukuk-structuring-issuance`; use this skill only for the underlying Shariah Board approval mechanics if that is specifically asked.
- Do not present AAOIFI standards as automatically and fully binding in Pakistan in every respect — SBP adopts specific standards on a phased/circular basis; always anchor an AAOIFI-adoption claim to the specific circular that mandates it.

## Extraction Workflow

1. Identify whether the question is about governance structure (Shariah Board, compliance/review/audit functions) or about a specific product's Shariah permissibility — these require different levels of specificity and the latter may exceed this skill's scope into fiqh territory best deferred to a qualified Shariah scholar.
2. Confirm which version of the SGF is being discussed — SBP has revised the SGF multiple times (2015, 2018, and a substantial 2024 revision effective for compliance in 2025); do not assume an older SGF's specific mechanics still apply without checking the current circular.
3. Distinguish a full-fledged Islamic bank from a conventional bank's Islamic banking window/branch — governance expectations (e.g., dedicated Shariah Board applicability) can differ by institutional form.
4. When AAOIFI standards are invoked, identify the specific standard number/name and confirm it is one SBP has actually directed IBIs to adopt, rather than assuming blanket AAOIFI applicability.
5. Keep the Shariah Board's religious/fiqh authority conceptually distinct from the Board of Directors' corporate governance authority — the SB's rulings on Shariah matters are binding on the IBI's operations.

## Technical Rules

- Do not describe Islamic banking as merely "interest-free conventional banking with different labels" — Shariah governance exists precisely because the underlying contracts (sale-based, lease-based, partnership-based) have materially different risk, ownership, and default mechanics than a conventional loan.
- Keep the Shariah Compliance function (first-line monitoring), Shariah Review (second-line testing), and Shariah Audit (third-line independent assurance) analytically distinct; do not collapse them into a single "Shariah compliance" bucket.
- Do not state a specific minimum number of Shariah Board scholars, specific compliance deadlines, or specific penal provisions as current fact without verifying against the currently effective SGF circular, since SBP revises these periodically.
- Purification of Shariah non-compliant income is a distinct accounting and governance concept from provisioning for credit losses; do not conflate the two.
- This skill does not substitute for a Shariah scholar's or qualified Shariah advisor's fatwa on whether a specific transaction structure is Shariah-compliant — it describes the governance apparatus, not fiqh rulings themselves.

## Validation Checklist

- Confirm which SGF version/circular year is the basis for any structural claim (Shariah Board composition, reporting lines, etc.).
- Verify whether the entity in question is a full-fledged Islamic bank or an Islamic banking window of a conventional bank.
- Check whether an AAOIFI-standard claim is tied to a specific SBP circular mandating that standard, rather than assumed as generally applicable.
- Confirm any numeric threshold (Shariah Board size, compliance deadlines) against the current SBP circular rather than an earlier version of the SGF.

## Common Pitfalls

- Treating the 2015/2018 SGF's specific mechanics as still current without checking the 2024 revision (IFPD Circular No. 08 of 2024) and its 2025 compliance timeline.
- Conflating Shariah Compliance, Shariah Review, and Shariah Audit into one undifferentiated function.
- Assuming all AAOIFI standards are binding in Pakistan by default rather than checking which specific standards SBP has directed for adoption.
- Answering a product-specific Shariah-permissibility question as if it were a governance-structure question, when it actually requires a scholar's fiqh opinion.
- Describing Islamic banking products as functionally identical to their conventional counterparts without noting the underlying contract structure difference (sale/lease/partnership vs. interest-bearing loan).

## Reference

- See [SBP Shariah Governance and Islamic Banking Reference](references/sbp-shariah-governance-islamic-banking.md) for SGF structure, source circulars, and extraction notes.
