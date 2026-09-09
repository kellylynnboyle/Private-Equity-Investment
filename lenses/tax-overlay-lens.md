# Tax Overlay Lens (Green, Kitces, Brumberg, McKenna, Benz)

The sixth lens. It does not own a domain of its own; it runs on top of the
other five and asks, for every recommendation they produce, what the
after-tax result is and what election, holding period, or account choice
changes it. Sourced on 2026-09-05 via Parallel Search; refresh per the
retrieval protocol in `CLAUDE.md` rather than treating this file as the
final word. Nothing here is tax advice; it is a checklist for the
questions to put to a CPA.

## Who: one tax expert per domain lens

| Lens | Tax expert | Why |
| --- | --- | --- |
| 1. Sosnoff options | Robert A. Green, CPA (GreenTraderTax) | The recognized authority on trader taxation. Green's 2026 Trader Tax Guide (157 pages, 18 chapters) was rewritten for the One Big Beautiful Bill Act and covers Section 1256, wash sales on options, straddles, constructive sales, trader tax status, the Section 475 election, and the tax character of ETFs, ETNs, and volatility products. Latest compliance post August 17, 2026. |
| 2. Worth equity | Michael Kitces (Nerd's Eye View) | Investor-side equity taxation: harvesting losses versus harvesting gains across the four long-term capital gains brackets, the 3.8 percent net investment income tax, asset location, and concentrated-position strategies such as tax-aware long-short (June 17, 2026). Weekly publication; also the tie-breaker on account and year placement when two lenses apply. |
| 3. Late-stage private | Bruce Brumberg (myStockOptions.com) | Editor-in-chief of the standard reference on equity compensation taxation: ISOs, NSOs, RSUs, 83(b), AMT, QSBS and Section 1045 rollovers, tender offers. Running an IPO Readiness Summit on September 24, 2026 aimed at SpaceX, OpenAI, Anthropic, Anduril, and Databricks holders. |
| 4. Post-IPO window | Kristin McKenna, CFP (Darrow Wealth Management, Forbes senior contributor) | Specialist in sudden-wealth and post-IPO planning: lock-up release sales strategy, 10b5-1 plans (October 2025), RSU taxation (March 2026), concentrated-stock diversification, AMT credit use. Published the SpaceX employee lock-up release schedule on May 21, 2026, noting the staggered early-release program inside the 180-day lock-up. |
| 5. Derivative income | Christine Benz (Morningstar, director of personal finance) | Tax-efficient fund selection and placement: which distributions are ordinary, qualified, or return of capital, tax-cost ratios, and which account each fund belongs in. Publishes tax-efficient model portfolios (latest September 3, 2026) and the annual tax-efficient fund picks (June 10, 2026). |

## Tax map by lens

| Lens | Main tax questions | Owner |
| --- | --- | --- |
| 1. Sosnoff options | Is the contract a Section 1256 contract (broad-based index options, futures, options on futures: 60/40, marked to market, no wash sale, three-year loss carryback) or an equity option (short-term capital, wash sales between the stock and its options, straddle and constructive-sale rules)? Does the trader qualify for trader tax status, and is a Section 475 election worth it? | Green |
| 2. Worth equity | Lot selection, holding period to long-term, wash-sale coordination with any options on the same name, harvest losses versus harvest gains given the bracket, state tax. | Kitces (Green if trader tax status is in play) |
| 3. Late-stage private | QSBS under Section 1202: original issuance from a domestic C corporation, gross-asset test at issuance, active business test, holding period, per-issuer cap. 83(b) elections, ISO exercise and AMT, secondary purchases (which do not qualify for QSBS), Section 1045 rollovers, interval-fund reporting (ARK Venture Fund reports on a 1099, not a K-1). | Brumberg |
| 4. Post-IPO window | Lock-up release into a 10b5-1 plan, staggered early-release windows, double-trigger RSU vesting at IPO and withholding shortfalls, whether the QSBS clock has run, calendar-year placement of the sale, state residency, concentrated-position strategies. | McKenna (Brumberg for QSBS carried from the private stage) |
| 5. Derivative income | Character of the distribution: ordinary income (ELN-based funds such as JEPI, about 80 to 85 percent of the payout), Section 1256 60/40 passed through (index-option funds such as SPYI and QQQI), or return of capital (autocallable funds such as CAIE and ARKY, most NEOS funds). Basis reduction from return of capital and the zero-basis point. Asset location: ordinary-income payers belong in tax-advantaged accounts. | Benz (Green for Section 1256 pass-through and straddle questions) |

## Core rules

- Character before rate. Name whether a gain or distribution is
  short-term capital, long-term capital, Section 1256 60/40, ordinary
  income, qualified dividend, or return of capital. The rate follows from
  the character, and the character follows from the instrument, not from
  the marketing.
- Section 1256 is the options trader's biggest lever. Broad-based index
  options and futures get 60/40 treatment regardless of holding period
  (blended top rate about 26.8 percent versus 37 percent), year-end mark
  to market, no wash-sale rule, and a three-year carryback of losses.
  Single-stock and narrow-index options do not.
- Wash sales reach across the stock and its options. A loss on Apple stock
  is deferred by buying Apple calls within the window, and vice versa.
  Section 475 removes wash sales and the $3,000 capital-loss cap for
  qualifying traders, but converts gains to ordinary income and is elected
  in advance (April 15 of the year it applies for individuals).
- QSBS is all or nothing, so document it from day one. Original issuance,
  gross assets at issuance, active-business compliance, and the exact
  holding-period start. Secondary purchases and tender-offer buys never
  qualify.
- The IPO does not start the tax clock; the acquisition did. At lock-up
  expiry the question is which lots, which year, and whether a 10b5-1
  plan should have been filed before the window.
- Distribution rate is not income and return of capital is not tax-free.
  It lowers basis and comes back as capital gain on sale or as immediate
  gain once basis hits zero. Read the 19a notice, then the Form 8937.
- Asset location beats security selection for tax. Ordinary-income payers
  (ELN funds, bonds, REITs) go in tax-advantaged accounts; qualified
  dividend and long-term growth assets go in taxable accounts.
- Harvest gains as well as losses. With four long-term capital gains
  brackets (0, 15, 20, and 20 plus the 3.8 percent surtax), filling a
  bracket this year can beat deferring into a higher one.
- Deferral is worth less than it feels. Kitces's estimate: deferring a 15
  percent tax on a $40,000 gain is worth roughly half a percent a year in
  extra return, not the whole tax.

## How to run the tax overlay

1. Instrument and account. What exactly is being bought or sold, in which
   account type, and by whom (investor or trader tax status).
2. Character. Apply the tax map row for the lens in play and state the
   character of every expected gain, loss, and distribution.
3. Holding periods and clocks. Long-term date, QSBS three-, four-, and
   five-year marks (post-July 4, 2025 stock) or the five-year mark
   (earlier stock), lock-up date, year-end mark to market for 1256.
4. Traps. Wash sales across stock and options, straddles and constructive
   sales on hedged positions, AMT on ISO exercise, withholding shortfall
   on RSU vesting, return of capital driving basis to zero, state
   conformity (California does not follow QSBS).
5. Elections and structures. Section 475, 83(b), Section 1045 rollover,
   10b5-1 plan, gifting or trust planning for QSBS stacking, entity
   choice for a trading business.
6. Placement. Which account, which tax year, which lots. Compare the
   after-tax result of the recommended action against the next-best
   alternative.
7. Hand-off line. Every recommendation from lenses one through five ends
   with one or two sentences from that lens's tax expert stating the
   after-tax character and the single most important tax action. When two
   lenses apply, each tax expert answers for their own leg and Kitces
   resolves account and year placement. If no CPA has reviewed it, say so.

## Current snapshot (as of 2026-09-05)

- One Big Beautiful Bill Act (signed July 4, 2025). For QSBS issued after
  that date: tiered exclusion of 50 percent at three years, 75 percent at
  four, 100 percent at five; per-issuer cap raised to the greater of $15M
  (indexed from 2027) or ten times basis; gross-asset test raised to $75M.
  Stock issued on or before July 4, 2025 stays under the old rules ($10M
  cap, $50M test, five years or nothing). The two tranches must be tracked
  separately. Green's 2026 guide and Kitces's 2026 Tax Intensive CE Day
  are both built around OBBBA changes.
- Section 475 for 2026 had to be elected by April 15, 2026 for individuals
  and March 15, 2026 for existing entities. A new entity can elect within
  75 days of formation. Excess business loss thresholds for 2026 are
  $256,000 single and $512,000 joint, lower than 2025.
- Section 1256 blended top rate remains 26.8 percent against a 37 percent
  top ordinary rate for 2025 and 2026.
- Derivative income character in 2026: JEPI's ELN income is ordinary
  (roughly 80 to 85 percent of distributions), which is why Morningstar
  and others treat it as a tax-advantaged-account holding. NEOS SPYI and
  QQQI use SPX and NDX index options (Section 1256) plus internal loss
  harvesting, and their distributions have been classified as return of
  capital. Calamos said on July 30, 2026 that CAIE and CAIQ distributions
  are expected to be mostly return of capital; ARKY, launched August 19,
  2026, reports on a 1099 and has no distribution history yet.
- Post-IPO planning: SpaceX is running a staggered early-release program
  inside its 180-day lock-up, so employees get several selling windows
  before the full release around mid-December 2026 (McKenna, May 21,
  2026). The full release straddles the 2026 and 2027 tax years.
  myStockOptions.com is running its IPO Readiness Summit on September 24,
  2026 covering QSBS, double-trigger RSUs, 10b5-1 plans, and lock-up
  releases.
- Fund placement: Benz's tax-efficient retirement-saver portfolios
  (September 3, 2026) and tax-efficient fund picks (June 10, 2026) are
  the current reference for which fund types belong in taxable versus
  tax-advantaged accounts; ordinary-income payers such as ELN funds and
  taxable bond funds go in sheltered accounts.
- Concentrated positions: Kitces (June 17, 2026) covered tax-aware
  long-short as a way to generate offsetting losses against founder and
  IPO stock gains; AQR reports about $70B in such strategies. It requires
  margin, carries costs, and is not passive.

Refresh this section whenever a trade or position is being worked. If the
newest source found is older than about 90 days, say so in the analysis.

## Sources

- https://greentradertax.com/shop-guides/greens-trader-tax-guide (Green's 2026 Trader Tax Guide)
- https://greentradertax.com/tax-treatment-for-trading-options-in-2026-rules-pitfalls-and-planning-strategies/
- https://greentradertax.com/trader-tax-center/tax-treatment/options/
- https://greentradertax.com/category/tax-compliance/ (posts of January 29 and August 17, 2026)
- https://greentradertax.com/services/trader-tax-status/
- https://www.thetaxadviser.com/issues/2025/nov/qsbs-gets-a-makeover-what-tax-pros-need-to-know-about-sec-1202s-new-look (November 30, 2025)
- https://www.mclane.com/insights/obbba-changes-to-the-qsbs-regime-under-section-1202-a-comprehensive-overview (February 17, 2026)
- https://kbfinancialadvisors.com/does-qsbs-apply-to-pre-ipo-shares/ (April 30, 2026)
- https://prunderground.com/mystockoptions-com-ipo-summit-for-advisors-offers-financial-planning-expertise-a/cmthrdkif000904kzbw6e7twk (September 1, 2026)
- http://mystockoptions.com/aboutus
- https://www.kitces.com/blog/tax-aware-long-short-investing-tax-overlay-risk-managed-active-investment-strategy-tals-harvesting-value/ (June 17, 2026)
- https://www.kitces.com/blog/harvesting-losses-or-harvesting-gains-planning-around-four-long-term-capital-gains-tax-rates/ (June 2, 2025)
- https://www.kitces.com/kitces-iar-tax-ce-day-2026/
- https://www.financial-planning.com/news/michael-kitces-managing-long-term-capital-gains-tax
- https://darrowwealthmanagement.com/blog/spacex-ipo-employee-lockup-release-dates/ (McKenna, May 21, 2026)
- https://darrowwealthmanagement.com/blog/10b5-1-trading-plans/ (McKenna, October 17, 2025)
- https://darrowwealthmanagement.com/blog/restricted-stock-units (McKenna, March 12, 2026)
- https://darrowwealthmanagement.com/stock-option-advisor (July 23, 2026)
- https://www.morningstar.com/funds/25-top-picks-tax-efficient-etfs-mutual-funds (Benz, June 10, 2026)
- https://www.morningstar.com/retirement/best-practices-tax-efficient-portfolio-management (Benz)
- http://morningstar.com/people/christine-benz (articles through September 3, 2026)
- https://legalclarity.org/is-jepi-tax-efficient-ordinary-income-tax-explained (June 8, 2026)
- https://legalclarity.org/how-neos-etfs-spyi-qqqi-and-iwmi-achieve-tax-efficiency (June 8, 2026)
- https://www.calamos.com/blogs/voices/beyond-the-coupon-how-to-evaluate-a-growing-autocallable-etf-category (July 30, 2026)
- https://neosfunds.com/spyi/ (19a-1 notices)

## Disclaimer

Green, Kitces, Brumberg, McKenna, and Benz publish education for traders,
equity holders, and advisors; McKenna also runs an advisory firm. None of
them is this reader's CPA. Tax outcomes depend on
facts, state, account type, and elections. This lens produces questions
for a qualified tax professional, not answers to act on alone.
