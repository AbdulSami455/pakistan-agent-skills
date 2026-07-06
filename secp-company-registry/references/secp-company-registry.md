# SECP Company Registry Reference

## Regulator

The Securities and Exchange Commission of Pakistan (SECP) is the federal regulator responsible for incorporating and regulating companies, non-banking financial companies (NBFCs), insurance/takaful firms, and — separately — Limited Liability Partnerships (LLPs) in Pakistan. Company incorporation and regulation is governed primarily by the **Companies Act, 2017** (which replaced the Companies Ordinance, 1984). SECP's registration and post-incorporation compliance functions are increasingly delivered through online e-Services rather than paper filings.

## Company Categories Under the Companies Act, 2017

SECP incorporates several distinct categories of company. These categories are not interchangeable, and a company's category is a formal legal attribute recorded at incorporation (it can change later only through a formal conversion process):

- **Private Limited Company** — the most common category for small and medium businesses. Minimum two members (a **Single Member Company**, see below, is the one-person exception). Cannot offer shares to the public. Name typically ends in "(Private) Limited" or "(Pvt.) Ltd."
- **Public Limited Company** — can offer shares/securities to the public. Two sub-types matter in practice:
  - **Listed public company** — a public company whose shares are listed on the Pakistan Stock Exchange (PSX). Subject to additional PSX and SECP listed-company regulations (e.g., Listed Companies (Code of Corporate Governance) Regulations).
  - **Unlisted public company** — registered as a public limited company but not listed on any exchange.
  Name ends in "Limited" (no "Private").
- **Single Member Company (SMC)** — a private company structure introduced to allow a single individual to incorporate a company alone, without needing a second member. Name typically carries the suffix "(SMC-Private) Limited."
- **Company Limited by Guarantee** — used for non-profit, charitable, or membership-based entities (e.g., trade associations, foundations, some NGOs) where members' liability is limited to a guaranteed amount rather than share capital. Often referred to informally as an "association not for profit" when it also obtains a licence under Section 42 of the Companies Act, 2017 (formerly Section 42 of the 1984 Ordinance) permitting it to omit "Limited" from its name.
- **Foreign Company (Section 435 registration)** — a company incorporated outside Pakistan that establishes a place of business in Pakistan (e.g., a branch or liaison office) must register with SECP under Section 435 of the Companies Act, 2017. This is a registration of the foreign company's Pakistani presence, not incorporation of a new Pakistani company — the entity remains a foreign-incorporated company operating a registered branch/liaison office locally. Its SECP filing requirements (returns, documents, authorized representative) differ from those of a locally incorporated company.

## LLPs Are a Separate Registry — Not Part of "Company" Registration

Limited Liability Partnerships were introduced in Pakistan under the **Limited Liability Partnership Act, 2017**, a separate statute from the Companies Act, 2017. Although both are administered by SECP and both use hybrid corporate/partnership features (limited liability for partners, separate legal personality), an LLP is **not** a "company" in the Companies Act sense:

- LLPs are registered, and their names/status looked up, through a distinct LLP registration process/register, not the standard company name-search used for private/public limited companies.
- An LLP's constitutional document is an "LLP agreement" between partners, not a Memorandum and Articles of Association.
- Do not report an LLP as if it were a "private limited company" or vice versa — they are different legal forms under different statutes, even though SECP is the common regulator for both.
- When a lookup task is ambiguous about whether an entity is a company or an LLP, check which register returned the match rather than assuming.

## Status Values

A SECP-registered company's status field is a key part of any registry lookup and generally falls into these categories (exact wording on SECP's search results may vary slightly by system version, so treat the following as the substantive categories rather than exact on-screen strings):

- **Active / In Operation** — the company is currently registered and has not been struck off, wound up, or dissolved. This does not by itself confirm the company is filing annual returns on time or is otherwise fully compliant — only that it has not been removed from the register.
- **Inactive / Defaulting / Non-filing** — some SECP-facing systems distinguish companies that are technically still on the register but have failed to file statutory returns (annual return, financial statements) for a period; treat any such flag as a compliance-status signal distinct from full active status if the source surfaces it.
- **Struck Off** — the company has been removed from the register, most commonly under the Companies Act's power for SECP to strike off a company that is not carrying on business or in operation (analogous to a defunct-company removal). A struck-off company generally ceases to have separate legal personality upon removal, subject to restoration provisions in the Act.
- **Under Liquidation / Winding Up** — the company is undergoing formal winding-up proceedings (voluntary or by court/SECP order) under the Companies Act's winding-up provisions. This is a distinct legal process from an administrative strike-off and can take considerably longer.
- **Dissolved** — the company has completed winding-up and has been formally dissolved, ending its legal existence.

Always report the status exactly as returned by the live lookup, along with the date the lookup was performed, since status changes over time and this skill's own SKILL.md already stresses not fabricating a status if a live check was not actually done.

## SECP e-Services / Business Registration Portal Structure

SECP has moved most registration and post-incorporation functions online. In practice, an agent or user is likely to encounter two related but distinct online surfaces (naming and structure have evolved over time, so confirm current URLs/branding rather than assuming these are fixed):

- **Public company/name search** — a public-facing, no-login search used to verify whether a name is registered and to see basic public particulars (registration number, incorporation date, category, status). This is the facility referenced in this skill's main SKILL.md lookup workflow.
- **e-Services / Business Registration Portal (login-based)** — the transactional portal used by applicants and company officers to: reserve a company name, submit incorporation documents (Memorandum and Articles of Association, or LLP agreement for LLPs), pay incorporation fees, and subsequently file statutory returns (annual return, financial statements, changes in directors/registered office, etc.). This portal requires registration/login and is not the same interface as the public name-search tool.
- Foreign company Section 435 registrations and NPO/Section 42 licensing typically involve additional document submission (e.g., approval from the relevant authority for Section 42 companies) beyond the standard private/public company incorporation flow.

Because these online surfaces are administered as web applications rather than documented public APIs, treat any URL, form field, or workflow description here as subject to change — the operative caution already stated in this skill's SKILL.md (verify the live page rather than assuming a stable structure) applies equally to the categories and status labels above; the legal categories (private/public/SMC/guarantee/foreign/LLP) are stable statutory concepts, but the on-screen presentation of status and portal navigation is not guaranteed to match this description indefinitely.

## Verification Note

The specific field labels, exact strike-off terminology, and current portal URLs should be confirmed against SECP's own site (`secp.gov.pk`, `eservices.secp.gov.pk`) at the time of use. The legal categories and the Companies Act 2017 / LLP Act 2017 split described above reflect the statutory framework and are stable; day-to-day portal UI details are not.
