# BE&OE Labour Migration Report Reference

## Source and Institutional Context

- **Bureau of Emigration & Overseas Employment (BE&OE)** is an attached department of the **Ministry of Overseas Pakistanis & Human Resource Development (MOPHRD)**.
- BE&OE's core statutory functions: registering intending emigrants, regulating and licensing Overseas Employment Promoters (OEPs, i.e., private recruiting agents), operating **Protectorate of Emigrants (POE)** offices in major cities (historically including Islamabad, Lahore, Karachi, Peshawar, Quetta, and others) where workers are registered before departure, and compiling official statistics on outbound labour deployment.
- BE&OE's official website is `beoe.gov.pk` (verify) — treat any deep-link path (e.g., a specific `/Labour-Migration-Report` slug) as unverified; government site structures change, and the exact URL path should be re-confirmed at retrieval time rather than hard-coded. Search the site's "Statistics" or "Publications"/"Reports" section for the current "Labour Migration Report" or annual "Yearbook" rather than relying on a specific historical URL.
- Sister organization, different mandate: **Overseas Pakistanis Foundation (OPF)** — also under MOPHRD, OPF runs welfare programs for the diaspora (OPF Housing Scheme, OPF schools/colleges, welfare fund payments for death/disability, repatriation assistance for deceased workers' bodies, and complaint-redressal for overseas Pakistanis). OPF does not register or regulate outbound workers and does not publish the Labour Migration Report; do not attribute OPF welfare figures to BE&OE deployment statistics or vice versa.

## Occupation / Skill-Category Taxonomy

BE&OE's registration system has historically classified outbound workers into skill tiers roughly as follows (exact labels can vary slightly by publication year — always defer to the report's own headers):

1. **Unskilled** — general laborers with no defined trade; historically the single largest category by volume of Pakistani labour deployment to the Gulf.
2. **Semi-skilled** — workers with some practical trade exposure but no formal certification (helpers, assistants).
3. **Skilled** — certified or experienced tradespeople: electricians, plumbers, welders, masons, carpenters, drivers, tailors, machine operators, and similar trades. This category is usually further broken out by specific trade in detailed tables.
4. **Highly skilled** — technicians, supervisors, foremen, and workers with specialized technical training beyond a basic trade.
5. **Highly qualified / Professional** — degree-holding professionals: engineers, doctors, nurses, accountants, teachers, IT professionals, managers.

Reports may also separately tabulate a category for **"others"** or workers whose occupation was not classified, and some years include specific high-volume trades (e.g., "driver," "mason," "tailor," "welder") as their own line items within the skilled category rather than only an aggregate.

## Typical Destination-Country Pattern

- Historically, **Gulf Cooperation Council (GCC)** countries have accounted for the large majority of registered Pakistani labour outflow. Approximate historical ordering by volume (verify current-year specifics against the actual table, as rank and share shift with destination-country labor policy):
  1. **Saudi Arabia** — typically the largest single destination by a wide margin over most of BE&OE's reporting history.
  2. **United Arab Emirates** — typically second-largest.
  3. **Oman**
  4. **Qatar**
  5. **Bahrain**
  6. **Kuwait**
- Non-GCC destinations appear in the tables at much smaller volumes: Malaysia, United Kingdom, other European destinations, and select East Asian/other markets. Government-to-government or bilateral labour-agreement placements (e.g., periodic arrangements with countries like South Korea under EPS, or seasonal/bilateral schemes) may appear as smaller distinct line items.
- Deployment volumes are sensitive to destination-country policy shifts — e.g., Saudi Arabia's various labour-market "Saudization"/Nitaqat-style localization drives, and the sharp global deployment contraction during 2020 due to COVID-19 travel restrictions — so year-over-year comparisons should account for such external shocks rather than treating trend lines as smooth.

## Province of Origin

- Provinces/regions tracked: Punjab, Sindh, Khyber Pakhtunkhwa, Balochistan, Gilgit-Baltistan, Azad Jammu & Kashmir, and Islamabad Capital Territory/federal areas.
- Punjab has historically supplied the largest share of registered overseas workers in absolute numbers, followed by Khyber Pakhtunkhwa and Sindh; exact shares vary by year and should be read from the specific report rather than assumed.

## Document Structure Notes

- Reports typically present: (a) a historical cumulative summary table (often from 1971 or the earliest year BE&OE has consistent records), (b) year-specific tables broken down by country, occupation, and province, and (c) sometimes a narrative summary highlighting notable shifts.
- Some editions are branded as a "Yearbook" rather than "Labour Migration Report" — treat these as the same underlying statistical series unless the document explicitly distinguishes them.

## Extraction Notes

- Always extract using the report's own category labels and verify province/country subtotals reconcile with the stated national total.
- Do not conflate "registered" (processed through BE&OE/POE) with "deployed" (actually departed) if the report distinguishes them.
- Cross-reference `pkr-remittances-tracker` only for the financial/remittance-value side of migration, and treat OPF welfare statistics as entirely out of scope for this skill.
- Treat any specific numeric deep-link URL for BE&OE's website as unverified (verify) — confirm the live path before citing it as a source link.
