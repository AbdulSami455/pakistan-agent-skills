---
name: secp-insurance-industry-statistics
description: SECP Insurance Industry Statistics skill. Use when analyzing, summarizing, comparing, or extracting information from the Securities and Exchange Commission of Pakistan's annual Insurance Industry Statistics publication, especially for insurer-wise premiums, assets, and takaful (Islamic insurance) statistics.
---

# SECP Insurance Industry Statistics

## Overview

Use this skill for the Securities and Exchange Commission of Pakistan's (SECP) annual Insurance Industry Statistics publication, which reports insurer-wise data on premiums, assets, and takaful operations for Pakistan's insurance sector. This is the right skill for granular, company-level insurance sector figures rather than a systemic risk narrative.

## Coverage

- Insurer-wise gross written premium, broken down by life and non-life (general) insurance segments.
- Insurer-wise total assets and key balance sheet figures.
- Takaful (Islamic insurance) operator statistics, reported alongside or distinct from conventional insurers.
- Market share and concentration figures derived from insurer-wise premium/asset data.
- Published annually by SECP, covering the insurance industry's most recently completed fiscal/calendar year of operation.

## Use This Skill For

- extracting a specific insurer's gross written premium or total assets for a given year
- comparing market share across life, non-life, and takaful segments
- identifying the largest insurers/takaful operators by premium or asset size
- tracking growth in takaful (Islamic insurance) statistics relative to conventional insurance
- comparing insurance industry aggregate figures across consecutive years

## Routing Rules

- Use this skill for SECP's insurer-level statistics (premiums, assets, takaful data).
- If the question is about systemic risk to the insurance sector as part of overall financial stability, prefer `sbp-financial-stability-review`, which includes an insurance risk section but does not provide the granular insurer-wise statistics this skill covers.
- If the question is about banking sector soundness ratios rather than insurance, prefer `sbp-financial-soundness-indicators`.
- If the question is about mutual fund data rather than insurance, prefer `mufap-mutual-funds`.

## Extraction Workflow

1. Identify the specific insurer or takaful operator named in the question, or confirm the question needs an industry-wide aggregate.
2. Confirm whether the figure needed is for the life segment, non-life (general) segment, or takaful, since SECP reports these as distinct categories.
3. Locate the specific year's statistics table rather than assuming continuity with a prior year's figures without checking.
4. Preserve whether a premium figure is gross written premium or net premium (after reinsurance), since these differ materially.
5. When ranking insurers by size, confirm whether the ranking basis is premium volume or total assets, as these can produce different orderings.

## Technical Rules

- Always specify life, non-life, or takaful segment when citing a premium or asset figure, since aggregating across segments without noting it can be misleading.
- Distinguish gross written premium from net premium and from net earned premium where the source provides multiple premium concepts.
- Keep takaful operator figures separate from conventional insurer figures unless the question explicitly asks for a combined industry total.
- Preserve insurer names exactly as listed by SECP, since some companies have similar names or have undergone mergers/rebranding.

## Validation Checklist

- Confirm the segment (life, non-life, takaful) matches what the question is asking about.
- Verify whether the premium figure cited is gross or net.
- Check the reporting year and whether the figures are provisional or final/audited.
- Confirm insurer names against any recent mergers or name changes before treating two entries as the same or different companies.

## Common Pitfalls

- Mixing life and non-life premium figures into a single "insurance premium" total without flagging the blend.
- Confusing gross written premium with net premium after reinsurance cessions.
- Treating takaful statistics as part of conventional insurer totals when SECP reports them separately.
- Using outdated insurer names after a merger or rebranding has occurred.
