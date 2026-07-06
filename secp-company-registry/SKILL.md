---
name: secp-company-registry
description: SECP eServices company registry lookup skill. Use when verifying a Pakistani company's registration status, incorporation date, registration number, or category (private limited, public limited, NPO, foreign company) via the Securities and Exchange Commission of Pakistan's public company/name search.
---

# SECP Company Registry

## Overview

Use this skill when a task requires confirming whether a company is registered with SECP, finding its incorporation date, registration number, or legal category. This is a verification and lookup skill, not a financial or filings-analysis skill.

## Important Caveat

SECP's public company search (accessible through SECP eServices) is an **HTML web search form, not a formal published API**. There is no documented, stable programmatic endpoint for this lookup. Treat any automated scripting against it as fragile:

- Form field names, search parameters, and result page structure can change without notice.
- CAPTCHAs or session tokens may gate the search at any time.
- Bulk or repeated automated queries may be rate-limited or blocked.

Because of this, this skill should guide a human or agent through a **manual lookup procedure**, describing what to expect on the page, rather than assuming a reliable scriptable interface exists. If programmatic access is attempted, it must be treated as best-effort and verified manually before being relied upon.

## Use This Skill For

- confirming a company name is registered with SECP
- checking a company's registration/incorporation date
- identifying a company's category (private limited, public limited, single member, NPO/association, foreign company, LLP)
- distinguishing an active company from one that has been struck off or is in liquidation
- cross-checking a company name variant against the official registered name

## Use This Skill For — Not

- Pulling financial statements or annual filings (not covered here)
- Researching insurance-sector entities in depth (see `secp-insurance-industry-statistics` for that)
- Legal case research involving a company (not a court-records skill)

## Lookup Workflow

1. Navigate to the SECP eServices company/name search facility (search "SECP eServices company search" if the URL has changed).
2. Search by company name (partial name matching is typically supported) or by registration/incorporation number if known.
3. Note the exact registered name returned — it may differ from the colloquial or trading name.
4. Record the fields typically shown: registration number, incorporation date, company category (e.g., private limited, public limited, NPO/association, foreign company branch), and current status (active, struck off, under liquidation, dissolved).
5. If multiple similarly named entities appear, disambiguate using incorporation date or registration number before reporting a result.
6. If the search interface fails to load, returns no formal data fields, or appears to have changed structure, report that the lookup could not be completed reliably rather than guessing at a result.

## Technical Rules

- Never fabricate a registration number, incorporation date, or status if the live lookup was not actually performed or the page did not return that field.
- Always state the lookup date when reporting registration status, since status can change (e.g., a company can be struck off after this skill was last used).
- Treat name-search results as approximate matches; only treat an exact registration-number match as a confirmed identity match.
- Do not assume the search form's URL or parameters are stable across sessions — re-verify the entry point if a prior approach fails.

## Validation Checklist

- Confirm the registered name exactly, including suffixes like "(Private) Limited" or "(Guarantee) Limited".
- Confirm whether the status field indicates active, struck off, dissolved, or in liquidation.
- Confirm the category (private/public/NPO/foreign) is read from the actual result, not inferred from the company name.
- Note if the result set returned zero matches versus the search failing to load.

## Common Pitfalls

- Treating a similarly named but distinct company as a match.
- Assuming SECP eServices exposes a stable JSON/API response — it does not, as of the latest verified state of this skill.
- Reporting incorporation date or status without noting the date the lookup was performed.
- Confusing SECP company registration with tax registration (FBR/NTN) — these are separate identifiers from separate agencies.

## Source

- SECP official website: `https://www.secp.gov.pk`
- SECP eServices portal: `https://eservices.secp.gov.pk` (company search, tracking, complaints)
- Company search: `https://eservices.secp.gov.pk/eServices/NameSearch.jsp`
- See [SECP Company Registry Reference](references/secp-company-registry.md) for company categories, the separate LLP registration regime, and status-value definitions.
