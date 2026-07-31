# Pakistan Anti-Money Laundering Enforcement Reference

## Source

- Anti-Money Laundering Act, 2010 (as amended) — Pakistan Code / National Assembly legislative archive: `https://www.na.gov.pk` (verify current consolidated text with all amendments, including post-2018/2020/2021 amendments made in response to FATF Action Plan requirements)
- Financial Monitoring Unit (Pakistan's Financial Intelligence Unit): `https://www.fmu.gov.pk`
- FATF public statements and Mutual Evaluation/Follow-up Reports on Pakistan: `https://www.fatf-gafi.org` (search "Pakistan" — verify specific report dates and findings before citing granular detail)
- Federal Investigation Agency (FIA) — financial crimes wing: `https://www.fia.gov.pk`
- National Accountability Bureau: `https://www.nab.gov.pk` (for the corruption-predicate-offence overlap only; see `nab-accountability-data` for NAB's own pipeline)

## AMLA Structure

- The Anti-Money Laundering Act, 2010 criminalizes money laundering as a standalone offence: converting, transferring, concealing, or acquiring property known (or believed) to be proceeds of a "predicate offence" — a crime listed in the Act's Schedule that generates the illicit proceeds being laundered.
- The **predicate offence Schedule** has been expanded through subsequent amendments (notably amendments made around 2020-2021 in response to FATF Action Plan deficiencies) to bring Pakistan's predicate-offence coverage closer to the FATF standard list (which spans categories such as corruption/bribery, narcotics trafficking, terrorism financing, fraud, tax crimes, smuggling, and other serious offences). Treat the exact current Schedule contents as needing verification against the current consolidated Act rather than assuming a fixed historical list.
- AMLA created dedicated **AML courts** (or designated existing courts) for trial of money-laundering offences, alongside provisions for provisional attachment, freezing, seizure, and confiscation of property connected to a laundering offence.

## Financial Monitoring Unit (FMU)

- FMU is Pakistan's Financial Intelligence Unit (FIU), established under AMLA, functioning as the central node receiving:
  - **Suspicious Transaction Reports (STRs)** — filed by banks, non-bank financial institutions, and Designated Non-Financial Businesses and Professions (DNFBPs, e.g., real estate agents, jewelers, lawyers/accountants in specified circumstances) when a transaction is suspected to involve laundering or terrorism financing.
  - **Currency Transaction Reports (CTRs)** — filed for cash transactions above a prescribed threshold.
- FMU analyzes these reports and, where warranted, disseminates financial intelligence to relevant law-enforcement/investigation agencies (FIA, NAB, ANF, police, or others depending on the suspected predicate offence) for further investigation. FMU itself does not investigate crimes or prosecute cases — its statutory role is intelligence intake, analysis, and dissemination, plus a supervisory/coordination role with reporting-entity regulators.
- FMU sits administratively linked to the State Bank of Pakistan for housekeeping purposes in some periods of its institutional history, but functions as an independent financial intelligence unit per FATF Recommendation 29 standards (verify current administrative housing arrangement).

## Investigation and Prosecution Pathway

- Because money laundering is predicate-offence-dependent, the investigating agency varies:
  - **Federal Investigation Agency (FIA)** — commonly investigates money laundering linked to financial fraud, banking crimes, human trafficking/smuggling, and other FIA-mandated predicate offences.
  - **National Accountability Bureau (NAB)** — investigates money laundering where the predicate offence is corruption/corrupt practices under NAB's own ordinance; see `nab-accountability-data` for NAB's inquiry-investigation-reference-plea-bargain pipeline, which can run in parallel with or feed into an AMLA laundering charge.
  - **Anti-Narcotics Force (ANF)** and provincial police may investigate laundering tied to narcotics or other offences within their respective mandates.
- Prosecution of the AMLA money-laundering charge itself proceeds before AML-designated courts, distinct from (though potentially parallel to) any accountability court proceeding on the underlying predicate offence.

## National AML/CFT Coordination Committee

- A high-level inter-agency body coordinating Pakistan's national AML/CFT strategy and FATF Action Plan implementation across FMU, SBP, SECP, FIA, NAB, and other stakeholder agencies/ministries. Exact current composition, chairing authority, and meeting cadence should be verified against the latest government notification rather than assumed static, since coordination-committee structures are periodically reconstituted.

## FATF Grey List Timeline

- Pakistan was placed on the FATF grey list (formally, the list of "Jurisdictions under Increased Monitoring") in **June 2018**, triggering a multi-point Action Plan addressing AML/CFT technical-compliance and effectiveness deficiencies.
- Pakistan was removed from the FATF grey list in **October 2022**, after FATF's on-site visit and assessment concluded the Action Plan items had been substantially addressed.
- This 2018-2022 timeline reflects well-documented public record and can be stated with confidence. Granular detail — the exact number of Action Plan action items, specific technical-compliance/effectiveness ratings by FATF Recommendation, or specific legislative amendment dates tied to individual action items — should be verified against the specific FATF Mutual Evaluation Report or Follow-up Report rather than asserted from memory.

## Extraction Notes

- Keep FMU's financial-intelligence function separate from the investigating agency's law-enforcement function and the court's prosecutorial/adjudicative function — these are three distinct stages.
- Match the predicate offence to the plausible investigating agency rather than defaulting to one agency for all cases.
- Cite the FATF 2018 grey-listing / 2022 exit timeline with confidence; hedge anything more granular.
- Cross-reference `nab-accountability-data` explicitly when a case involves corruption as the predicate offence, since NAB's pipeline and the AMLA laundering charge can run in parallel on the same underlying facts.
