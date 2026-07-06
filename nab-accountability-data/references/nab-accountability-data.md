# NAB Accountability Data Reference

## Source

- National Accountability Bureau (NAB) official website: `https://www.nab.gov.pk` (verify current domain before citing as a live link).
- Governing law: National Accountability Ordinance, 1999 (NAO 1999), as amended. Key amendment episodes (e.g., changes around 2022 that narrowed NAB's scope, adjusted the monetary threshold for cognizable cases, and altered plea-bargain/voluntary-return procedure) are publicly documented but their exact provisions, years, and current legal status (some amendments have themselves been challenged/reviewed by superior courts) should be **verified against the current consolidated text of the NAO 1999 and recent superior-court rulings** rather than cited from memory, since this is an area with a genuinely contested and shifting legal history.
- NAB periodically issues press releases and an annual-style disclosure of case statistics and recovery figures; treat NAB's own announcements as a primary but self-reported source, and note that independent verification (e.g., court records, media investigation) may present a different picture, particularly on recovery composition.

## Case Pipeline

| Stage | Description |
|---|---|
| **Complaint / Complaint Verification** | A complaint is received and given a preliminary look to decide if it warrants an inquiry. |
| **Inquiry** | Fact-finding stage; NAB can call for records/documents and call individuals for questioning. No formal charge yet. Many complaints are closed at this stage without proceeding further. |
| **Investigation** | A more formal stage after an inquiry finds sufficient grounds; can include arrest of the accused, subject to relevant legal safeguards and, under various amendments, differing arrest-authorization requirements. |
| **Reference** | The formal charge document filed by NAB in an Accountability Court, setting out the specific allegations and evidence. |
| **Accountability Court Trial** | A special court established under the NAO 1999 (distinct from ordinary Sessions/Magistrate courts) tries the reference; can result in acquittal or conviction. |
| **Appeal** | A convicted (or aggrieved) party can appeal to the relevant High Court, and potentially the Supreme Court thereafter. |

An "under NAB inquiry" status is the most preliminary possible stage — it is not equivalent to being charged, and a large proportion of inquiries historically do not progress to a reference.

## Plea Bargain and Voluntary Return

- **Voluntary Return (VR)**: an accused person, before or during the inquiry/investigation stage (and in some formulations before a reference is filed), can return the allegedly ill-gotten assets/gains to NAB, resulting in the matter being closed without proceeding to a reference or trial.
- **Plea Bargain (PB)**: typically occurs after a reference has been filed / during trial — the accused admits to holding ill-gotten assets and agrees to return them (in part or full, sometimes with an additional penalty/surcharge), subject to court approval, in exchange for the reference being disposed of without a full trial verdict on guilt.
- Both mechanisms are **not equivalent to a criminal conviction** — there is no trial finding of guilt in the same sense as a contested trial verdict. This is a frequent point of public confusion when media reports describe someone as having "returned looted money" as though that were the same as being "convicted of corruption."
- These mechanisms have been the subject of sustained public and legal debate in Pakistan, including criticism that they allow high-profile accused persons to avoid a full trial and criminal conviction by returning only a portion of alleged assets. (Verify current statutory conditions/limits on plea bargain and voluntary return against the current NAO 1999 text, as amendments have altered these provisions.)

## Recovery Figures — Cash vs. Non-Cash

- NAB periodically announces cumulative recovery figures (amounts recovered since NAB's inception or over a stated period) via convictions, plea bargains, and voluntary returns.
- A recurring and important caveat, documented in NAB's own historical disclosures and independent analysis: a substantial share of these headline recovery figures has consisted of **non-cash assets** — land, property, shares, vehicles, and other assets — valued at an **assessed figure** at the time of recovery, rather than cash actually deposited into the national treasury.
- This distinction matters because:
  - An assessed asset value may not reflect what the asset would actually realize if sold (liquidation value can differ materially from assessed value).
  - "Recovered" does not always mean the asset has been transferred to, and is generating value for, the government treasury at the time of the announcement — the disposal/transfer process for non-cash assets can itself take significant additional time.
  - Reporting a NAB recovery figure as "Rs. X cash recovered" when the underlying figure is predominantly non-cash asset value is a common and materially misleading simplification.
- When citing a NAB recovery figure, always note the source period, and flag explicitly if the cash/non-cash breakdown is not stated in the source — do not assume a headline total is cash unless the source explicitly says so.

## Disambiguation: NAB vs. AGP Audit vs. FIA vs. Police

| | NAB | Auditor-General of Pakistan (AGP) | FIA | Ordinary Police |
|---|---|---|---|---|
| Type of body | Investigative + prosecutorial (corruption-specific) | Constitutional audit body (financial/compliance audit) | Federal investigative agency (broad federal-crime mandate) | Provincial law-enforcement (general criminal law) |
| Governing law | National Accountability Ordinance, 1999 | Constitution of Pakistan (Article 168-171) + Auditor-General's (Functions, Powers and Terms and Conditions of Service) Ordinance, 2001 (verify) | Federal Investigation Agency Act, 1974 | Provincial Police Acts / Police Order |
| Typical output | Inquiry/investigation/reference; Accountability Court trial; conviction, acquittal, plea bargain, or voluntary return | Audit report with "paras"/objections on irregularities, overpayments, non-compliance in government accounts | FIR, investigation, and prosecution for cybercrime, human trafficking/smuggling, passport/immigration fraud, and other scheduled federal offenses | FIR, investigation, and prosecution under the Pakistan Penal Code and other general criminal law |
| Who reviews findings | Accountability Court (trial), then High Court/Supreme Court on appeal | Public Accounts Committee (PAC) of the National Assembly reviews audit paras; PAC can recommend further action but does not itself convict anyone | Ordinary criminal courts (or special courts for specific offense categories) | Ordinary criminal courts (Magistrate/Sessions) |
| Key distinction to preserve | A NAB reference is a formal criminal allegation of corruption, tested at trial | An AGP audit "objection"/"irregularity" is a compliance finding, **not** a judicial or criminal determination — it is not proof of corruption until/unless separately investigated and prosecuted by a competent authority (which may or may not be NAB) | FIA's mandate is broader federal crime, not corruption-by-public-office-holder specifically (though some overlap can exist in specific scheduled offenses) | General jurisdiction; corruption by public office-holders as defined under NAO 1999 is generally NAB's specific domain, not ordinary police's |

**The single most important disambiguation for this skill**: media and secondary sources very frequently report "AGP found irregularities of Rs. X" as if it were equivalent to "Rs. X was stolen/embezzled" or "NAB is investigating Rs. X in corruption." These are not the same claim. An AGP audit para reflects a compliance/documentation/procedural finding reviewed by the PAC, which can (but frequently does not) lead to a separate referral for criminal investigation by NAB, FIA, or another agency. Absent an actual NAB reference or FIR, an AGP finding should be reported as an audit irregularity, not as established corruption. A dedicated AGP-audit-focused skill (not part of this repo as of this writing) would be the appropriate place for audit-specific figures and PAC-review workflow — this skill's scope stops at flagging the distinction, not providing AGP audit data itself.

## Extraction Notes

- Always state the pipeline stage (inquiry/investigation/reference/trial/conviction/appeal) explicitly when describing a NAB case.
- Always state whether a cited recovery figure is cash, non-cash asset value, or unspecified/mixed.
- Never restate an AGP audit finding as a NAB corruption finding without an explicit, sourced NAB reference or FIR connecting the two.
- Never restate a plea bargain or voluntary return as a "conviction."
- Flag specific NAB amendment years, monetary thresholds, or procedural details you are not fully confident of as "(verify)" rather than asserting them as settled, given the genuinely contested and multiply-amended history of the NAO 1999.
