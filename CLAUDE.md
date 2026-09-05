# Project guidance for Claude

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

### Scope

This default applies to options work only. Private equity and other
investment analysis in this repo is not governed by this lens.
