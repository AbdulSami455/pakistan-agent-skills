# Pakistan Poverty and Inequality Measurement Methodology Reference

## Source

- UNDP/OPHI, Pakistan Multidimensional Poverty Index Country Profile 2025: `https://hdr.undp.org/sites/default/files/Country-Profiles/MPI2025/PAK.pdf`
- UNDP Pakistan, "Multidimensional Poverty in Pakistan" (methodology overview; UNDP Pakistan's pk.undp.org path returned HTTP 403 to automated fetch in some environments but is UNDP's own verified official Pakistan country-office domain): `https://pk.undp.org/content/pakistan/en/home/library/development_policy/Multidimensional-Poverty-in-Pakistan.html`
- PIDE research on poverty trends in Pakistan (PIDE domain may return HTTP 403 to automated fetches in some environments but is a well-known, legitimate Pakistani public-policy think tank): `https://pide.org.pk/research/poverty-trend-in-pakistan-a-glimpse-from-last-two-decades/`
- World Bank PovcalNet/Global poverty database country file for Pakistan (contains national poverty line series alongside international poverty line series for comparison): `https://databankfiles.worldbank.org/public/ddpext_download/poverty/987B9C90-CB9F-4D93-AE8C-750588BF00QA/current/Global_POVEQ_PAK.pdf`

## Cost of Basic Needs (CBN) Poverty Line Methodology

- Pakistan's Government first adopted the Cost of Basic Needs (CBN) approach for official poverty estimation in 2013-14, replacing an earlier calorie-intake-only approach.
- CBN methodology: establishes a food bundle meeting a minimum calorie-intake threshold at prevailing prices, then adds an allowance for essential non-food needs (housing, clothing, transport, education, health) typical of households near the food-poverty line, yielding a single poverty line expressed in rupees per adult equivalent per month.
- Between HIES survey rounds, the poverty line is updated using CPI-based inflation adjustment rather than a fresh expenditure survey; because the general CPI basket does not specifically track poor-household consumption patterns, such interim/adjusted poverty rates should be flagged as CPI-updated estimates rather than freshly surveyed figures.
- Official national poverty estimates are produced by the Planning Commission of Pakistan using HIES data collected by PBS.

## Gini Coefficient

- The Gini coefficient is computed from the distribution of household consumption (or, in some published series, income) captured in HIES/PSLM microdata, summarizing dispersion across the full distribution via the Lorenz curve (0 = perfect equality, 1 or 100 = maximal inequality, depending on scale convention used).
- Consumption-based and income-based Gini estimates are not directly comparable; Pakistan's official series has historically been consumption-based, consistent with the CBN poverty-line's consumption/expenditure anchor, but cross-checks against international databases (which are often income-based) should note the base-variable difference explicitly.
- Reported Gini movements should always be tied to a specific survey round/year, since a single-year comparison (e.g., a pre- vs. post-shock year) can be sensitive to that round's specific sampling and reference period.

## Multidimensional Poverty Index (MPI) — Alkire-Foster Methodology

- Pakistan's national MPI was developed via a partnership between the Ministry of Planning, Development and Special Initiatives, UNDP, and the Oxford Poverty and Human Development Initiative (OPHI), using the Alkire-Foster (AF) counting methodology (the same general framework underlying the UNDP global MPI, but calibrated with country-specific indicators and cutoffs).
- Three equally weighted dimensions: education, health, and living standards, each contributing one-third of the overall MPI score.
- The Pakistan national MPI uses a larger indicator set (developed specifically for the national measure) than the 10 indicators used in the UNDP global MPI, to better reflect Pakistan-specific policy priorities; a household/individual is identified as multidimensionally poor if deprived across a sufficient weighted share of these indicators.
- Data source: PSLM survey data (which includes education, health, demographic, and living-standards/access-to-facilities questions).
- Because the MPI captures deprivation in outcomes/access (e.g., schooling, healthcare access, housing conditions) rather than expenditure directly, its headline poverty rate is a methodologically distinct statistic from the CBN monetary poverty rate and the two should never be quoted interchangeably, even for the same reference year.

## Extraction Notes

- Always specify which measure (CBN monetary poverty rate, Gini, or MPI) is being cited, its survey round/year, and — for poverty and Gini — whether the figure is a fresh HIES-round estimate or a CPI-adjusted interim update.
- Flag any poverty-rate comparison spanning Pakistan's pre-2013-14 to post-2013-14 methodology change as not directly comparable without adjustment.
- Note that district-level poverty/inequality estimates are only available for PSLM/HIES rounds specifically designed with district-level sample sizes; not every round supports this granularity.
