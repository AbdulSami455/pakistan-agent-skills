---
name: pakistan-gazette-notifications
description: Pakistan Gazette and notification skill. Use when verifying official publication dates, legal effect, or wording of Acts, Ordinances, statutory rules, SROs, notifications, appointments, and election gazettes published in the Gazette of Pakistan or related official gazette channels.
---

# Pakistan Gazette Notifications

## Overview

Use this skill when the authoritative question is not "what was proposed?" but "what was officially notified and when did it take effect?" The Gazette is the publication record for many legal and administrative acts of the Government of Pakistan.

This skill complements the legislative tracker. The legislative tracker follows bills through Parliament; this skill follows the official publication and notification record.

## Coverage

- Acts of Parliament and provincial acts when published in official gazette form
- Ordinances and their publication details
- Statutory regulatory orders and notifications
- Service notifications, appointments, transfers, promotions, and removals
- Election-related gazette notifications
- Commencement, amendment, repeal, and substitution notices
- Official publication dates, issue numbers, and effective dates where stated

## Use This Skill For

- confirming whether a law has been officially gazetted
- checking the publication date for an Act, Ordinance, or notification
- distinguishing an administrative notification from a binding legal instrument
- verifying election gazette notices and formal declarations
- locating the wording of a statutory rule, order, or notification as officially published

## When Not to Use This Skill

- For bill status before assent, use `parliament-legislative-tracker`.
- For constituency results and election outcomes before gazette publication, use `ecp-election-results`.
- For court judgments or judicial statistics, use the relevant judicial skill instead.
- For legal interpretation, this skill is a source-verification tool, not a substitute for legal analysis.

## Routing Rules

- Use this skill when the question involves official publication, not just passage or approval.
- If a bill has passed Parliament but the user asks whether it is in force, check the gazette publication and commencement wording.
- If the source says "promulgated," "notified," or "published," verify the gazette entry before making a final claim.

## Extraction Workflow

1. Identify the instrument type: Act, Ordinance, SRO, notification, order, or gazette result.
2. Record the publication date, issue number, and issuing authority.
3. Check whether the text includes a commencement date or an immediate-effect clause.
4. Preserve the title and exact instrument name as printed.
5. If multiple gazette items are related, keep them separate unless the source explicitly consolidates them.

## Technical Rules

- Do not treat a draft, press note, or cabinet approval as equivalent to gazette publication.
- Do not assume publication date and commencement date are the same.
- Preserve whether the item is federal, provincial, or election-related.
- Distinguish an Ordinance from an Act even if both appear in the same gazette issue.
- If the legal effect depends on a subsequent notification, do not stop at the parent instrument.

## Validation Checklist

- Confirm the instrument type and official publication channel.
- Verify the issue date and whether the notice is signed or merely reported.
- Check whether commencement or effectiveness is explicitly stated.
- Confirm whether a later amendment or repeal has superseded the item.
- For election items, confirm whether the gazette is the final official notice or a precursor.

## Common Pitfalls

- Treating parliamentary passage as the same thing as gazette publication.
- Missing the commencement clause and assuming immediate effect.
- Confusing an administrative press release with an official notification.
- Mixing federal and provincial gazette instruments.
- Using a gazette item after it has been superseded by a later notice.

## Reference

- See [Pakistan Gazette Notifications Reference](references/pakistan-gazette-notifications.md) for source-family notes, publication types, and extraction rules.
