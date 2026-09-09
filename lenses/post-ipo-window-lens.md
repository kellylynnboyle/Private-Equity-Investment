# Post-IPO Window Lens (Damodaran, Ritter, Renaissance Capital)

Default lens for a newly public stock from lock-up expiry (about month
six) through the first anniversary of the IPO (month twelve). Sourced on
2026-09-05 via Parallel Search; refresh per the retrieval protocol in
`CLAUDE.md` rather than treating this file as the final word.

## Why this window gets its own lens

- The lock-up expires and insider supply hits the market for the first time.
- The first two or three public earnings reports land, so the IPO story
  meets real numbers and the multiple gets re-set.
- Sell-side initiations are done, index inclusion decisions arrive, and the
  first full-year guidance is issued.
- The Worth lens cannot run yet. Its anchor is the 150-day moving average,
  and a stock at month six has roughly 125 trading days of history. It
  becomes usable around month seven or eight.
- The private lens (Gerstner, Baker, Wood) is through the IPO and has moved
  on to the next private name.

## Who

| Expert | Role | Why |
| --- | --- | --- |
| Aswath Damodaran (NYU Stern) | Primary: valuation | His "story to numbers" framework is exactly what months six to twelve test. He publishes live valuations of IPOs with spreadsheets, revised SpaceX on June 4, 2026 two days after the prospectus, and holds no fund positions. |
| Jay Ritter (University of Florida) | Base rates | Maintains the canonical IPO database, long-run statistics updated August 27, 2026. Gives the prior before the specific name is examined. |
| Renaissance Capital (Kathleen Smith, Matt Kennedy) | Aftermarket mechanics | Runs the Renaissance IPO Index and the IPO ETF, tracks the lock-up calendar and float, and publishes weekly IPO aftermarket research. The practitioner view on supply and who actually sells. |

## Damodaran's frame

- Every number needs a story and every story needs a number. A young
  company valuation is a marriage of narrative and cash flows, not a
  projection of last year.
- Less is more. Six variables carry the valuation: revenue growth, target
  operating margin, sales to invested capital, cost of equity, cost of
  debt, and probability of failure. Do not build a 300-line model.
- Internal consistency. High growth with low reinvestment and low risk is
  a red flag. Terminal value must assume growth below the economy's rate
  with reinvestment to support it, never a multiple of revenue.
- Failure risk is explicit, not squeezed into the discount rate. Use the
  cross-sectional distribution of cost of capital (roughly the 10th to 90th
  percentile band) rather than estimating to two decimals.
- On a young company, the financials do not answer the big questions. His
  own words after the SpaceX prospectus: "it is a young company, where the
  answers to the big questions are not in those financials."
- Investor versus trader. Long-term investors focus on fundamentals and
  execution; traders depend on sentiment and momentum. Say which you are.
- Update the story as the numbers arrive. Each quarter, re-check the six
  variables against what was reported and re-value. The first year is
  where the IPO narrative is confirmed or broken.

## Ritter's base rates (1980 to 2024, updated Feb to Aug 2026)

| Cut | Three-year market-adjusted buy-and-hold return |
| --- | --- |
| All IPOs (9,253) | about -20.5% |
| Pre-issue sales under $1B | about -22.4% |
| Pre-issue sales $1B and up | about -2.1% |
| Tech | about -12.7% |
| Non-tech | about -24.9% |

- The average IPO underperforms the market by roughly 5.5 percent a year
  over its first three years, so the burden of proof sits on the company.
- Big, profitable, and tech-sector IPOs come close to matching the market.
  Small, unprofitable, and non-tech IPOs do most of the underperforming.
- Lock-up expiry: average decline of 1 to 3 percent on the day and about
  2.4 percent over the following month, milder (around 0.5 percent) for
  large floats. Eligibility to sell is not the same as selling.
- Small floats have historically outperformed in the aftermarket; float
  size and who owns the unlocked shares matter more than the calendar date.
- 2025 IPO cohort: 90 operating-company IPOs, average first-day return
  29.3 percent, $13.1B left on the table. A hot first day is not a
  predictor of year-one performance.

## Renaissance Capital's mechanics

- The Renaissance IPO Index holds names for a rolling three-year window,
  adds large IPOs after a seasoning period, weights by float-adjusted cap
  with a 10 percent cap, and cycles constituents out at the three-year
  mark. Index adds and drops are themselves flow events.
- Track the lock-up calendar from the S-1: date, share count subject to
  lock-up, and the split between founders, employees, and financial
  investors. VC and PE holders are motivated sellers; founders often hold.
- Watch float versus locked shares. A small float with a large locked
  block is the most exposed setup; a large float with a small locked block
  barely notices expiry.
- Watch the IPO ETF's own performance as a read on the cohort. Through
  December 2025 the ETF returned 5.4 percent over one year and -6.5 percent
  annualized over five years, against a strongly positive S&P 500.
- Use IPO Pro for dates and filings; use the weekly IPO research for the
  aftermarket read.

## How to run a post-IPO window analysis

1. Calendar. Lock-up expiry date, share count unlocking, holder mix, index
   inclusion dates, and the earnings dates that fall in the window.
2. Ritter prior. Place the name in the base-rate table by size,
   profitability, sector, and float. State the expected drag.
3. Damodaran re-valuation. Take the IPO-time story and the six variables,
   update each with the quarters reported since listing, and re-value.
   State whether the reported numbers confirmed or broke the story.
4. Renaissance supply check. Who is unlocking, are they motivated sellers,
   what is the float after expiry, and how did comparable recent IPOs trade
   through their own expiry.
5. Verdict. Investor or trader framing, position size, and the plan for
   the handoff to the Worth lens once the 150-day average exists.
6. Flag the gap. If price is far from the re-valued number, say which way
   and whether the coming quarters can close it.

## Current commentary snapshot (as of 2026-09-05)

- Damodaran on SpaceX (June 4, 2026): post-prospectus equity value about
  $1.3T and roughly $100 per share against a $135 offer price and about
  $1.8T implied market value. "At $1.8 trillion, it looks overpriced to me,
  but that is a personal judgment." He raised launch margins to 45 percent,
  doubled long-run AI revenue but cut AI margins from 45 to 25 percent, and
  called the $26T AI total addressable market in the prospectus "fantasy
  land." He would not buy at $1.8T and would not short it. The SpaceX
  lock-up window opens around mid-December 2026.
- Damodaran (August 20, 2026): "AI's Bar Mitzvah Moment," arguing AI has
  moved from hype and hope to business questions. Relevant to every AI
  IPO's first-year story.
- Ritter's long-run statistics were refreshed August 27, 2026 with returns
  through December 2025; the base-rate table above is from that update.
- Renaissance IPO ETF, September 4, 2026: CoreWeave is the largest
  holding at about 8.7 percent. CoreWeave's own lock-up expired after its
  Q2 2025 earnings following a roughly 200 percent run from its March 2025
  IPO, and is the most recent large-cap template for an AI name passing
  through this window.
- Renaissance's 2026 IPO Outlook named OpenAI and Anthropic among the
  largest candidates and expected a pickup in unicorn listings.

Refresh this section whenever a stock inside its first year of trading is
being worked. If the newest source found is older than about 90 days, say
so in the analysis.

## Sources

- https://aswathdamodaran.blogspot.com/2026/06/a-weeks-ago-i-assessed-value-of-spacex.html (June 4, 2026)
- https://aswathdamodaran.blogspot.com/2026/04/to-trillion-dollars-and-beyond-spacex.html (April 2026)
- https://aswathdamodaran.blogspot.com/2026/08/ais-bar-mitzvah-moment-from-hype-hope.html (August 20, 2026)
- https://www.cnbctv18.com/market/looks-overpriced-valuation-expert-aswath-damodaran-feels-spacex-is-overpriced-ipo-ws-l-19920409.htm (June 5, 2026)
- https://rpc.cfainstitute.org/blogs/enterprising-investor/2022/tell-me-a-story-aswath-damodaran-on-valuing-young-companies
- https://pages.stern.nyu.edu/~adamodar/pdfiles/country/YoungCoforforIndiaRealShort2023.pdf (ten rules for valuing young companies)
- https://site.warrington.ufl.edu/ritter/ipo-data (updated March 9, 2026)
- https://site.warrington.ufl.edu/ritter/files/IPOs-long-run-returns-on-IPOs.pdf (August 27, 2026)
- https://www.renaissancecapital.com/review/IPO_Outlook_2026_Public.pdf (December 22, 2025)
- https://www.renaissancecapital.com/IPO-Center
- https://etfs.renaissancecapital.com/us-ipo-etf (holdings as of September 4, 2026)
- https://etfs.renaissancecapital.com/docs/renaissance-ipo-etf-summary-prospectus.pdf (January 31, 2026)
- https://etfs.renaissancecapital.com/articles/111299/introduction-to-the-renaissance-ipo-etf-tracking-the-new-stock-asset-class

## Disclaimer

Damodaran and Ritter are academics with no fund positions. Renaissance
Capital manages the IPO ETF and sells IPO research. None of this is
investment advice. This lens is an analytical frame, not a recommendation
to trade.
