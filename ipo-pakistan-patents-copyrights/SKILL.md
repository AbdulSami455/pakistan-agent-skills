---
name: ipo-pakistan-patents-copyrights
description: IPO Pakistan patents and copyright skill. Use when explaining patent registration, examination, and enforcement under the Patents Ordinance 2000, or copyright registration and enforcement under the Copyright Ordinance 1962 (as amended), through the Intellectual Property Organization of Pakistan — for inventors, publishers, software developers, or legal teams handling invention protection or authorship rights, as distinct from trademark/brand-name workflow.
---

# IPO Pakistan Patents and Copyrights

## Overview

Use this skill for patent and copyright workflow in Pakistan administered through the Intellectual Property Organization of Pakistan (IPO Pakistan): what qualifies as a patentable invention or a copyrightable work, how each right is registered/granted, examination and opposition mechanics, term of protection, and infringement remedies. This is the right skill for invention protection and authorship-rights questions; it does not cover trademarks or brand-name clearance, which is a separate registry and process.

## Coverage

- **Patents — Patents Ordinance, 2000**: governs patent filing, examination, and grant in Pakistan, administered by the Patent Office (a wing of IPO Pakistan) in Karachi. A patentable invention must be new, involve an inventive step, and be capable of industrial application; the Ordinance also lists non-patentable subject matter (e.g., discoveries, scientific theories, mathematical methods, and certain categories such as methods of medical treatment). Filing can be a complete or provisional specification; examination is on request (not automatic on filing) and includes a search and substantive examination before acceptance; accepted applications are published/open to opposition before grant.
- **Patent term and post-grant obligations**: standard patent term under the Ordinance is 20 years from the filing date, subject to payment of periodic renewal/maintenance fees (verify current fee schedule) — failure to pay renewal fees can result in lapse. Pakistan is a member of the Paris Convention, allowing convention-priority filings from an earlier foreign application within the priority window (typically 12 months for patents).
- **Copyright — Copyright Ordinance, 1962 (as amended)**: governs copyright in literary, dramatic, musical, and artistic works, along with cinematograph films and sound recordings; administered by the Copyright Office, also under IPO Pakistan. Unlike patents and trademarks, copyright protection arises automatically upon creation/fixation of an original work and does not require registration to exist — registration with the Copyright Office is optional but creates a public record and evidentiary presumption useful in infringement litigation. Software/computer programs are protected as literary works under Pakistani copyright law.
- **Copyright term**: for most literary, dramatic, musical, and artistic works, the general rule is life of the author plus a fixed number of years post-mortem (commonly referenced as 50 years, consistent with the Berne Convention minimum — verify the exact figure in the current consolidated Ordinance text for the specific work category, since terms differ for photographs, government works, and cinematograph films/sound recordings, which are typically calculated from publication rather than the author's life).
- **International framework**: Pakistan is a member of the World Intellectual Property Organization (WIPO), a party to the Paris Convention for the Protection of Industrial Property (patents, industrial designs) and the Berne Convention for the Protection of Literary and Artistic Works (copyright), and a WTO member subject to the TRIPS Agreement's minimum IP-protection standards.
- **Infringement and enforcement**: both statutes provide civil remedies (injunction, damages/accounts of profits, delivery-up) and criminal penalties for infringement, with IP-specific tribunals in some provinces; enforcement in practice also intersects with customs border-measures for counterfeit/pirated goods and with the Intellectual Property Organization of Pakistan Act 2012, which created IPO Pakistan as the umbrella federal body overseeing the Patent Office, Trademarks Registry, and Copyright Office.

## Use This Skill For

- explaining what qualifies as a patentable invention versus excluded subject matter under the Patents Ordinance 2000
- walking through the patent filing-to-grant pipeline: specification filing, examination request, search/substantive examination, publication, opposition, grant
- explaining that copyright protection is automatic upon creation and that Copyright Office registration is optional evidentiary support, not a precondition of the right
- distinguishing patent term (20 years from filing) from copyright term (life-plus-years, varying by work category)
- explaining civil and criminal infringement remedies available under either statute
- clarifying the institutional relationship between IPO Pakistan (the umbrella body under the IPO Pakistan Act 2012) and its constituent Patent Office / Copyright Office / Trademarks Registry

## When Not to Use This Skill

- For trademark search, filing, opposition, or renewal workflow, use `ipo-pakistan-trademarks` instead — trademarks are a separate registry and process under IPO Pakistan, governed by different substantive law (the Trade Marks Ordinance regime, not the Patents Ordinance or Copyright Ordinance).
- For SECP company incorporation or company-name registry checks, use `secp-company-registry`.
- For competition-law issues around IP misuse (e.g., abuse of a dominant patent position), `ccp-competition-enforcement` may be relevant for the competition-law side, not this skill.
- For definitive legal advice on drafting a patent specification, filing a copyright infringement suit, or an active enforcement proceeding, recommend a qualified IP lawyer/patent agent; this skill provides structural orientation only.

## Routing Rules

- If the question is about a brand name, logo, or mark, route to `ipo-pakistan-trademarks` — do not apply patent/copyright mechanics to a trademark question.
- If the question is about an invention, process, or technical innovation, apply the Patents Ordinance 2000 framework.
- If the question is about a literary, artistic, musical, dramatic work, software, film, or sound recording, apply the Copyright Ordinance 1962 (as amended) framework, and clarify that the right exists on creation regardless of registration.
- If the question conflates "IPO Pakistan" generally with only trademarks, clarify that IPO Pakistan (under the IPO Pakistan Act 2012) is the umbrella body covering patents, copyright, trademarks, and industrial designs as distinct sub-registries.
- If the question involves a specific current fee, exact renewal deadline, or a pending legislative amendment, flag it for verification rather than asserting a precise figure from memory.

## Extraction Workflow

1. Identify whether the right at issue is a patent (invention) or a copyright (creative/literary/software work) — this determines which Ordinance and which IPO Pakistan sub-office applies.
2. For patents, identify the stage: pre-filing novelty search, provisional vs. complete specification filing, examination request, opposition, or post-grant renewal.
3. For copyright, confirm whether the question is about the existence of the right (automatic, no registration needed) or about registration as an evidentiary/administrative step.
4. Note the work category for copyright term purposes (literary/artistic/musical/dramatic vs. cinematograph film/sound recording/photograph/government work), since term calculation differs.
5. If infringement is at issue, separate civil remedies (injunction, damages, accounts of profits) from criminal penalties, and note whether customs border-measures are relevant (counterfeit/pirated goods).
6. Flag any specific fee, deadline, or amendment status as needing verification against the current IPO Pakistan schedule or Gazette notification.

## Technical Rules

- Patent protection requires registration/grant; copyright protection does not — do not describe copyright as requiring registration to exist under Pakistani law.
- Patent term runs 20 years from the filing date (subject to renewal fee payment); copyright term is life-of-author-plus-years for most categories, with different rules for films, sound recordings, photographs, and government works — do not apply a single term rule across both regimes or across all copyright work categories.
- IPO Pakistan trademarks are governed by separate substantive law from patents/copyright; do not treat a trademark registration certificate as evidence of patent or copyright protection, or vice versa.
- Patent examination in Pakistan is request-based, not automatic upon filing — an application can sit unexamined until examination is formally requested within the prescribed period.
- Software is protected in Pakistan as a literary work under copyright, not as a patentable invention by default; software-related patent claims face the same novelty/inventive-step/industrial-application test and common exclusions applied cautiously to computer-implemented inventions.

## Validation Checklist

- Confirm whether the question concerns a patent (invention) or copyright (creative/literary/software work) before applying statute-specific mechanics.
- Confirm copyright's automatic-protection-on-creation principle is not misstated as requiring registration.
- Confirm the correct term rule is applied for the specific copyright work category, not a single blanket figure.
- Flag any specific fee, precise renewal deadline, or amendment/bill status as needing current verification.
- Distinguish this skill's scope from `ipo-pakistan-trademarks` when a query mixes multiple IP right types.

## Common Pitfalls

- Treating copyright as requiring formal registration to exist, when protection in Pakistan (as in most Berne Convention jurisdictions) arises automatically on creation/fixation.
- Assuming a single 20-year term applies to copyright the way it does to patents.
- Conflating the Trademarks Registry process with the Patent Office or Copyright Office process, since all three sit under the same umbrella body (IPO Pakistan) but operate under different statutes.
- Citing a precise current fee or renewal deadline from memory without flagging it as needing verification against the current schedule.
- Ignoring that patent examination must be actively requested and is not automatic upon filing.

## Reference

- See [IPO Pakistan Patents and Copyrights Reference](references/ipo-pakistan-patents-copyrights.md) for statute detail, term rules, and extraction notes.
