# Derivative Income Lens (Morningstar, Reiner, Kaufman)

Default lens for passive-income products that manufacture yield from
options or structured notes: covered-call ETFs, equity-linked-note funds
such as JEPI, and autocallable income ETFs such as ARKY and CAIE. Sourced
on 2026-09-05 via Parallel Search; refresh per the retrieval protocol in
`CLAUDE.md` rather than treating this file as the final word.

## What this lens covers

- Covered-call and call-overwrite ETFs (JEPI, JEPQ, QYLD, XYLD, SPYI,
  QQQI, DIVO, GPIX, and the single-stock YieldMax family).
- Equity-linked-note (ELN) income funds, where the option premium is
  delivered through a note from a bank counterparty.
- Autocallable income ETFs (CAIE, CAIQ, ARKY), where income is a
  contingent coupon paid only while the reference asset stays above a
  barrier, and principal is at risk below it.
- Any fund whose headline "yield" is a distribution rate rather than
  earned interest or dividends.

It does not cover dividend-growth or high-dividend stock investing. That
is a different question with different experts.

## Who

| Expert | Role | Why |
| --- | --- | --- |
| Morningstar derivative-income analysts (Zachary Evens, Brendan McCann, Jeffrey Ptak) | Independent lens | Evens wrote the definitive plain-English analysis of the first autocallable ETF and its two risks. McCann rated JEPI on August 26, 2026: "solid approach to covered calls still carries long-term costs." They cover the category continuously and hold no positions. |
| Hamilton Reiner (JPMorgan, JEPI and JEPQ) | Practitioner of ELN income | Architect of the largest derivative-income fund (about $46B) and its Nasdaq sibling (about $41B). Delivers option premium through ELNs spread across four or five issuers with none above 5 percent of assets. The operating standard other ELN funds are measured against. |
| Matt Kaufman (Calamos, Global Head of ETFs) | Autocallable specialist | Launched the first autocallable ETF, CAIE, on June 25, 2025. It is the direct comparable for ARKY and the most current public voice on autocallable structure, laddering, and barrier management. |

Theory citation: Roni Israelov and Lars Nielsen, "Covered Calls
Uncovered" (Financial Analysts Journal, 2015). Option-selling income
decomposes into equity exposure, short volatility, and an equity-reversal
bet. Equity exposure is the main driver of risk and return. The
distribution is not the return.

## Core rules

- Distribution rate is not yield and yield is not return. Judge every
  product on total return versus its reference asset, then ask how much of
  the distribution was return of capital.
- The income is payment for a risk you are taking. Covered calls sell the
  upside. Autocallables sell the downside below a barrier. Name the risk
  sold before admiring the coupon.
- NAV erosion is the tell. If the distribution exceeds what the option
  overlay and the underlying earn over a cycle, the share price ratchets
  down and future income falls with it. Check NAV since inception, not
  just the payout.
- Volatility is the fuel. Higher implied volatility in the reference
  asset means a higher coupon and a bigger loss when the reference moves
  through the strike or barrier. Single-stock products pay the most and
  break the hardest.
- Counterparty and wrapper risk are real. ELNs and swaps carry issuer
  risk. Count the counterparties and their concentration.
- Tax character matters. Return-of-capital distributions defer tax and
  lower cost basis; ordinary income does not. Read the 19a notice and
  Form 8937.
- Bonds are ballast; these are not. Derivative-income funds fall when
  stocks fall sharply and do not recover. Do not size them as the
  fixed-income sleeve.

## Structure by structure

### Covered-call and call-overwrite ETFs

- Ask what is overwritten (index or single stock), how much (100 percent
  or partial), how far out of the money, and how often (monthly, weekly,
  0DTE). More overwriting and closer strikes mean more income and less
  upside.
- JEPI is the reference design: a defensive low-volatility S&P 500 stock
  sleeve plus out-of-the-money index calls delivered through ELNs, about
  7 to 8 percent distribution, 0.35 percent fee. JEPQ is the Nasdaq
  version at about 10 percent.
- Distribution rates above roughly 15 percent on an index, or any
  single-stock overwrite fund, should be presumed to be returning capital
  until the NAV history proves otherwise.

### Equity-linked-note income funds

- The ELN is a bank note whose payoff replicates the option overlay.
  Regulatory cap of 20 percent of assets in ELNs; JEPI stays under it
  and under 5 percent per issuer.
- Check: number of issuers, max concentration, and whether the note
  replicates a call overwrite (upside sold) or a put-like structure
  (downside sold).

### Autocallable income ETFs

- Coupon barrier: the level below which the coupon is skipped. Principal
  barrier: the level below which principal is lost at maturity. Call
  trigger: the level at which the note is redeemed early and coupons stop.
- CAIE references a volatility-targeted S&P 500 index with a 60 percent
  barrier through 52 or more laddered notes, swap counterparty JPMorgan.
  Weighted coupon about 14 percent, all notes above barrier as of
  September 1, 2026, roughly 21 percent one-year total return.
- ARKY references 25 to 50 individual ARK innovation stocks with 50 to 60
  percent barriers, sub-advised by SCG Asset Management, primary swap
  counterparty Morgan Stanley. Target coupon 17.5 percent, 0.85 percent
  fee, launched August 19, 2026 with about $28M in assets.
- The difference in coupon is the difference in what is sold. An index
  with a volatility target is unlikely to fall 40 percent and stay there.
  A single innovation stock does that routinely; the 2022 drawdown would
  have breached many 50 percent barriers. Upside is capped at the coupon
  in both cases.
- A "memory" feature pays skipped coupons later if the reference recovers
  above the barrier. Useful, but it does not restore principal.

## How to run a derivative-income analysis

1. Name the structure. Covered call, ELN overwrite, or autocallable. Index
   or single stock. Overwrite ratio, strike distance, barrier levels, call
   trigger, tenor, and observation frequency.
2. Name the risk sold. Upside above the strike, downside below the
   barrier, or both. State the worst historical drawdown of the reference
   asset against the barrier.
3. Total return check. Fund total return since inception versus the
   reference asset and versus JEPI or CAIE as the category benchmark. NAV
   path since inception.
4. Distribution character. Return of capital share from the 19a notice
   and Form 8937; ordinary income share; effect on cost basis.
5. Wrapper check. Counterparties and concentration, fee, assets under
   management, bid-ask spread, premium or discount history, track record
   length.
6. Portfolio role. It is an equity substitute with capped upside, not a
   bond substitute. Size it against the equity sleeve and pair it with
   the Sosnoff lens for the short-volatility mechanics it cannot manage.
7. Flag the marketing. If the pitch leads with the distribution rate and
   buries the barrier or the NAV path, say so.

## Current commentary snapshot (as of 2026-09-05)

- Category size: roughly 200 derivative-income ETFs holding about $147B
  as of September 2025, with JEPI and JEPQ about half of it. JEPI is
  about $46B and JEPQ about $41B as of late August 2026.
- Morningstar on JEPI (August 26, 2026, Brendan McCann): Above Average
  people and process, cheapest-quintile fee at 0.35 percent against a
  category median near 0.97 percent, and a long-term cost to the covered
  call approach. Hamilton Reiner was promoted to CIO of US core equity in
  2025 and remains lead manager.
- Morningstar on autocallables (Zachary Evens, updated October 29, 2025):
  "no free lunch." Two risks: coupons not paid continuously, and not all
  principal returned. CAIE distributions have been classified as return of
  capital.
- Calamos CAIE (September 1, 2026): $1.3B, weighted coupon 14.05 percent,
  100 percent of 52 notes paying, weighted mark-to-market 97.9 percent,
  one-year total return about 21 percent. CAIQ (Nasdaq version) launched
  November 2025 with a weighted coupon near 18 percent in January 2026.
- ARK ARKY (launched August 19, 2026): first ARK income product, 17.5
  percent target coupon, single-stock autocallables on the ARK universe,
  50 to 60 percent barriers, SCG Asset Management sub-adviser, Morgan
  Stanley swap counterparty, 0.85 percent fee, about $28M in assets, no
  distribution history yet. ARK's own description: "ARKY seeks income,
  not appreciation."
- Autocallable ETF category reached about $2B in its first year per ARK's
  August 2026 launch material.
- High end of the covered-call market (September 3, 2026): QQQI about 14
  percent, YieldMax CHPY about 42 percent, ULTY about 95 percent
  distribution rates. Rates in that range are the NAV-erosion end of the
  spectrum and should be judged on total return only.

Refresh this section whenever a covered-call, ELN, or autocallable product
is being worked. If the newest source found is older than about 90 days,
say so in the analysis.

## Sources

- https://www.morningstar.com/funds/next-generation-income-etf (Zachary Evens, updated October 29, 2025)
- https://www.morningstar.com/etfs/arcx/jepi/quote (Brendan McCann analysis, August 26, 2026)
- https://www.morningstar.com/alternative-investments/ask-your-advisor-these-questions-before-investing-derivative-income-etfs
- https://am.jpmorgan.com/content/dam/jpm-am-aem/americas/us/en/literature/fact-sheet/etfs/FS-JEPI.PDF (July 31, 2026)
- https://www.calamos.com/funds/etf/calamos-autocallable-income-caie (dashboard as of September 1, 2026)
- https://www.riachannel.com/calamos-investments-matt-kaufman-on-the-first-autocallable-income-etf/
- https://www.etftrends.com/alternatives-content-hub/will-autocallable-income-etfs-keep-building-steam-2026 (January 30, 2026)
- https://www.ark-funds.com/funds/arky
- https://www.ark-funds.com/articles/etf/intro-to-arky (August 18, 2026)
- https://www.prnewswire.com/news-releases/ark-invest-launches-its-first-income-strategy-arky-targeting-17-5-income-through-its-innovation-equity-universe-302854835.html (August 19, 2026)
- https://etfdb.com/etf/ARKY (September 3, 2026)
- https://dividend.watch/lists/covered-call-etfs (September 3, 2026)
- https://www.aqr.com/-/media/AQR/Documents/Insights/Journal-Article/Covered-Calls-Uncovered.pdf (Israelov and Nielsen, 2015)

## Disclaimer

Reiner and Kaufman run the funds they discuss. Morningstar analysts hold
no positions. ARK and SCG are the issuer and sub-adviser of ARKY. None of
this is investment advice. This lens is an analytical frame, not a
recommendation to buy any product.
