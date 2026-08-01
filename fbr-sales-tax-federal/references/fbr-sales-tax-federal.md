# FBR Federal Sales Tax Reference

## Source

- Sales Tax Act, 1990 (as amended) — FBR's consolidated Sales Tax laws page: `https://www.fbr.gov.pk/sales-tax-acts/131147` (verify current path; FBR's site structure and numeric paths change periodically)
- Sales Tax Rules, 2006, and Sales Tax Special Procedures Rules, 2007 (verify current consolidated versions on `fbr.gov.pk`)
- FBR IRIS e-filing portal (registration and return filing): `https://iris.fbr.gov.pk`
- Annual Finance Act (amends Sales Tax Act rates/thresholds/Schedules each fiscal year) — Finance Division: `https://www.finance.gov.pk`

## Legal Structure

- The Sales Tax Act, 1990 is the principal federal statute; it charges sales tax on (a) taxable supplies made in Pakistan by a registered person in the course of taxable activity, and (b) goods imported into Pakistan.
- The Act's **Schedules** enumerate goods subject to specific treatment: the Third Schedule historically lists goods taxed on retail price basis; the Fifth Schedule lists zero-rated supplies; the Sixth Schedule lists exempt supplies; other Schedules address reduced rates or sector-specific treatment. Schedule contents are amended frequently via the annual Finance Act and standalone SROs — always verify current Schedule placement for a specific good rather than assuming a historical classification still holds.
- Administration sits with FBR's **Inland Revenue** wing for domestic registration, audit, and return processing; import-stage sales tax collection is executed by **Pakistan Customs** at the import/clearance stage (via WeBOC/Pakistan Single Window) but the charging authority remains the Sales Tax Act.

## Registration

- Registration is triggered by categorical criteria (manufacturer, importer, wholesaler/dealer/distributor, exporter, or a retailer above a specified turnover/criteria threshold) rather than a single universal turnover figure — the exact categorical triggers and any turnover thresholds (e.g., for retailers) are set by the Act/Rules and revised periodically (verify current figure).
- Registration is completed through **IRIS**, FBR's online tax administration portal, producing a Sales Tax Registration Number (STRN), which for most business taxpayers is linked to the same National Tax Number (NTN)/Business registration used for income tax purposes.
- Unregistered persons making taxable supplies above the applicable threshold are liable to compulsory registration and can face penal consequences under the Act for failure to register.

## Rate Structure

- The **standard rate** is an ad valorem percentage applied to the value of taxable supply; it has been amended multiple times historically via Finance Acts and is currently around the high-teens percentage range as of recent Finance Acts — always verify the specific rate in force for the tax period in question rather than citing a fixed number from memory (verify current rate).
- **Reduced rates** apply to specified goods/sectors under notified SROs or Schedule provisions (e.g., certain essential goods, or sector-specific reduced-rate regimes) — these are narrower carve-outs from the standard rate, not the default.
- **Zero-rating** (0% rate) applies to specified categories, most notably exports of goods, and certain other categories listed in the Fifth Schedule; a zero-rated supplier can still claim/refund input tax paid on inputs used to make the zero-rated supply.
- **Exemption** (no tax charged at all) applies to goods listed in the Sixth Schedule; a supplier of wholly exempt goods generally cannot adjust or refund input tax attributable to those exempt supplies, since no output tax is being charged against which to offset it.

## Input/Output Tax Mechanism and Filing

- A registered person's **output tax** is the sales tax charged on their taxable supplies during a tax period; **input tax** is the sales tax they paid on their own purchases/imports used in the taxable activity. The **net tax payable** is output tax minus adjustable input tax for the period; if input tax exceeds output tax, the excess may be carried forward or, for specified categories (notably exporters), claimed as a refund.
- Input tax attributable to exempt supplies (or to non-business use) is not adjustable; a registered person making both taxable and exempt supplies must apportion input tax between the two, per formulas set out in the Rules.
- The **Sales Tax Return (STR)**, commonly filed monthly, is submitted electronically through IRIS, declaring supplies made, purchases made, output tax, input tax, and the resulting payable/refundable/carried-forward position for the period. Filing and payment due dates are administratively set (historically clustered around mid-to-late month following the tax period) and should be verified against the current FBR-notified schedule rather than assumed fixed.
- FBR also runs a **sales tax withholding** regime (Sales Tax Special Procedures (Withholding) Rules) under which specified withholding agents (e.g., government departments, large companies, or specified sectors) withhold a portion of sales tax on payments to suppliers and deposit it directly, modifying the standard full-charge/full-credit flow for those transactions.

## Extraction Notes

- Always separate goods (this skill, Sales Tax Act 1990, federal) from services (provincial sales tax statutes, `provincial-sales-tax-authorities`) — the two are governed by entirely different legislatures' laws even where invoiced together.
- Flag any specific rate, threshold, or filing-deadline figure as subject to Finance Act/SRO revision and requiring current-period verification.
- Keep zero-rated and exempt supplies analytically distinct given their different input-tax-credit consequences.
- Note that import-stage sales tax is a Sales Tax Act charge operationally collected by Customs, not a customs-tariff-schedule item; route tariff-classification questions to `fbr-customs-tariff`.
