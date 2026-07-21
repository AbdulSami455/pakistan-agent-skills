# Pakistan GDP Reconciliation Methodology Reference

## Source

- PBS National Accounts backward-revised series (2015-16 base): `https://www.pbs.gov.pk/wp-content/uploads/2020/07/National-Accounts-of-Pakistan-Backward-Revisions-for-the-Years-1999-2000-to-2014-15-on-the-base-year-2015-16-2.pdf`
- PBS National Accounts hub: `https://www.pbs.gov.pk/national-accounts-2/`
- National Accounts Committee press release example (99th meeting): `https://www.pbs.gov.pk/sites/default/files/2022-04/Press%20Brief%2099th%20Meeting.pdf`
- SBP Annual Report FY23, Chapter 7 ("Pakistan's National Statistical System: A Primer" — covers PBS/SBP/NAC institutional roles): `https://www.sbp.org.pk/reports/annual/aarFY23/Chapter-07.pdf`
- SBP Research Bulletin: "Quarterisation of National Income Accounts of Pakistan" (Hanif, Iqbal, Malik; SBP Working Paper 54 / Research Bulletin Vol. 9, No. 1): `https://www.sbp.org.pk/research/bulletin/2013/Vol-9-1/Quarterisation%20of%20National%20Income%20Accounts%20of%20Pakistan.pdf`
- Mirror copy (MPRA): `https://mpra.ub.uni-muenchen.de/45334/1/MPRA_paper_45334.pdf`
- PIDE commentary on rebasing and measurement issues (PIDE domain returns HTTP 403 to automated fetches in some environments but is a well-known, legitimate Pakistani public-policy think tank — verify manually if fetching): `https://pide.org.pk/research/pending-pakistans-revised-base-estimates-of-gdp-and-measurement-issues-in-lsm/`

## Institutional Process

1. **PBS compilation**: PBS's National Accounts wing compiles GDP by production (sectoral value-added: agriculture, industry, services) and expenditure approach, drawing on LSM (Large-Scale Manufacturing) indices, agriculture crop/livestock estimates, and administrative/tax data.
2. **Provisional estimate**: PBS issues a provisional growth estimate for the outgoing fiscal year, typically presented as a working paper ahead of formal approval.
3. **National Accounts Committee (NAC)**: A committee including Planning Commission, Ministry of Finance, SBP, and provincial representatives reviews and formally approves ("finalizes") the GDP growth figure — this NAC-approved figure is what becomes the official cited number (e.g., in the Pakistan Economic Survey and the federal budget documents).
4. **Revision cycle**: Subsequent NAC meetings revise prior years' estimates as more complete source data becomes available (e.g., final LSM data, completed agriculture census-linked benchmarks).

## Documented SBP-PBS Discrepancy Pattern

- FY21 example: SBP's own growth assessment stood near 3%, while PBS's provisional working paper put growth at 3.94%; the NAC ultimately adopted the PBS-anchored 3.94% figure as Pakistan's official FY21 growth rate after committee reconciliation. This illustrates that SBP's independently modeled growth number is a policy input for monetary decisions, not a rival official statistic — the single official GDP series is the NAC-approved PBS series.

## Rebasing History

- Base year changed from 1999-2000 to 2005-06 in an earlier rebasing round.
- Base year changed from 2005-06 to 2015-16, announced/implemented around January 2022, aligned to the 2008 System of National Accounts (SNA) framework. PBS conducted approximately 42 sector-specific benchmark studies to derive new weights from FY2015-16 data.
- Effect: nominal GDP level was revised upward by roughly 11% relative to the old 2005-06-base series, reflecting both new weights and expanded coverage (not a pure re-indexing).
- PBS has stated an intent to rebase national accounts (and separately, price statistics) on a roughly five-year cycle going forward, in line with international statistical practice — treat any specific future base year as needing confirmation against the current PBS release.
- Because rebasing changes sectoral weights and sometimes definitional coverage, backward-revised series (PBS publishes these for the years bridging old and new base) should be used for any multi-year comparison spanning a rebasing event, rather than naively linking growth rates computed on different bases.

## Quarterly Estimation ("Quarterisation") Methodology

- Pakistan's core national accounts compilation is annual; quarterly GDP estimates are derived through indicator-based interpolation/quarterisation techniques (e.g., Chow-Lin type or similar benchmarking methods use monthly/quarterly indicator series — LSM index, import data, etc. — to distribute the annual total across quarters).
- SBP's research department has published methodology on this (see Quarterisation working paper above); PBS's own Quarterly National Accounts (QNA) release uses its own production-and-expenditure-side quarterly compilation approach. Third-party or academic quarterisation exercises may use different indicator sets and are not automatically consistent with PBS's official QNA figures — treat PBS's QNA release as authoritative for official quarterly figures.

## Extraction Notes

- Always tag a GDP growth or level figure with: (a) source (PBS/NAC vs. SBP assessment vs. IMF/WB), (b) vintage (provisional/NAC-approved/revised), (c) base year, and (d) fiscal year.
- When a ratio (debt/GDP, tax/GDP) shifts sharply across a rebasing year, decompose how much of the shift is denominator-driven (GDP level revision) vs. numerator-driven (actual debt or revenue change) before attributing the shift to policy performance.
