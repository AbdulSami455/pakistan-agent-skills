# PSX Historical Data Reference

## Sources

- PSX Data Portal historical archive (official, authoritative): `https://dps.psx.com.pk`
- `psxdata` Python package: `https://pypi.org/project/psxdata/` (GitHub: `https://github.com/mtauha/psxdata`) — convenience scraper, not the source of record.

## Corporate Action Adjustment

Raw (unadjusted) historical price series show mechanical discontinuities around:

- **Bonus share issues**: ex-bonus date shows a price drop roughly proportional to the dilution (e.g., a 20% bonus issue mechanically reduces price per share by roughly 1/1.2), reflecting the same total company value spread over more shares — not a market sell-off.
- **Right share issues**: similar mechanical adjustment around the ex-right date, complicated by the fact that new capital is actually raised (unlike a bonus issue).
- **Stock splits**: less common on PSX than bonus issues, but functionally similar — share count changes, price adjusts proportionally.

If a data source does not clearly state whether its historical series is adjusted for these events, treat cross-period return calculations spanning such an event with caution and flag the ambiguity.

## Circuit Breaker Behavior

- PSX applies a percentage-based daily price movement limit around the previous close for most securities.
- A session where a stock's open, high, low, and close are identical (or nearly so) is often a circuit-breaker "lock" — the stock could not trade beyond that limit that session — rather than genuinely flat trading activity.
- This is most common during periods of significant company-specific news (earnings surprises, corporate action announcements) or broad market stress.

## Trading Calendar

- PSX's trading week and holiday calendar follows Pakistan's gazetted public holidays, which differ from other markets' calendars (e.g., Eid holidays shift annually per the lunar calendar, and Pakistan-specific holidays like Independence Day and Iqbal Day are non-trading days).
- Do not assume a fixed ~252-trading-day year; verify the actual number of trading sessions for the specific year(s) in question if precision matters (e.g., for annualizing returns).

## Delisting, Suspension, and Symbol Changes

- A company can be suspended from trading by PSX (e.g., pending a regulatory inquiry, failure to file financials) or delisted entirely (e.g., after a merger, or forced delisting for non-compliance).
- A historical series that ends abruptly should be checked against the company's current listing status before being treated as a data-retrieval gap.
- Ticker symbols can be reassigned or changed following a corporate name change or merger; verify that a "continuous" series is not silently spanning two different underlying corporate entities.

## Extraction Notes

- When validating `psxdata.stocks()` output, cross-reference any anomalous session (identical OHLC, unexpected gap, extreme single-day move) against known corporate actions or circuit-breaker context before treating it as a parsing defect.
- Prefer the PSX Data Portal's own historical archive as the authoritative cross-check for any dataset used in a report, research paper, or financial analysis.
