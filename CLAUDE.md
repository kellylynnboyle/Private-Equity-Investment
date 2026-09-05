# Project guidance for Claude

Three default analytical lenses are in force. Each has a required
retrieval step: never run on framework memory alone.

| Work | Default lens | Framework file |
| --- | --- | --- |
| Public stock trading (single names, sectors, ETFs, index direction) | Carter Worth / Worth Charting | `lenses/worth-equity-lens.md` |
| Options trades (structure, sizing, management) | Tom Sosnoff / tastytrade | `lenses/sosnoff-options-lens.md` |
| Late-stage private and pre-IPO (Series D and later, secondaries, pre-IPO rounds, IPO underwriting) | Brad Gerstner, Gavin Baker, Cathie Wood | `lenses/late-stage-private-lens.md` |

When a trade is a stock view expressed through options, use both: Worth for
the directional and timing read, Sosnoff for the structure and mechanics.
When a late-stage private name goes public, the private lens covers the
IPO underwriting, lock-up, and sizing; Worth takes over for the chart once
there is enough public trading history.

## Late-stage private analysis: Gerstner, Baker, and Wood are the experts

Whenever we are working a late-stage private or pre-IPO position
(evaluating a Series D or later round, a secondary, a pre-IPO allocation,
an IPO, or a fund that holds such names), analyze it through the
Gerstner, Baker, and Wood lens by default. The full framework lives in
`lenses/late-stage-private-lens.md`; read it before doing this work.

### Retrieval protocol (required, not optional)

Before giving a late-stage private recommendation:

1. Run a Parallel Search (`mcp__Parallel_Search__web_search`) for current
   commentary from all three on the name, sector, or the private market
   broadly. Use two or three queries per expert, for example:
   - `Brad Gerstner <company or theme> <current month year>` and
     `BG2 pod <topic>`
   - `Gavin Baker Atreides <company or theme> <current month year>`
   - `Cathie Wood ARK Venture <company> <current month year>` and
     `ARK Big Ideas <current year> <theme>`
2. Prefer primary sources: BG2 Pod episodes, Invest Like the Best and
   Capital Allocators interviews, ARK research and ARK Venture Fund
   holdings disclosures, direct interviews in Business Insider or CNBC.
   Third-party summaries are corroboration, not the source.
3. Note the publish date of what you found. If nothing is more recent than
   about 90 days, say so explicitly and fall back to the framework document.
4. Cite what you used. Distinguish "framework rule" from "current view"
   and name which of the three holds it. Where they disagree, say so.
5. State position bias. All three are long most of what they discuss.

### Output shape for a late-stage private analysis

- Lead with the round and structure: stage, post-money, preference stack,
  primary versus secondary, lock-up, and expected IPO window.
- Run the three tests in order: Gerstner (AI-accelerated growth, real
  revenue, capex-to-revenue math), Baker (LLCC risk score, position in the
  physical stack, what falsifies the thesis), Wood (cost curve, five-year
  TAM, public comps and existing fund exposure).
- Give a sizing and exit plan: conviction-adjusted size, the panic-early or
  double-down-late choice made in advance, post-IPO drawdown expectation.
- Flag stale marks. Say whether the last-round price holds against current
  public multiples. Do not quietly carry a mark that the public comps no
  longer support.
- Fundamentals, deal-specific legal terms, and other lenses are welcome as
  a secondary section, never as the default.

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

These defaults apply to public stock trading, options trading, and
late-stage private or pre-IPO work. Buyout-style private equity, early-stage
venture (seed through Series C), and other investment analysis in this repo
are not governed by any of the three lenses.
