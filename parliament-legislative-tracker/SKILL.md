---
name: parliament-legislative-tracker
description: Pakistan legislative bill-tracking skill. Use when tracking a bill's status (introduced, in committee, passed by National Assembly, passed by Senate, presidential assent) through the National Assembly and Senate of Pakistan websites or openparliament.pk's Legislative Tracker.
---

# Parliament Legislative Tracker

## Overview

Use this skill when a task asks where a specific bill stands in Pakistan's federal legislative process, or asks for a list of bills currently pending, passed, or assented to. This is a status-tracking skill built on structured HTML pages, not a full-text legal research tool.

## Important Caveat

There is **no confirmed formal API** for the National Assembly (NA) bill-tracking pages, the Senate bill-tracking pages, or openparliament.pk's Legislative Tracker. All of these are structured HTML pages intended for human browsing:

- Treat extraction from these sources as HTML-structure parsing, not API consumption.
- openparliament.pk and similar aggregator/civic-tech sites are convenient for browsing and search but **may lag behind the official NA/Senate pages** — always verify a bill's current status against the official National Assembly or Senate site directly before reporting it as final, especially for time-sensitive questions (e.g., "has this bill passed yet").
- Page structure, bill numbering schemes, and session/year archives can change between parliamentary sessions.

## Coverage

- National Assembly bill status pages (introduced bills, bills passed by NA, bills sent to Senate)
- Senate of Pakistan bill status pages (bills received from NA, Senate-originated bills, Senate committee reports)
- openparliament.pk Legislative Tracker (aggregated bill status, often with committee and timeline detail not always easy to find on official sites)

## Use This Skill For

- determining a bill's current stage: introduced, referred to committee, passed by NA, passed by Senate, presidential assent/promulgation, lapsed
- identifying which committee a bill is currently with
- finding the date a bill was introduced, passed, or assented to
- listing bills introduced in a given parliamentary session or year
- distinguishing a government bill from a private member's bill

## Use This Skill For — Not

- Full statutory text retrieval or legal interpretation of an Act
- Case law or judicial commentary (see `ljcp-judicial-statistics` for court statistics, not bill tracking)
- Provincial assembly bills (NA and Senate cover the federal legislature only)

## Extraction Workflow

1. Identify the bill by exact short title and, if available, bill number/year — titles can be similar across sessions.
2. Check the official NA bill-status page first for: introduction date, mover, committee referral, and passage date.
3. Cross-check the Senate bill-status page for Senate-stage progress if the bill has passed the NA.
4. Use openparliament.pk's Legislative Tracker as a secondary cross-check or for a consolidated timeline view, but flag it as a secondary source.
5. Note the presidential-assent date and gazette notification if the bill has become an Act — this is the final confirming stage.
6. If sources disagree, state the discrepancy explicitly and prefer the official chamber site's stated status.

## Technical Rules

- Always record which source (NA site, Senate site, or openparliament.pk) a status claim came from.
- Treat "passed by NA" and "passed by Senate" as distinct stages — a bill is not law until it clears both chambers (or a joint sitting, where applicable) and receives assent.
- Do not assume a bill listed as "introduced" is still active — check for lapse, withdrawal, or session-end status.
- Bill titles are sometimes amended between introduction and passage; note if the title changed.

## Validation Checklist

- Confirm the bill number/year and short title match exactly across sources.
- Confirm which chamber's stage was last updated and the date of that update.
- Verify whether presidential assent has actually occurred versus the bill merely having passed both chambers.
- Flag any status claim sourced only from an aggregator without official-site cross-check.

## Common Pitfalls

- Reporting an aggregator's bill status as current without checking the official NA/Senate page for a more recent update.
- Confusing a Senate-originated bill with an NA-originated bill that has been transmitted to the Senate.
- Treating committee referral as equivalent to committee approval/reporting-back.
- Citing a bill number without specifying which assembly session/year it belongs to, since numbering can reset per session.

## Source

- National Assembly of Pakistan: `https://na.gov.pk`
- Senate of Pakistan: `https://senate.gov.pk`
- Pakistan Legislative Tracker (openparliament.pk): `https://openparliament.pk`
- National Assembly bill tracking: `https://na.gov.pk/en/bills.php`
