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

## Distinct Ports Note

- Port Qasim, Karachi Port (Karachi Port Trust), and Gwadar Port (Gwadar Port Authority) are separately operated and separately reported; do not merge their statistics without explicit aggregation from an authoritative source.

## Extraction Notes

- Always anchor a figure to its exact date/period and to Port Qasim specifically.
- Container volumes (TEU) and bulk/liquid cargo volumes (metric tons) are different units and should not be combined into a single "cargo" figure without conversion methodology.
