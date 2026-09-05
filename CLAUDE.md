# Project guidance for Claude

Two default analytical lenses are in force. Each has a required retrieval
step: never run on framework memory alone.

| Work | Default lens | Framework file |
| --- | --- | --- |
| Public stock trading (single names, sectors, ETFs, index direction) | Carter Worth / Worth Charting | `lenses/worth-equity-lens.md` |
| Options trades (structure, sizing, management) | Tom Sosnoff / tastytrade | `lenses/sosnoff-options-lens.md` |

When a trade is a stock view expressed through options, use both: Worth for
the directional and timing read, Sosnoff for the structure and mechanics.

## Public stock analysis: Worth lens is the default

Whenever we are working a public stock trade (screening a name, judging a
sector, sizing a long or short, deciding whether to trim or add), analyze
it through the Carter Worth lens by default. The full framework lives in
`lenses/worth-equity-lens.md`; read it before doing equity trading work.

### Retrieval protocol (required, not optional)

Before giving a stock trading recommendation:

1. Run a Parallel Search (`mcp__Parallel_Search__web_search`) for current
   Carter Worth commentary relevant to the name, sector, or index. Use two
   or three queries, for example:
   - `Carter Worth <ticker or sector> <current month year>`
   - `Worth Charting <theme>` (e.g. 150-day, breakout, relative strength)
   - `Carter Worth CNBC Fast Money <current month year>`
2. Prefer primary sources: CNBC video pages and articles, Worth Charting
   press pages, podcast appearances. The Quiver Quantitative CNBC tracker
   is a useful index of his recent calls but should be corroborated.
3. Note the publish date of what you found. If nothing is more recent than
   about 90 days, say so explicitly and fall back to the framework document.
4. Cite what you used. Distinguish "framework rule" from "current call" so
   the reader can tell which is which.

### Output shape for a stock analysis

- Lead with the Worth read: price versus the 150-day moving average and
  its slope, the long-term trendline or channel, volume confirmation,
  relative strength versus the S&P 500, and any historical analog.
- State the technical juncture first (breakout, extended, reversal at
  support or resistance), then any current Worth call on the name or
  sector, with a source and date.
- Flag where the trade fights the chart (buying an extended name far above
  its 150-day, shorting into a volume-confirmed breakout). Do not quietly
  rationalize it with a fundamental story.
- Fundamentals and other lenses are welcome as a secondary section, never
  as the default.

## Options analysis: Sosnoff lens is the default

Whenever we are working an options trade (screening, structuring, sizing,
managing, or reviewing a position), analyze it through the Tom Sosnoff /
tastytrade lens by default. The full framework lives in
`lenses/sosnoff-options-lens.md`; read it before doing options work.

### Retrieval protocol (required, not optional)

Do not run on framework memory alone. Before giving an options recommendation:

1. Run a Parallel Search (`mcp__Parallel_Search__web_search`) for current
   tastytrade / tastylive / Sosnoff commentary relevant to the trade. Use two
   or three queries, for example:
   - `Tom Sosnoff <underlying or theme> <current month year>`
   - `tastylive market measures <topic>` (e.g. strangles, IV rank, 21 DTE)
   - `tastytrade <strategy> <current year>`
2. Prefer primary sources: tastylive.com show pages and blog, tastylive
   YouTube segments, Sosnoff interviews. Third-party summaries are fine for
   corroboration but should not be the only source.
3. Note the publish date of what you found. If nothing is more recent than
   about 90 days, say so explicitly and fall back to the framework document.
4. Cite what you used. In the analysis, distinguish "framework rule" from
   "current commentary" so the reader can tell which is which.

### Output shape for an options analysis

- Lead with the Sosnoff read: IV rank environment, duration, strike/delta,
  size, and the management plan (profit target and 21 DTE rule).
- State the mechanical rule first, then any current commentary that adjusts
  it, with a source and date.
- Flag where the trade violates a core mechanic (low IV rank, illiquid
  underlying, oversized relative to buying power, undefined risk in a small
  account). Do not quietly rationalize it.
- Other lenses (a discretionary directional view, fundamentals, a different
  options school) are welcome as a secondary section, never as the default.

## Scope

These defaults apply to public stock and options trading work only.
Private equity and other investment analysis in this repo is not governed
by either lens.
