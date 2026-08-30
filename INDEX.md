# Literature Scout Index

One line per dated run in `queue/`. See REJECTED.md for ideas already tested/killed — do not
re-propose those without a genuinely new angle.

- **2026-08-21** — 2 candidates: options-implied volatility skew ("smirk") as a cross-sectional
  entry signal (strong US evidence, mechanism plausible, no known India stock-level replication,
  F&O universe capped ~180 names); promoter/insider trading via SEBI PIT disclosures (direct India
  evidence, but most of the documented abnormal return sits in the pre-disclosure window — needs
  post-disclosure-only testing). Also recorded: FII/DII flow and mutual-fund flow-induced-pressure
  data investigated and not proposed (weak/artifact-contaminated evidence — see file for the
  Wardlaw 2020 critique); analyst estimate revisions investigated, no citable India-specific result
  found.
- **2026-08-23** — 1 candidate: promoter share pledging as a risk/avoid overlay (multiple
  India-specific studies converge on higher crash risk, downside risk, and earnings-quality
  deterioration for high-pledge firms; distinct data type and mechanism from the 2026-08-21
  promoter-transaction candidate; flagged as needing an explicit size/beta confound check before
  trusting it, per the profitability-factor postmortem). Also recorded as investigated-not-proposed:
  credit-risk/rating anomaly (looks like the same small-cap/illiquidity proxy that killed
  profitability), accrual anomaly (India evidence too weak per international replication study),
  earnings-call textual sentiment (no citable India-specific effect size), bulk/block deal
  disclosures (same pre-disclosure front-running flaw as last week's promoter-transaction
  candidate), BRSR/ESG disclosures (one study found a null result), and FII/DII flow +
  analyst revisions re-checked with no new result.
- **2026-08-23 (data-availability follow-up, not a new candidate)** —
  `data-sources/promoter-pledge-data-availability.md`: manual check (not the automated scout) of
  whether promoter-pledge data for the open pledging candidate above is actually obtainable.
  Screener.in ruled out (no pledge field at all). Trendlyne.com has the field, but point-in-time
  history is paywalled behind its ~Rs 2,190/yr GuruQ plan rather than free; whether that plan's
  history is deep/granular enough for a backtest has not yet been verified.
- **2026-08-30** — 2 candidates: media coverage / investor-attention ("neglected firm") effect —
  count of news/analyst attention (not sentiment tone) as a new alt-data type, replicated in the US
  (Fang & Peress 2009) and China, plausible limited-attention mechanism, but no India-specific study
  found and a real risk it's another small-cap/size proxy per this project's profitability
  postmortem; data obtainable via the free GDELT feed. IPO lock-up expiration as a short-window
  selling-pressure signal — mechanical supply-shock mechanism (not info/behavioral), replicated in
  the US, China and Malaysia, no India-specific study found, and needs care since it's a short-
  window avoid/de-risk overlay for a long-only book, not a standard entry factor. Also recorded as
  investigated-not-proposed: firm-level institutional ownership change (evidence genuinely
  contradictory — one India study claims a positive effect but is probably aggregate-level, not
  firm-level, and the best cross-country study found is null/weak), GST e-way bill data (no
  return-predictability evidence exists yet, would need a case built from scratch), and
  single-stock-futures basis/cost-of-carry (the one India study found gives same-day information
  content only, not a forward signal).
