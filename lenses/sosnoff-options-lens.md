# Sosnoff / tastytrade Options Lens

Default lens for all options analysis in this repo. Sourced on 2026-09-05
via Parallel Search; refresh per the retrieval protocol in `CLAUDE.md`
rather than treating this file as the final word.

## Who

Tom Sosnoff is a former CBOE market maker and OEX pit trader, founder of
thinkorswim (sold to TD Ameritrade) and tastylive/tastytrade, and co-host of
tastylive LIVE with Tony Battista. The research behind the mechanics comes
from the tastylive research team (Market Measures, Kai Zeng, Michael
"Dr. Data" Rechenthin, Julia Spina).

## Core thesis

- Implied volatility has historically overstated realized volatility, so the
  structural edge for a retail trader is being a net seller of premium.
- Edge is mechanics plus scale, not prediction. Numbers over narratives;
  no macro guessing, no chart worship.
- Law of large numbers: many small, independent trades so results converge
  to their expected probabilities. "Trade small, trade often."

## Entry mechanics

| Mechanic | Rule |
| --- | --- |
| Volatility filter | Sell premium when IV rank is elevated. IVR above 30 is the study floor; above 50 is the preferred zone. Low IVR means smaller, choosier, and more defined-risk. |
| Duration | Target roughly 45 days to expiration. The 45 DTE result is conditional on managing the trade, not holding to expiry. |
| Duration vs IV | When IVR is low, go longer (about 60 DTE); when IVR is high, shorter (about 30 DTE) keeps daily P/L consistent (tastylive research, Aug 2024). |
| Strikes | Pick by probability of profit and credit received. Short strikes around 16 to 20 delta (about one standard deviation) are the common baseline; closer to the money for more credit. Entry POP should be over 50 percent. |
| Liquidity | Only liquid underlyings with tight bid/ask. Work limit orders near the mid; do not chase fills. |
| Structures | Strangles, iron condors, verticals, covered calls, naked puts. Defined risk in small accounts or low IV; undefined risk only when size is small and the book is diversified. |

## Management mechanics

- Close winners at 50 percent of max credit for most strategies. Calendars,
  diagonals, and iron flies manage earlier, in the 10 to 50 percent range.
- Exit or roll at 21 DTE regardless of P/L to cut gamma risk. tastylive
  research shows exiting at 21 DTE reduces P/L volatility across durations.
- Losers: roll or convert early to re-cap risk. Close anything that breaches
  the max-loss threshold or the sizing rule. Do not improvise stops
  mid-trade; the stop is decided up front through size and structure.
- Do not close for a trivial winner that fails to cover commissions.

## Portfolio mechanics

- Position size about 0.5 to 2 percent of the account per trade, with caps
  per symbol and per theme.
- Deployment scales with volatility. Higher IV means more trades and more
  buying power used; low IV means fewer, tighter, more defined-risk trades.
  Increase the count of trades, not the size of any one trade.
- Diversify on three axes: underlying, strategy, and duration.
- Keep the book near delta neutral in aggregate; harvest theta where it is
  efficient.

## Current commentary snapshot (as of 2026-09-05)

- tastylive continues daily programming (tastylive LIVE, Market Measures,
  Sosnoff Says) with Market Measures episodes running through at least July
  2026. Recent guests include Cem Karsan on volatility and positioning
  (Aug 20, 2026) and Cboe's Henry Schwartz on the midterm-election vol
  curve, which showed no apparent kink through the election cycle.
- A Sept 3, 2026 independent six-month test of the Sosnoff 45 DTE low-delta
  short-put approach on S&P 500 futures was published (Casey Stubbs
  Substack). Treat it as third-party corroboration, not tastylive research.
- Sosnoff's 2025 interviews (IBD, Words of Wisdom podcast) restate the same
  playbook: hundreds of small positions, roughly 100 trades a day, sizing
  off VIX rather than conviction.

Refresh this section whenever an options trade is being worked. If the
newest source found is older than about 90 days, say so in the analysis.

## Sources

- https://www.tastylive.com/talent/tom-sosnoff
- https://www.tastylive.com/shows/market-measures
- https://www.tastylive.com/news-insights/how-iv-impacts-dte-selection (Kai Zeng, Aug 2024)
- https://www.tastylive.com/concepts-strategies/managing-winners
- https://www.tastylive.com/definitions/high-implied-volatility-strategies
- https://www.tastylive.com/definitions/expected-returns
- https://www.tastylive.com/shows/market-measures/episodes/management-with-high-ivr-08-29-2022
- https://www.forex.in.rs/trade-small-often (Words of Wisdom interview summary, Oct 2025)
- https://www.youtube.com/watch?v=00P-Gurxe6k (IBD interview, Oct 2025)
- https://caseystubbs.substack.com/p/i-spent-six-months-testing-tom-sosnoffs (Sept 3, 2026)
- https://www.linkedin.com/company/tastyliveshow (Aug 2026 posts)

## Disclaimer

tastylive content is educational, not investment advice. This lens is an
analytical frame, not a recommendation to trade.
