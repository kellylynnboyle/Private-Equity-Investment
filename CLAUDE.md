# Boyle Family Office — Private-Equity-Investment repo

This repository is internal due-diligence and competitive-monitoring research
maintained for **Boyle Family Office** (principal: Kelly Lynn Boyle). It keeps
independent, source-cited research current on AG Dillon & Co.'s Pre-IPO Stock
offerings (SMA and Bi-Annual Fund structures) and the competitive landscape
for RIA-distributed pre-IPO / late-stage private-equity access.

## Scope & house rules

- **Research and monitoring only.** Nothing here is or should be written as an
  investment recommendation. Automated updates must not add recommendation
  language — that judgment call stays with Kelly.
- Flag non-neutral sources inline (a firm's own fact sheet, marketing site, or
  press release) and never present that material as independent data.
- Every file under `research/`, `offerings/`, and `reports/` opens with the
  header in **File header convention** below.
- Treat existing baseline research as authoritative until something has
  actually changed. Before starting new research: `git fetch origin --prune`,
  check `main` and open PRs for existing work, and search Open Brain (topics
  `private-equity-investment`, `routine-optimization`, `pre-ipo-markets`) for
  guidance left by earlier runs. Don't re-derive or duplicate work a prior run
  already did — append a dated "Update — YYYY-MM-DD" section instead of
  rewriting a file wholesale, so the history of what changed when is
  preserved.
- If a change needs to land and a PR for this work is already open, push to
  that PR's branch rather than opening a new one. This repo previously
  accumulated several duplicate branches doing the same research in parallel
  because each session started blind — avoid repeating that.

## Repo structure

- `research/agdillon-competitive-landscape.md` — AG Dillon positioning
  (Pre-IPO Stock SMA vs. Bi-Annual Fund Offerings) and the Tier 1 / Tier 2
  competitor breakdown.
- `offerings/<firm>/current-offerings.md` — one file per tracked firm
  (AG Dillon plus competitors), with sourced pricing, AUM, holdings, and fee
  terms.
- `due-diligence/` — Boyle Family Office's own position/allocation tracking
  and firm-specific diligence notes, as distinct from the market-wide
  competitive research above. See
  `due-diligence/boyle-family-office-agdillon-position.md`.
- `reports/` — principal-facing summaries synthesized from the above.

## File header convention

Every file under `research/`, `offerings/`, and `reports/` should start with:

> **Prepared for Boyle Family Office — internal research only, not investment advice.**

## Boyle Family Office position data

`due-diligence/boyle-family-office-agdillon-position.md` tracks the family
office's *actual* AG Dillon position — separate from the market-wide
competitive research elsewhere in this repo. That file's financial fields
(amount committed, entry date, custodian, holdings) must only ever be filled
in from information Kelly provides or an actual account/custodian statement.
An automated routine must never fabricate or estimate those figures; leave
them marked `TBD` until supplied.
