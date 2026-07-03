---
name: bisp-social-protection-statistics
description: BISP social protection statistics skill. Use when analyzing, summarizing, comparing, or extracting information from the Benazir Income Support Programme's (BISP) annual reports, beneficiary statistics, payment disbursement data, or poverty-targeting publications, especially for cash transfer coverage, beneficiary counts, and program expenditure.
---

# BISP Social Protection Statistics

## Overview

Use this skill for questions about Pakistan's flagship social protection cash transfer programme, the Benazir Income Support Programme (BISP), and its successor branding under the broader Ehsaas/Benazir umbrella. This covers BISP's annual reports, beneficiary statistics, payment disbursement records, and poverty-targeting publications — distinct from general poverty estimates in PSLM or the PES social-protection narrative.

## Coverage

- Published by BISP (Benazir Income Support Programme), under the Ministry of Poverty Alleviation & Social Safety.
- Typical content: total number of beneficiary families/households enrolled; quarterly or annual payment disbursement totals (amount disbursed, number of payments); beneficiary breakdown by province, district, or gender of recipient; poverty scorecard (NSER) registration and survey coverage statistics; complementary programme coverage (e.g., Benazir Taleemi Wazaif education stipends, Benazir Nashonuma nutrition support) when reported within BISP publications.
- BISP publishes annual reports and periodic statistical summaries; payment data may also appear in quarterly or monthly disbursement reports.
- Programme branding has evolved (BISP → Ehsaas → Benazir Kafaalat/Benazir Income Support); preserve the programme name used in the source document.

## Use This Skill For

- extracting total beneficiary household counts for BISP/Benazir cash transfers
- identifying payment disbursement totals (amount and number of transactions) for a period
- breaking down beneficiaries by province, district, or gender
- tracking NSER (National Socio-Economic Registry) registration or survey coverage
- comparing programme coverage or disbursement across fiscal years

## Routing Rules

- Use this skill for BISP/Benazir programme-specific statistics (beneficiary counts, disbursements, NSER coverage). For general national poverty rates or inequality measures, prefer `pbs-pslm` for survey-based poverty estimates or `pes-social-sectors` (Chapter 16: Social Protection) for the annual narrative summary.
- For the Pakistan Economic Survey's social-protection chapter narrative (headline poverty trend, broad programme overview), prefer `pes-social-sectors` for the summary and this skill for underlying BISP programme detail.
- For provincial social welfare programme statistics outside BISP's federal mandate, check provincial development statistics skills (`punjab-development-statistics`, `sindh-development-statistics`, etc.) rather than assuming BISP covers provincial programmes.
- BISP disbursement amounts are programme expenditure, not remittance inflows; do not conflate with `pkr-remittances-tracker`.

## Extraction Workflow

1. Identify the report period (fiscal year, quarter, or month) and the specific programme component (Kafaalat, Taleemi Wazaif, Nashonuma, etc.) if the question is component-specific.
2. Distinguish beneficiary household counts from individual recipient counts; BISP typically reports at the household level.
3. Extract disbursement figures from statistical tables rather than narrative summaries.
4. Preserve the programme name as used in the source document (BISP, Ehsaas, Benazir Kafaalat, etc.).
5. Note whether beneficiary counts are cumulative enrolled stock or new enrollments during the period.

## Technical Rules

- Beneficiary counts are typically reported as households/families, not individuals; do not multiply by an assumed household size unless the source provides an individual count.
- Disbursement totals and beneficiary counts are different metrics; a period's disbursement total does not directly imply the number of active beneficiaries without checking the payment frequency.
- NSER registration coverage and active beneficiary counts are distinct; not all registered households receive payments in every period.
- Programme rebranding across years (BISP → Ehsaas → Benazir) may affect table labels; preserve the source terminology and note any mapping if comparing across rebranding periods.

## Validation Checklist

- Confirm the report period and programme component.
- Verify whether the count is households or individuals.
- Check whether disbursement is for a single payment cycle or cumulative for the period.
- Confirm whether beneficiary figures are active recipients or cumulative enrolled stock.

## Common Pitfalls

- Conflating BISP beneficiary counts with national poverty headcount rates from PSLM.
- Treating a single payment cycle's disbursement as annual programme expenditure without checking payment frequency.
- Mixing BISP cash transfer disbursements with worker remittance inflows.
- Assuming all NSER-registered households are active payment recipients.

## Reference

- See [BISP Social Protection Reference](references/bisp-social-protection-statistics.md) for report structure and extraction notes.
