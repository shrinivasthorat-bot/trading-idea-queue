# Data availability check — promoter share pledging (2026-08-23)

Follow-up to the 2026-08-23 literature-scout candidate "promoter share pledging as a
risk/avoid overlay" (see `queue/2026-08-23.md`, Candidate 1). That entry proposed the signal on
the strength of the academic evidence but only asserted, without checking, that pledge data is
"realistically obtainable." This is a manual investigation (human + assistant, not the automated
scout) into whether that's actually true — i.e. whether the specific series a backtest needs
(promoter pledge % per company per quarter, as it stood at each point in time) can actually be
gotten hold of, and at what cost.

This is a data-availability check, not a re-review of the trading signal itself. It does not
change the candidate's status in `queue/2026-08-23.md` or its evidentiary strength; it only
narrows what's known about sourcing the data.

## Confirmed by direct check

**1. Screener.in does not expose promoter pledge data at all.** Checked live on two company
pages (Vedanta / VEDL and Zee Entertainment / ZEEL). The free "Shareholding Pattern" table on
both pages shows only Promoter / FII / DII / Public percentages, with history going back to
roughly Sep 2023 (~12 quarters) — no pledge column, and no mention of the word "pledge" anywhere
on either page. Screener.in is ruled out as a source for this factor. This is consistent with
this project's earlier experience that Screener.in has shallow or no history for fields outside
its default financial statements.

**2. Trendlyne.com does have a real promoter pledge field, confirmed live and unauthenticated.**
Trendlyne's public "High promoter stock pledges" screener
(https://trendlyne.com/fundamentals/screen/15321/highest-promoter-stock-pledges/) returned
current "Promoter holding pledge percentage % Qtr" values across 586 stocks, each with a
per-stock disclosure date — e.g. Nazara Technologies at 86.97%, Arvind at 7.24%. No login was
required to view this current snapshot.

**3. But point-in-time history is paywalled, not free.** What a backtest actually needs is not
today's pledge percentage but the ability to reconstruct what the pledge percentage *was* as of
each past quarter. Trendlyne's per-symbol historical time-series pages (the "holding-overtime"
URLs) redirect unauthenticated users to a login wall. Checked
https://trendlyne.com/subscription/plans/: both the "Stock Screener Rewind" feature and the "Data
Downloader" capability for latest-plus-historical data (as opposed to latest-data-only, which is
included on the free/PRO tiers) are gated to the GuruQ plan and above. GuruQ is priced at roughly
Rs 2,190/year (~$26/year) — notably the base India-tier plan, not one of the more expensive
Global/PRO tiers.

## Net conclusion (confirmed)

This is not a dead end the way the fundamentals point-in-time backfill was. For a small annual
subscription (~Rs 2,190/yr), Trendlyne likely provides genuine point-in-time pledge history. The
free alternative is scraping NSE/BSE Regulation 31 disclosures directly — individual per-company
PDF/XBRL filings, with no bulk historical CSV found — which is materially more engineering effort,
comparable to how the `xbrl_collector` had to be built from scratch for financials data.

## Not yet done

**4. Whether GuruQ's historical export is actually good enough has not been verified.** Before
paying for GuruQ, someone needs to check inside a trial or paid account that the historical
export (a) goes back far enough — ideally 5+ years, to get enough quarterly pledge-level
formations for a Fama-MacBeth-style test — and (b) is genuinely per-stock granular, not just a
shallow-lookback version of the current screen. This has not been checked. Until it is, treat the
"Trendlyne solves this for ~$26/yr" conclusion above as *likely* rather than *confirmed* — the
subscription cost is a low bar to clear, but it hasn't been cleared yet.
