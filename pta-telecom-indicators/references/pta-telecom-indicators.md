# PTA Telecom Indicators Reference

## Major Mobile Operators

Pakistan's cellular market has consisted of four nationwide mobile network operators (MNOs) for most of the last decade:

- **Jazz** — operated by VEON-backed Pakistan Mobile Communications Limited (PMCL); historically the largest operator by subscriber count, formed from the earlier merger of Mobilink and Warid Telecom (that Mobilink-Warid merger completed around 2016, after which the combined entity was rebranded Jazz).
- **Zong** — operated by China Mobile Pakistan (CMPak), a subsidiary of China Mobile.
- **Telenor Pakistan** — operated by Telenor Group (Norway) until its Pakistan business was sold/merged into the PTCL Group (see merger note below).
- **Ufone** — operated by Pakistan Telecommunication Company Limited (PTCL) Group's mobile arm (PTML); PTCL Group is itself majority-owned by Etisalat (UAE).

### Ufone–Telenor Pakistan Merger

PTCL Group (Ufone's parent) and Telenor Group announced a deal for PTCL Group to acquire/merge Telenor's Pakistan operations with Ufone, combining the two into a single operator. This was reported and pursued over several years with regulatory (PTA/competition authority) approvals sought along the way.

**Flag for verification**: the exact completion date of this merger, the final combined entity's branding (whether it continues as "Ufone," becomes a new joint brand, or retains dual branding for a transition period), and the current shareholding structure (e.g., whether Telenor Group retained any residual stake in the merged entity) should all be verified against a current PTA or company press release before being stated as settled fact. Treat any specific "merger completed on [date]" claim from this skill's own memory as needing a live check — this is exactly the kind of recent-corporate-action detail that can be stale. When reporting operator-level figures from a PTA table, check whether that table's period predates or postdates the merger's effective date, since subscriber bases would be reported separately (Ufone and Telenor Pakistan as two operators) before the merger and combined afterward.

Because of this, when asked "how many operators does Pakistan have," the safest answer names the four legacy brands (Jazz, Zong, Telenor Pakistan, Ufone) and explicitly notes that Ufone and Telenor Pakistan have been merging/have merged under PTCL Group, with the current operator count (three vs. four) depending on the merger's status as of the reporting period in question.

## Teledensity/Subscriber Counts vs. Unique Subscribers

- **Subscriber counts** as reported in PTA's Telecom Indicators (e.g., "total cellular subscribers") count **SIM connections**, not people. Pakistan has widespread multi-SIM ownership (a single person commonly holds SIMs from two or more operators, e.g., for better in-network rates, backup connectivity, or separate data/voice lines), so the headline subscriber figure structurally overstates the number of distinct individuals using mobile service.
- **Teledensity** is calculated as (total SIM/mobile connections ÷ population) × 100, expressed as a percentage. Because the numerator counts connections rather than people, Pakistan's teledensity figures can exceed what a naive "percent of people with a phone" interpretation would suggest, and can even nominally exceed 100% in some reporting periods/denominator bases if connections outnumber population.
- **Unique subscriber estimates** (as distinct from raw connections) are a different, harder-to-measure figure requiring identity-based deduplication (e.g., via SIM registration/biometric verification data). Industry bodies (e.g., GSMA) periodically publish unique-mobile-subscriber estimates for Pakistan that are materially lower than PTA's headline SIM/connection counts. When a task needs "how many people in Pakistan have a mobile phone" rather than "how many SIM connections exist," flag that PTA's standard Telecom Indicators table answers the latter, not the former, and a unique-subscriber estimate (if available, often from GSMA or similar) is a different and generally lower number.
- The same distinction applies to broadband: a "broadband subscriber" count in PTA's tables is a connection count (which can include multiple mobile broadband/data SIMs or multiple fixed connections associated with the same household or person), not a unique-user count.

## PTA's Quarterly Telecom Indicators vs. Other PTA Publications

PTA publishes several distinct products; conflating them is a common extraction error:

- **Telecom Indicators** (the core dataset this skill targets): a statistical table/dashboard, updated on a periodic basis (historically monthly and/or quarterly depending on the indicator and period), covering topline sector metrics — total cellular subscribers, broadband subscribers, fixed-line subscribers, teledensity, broadband penetration, and (where reported) 3G/4G subscriber splits and operator-level breakdowns. This is a numbers-first, minimal-narrative product, best suited for point-in-time or trend subscriber/penetration figures.
- **PTA Annual Report**: a fuller yearly document combining narrative (sector overview, regulatory developments, consumer protection activity, policy initiatives) with detailed annexure tables, including operator-level revenue and market-share breakdowns, investment figures, and complaint-handling statistics for the fiscal year. Use this when a task needs sector narrative, regulatory context, or annual financial/revenue detail rather than just a subscriber count.
- **Spectrum auction reports/press releases**: separate one-off publications tied to specific spectrum auction events (e.g., allocation of specific frequency bands to specific operators, auction proceeds, license terms). These are event-driven documents, not part of the recurring Telecom Indicators or Annual Report cadence — use them only when the task specifically concerns spectrum allocation, auction outcomes, or licensing terms, not general subscriber/revenue trends.
- **Other PTA publications**: PTA also periodically issues consumer-facing reports (e.g., quality-of-service survey results), regulatory determinations, and press releases on specific enforcement actions (e.g., SIM blocking drives, biometric re-verification campaigns) — these are supplementary and should not be treated as part of the core Telecom Indicators series.

**Practical rule**: if the question is "how many X subscribers as of [period]" or "what is teledensity/broadband penetration," go to Telecom Indicators. If the question is "how did the sector perform this fiscal year," "what was operator revenue," or "what regulatory actions did PTA take," go to the Annual Report. If the question is about a specific spectrum auction or license award, go to the relevant auction-specific publication.

## Extraction Notes

- Always state the "as of" period for any subscriber/teledensity figure; PTA updates these periodically and a stale figure quoted without a date can materially mislead.
- When citing operator-level figures, check whether the reporting period predates the Ufone–Telenor Pakistan merger's effective date, and label the operator accordingly (reported separately vs. combined).
- Do not present SIM/connection-based subscriber or teledensity figures as equivalent to unique-user counts without flagging the distinction.
- Broadband figures may combine fixed and mobile broadband; check the specific table's scope before combining or comparing across periods where the definition may have shifted.

## Reference

- Pakistan Telecommunication Authority: `https://www.pta.gov.pk`
- Telecom Indicators: `https://www.pta.gov.pk/telecom-indicators` (or the "Indicators"/"Publications" section of the PTA site)
- PTA Annual Reports: `https://www.pta.gov.pk/annual-reports`
- GSMA Mobile Economy / unique-subscriber estimates (for cross-checking connection counts against unique-user estimates): GSMA Intelligence publications
- Verify current operator count/branding (Jazz, Zong, Telenor Pakistan, Ufone, and the status of the Ufone-Telenor merger) against PTA's current licensed-operator list before citing as fact
