# Crisis Probability Engine

A 100-year leading-indicator framework for predicting financial crises, built around a single self-contained HTML dashboard with live data feeds and a companion portfolio action plan.

## Files

| File | What it is |
|---|---|
| **`crisis-engine.html`** | Single-file interactive dashboard. Open in any browser — no server, no build step. Loads Chart.js from CDN, fetches live data from FRED and CoinGecko. |
| **`Portfolio-Action-Plan.md`** | Position-level action plan based on the current composite score of 23/41. |
| **`Predictive-Crisis-Framework-2026.md`** | The full framework document — scoring formula, probability calibration, AI-bubble overlay. |
| **`Synthesis-100-Years-Financial-Crises.md`** | 100-year synthesis across 16 major crises (1929–2025). |
| **`Historical-Crises-Reference-1925-2025.md`** | Hard-number reference table for each historical crisis. |
| **`2026-07-12-ai-crisis-prediction-model.html`** | Earlier dashboard prototype (kept for reference). |
| **`2026-07-12-crisis-indicators-research.md`** | Indicator research notes. |

## Quick start

```bash
# Just open the dashboard in your browser
open crisis-engine.html
```

Then click **⟳ Refresh Live Data** to pull real-time readings from FRED (yield curve, HY OAS, NFCI, fed funds, CPI, etc.) and CoinGecko (BTC, ETH).

## What the dashboard does

### 📊 Live Dashboard tab
- Composite score (0–41) with probability gauge
- P(crisis) for 6, 12, and 24 months — historically calibrated
- **All 11 core indicators + 3 AI-overlay indicators are editable** — override any cell to stress-test scenarios, the score recalculates instantly
- Score trend (persists in browser localStorage)
- Live macro panel (Fed funds, real fed funds, CPI, ISM, 10Y, 2Y)
- Trigger list: "what would push score to 30+"

### 🧪 Backtest tab
- Hit rate, false positive rate, Brier score, AUC across 18 historical crises
- Calibration scatter (predicted vs actual)
- Per-crisis detail with hit/miss classification
- Indicator reliability table

### 👁 Ticker Watchlist tab
- Equity stress signals (regional banks, credit cards, REITs, China tech, travel)
- Fixed income (HY, IG, EM, long-duration, MOVE, FRA-OIS)
- Volatility (VIX, VIX term structure, VVIX, SKEW)
- FX (DXY, USDJPY, EURUSD, USDCNH, AUDJPY)
- Live crypto (BTC, ETH) and commodities

### 📐 Methodology tab
- Full scoring formula (transparent, rule-based)
- Probability mapping table
- Citations (~40 academic / central-bank sources)
- Limitations

## Scoring formula (summary)

| Category | Max points |
|---|:-:|
| Yield curve | 3 |
| HY OAS complacency | 2 |
| Shiller CAPE | 4 |
| NFCI | 2 |
| LEI | 3 |
| ISM PMI | 3 |
| Real fed funds | 3 |
| Buffett indicator | 4 |
| Margin debt / MC | 3 |
| Bank stress | 2 |
| Debt/GDP | 3 |
| **Core total** | **35** |
| Mag-7 concentration | +2 |
| Hyperscaler capex/rev | +2 |
| AI private market cap | +2 |
| **AI overlay total** | **+6** |
| **GRAND TOTAL** | **41** |

## Calibration

| Score | P(6m) | P(12m) | P(24m) | Band |
|:-:|:-:|:-:|:-:|---|
| 0-6 | 4% | 8% | 18% | Quiet |
| 7-12 | 8% | 18% | 32% | Yellow |
| 13-18 | 18% | 32% | 45% | Amber |
| 19-24 | 32% | 50% | 62% | Red |
| 25-31 | 55% | 70% | 78% | Crisis Imminent |
| 32+ | 75% | 85% | 92% | Acute |

## Live data sources

- **FRED** (St. Louis Fed): `T10Y3M`, `BAMLH0A0HYM2`, `NFCI`, `FEDFUNDS`, `CPIAUCSL`, `MANEMP`, `DGS10`, `DGS2`, etc.
- **CoinGecko**: BTC, ETH (price + 24h change)
- CORS proxy: `api.allorigins.win`

## Limitations

- Calibration is rule-of-thumb from post-war experience, not formal logistic regression
- Indicator readings for pre-1950 crises are estimates; many modern indicators (NFCI, HY OAS) postdate them
- Model is a tool, not a forecast — markets can remain irrational longer than analysts can remain solvent
- **Not investment advice**

## License

MIT — use freely. Citations appreciated.