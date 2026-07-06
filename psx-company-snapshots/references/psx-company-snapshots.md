# PSX Company Snapshots Reference

## Sources

- PSX Data Portal (official, authoritative for quotes): `https://dps.psx.com.pk`
- Company financial filings (authoritative for fundamentals): filed under the Companies Act 2017 and PSX listing regulations; typically available via the company's own investor-relations page and via PSX's Corporate Announcements / Financial Results sections.
- `psxdata` Python package: `https://pypi.org/project/psxdata/` (GitHub: `https://github.com/mtauha/psxdata`) — convenience scraper, not the source of record.

## Typical Quote Fields

- Last traded price
- Change (absolute and percentage) versus previous close
- Day's high / low
- Volume (shares traded)
- Previous close

## Typical Fundamentals Fields

- EPS (earnings per share) — usually reported both for the latest quarter and trailing twelve months
- P/E ratio (price-to-earnings)
- Book value per share
- Dividend per share and dividend yield
- Market capitalization
- Payout history (cash dividend, bonus/right share ratio) for recent periods

## Corporate Actions and Comparability

- **Bonus shares**: issued as additional shares to existing shareholders (e.g., "20% bonus" = 20 new shares per 100 held); mechanically increases share count and dilutes per-share metrics like EPS and book value, even though total equity/earnings are unchanged. Historical per-share data before a bonus issue must be adjusted for the new share count to remain comparable.
- **Right shares**: offered to existing shareholders at a discount to raise capital; increases share count and total equity, and typically dilutes per-share metrics differently from a bonus issue since new capital is actually raised.
- **Cash dividends**: distributed from profits; do not affect share count but do reduce retained earnings.
- Failing to account for these actions is one of the most common sources of an apparently "sudden" EPS or price drop that is actually a mechanical adjustment, not a change in company performance.

## Circuit Breakers

- PSX applies daily price-movement limits (a percentage band around the previous day's closing price) to most listed securities. A stock that hits its upper or lower circuit for the session is halted at that level — the closing price on such a day reflects the circuit limit, not necessarily where the stock would have settled without the constraint.

## Fiscal Year-End Variation

- Most Pakistani listed companies use a June 30 fiscal year-end, aligned with government and standard corporate practice.
- Some companies — often multinational subsidiaries or those aligned with a foreign parent's reporting calendar — use a December 31 or other fiscal year-end.
- Always confirm the specific company's fiscal year-end before describing a fundamentals figure as "the latest annual report" or comparing it period-over-period against another company.

## Extraction Notes

- When using `psxdata.fundamentals()`, treat returned fields as a snapshot subject to the package's own scraping/update cadence — cross-check against the company's actual filed financial statements for anything citation-grade.
- Missing fundamentals fields (e.g., no dividend declared in a loss-making period) should be treated as "not applicable" rather than a parsing error, but verify which case applies before asserting either.
