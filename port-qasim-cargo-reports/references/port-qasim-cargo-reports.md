# Port Qasim Cargo Reports Reference

## Source

- Port Qasim Authority (PQA)
- PQA official website: `https://www.pqa.gov.pk`
- Daily shipping notices, cargo statistics, and trade data published on the PQA website under "Shipping" or "Trade & Traffic" sections

## Typical Report Fields

- Vessel name, type, arrival/berthing date, berth/terminal assignment
- Cargo type and quantity handled per vessel
- Terminal-wise cumulative throughput (daily/monthly/fiscal-year-to-date)
- Commodity categories: containers (TEU), bulk grain, coal, LNG/LPG, POL products, general cargo

## Named Terminals at Port Qasim

- **QICT — Qasim International Container Terminal**: the main container terminal operator at Port Qasim.
- **PIBT — Pakistan International Bulk Terminal**: a major coal/dry-bulk cargo terminal at Port Qasim. Note: PIBT is at Port Qasim, not Karachi Port — it is sometimes miscited as a Karachi Port facility.
- **Engro Elengy Terminal Pakistan Limited** (and the related Engro/Vopak-associated LNG terminal facilities): LNG import/regasification terminal(s) at Port Qasim, part of Pakistan's LNG supply chain.
- **FOTCO — Fauji Oil Terminal and Distribution Company**: a liquid bulk/oil terminal at Port Qasim.
- Pakistan Deepwater Container Terminal (PDWCT), if referenced, is understood to be a Karachi Port facility rather than a Port Qasim one — do not list it here (verify).

## Distinct Ports Note

- Port Qasim, Karachi Port (Karachi Port Trust), and Gwadar Port (Gwadar Port Authority) are separately operated and separately reported; do not merge their statistics without explicit aggregation from an authoritative source.
- Cross-check: PIBT, the Engro LNG terminals, and FOTCO are Port Qasim facilities — not Karachi Port facilities, despite occasionally being miscited as such. KICT, PICT, and SAPT are the Karachi Port container terminals (see `karachi-port-cargo-reports`); QICT is the Port Qasim equivalent. Do not swap these terminal-to-port assignments.

## Extraction Notes

- Always anchor a figure to its exact date/period and to Port Qasim specifically.
- Container volumes (TEU) and bulk/liquid cargo volumes (metric tons) are different units and should not be combined into a single "cargo" figure without conversion methodology.
