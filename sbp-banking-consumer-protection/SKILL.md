---
name: sbp-banking-consumer-protection
description: SBP banking consumer-protection skill. Use when explaining how an individual disputes a bank charge, complains about poor service, or escalates an unresolved banking complaint through a bank's Complaint Management Unit and, if unresolved, the Banking Mohtasib Pakistan (Banking Ombudsman) — as distinct from SBP's monetary-policy or financial-stability functions.
---

# SBP Banking Consumer Protection

## Overview

Use this skill for an individual bank customer's complaint and dispute-resolution process in Pakistan: escalation through a bank's own Complaint Management Unit (CMU), State Bank of Pakistan's consumer-protection framework, and the Banking Mohtasib Pakistan (BMP), an independent statutory ombudsman for banking disputes. This is a consumer-process reference skill, not a monetary-policy, banking-sector-soundness, or financial-stability skill.

## Coverage

- First-tier resolution: every bank is required to maintain a Complaint Management Unit (CMU) as the first point of contact for a customer complaint (e.g., disputed transaction, service quality, fee dispute, ATM/card issue).
- SBP's consumer-protection framework: State Bank sets rules/regulations banks must follow on complaint handling, disclosure, and fair treatment of customers, and maintains its own consumer-protection department oversight function.
- Banking Mohtasib Pakistan (BMP): an independent statutory ombudsman body (under the Federal Ombudsman Institutional Reforms Act) that a customer can approach if a bank's CMU fails to resolve a complaint within a specified period (typically around 45 days) or the customer remains unsatisfied with the CMU's response.
- Scope of BMP complaints: violations of banking law/regulation, excessive delays or inefficiency, poor service, discriminatory treatment, and similar service/conduct issues; BMP's process is largely conciliatory and free of charge, without requiring legal representation.
- Escalation sequence: bank's CMU first, then BMP if unresolved — this sequence should generally not be skipped.

## Use This Skill For

- explaining the general steps a customer should take to dispute a bank charge or service issue
- describing when and how to escalate an unresolved bank complaint to the Banking Mohtasib
- clarifying what types of issues fall within Banking Mohtasib's scope
- explaining that the Banking Mohtasib process is free and does not require legal representation
- distinguishing SBP's consumer-protection/complaint-handling role from its monetary-policy or banking-supervision functions

## When Not to Use This Skill

- For SBP's monetary policy decisions (policy rate) — use `sbp-monetary-policy-statement` instead.
- For bank-wise soundness indicators (NPL ratios, capital adequacy) — use `sbp-financial-soundness-indicators` instead; that is supervisory/prudential data, not individual consumer dispute resolution.
- For systemic financial-stability risk narrative — use `sbp-financial-stability-review` instead.
- For a specific individual's live complaint status — direct the user to the bank's CMU or BMP's official tracking channel rather than asserting a status.

## Routing Rules

- Use this skill for an individual customer's complaint/dispute process, not for macro-level banking-sector statistics or monetary policy.
- If the question is about aggregate bank soundness or systemic risk rather than an individual complaint, route to `sbp-financial-soundness-indicators` or `sbp-financial-stability-review` respectively.
- Always describe the escalation sequence (CMU first, then BMP) rather than suggesting BMP as a first-resort option without going through the bank's own complaint channel first.

## Extraction Workflow

1. Identify the nature of the complaint (disputed transaction, fee, service quality, discriminatory treatment, etc.) to confirm it falls within typical CMU/BMP scope.
2. Confirm whether the customer has already filed with the bank's CMU and how long it has been pending, since BMP escalation generally requires either CMU non-response within the specified period or an unsatisfactory CMU resolution.
3. Describe the general BMP complaint process (written complaint, no cost, no lawyer required, conciliatory approach) without asserting a guaranteed outcome.
4. If the question is actually about a systemic/sector-wide banking issue rather than an individual dispute, redirect to the appropriate SBP sector-statistics or policy skill instead.

## Technical Rules

- CMU escalation is generally the required first step before BMP; do not present BMP as a direct first-resort channel bypassing the bank's own complaint process.
- BMP's process is conciliatory and free of charge, without requiring legal representation — do not describe it as a formal litigation process.
- Keep SBP's consumer-protection/complaint-oversight role distinct from its monetary-policy and prudential-supervision roles, which are separate SBP functions covered by other skills.
- BMP addresses banking-sector complaints specifically; a complaint about a non-bank financial institution (e.g., certain NBFCs, insurance) may fall under a different ombudsman or regulator.

## Validation Checklist

- Confirm the complaint type falls within typical CMU/BMP banking-dispute scope.
- Verify whether the customer has already attempted CMU resolution before suggesting BMP escalation.
- Check that the question is about an individual dispute rather than aggregate banking-sector data, which belongs to a different skill.
- Confirm BMP's process is described accurately as free, conciliatory, and not requiring legal representation.

## Common Pitfalls

- Suggesting Banking Mohtasib escalation without first confirming the customer has gone through the bank's own CMU process.
- Confusing SBP's consumer-protection/complaint role with its monetary-policy or bank-soundness-supervision functions.
- Describing the Banking Mohtasib process as a paid or legally represented formal litigation process rather than a free, conciliatory one.
- Treating a non-bank financial complaint (e.g., insurance) as if it fell under Banking Mohtasib's specifically banking-sector scope.

## Reference

- See [SBP Banking Consumer Protection Reference](references/sbp-banking-consumer-protection.md) for process structure and extraction notes.
