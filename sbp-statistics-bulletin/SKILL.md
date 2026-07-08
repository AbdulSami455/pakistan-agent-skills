---
name: sbp-statistics-bulletin
description: SBP statistics and banking indicators skill. Use when analyzing, summarizing, comparing, or extracting information from State Bank of Pakistan statistical releases, especially for monetary aggregates, exchange rates, foreign exchange reserves, interest rates, banking sector balance-sheet items, deposits, advances, and other official time-series data.
---

# SBP Statistics Bulletin

## Overview

Use this skill for numerical time-series questions that come from the State Bank of Pakistan (SBP) rather than from narrative policy documents. This is the right skill when the task needs a current or historical series for reserves, exchange rates, money supply, bank deposits, advances, policy rates, or other SBP-published banking indicators.

This is a data and series-interpretation skill, not a monetary-policy narrative skill and not a bank-specific annual-report skill.

## Coverage

- Monetary aggregates: reserve money, broad money, net domestic assets, net foreign assets, and related stock measures.
- Banking sector indicators: deposits, advances, investment, lending by sector, and aggregate balance-sheet items for scheduled banks.
- Foreign exchange and reserves: SBP-held reserves, exchange-rate series, and other official FX indicators published by SBP.
- Interest-rate series: policy rate history, corridor-related rates, and other SBP-published benchmark rates when the question is about the numerical series rather than the policy rationale.
- Frequency-sensitive releases: weekly, fortnightly, monthly, quarterly, and annual statistical tables that may appear across SBP statistical publications.

## Use This Skill For

- extracting the latest official foreign-exchange reserves or exchange-rate series from SBP
- tracing a policy-rate or benchmark-rate series across time
- pulling banking-sector aggregates such as deposits, advances, or investment
- comparing monthly or weekly SBP indicators over a fiscal year or calendar year
- reconciling a macro figure in the Pakistan Economic Survey with the underlying SBP time series

## When Not to Use This Skill

- For SBP's policy decision narrative or MPC rationale, use `sbp-monetary-policy-statement`.
- For banking-sector stress, solvency, or systemic-risk commentary, use `sbp-financial-soundness-indicators` or `sbp-financial-stability-review`.
- For annual narrative analysis of the economy, use `sbp-annual-report` or the relevant Pakistan Economic Survey skill.
- For a company-specific annual report or financial statement, use the company-level source instead of SBP statistics.

## Routing Rules

- Use this skill when the question is primarily about an official SBP series, not the policy text around it.
- If a user asks "why did SBP change the rate?" route to `sbp-monetary-policy-statement`.
- If a user asks "what are the current reserves / exchange rate / deposits / advances?" route to this skill.
- If the question needs broad macro narrative, cross-reference `pes-macro-and-prices` or `sbp-annual-report` for interpretation, but keep the numerical series from SBP.

## Extraction Workflow

1. Identify the exact indicator and its frequency.
2. Confirm whether the question needs a point-in-time stock, a monthly flow, or a trend series.
3. Preserve the reporting date, unit, and currency exactly as SBP presents them.
4. If the indicator appears in more than one SBP release family, prefer the most direct statistical table over narrative summaries.
5. If a figure is time-sensitive, note the publication vintage and do not treat an older bulletin as current.

## Technical Rules

- Do not mix stock measures and flow measures without labeling them clearly.
- Do not compare weekly and monthly indicators as if they are the same frequency.
- Preserve SBP's terminology for reserves, exchange rates, and rate corridor items rather than normalizing labels too aggressively.
- When a figure can be reported in multiple units or bases, keep the source unit and do not convert silently.
- Distinguish the policy rate from market lending rates, deposit rates, or Treasury-bill yields.

## Validation Checklist

- Confirm the indicator name, frequency, and reporting date.
- Verify whether the value is a stock, a flow, or a point-in-time rate.
- Check that the source is SBP statistical data rather than a narrative publication.
- Confirm whether the series is in PKR, USD, percent, or another unit.
- If comparing periods, verify that both values are from the same series definition.

## Common Pitfalls

- Confusing SBP statistical tables with SBP policy commentary.
- Mixing reserves, deposits, and bank balances as if they are interchangeable.
- Treating a monthly series as if it were weekly, or vice versa.
- Quoting an old publication as if it were the latest available series.
- Confusing policy rate history with commercial lending rates.

## Reference

- See [SBP Statistics Bulletin Reference](references/sbp-statistics-bulletin.md) for source-family notes, interpretation rules, and official links.
