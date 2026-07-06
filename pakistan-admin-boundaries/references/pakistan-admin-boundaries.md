# Pakistan Admin Boundaries Reference

## The Top-Level Units (Admin1)

Pakistan's Admin1 layer is not a uniform set of "four provinces" — it mixes provinces with two territories of distinct constitutional status:

- **Punjab** — province; capital Lahore.
- **Sindh** — province; capital Karachi.
- **Khyber Pakhtunkhwa (KP)** — province; capital Peshawar. Absorbed the former Federally Administered Tribal Areas (FATA) as part of the 25th Constitutional Amendment (2018), merging FATA's agencies into KP as regular districts (see below).
- **Balochistan** — province; capital Quetta.
- **Islamabad Capital Territory (ICT)** — the federal capital territory, not a province; administered directly by the federal government, not by a provincial assembly/chief minister.
- **Azad Jammu & Kashmir (AJK)** — self-governing territory with its own President, Prime Minister, Legislative Assembly, and constitution (the Azad Jammu and Kashmir Interim Constitution Act, 1974). It is **not one of Pakistan's four provinces** and is not represented in the National Assembly or Senate on the same basis as a province. Its constitutional status is tied to the unresolved Kashmir dispute.
- **Gilgit-Baltistan (GB)** — self-governing territory with its own Assembly and Chief Minister since the Gilgit-Baltistan (Empowerment and Self-Governance) Order, 2009, later amended. Like AJK, GB is **not a province** and its final constitutional status also remains linked to the Kashmir dispute; it is administered under a distinct governance order rather than the 1973 Constitution's normal provincial framework.

When a task requires "all provinces," AJK and GB should generally be flagged as territories rather than silently folded into a province count of six. Many national statistical products (e.g., PBS series, PES chapters) report AJK and GB separately, or omit them entirely — always check whether a given dataset's "national total" actually includes them (see `ajk-development-statistics` and `gb-development-statistics` for territory-specific series).

## Admin2/Admin3/Admin4: Divisions, Districts, Tehsils

- **Division (Admin2)**: an intermediate grouping of districts, reintroduced/retained in most provinces primarily for administrative-field purposes (Commissioner's office). Not every statistical source reports at division level, and not every province uses divisions identically.
- **District (Admin3)**: the most commonly used sub-national reporting unit across census, PSLM, agriculture census, and most government statistics. Headed administratively by a Deputy Commissioner.
- **Tehsil (Admin4)**: sub-district unit, headed by an Assistant Commissioner. Called **Taluka** in Sindh in common usage, and the term **Sub-Division** is also used in some contexts (particularly in parts of KP and Balochistan) roughly at this level, though the mapping to "tehsil" is not always exact — confirm the specific province's terminology before assuming equivalence.

Boundaries at all three sub-national levels are periodically redrawn: districts are split into new districts, tehsils are created within a district, and occasionally a division is reorganized. This means a name-only join between two datasets from different years can silently misattribute figures if a split occurred in between.

## Known District Splits and Creations (Representative, Not Exhaustive)

District-level change is ongoing in Pakistan; the list below is illustrative of the kind of change to expect, not a complete inventory. Always confirm current district counts against the latest PBS/COD-AB release rather than treating this list as final.

- **FATA merger into KP (2018)**: The 25th Amendment merged the seven tribal "Agencies" and six Frontier Regions of the former FATA into KP. The tribal agencies became new KP districts, generally following these lines (spelling varies by source):
  - Khyber
  - Kurram
  - Orakzai
  - Bajaur
  - Mohmand
  - North Waziristan
  - South Waziristan
  - The former Frontier Regions were largely merged into adjoining settled districts (e.g., FR Peshawar into Peshawar, FR Kohat into Kohat, FR Bannu into Bannu, FR Lakki into Lakki Marwat, FR Tank into Tank, FR Dera Ismail Khan into D.I. Khan), rather than becoming standalone districts, though the exact administrative treatment has been adjusted more than once since 2018 — verify current status before citing a specific FR's district assignment.
  - South Waziristan itself was later further split into **South Waziristan Upper** and **South Waziristan Lower** — treat this specific bifurcation as reported by multiple sources, but confirm the exact effective date against a current official/PBS list before quoting it, since it is a comparatively recent and less universally reflected change.
- **Punjab**: Punjab has created new districts by splitting existing ones on more than one occasion in recent years (for example, splits carving new districts out of larger existing ones such as Sahiwal, Vehari, or Multan-area districts have been reported/proposed at various points). Punjab's district count has not been static; do not assume a district list from even a few years ago is current — confirm against the latest official notification.
- **Balochistan and Sindh** have also seen occasional district creations (e.g., new districts split from larger existing ones). As with Punjab, treat any specific historical count as time-bound rather than assuming it still holds.

**Guidance**: Because district creation is an ongoing process and this agent's training data has a cutoff, never assert a total district count (e.g., "Pakistan has X districts") as a fixed, current fact without flagging that it should be checked against the latest PBS or COD-AB release. The safe framing is: name the specific district(s) relevant to the task, and note that province-wide totals shift over time.

## P-Codes (Pcodes)

A **P-code** (place code, sometimes written "pcode") is a unique alphanumeric identifier assigned to an administrative unit, used to unambiguously reference that unit across datasets, GIS layers, and humanitarian/development data systems — independent of how the unit's name is spelled, translated, or abbreviated.

- P-codes follow a hierarchical structure: a country code prefix (e.g., `PK` for Pakistan), followed by level-specific segments that nest a district's code inside its parent province's code, and a tehsil's code inside its parent district's code.
- In the HDX COD-AB Pakistan dataset, each administrative level (Admin1 province/territory, Admin2 division, Admin3 district, Admin4 tehsil) carries its own P-code field (commonly named something like `ADM1_PCODE`, `ADM2_PCODE`, `ADM3_PCODE`, `ADM4_PCODE` in the shapefile/GeoJSON attribute tables, though exact field names can vary slightly by release version).
- P-codes are the standard used by UN OCHA and the wider humanitarian community (e.g., in the Humanitarian Data Exchange, in cluster/sector response plans, and in disaster response mapping) specifically because place names in Pakistan can have multiple spellings (transliteration variants), can be duplicated across provinces (rare) or across districts (tehsil-name collisions are common), and can change when a district is renamed or split.
- **Practical rule**: when joining or merging any two datasets that both carry P-codes, join on the P-code rather than the name string. When only one dataset has P-codes, use the P-code dataset's hierarchy to disambiguate the other dataset's name-based entries before merging.
- P-codes are versioned along with the COD-AB dataset itself — when a district is split, the new districts typically receive new P-codes, and the parent district's P-code may be retired or reassigned to a residual unit. Always check the P-code set's vintage/version against the time period of the data being joined.

## Extraction Notes

- Treat "province" and "territory" as distinct labels; do not describe AJK or GB as one of Pakistan's provinces even when loosely referred to as such in casual usage.
- When a task references a district that no longer exists in its old form (because it has since been split), name both the historical district and its current successor district(s) if known, and flag the change explicitly.
- Division-level reporting is not universal — a "division" figure requested for a province that does not report at that level should be flagged as unavailable at that granularity, not approximated from district figures without saying so.

## Reference

- HDX (Humanitarian Data Exchange) COD-AB Pakistan dataset: `https://data.humdata.org/dataset/cod-ab-pak`
- UN OCHA Pakistan: `https://www.unocha.org/pakistan`
- Pakistan Bureau of Statistics administrative unit lists (for cross-checking current district counts): `https://www.pbs.gov.pk`
- Constitution of Pakistan, 1973, and the 18th and 25th Constitutional Amendments (for AJK/GB/FATA-KP status changes)
