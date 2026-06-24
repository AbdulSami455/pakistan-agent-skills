---
name: sbp-ict-exports-special-section
description: SBP IT/ICT Exports Special Section skill. Use when analyzing, summarizing, comparing, or extracting information from the State Bank of Pakistan's Annual, Half-Year, or Quarterly Report "Special Section" chapters that specifically deep-dive on IT/ICT export trends, as distinct from the general SBP annual report or PES's digital economy chapter.
---

# SBP ICT Exports Special Section

## Overview

Use this skill for the State Bank of Pakistan's (SBP) periodic "Special Section" chapters that focus specifically on IT and ICT export performance. SBP's Annual Report, Half-Year Report, and Quarterly Report each occasionally carry a dedicated special/feature section analyzing IT/ICT exports in more analytical depth than the report's routine external-sector tables. This is the right skill for that specific deep-dive content, not for the general SBP annual report's macro narrative or PES's brief digital-economy mention.

## Coverage

- Appears as a "Special Section" or boxed feature chapter within SBP's Annual Report, Half-Year Report, or Quarterly Report (State Bank of Pakistan, sbp.org.pk); not every edition of every report contains one — confirm whether the specific edition in question has an IT/ICT special section before relying on it.
- Typical content: definition and scope of IT/ICT exports as tracked in balance-of-payments data (software, IT services, business process outsourcing, telecom services where included); export value trends over recent years; sub-segment breakdown (e.g., software exports vs. IT-enabled services); destination-market analysis for IT/ICT exports; discussion of freelancer/remittance-like inflows captured under IT exports versus formal corporate exports; policy discussion (e.g., tax incentives, IT export facilitation schemes, exchange retention schemes for IT exporters); comparison with regional peer countries in some editions.
- Document is a self-contained analytical chapter/box within a larger periodic report; it does not have a fixed page template across editions, and its presence is not guaranteed in every report cycle.

## Use This Skill For

- extracting IT/ICT export value trends as analyzed specifically in an SBP special section
- understanding SBP's balance-of-payments definition and scope of what counts as "IT/ICT exports"
- sourcing sub-segment (software vs. IT-enabled services) breakdowns of IT export performance
- identifying SBP's discussion of IT-exporter policy measures (tax incentives, retention schemes)
- distinguishing formally banked IT export receipts from freelancer/informal channel inflows as the special section frames them

## Routing Rules

- Use this skill only for the dedicated IT/ICT special-section content. Use `sbp-annual-report` for SBP's general annual report narrative (monetary policy, financial stability, broader economic review) — that skill covers the report as a whole, not this specific feature chapter.
- Use `pes-infrastructure-digital-and-climate` only for the Pakistan Economic Survey's brief IT/telecom chapter narrative, which does not carry SBP's balance-of-payments-based export analytical depth.
- Use `i2i-startup-ecosystem-report` for venture-funding and ecosystem-player content; this skill is about export earnings and balance-of-payments classification, not startup funding.
- If the report edition under discussion does not contain an IT/ICT special section, say so rather than substituting general SBP export tables as if they were the deep-dive content.

## Extraction Workflow

1. Identify which SBP report (Annual, Half-Year, or Quarterly) and which edition/period contains the special section in question.
2. Confirm the section is specifically the IT/ICT special/feature chapter, not the report's routine external-sector or trade tables.
3. Extract the stated definition/scope of IT/ICT exports used in that edition, since classification can evolve between editions.
4. Preserve sub-segment breakdowns (software vs. services) and destination-market detail separately.
5. Separate formally recorded export receipts from any freelancer/informal-channel discussion the section provides.

## Technical Rules

- IT/ICT export figures here are based on SBP's balance-of-payments classification, which can differ from PBS or commerce-ministry trade definitions; do not merge figures from different classification systems without noting the difference.
- Keep nominal growth distinct from any inflation- or exchange-rate-adjusted commentary the section provides.
- Policy measures (tax incentives, retention schemes) discussed in the section are policy descriptions, not guaranteed realized outcomes; label them as such.
- If peer-country comparisons appear, preserve the comparison basis (e.g., export value, growth rate) exactly as the section frames it.

## Validation Checklist

- Confirm which SBP report and edition the special section is drawn from before quoting a figure.
- Verify that the content is genuinely the IT/ICT special section and not the report's general external-sector table.
- Check whether a figure is software exports, IT-enabled services, or a combined IT/ICT total.
- Confirm the reference period (full year, half year, or quarter) before quoting growth rates.

## Common Pitfalls

- Citing SBP's routine external-sector export tables as if they were the special section's deeper analysis.
- Merging SBP balance-of-payments IT export figures with PBS/commerce-ministry trade figures without flagging the classification difference.
- Treating a special section's policy discussion as a confirmed outcome rather than a description of measures in progress.
- Assuming every SBP report edition contains an IT/ICT special section when it may not.

## Reference

- See [SBP ICT Exports Special Section Reference](references/sbp-ict-exports-special-section.md) for scope definitions and routing notes.
