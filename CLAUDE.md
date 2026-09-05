# Project guidance for Claude

Five default analytical lenses are in force. Each has a required
retrieval step: never run on framework memory alone.

| Work | Default lens | Framework file |
| --- | --- | --- |
| Public stock trading (single names, sectors, ETFs, index direction) | Carter Worth / Worth Charting | `lenses/worth-equity-lens.md` |
| Options trades (structure, sizing, management) | Tom Sosnoff / tastytrade | `lenses/sosnoff-options-lens.md` |
| Late-stage private and pre-IPO (Series D and later, secondaries, pre-IPO rounds, IPO underwriting) | Brad Gerstner, Gavin Baker, Cathie Wood | `lenses/late-stage-private-lens.md` |
| Post-IPO window (lock-up expiry at about month six through month twelve) | Aswath Damodaran, Jay Ritter, Renaissance Capital | `lenses/post-ipo-window-lens.md` |
| Derivative income (covered-call ETFs, equity-linked-note funds such as JEPI, autocallable funds such as ARKY) | Morningstar derivative-income analysts, Hamilton Reiner, Matt Kaufman | `lenses/derivative-income-lens.md` |

When a trade is a stock view expressed through options, use both: Worth for
the directional and timing read, Sosnoff for the structure and mechanics.

The derivative-income lens runs alongside the Worth lens: Worth says when
to commit or trim capital in a name or index, and the derivative-income
lens says whether a packaged income product on that exposure is paying
enough for the risk it sells. When the analysis reaches the option
mechanics inside such a product (strike distance, barrier, tenor, what
cannot be managed), bring in the Sosnoff lens.

Lifecycle handoffs for a company that goes public:

1. Private lens through the IPO pricing and the first day of trading.
2. Post-IPO window lens from listing through month twelve, with the
   lock-up expiry as its centerpiece. It is the sole default from listing
   to about month seven, because the Worth lens's 150-day moving average
   does not exist yet.
3. Worth lens joins once roughly 150 trading days exist (about month seven
   or eight) and becomes the sole default after the first anniversary.

## Post-IPO window analysis: Damodaran, Ritter, and Renaissance are the experts

Whenever we are working a stock inside its first twelve months of public
trading (a lock-up expiry, the first public earnings, an index inclusion,
or a decision to buy, add, trim, or short a recent IPO), analyze it
through the Damodaran, Ritter, and Renaissance lens by default. The full
framework lives in `lenses/post-ipo-window-lens.md`; read it before doing
this work.

### Retrieval protocol (required, not optional)

Before giving a recommendation on a stock in its first year of trading:

1. Run a Parallel Search (`mcp__Parallel_Search__web_search`) for current
   material on the name and the cohort. Use two or three queries per
   source, for example:
   - `Damodaran <company> valuation <current year>` and
     `Musings on Markets <company or theme>`
   - `Ritter IPO long-run returns <current year>` and
     `<company> lock-up expiration date shares`
   - `Renaissance Capital <company> IPO aftermarket` and
     `Renaissance IPO ETF holdings <current month year>`
2. Prefer primary sources: Damodaran's blog and spreadsheets, Ritter's
   University of Florida data pages, Renaissance Capital's IPO Center, ETF
   holdings, and research, and the company's own S-1 and 10-Q filings for
   lock-up terms and reported numbers.
3. Note the publish date of what you found. If nothing is more recent than
   about 90 days, say so explicitly and fall back to the framework document.
4. Cite what you used. Distinguish "framework rule," "base rate," and
   "current view," and name which source holds it.

### Output shape for a post-IPO window analysis

- Lead with the calendar: lock-up expiry date and share count, holder mix,
  index inclusion dates, and the earnings dates inside the window.
- Give the Ritter prior: where the name sits in the base-rate table by
  size, profitability, sector, and float, and the expected drag.
- Run the Damodaran re-valuation: the IPO-time story and six variables,
  updated for the quarters reported since listing, and whether the numbers
  confirmed or broke the story.
- Run the Renaissance supply check: who is unlocking, whether they are
  motivated sellers, the float after expiry, and how comparable recent
  IPOs traded through their own expiry.
- Close with the verdict, investor or trader framing, position size, and
  the planned handoff to the Worth lens.
- Flag stale narratives. If the stock still trades on the IPO story after
  the numbers have contradicted it, say so. Do not quietly carry the
  roadshow narrative forward.

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

## Derivative income analysis: Morningstar, Reiner, and Kaufman are the experts

Whenever we are working a passive-income product that manufactures yield
from options or structured notes (a covered-call ETF, an equity-linked-note
fund such as JEPI, an autocallable income ETF such as ARKY or CAIE, or any
fund whose headline yield is a distribution rate), analyze it through the
Morningstar, Reiner, and Kaufman lens by default. The full framework lives
in `lenses/derivative-income-lens.md`; read it before doing this work.
Dividend-growth and high-dividend stock investing are not covered by this
lens.

### Retrieval protocol (required, not optional)

Before giving a recommendation on a derivative-income product:

1. Run a Parallel Search (`mcp__Parallel_Search__web_search`) for current
   material on the product and its category. Use two or three queries per
   source, for example:
   - `Morningstar <ticker> analysis <current year>` and
     `Morningstar derivative income ETF <current month year>`
   - `JEPI fact sheet <current month year>` and
     `Hamilton Reiner covered call <current year>`
   - `Calamos CAIE autocallable dashboard` and
     `Matt Kaufman autocallable ETF <current year>`
   - `<ticker> 19a notice return of capital` and
     `<ticker> holdings <current month year>`
2. Prefer primary sources: the issuer's fund page, fact sheet, holdings,
   19a notices and Form 8937, Morningstar analyst reports, and the
   prospectus for barrier, strike, and counterparty terms.
3. Note the publish date of what you found. If nothing is more recent than
   about 90 days, say so explicitly and fall back to the framework document.
4. Cite what you used. Distinguish "framework rule," "issuer claim," and
   "independent analysis," and name which source holds it.
5. State position bias. Issuers and portfolio managers are describing
   their own products.

### Output shape for a derivative-income analysis

- Lead with the structure: covered call, ELN overwrite, or autocallable;
  index or single stock; overwrite ratio or barrier levels; tenor;
  counterparties.
- Name the risk sold, and the reference asset's worst historical drawdown
  against the strike or barrier.
- Give total return since inception versus the reference asset and versus
  JEPI or CAIE as the category benchmark, with the NAV path.
- Give distribution character: return-of-capital share and its effect on
  cost basis.
- Close with the portfolio role (equity substitute with capped upside,
  never a bond substitute), sizing against the equity sleeve, and the
  Sosnoff cross-check on the option mechanics.
- Flag distribution-rate marketing. If the pitch leads with the payout and
  buries the barrier or the NAV path, say so. Never quote a distribution
  rate as if it were a yield or a return.

## Scope

These defaults apply to public stock trading, options trading, late-stage
private or pre-IPO work, the first year of post-IPO trading, and packaged
derivative-income products. Buyout-style private equity, early-stage
venture (seed through Series C), dividend-stock investing, and other
investment analysis in this repo are not governed by any of the five
lenses.
