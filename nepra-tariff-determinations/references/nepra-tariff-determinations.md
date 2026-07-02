# NEPRA Tariff Determinations Reference

## Source

- National Electric Power Regulatory Authority (NEPRA), Government of Pakistan
- NEPRA official website: `https://www.nepra.org.pk`
- Tariff section (generation, transmission, distribution determinations and periodic adjustments): use the Tariff navigation on `https://nepra.org.pk` rather than relying on a single sub-page URL, which may move between releases.
- Determinations are published as individual PDF notifications, often gazetted (published in the Gazette of Pakistan) once finalized.

## Document Structure

- Case/docket reference number and petitioner (licensee) name.
- Petition summary: what tariff or adjustment the licensee requested.
- NEPRA's analysis: cost-of-service review, return-on-equity/return-on-equity-during-construction assumptions (for generation), or revenue requirement analysis (for distribution).
- Approved tariff structure: capacity and energy payment components (generation) or slab/fixed-variable structure (distribution).
- Effective date and, where applicable, indexation or adjustment mechanism going forward.

## Key Indicator Types

- generation tariff: capacity payment (Rs/kW/month or similar) and energy payment (Rs/kWh) by technology
- distribution/supply tariff: consumer category slab rates and fixed charges
- periodic adjustments: fuel charge adjustment (FCA), quarterly tariff adjustment (QTA), monthly fuel price adjustment (MFPA)
- Multi-Year Tariff (MYT) framework parameters and indexation formula

## Extraction Notes

- Always identify the specific licensee, technology, and case/docket reference before quoting a tariff figure.
- Distinguish the base/reference tariff from periodic adjustments layered on top of it; the two must be combined (not substituted) to state a consumer or project's effective all-in rate.
- Preserve capacity vs. energy payment splits for generation tariffs rather than collapsing them into a single blended number unless the source itself reports a blended rate.
- Cross-reference `igcep-capacity-plan` only for indicative planning-stage cost assumptions; those are not the same as an actual NEPRA determination and should not be cited interchangeably.
