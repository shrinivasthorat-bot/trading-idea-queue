# Rejected / Closed Ideas

Ideas that have been tested and killed, or deprioritized with a documented reason.
Do not re-propose these in future literature-scout runs without a genuinely new angle —
and if you think you have one, say explicitly why it differs from what's recorded here.

---

## 1. Pure price/technical entry signals
**Status:** DEAD. Closed door — do not propose new technical indicators as an entry signal.
**Finding:** Composite technical score IC ~ 0. All 11 individual indicators tested (RSI, MACD,
OBV, Bollinger Bands, EMA trend, ADX, Supertrend, volume, Stochastic RSI, candlestick patterns,
VWAP) came back null under a family-wise permutation test (p=0.330). A promising sign-consistency
pattern (3-month trend) failed out-of-sample (p=0.902).

## 2. Profitability factors (gross profitability, ROE, ROA, margins)
**Status:** REJECTED — negative result, root cause identified.
**Finding:** Tested negative on 20-year India data (Q5-Q1 ~ -16%/yr). Root cause: the factor is a
small-cap/high-beta risk premium in disguise, not real alpha — coefficients collapse once
controlled for size and beta (|t|<2), while size alone stays significant.

## 3. Residual momentum and "Trend-Clarity" indicator
**Status:** REJECTED. Tested, rejected (details not further specified in project notes).

## 4. PEAD (post-earnings-announcement drift)
**Status:** DEPRIORITIZED, not formally tested in-house.
**Finding:** Published India-relevant work (Chordia et al.) finds PEAD is approximately zero net
of costs in liquid names.

## 5. Exit/sizing logic (Chandelier trailing stop, partial take-profit, position caps)
**Status:** OUT OF SCOPE — already tuned and deployed. This is a separate workstream from
entry-signal research; the literature scout should not propose exit/sizing mechanics.

---

*(Appended by later scout runs below this line, each with date and reason.)*
