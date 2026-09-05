# Project guidance for Claude

Five domain lenses, each with its own tax expert, and one routine. Never
run on framework memory alone: every recommendation is preceded by a
retrieval step and ends with a tax hand-off line.

## Routing table

| # | Trigger | Domain experts | Tax expert | Lens file |
| --- | --- | --- | --- | --- |
| 1 | Options trade: structure, sizing, management | Tom Sosnoff / tastytrade | Robert Green (GreenTraderTax) | `lenses/sosnoff-options-lens.md` |
| 2 | Public stock: single name, sector, ETF, index direction; any stock past its first IPO anniversary | Carter Worth / Worth Charting | Michael Kitces (Nerd's Eye View) | `lenses/worth-equity-lens.md` |
| 3 | Late-stage private: Series D and later, secondaries, tender offers, pre-IPO rounds, IPO underwriting | Brad Gerstner, Gavin Baker, Cathie Wood | Bruce Brumberg (myStockOptions.com) | `lenses/late-stage-private-lens.md` |
| 4 | Post-IPO window: listing through month twelve, lock-up expiry at the center | Aswath Damodaran, Jay Ritter, Renaissance Capital | Kristin McKenna (Darrow Wealth Management) | `lenses/post-ipo-window-lens.md` |
| 5 | Derivative income: covered-call ETFs, ELN funds such as JEPI, autocallable funds such as ARKY and CAIE | Morningstar derivative-income analysts, Hamilton Reiner, Matt Kaufman | Christine Benz (Morningstar) | `lenses/derivative-income-lens.md` |

The tax framework shared by all five tax experts, including the tax map by
lens and the seven-step full analysis, is `lenses/tax-overlay-lens.md`.

## The routine

One pass per task. Do not repeat steps per lens; when two lenses apply,
run them inside the same pass.

1. **Route.** Pick the lens or lenses from the table. Read the lens file
   and the tax lens file before analyzing.
2. **Retrieve once.** Make one Parallel Search call
   (`mcp__Parallel_Search__web_search`) with four to six queries: two or
   three from the domain row and one or two from the tax row of the query
   table below. Add a second call only if the first returns nothing newer
   than about 90 days or the trade raises a question the first did not
   cover. Prefer primary sources (the expert's own publication, the fund's
   own documents, the filing, the IRS form). Third-party summaries are
   corroboration only.
3. **Date-check.** Note the newest publish date found. If it is older than
   about 90 days, say so and fall back to the lens file. Tax rules move by
   year: if the newest tax source is from a prior tax year, flag it.
4. **Analyze** in the order given by the lens file's "How to run" section.
   State the mechanical rule first, then any current commentary that
   adjusts it, each with source and date.
5. **Deliver.** Lead with the lens read. Flag any violation of a core
   mechanic plainly; do not rationalize it. Other lenses and fundamentals
   go in a secondary section, never as the default. End with the tax
   hand-off: one or two sentences giving the tax character of the expected
   result and the single most important tax action or election. If the tax
   answer changes the recommendation, put the tax reason first. If no CPA
   has reviewed the position, say so.
6. **Label.** Cite what was used. Mark each claim as framework rule, base
   rate, current commentary, issuer claim, or statute and IRS guidance.
   State position bias: fund managers and issuers describe their own
   products; academics and Morningstar analysts hold no positions.

## Query table

Replace angle-bracket terms. Use the current month and year.

| # | Domain queries | Tax queries |
| --- | --- | --- |
| 1 | `Tom Sosnoff <underlying or theme> <month year>`; `tastylive market measures <topic>`; `tastytrade <strategy> <year>` | `GreenTraderTax <Section 1256 / wash sale options / Section 475 / straddle> <year>` |
| 2 | `Carter Worth <ticker or sector> <month year>`; `Worth Charting <150-day / breakout / relative strength>`; `Carter Worth CNBC Fast Money <month year>` | `Kitces <harvesting gains / tax-loss harvesting / asset location / net investment income tax>` |
| 3 | `Brad Gerstner <company or theme> <month year>`; `BG2 pod <topic>`; `Gavin Baker Atreides <company> <month year>`; `Cathie Wood ARK Venture <company> <month year>` | `myStockOptions <QSBS / 83(b) / ISO AMT / tender offer> <year>`; `QSBS Section 1202 <year>` |
| 4 | `Damodaran <company> valuation <year>`; `Ritter IPO long-run returns <year>`; `<company> lock-up expiration date shares`; `Renaissance IPO ETF holdings <month year>` | `Kristin McKenna <company> lockup <year>`; `Darrow Wealth <10b5-1 / RSU / concentrated stock> <year>` |
| 5 | `Morningstar <ticker> analysis <year>`; `JEPI fact sheet <month year>`; `Calamos CAIE autocallable dashboard`; `<ticker> holdings <month year>` | `Christine Benz tax-efficient <fund type> <year>`; `<ticker> 19a notice return of capital`; `<ticker> Form 8937` |

## Pairings and handoffs

- **Stock view expressed through options:** Worth for direction and timing,
  Sosnoff for structure and mechanics. Tax: Green for the option leg,
  Kitces for the stock leg.
- **Derivative-income product on a name or index:** Worth says when to
  commit or trim; the derivative-income lens says whether the product pays
  enough for the risk it sells; Sosnoff when the analysis reaches the
  option mechanics inside the product. Tax: Benz for placement and
  character, Green if the fund passes through Section 1256 or straddle
  issues.
- **Lifecycle of a company going public:** lens 3 through pricing and the
  first day of trading; lens 4 from listing through month twelve, and the
  sole default until about month seven because the Worth lens's 150-day
  moving average does not exist yet; lens 2 joins once roughly 150 trading
  days exist and is the sole default after the first anniversary. Tax:
  Brumberg through the IPO, McKenna through the lock-up and first year,
  Kitces after that.
- **Two tax experts in one task:** each answers for their own leg. Kitces
  resolves account placement and year placement across legs.

## Hard rules

- Never quote a distribution rate as yield or return. Return of capital is
  deferred tax, not no tax.
- Never state a QSBS exclusion without the issuance date and which regime
  applies (on or before July 4, 2025, or after).
- Never carry a private mark or an IPO narrative that the public numbers no
  longer support without saying so.
- Never present a recommendation that violates a lens's core mechanic
  (low IV rank, buying far above the 150-day, unproven barrier management,
  oversized position) as if the mechanic did not exist.
- The tax hand-off produces questions for a CPA, not tax advice.

## Scope

These defaults apply to public stock trading, options trading, late-stage
private or pre-IPO work, the first year of post-IPO trading, and packaged
derivative-income products. Buyout-style private equity, early-stage
venture (seed through Series C), dividend-stock investing, and other
investment analysis in this repo are not governed by these lenses.
