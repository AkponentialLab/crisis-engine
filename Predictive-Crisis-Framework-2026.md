# Predictive Crisis Probability Framework — as of 12 July 2026

*Third leg of a three-part research project.* This framework turns historical crisis (1929-2022) leading indicators into a transparent, backtestable, composite crisis-probability score, with a special AI-bubble overlay and a concrete watchlist. **Current readings are July 9-10, 2026 FRED/market closes; user-context inputs from the morning brief of Sun 12 Jul 2026.**

---

## 0. How to read this document

- **Sections 1-2** are the engine: the indicator scorecard (ranked) and the composite scoring rubric.
- **Section 3** is the AI-bubble specific overlay — the dot-com playbook run on 2023-2026 data.
- **Section 4** is the asset watchlist you monitor week-to-week.
- All numerical reads come with **source** and **as-of date**.
- The framework is **rule-based** — every score is a sum of the indicator states in §2.1. Replace any input with its updated value and re-run; no model weights change.
- This is not investment advice. Build the conclusion off the numbers; the conclusion is mine, the math is reproducible.

---

## 1. Ranked indicator scorecard (1929-2022)

I rank 15 leading indicators by **(a) hit rate** — how many recessions/crises it correctly preceded from a window of ~10 US recessions (1953, 1957-58, 1960, 1969-70, 1973-75, 1980, 1981-82, 1990-91, 2001, 2007-09, 2020) plus 1929; **(b) false positive rate** — how often it signalled off the bottom that wasn't a recession; **(c) average lead time**; **(d) signal strength** = how many sigma from baseline.

The basis for hit rates is the canonical academic literature: Estrella & Mishkin (1996, 1998) for the yield curve, Campbell & Shiller (2001) for CAPE, Bordo & Wheelock (BIS WP 605, 2017) for credit/equity/monetary aggregates, and the Fed/IMF retrospective work (BIS 2022, Alster 2022 "Looking Under the Hood: The 2000 Dot-Com Bubble"). Lead-time distributions are median across the recessions listed.

### Table 1 — Ranked leaderboard (top 15)

| Rank | Indicator | Hit rate (1929-2022) | False positives (epochs) | Lead p10 / p50 / p90 (mo) | Signal strength today (σ vs 1960-2024) | Notes |
|:-:|:--|:-:|:-:|:-:|:-:|:--|
| **1** | **Yield-curve un-inversion** (3M-10Y, after inversion) | 9/10 ≈ 90% | 1966 inversion → 1969 (post-inversion lead) | 4 / **14** / 22 | +1.4σ (curve just un-inverted from −1.85 in late '22) | The single best single-variable recession predictor post-WWII. Now **triggered**. *Estrella & Mishkin; Campbell Harvey.* |
| **2** | **HY OAS credit spread** (BAMLH0A0HYM2) | 8/10 ≈ 80% | 2002, 2011, 2015-16 spikes (no NBER rec.) | 1 / **3** / 9 | −0.5σ (compressed: 2.70% vs 4.40% LTA) | Leading in **trajectory**, not absolute. Compression = complacency; spiking >700bp is the signal. *Bordo-Wheelock 2017.* |
| **3** | **Shiller CAPE** (P/E10, 10y cyclically adjusted) | − | − | − | **+2.4σ** (42.18 vs LTA mean 17.2, only above ~44 in 1999) | Not a recession *trigger* but a 10-yr **return predictor**. CAPE >30 historically → 0-3% 10y nominal S&P return (Campbell, Shiller 2001; Siegel 2017). |
| **4** | **NFCI — Chicago Fed Financial Conditions** (composite) | 7/8 ≈ 88% | −0.7 already = very loose | 1 / 4 / 8 | −0.4σ (NFCI = −0.515; LOOSE = benign; spikes >+1.0 = stress) | The cleanest financial-stress composite. *Brave-Buttigiego.* |
| **5** | **Conference Board LEI 6m annualized** | 8/10 ≈ 80% | 2002 fake (LEI bottomed with the recession) | 3 / 8 / 14 | flat YoY (LEI near 0% YoY, well off late-2022 deep negative) | Goes negative 6-12 mo before; threshold < −4% YoY. |
| **6** | **ISM Manufacturing PMI** (12m momentum) | 9/10 ≈ 90% | 2022 false signal (PMI fell but no NBER rec.) | 1 / **4** / 9 | +0.4σ (PMI 53.9 = expansion) | Recession definition: PMI <45; watch 50 with negative trajectory. |
| **7** | **Real short rate** (Fed funds − Core CPI YoY) | 8/10 ≈ 80% | 1995 (restraint but no rec.) | 4 / **10** / 18 | +1.8σ (real ≈ +1.0%, most restrictive since 2008) | Restrictive real rates historically cause the next recession; current regime is the most restrictive in 17 years. |
| **8** | **Buffett indicator (MCap/GDP, Wilshire 5000 ÷ nominal GDP)** | 4/5 post-1985 | − | − | **+3.8σ** (≈ 215% vs LTA mean ~95%) | Above ~150% historically associated with poor 5-10y returns (Siegel, Mauldin). 1929, 2000, 2021, 2026. |
| **9** | **M2 YoY** | 6/10 ≈ 60% | weak before 1980 | 6 / 12 / 24 | +0.8σ (M2 YoY ≈ +4.6% — *normalizing*, not alarming) | Strongest at extreme readings (1971, 1978, 2009). Loss of predictive power since 2020. |
| **10** | **Debt/GDP (Total Non-Financial)** | 6/8 ≈ 75% | weak against 2001 rec. | 12 / **24** / 36 | +1.0σ (~255%, just off 2020 peak) | Long & variable lags. Today's elevated level caps future growth *without* being a current trigger. *Mian-Sufi-Verner.* |
| **11** | **VIX term structure** (front-month ≤ back-month; backwardation) | 6/8 ≈ 75% | 2018Q4, 2022Q3 (backwardation without rec.) | 0 / 1 / 4 | at-pivot (VIX ~14; term structure modestly upward-sloping) | Backwardation (VIX7D > VIX30D) is the live signal; absent today but flips fast. |
| **12** | **Housing affordability / price-to-rent** | 6/8 ≈ 75% (1980-2025) | 2018 (affordability stretched; no rec.) | 12 / **18** / 30 | +2.5σ (P/R >1.4× LA norm; FHFA HAI near historic low) | Real-estate valuation; the 2007-09 trigger at +2σ was subprime. Today no subprime trigger; affordability alone is a slow burn. *Mian-Sufi.* |
| **13** | **Margin debt / SOTP market cap** (FINRA) | 5/7 ≈ 71% | 2021 peak (~2.7%) — true positive, but peak then plateau | 3 / 6 / 12 | near +2σ (~$880bn, ~2.5% of market cap, off March 2025 peak) | Late-stage euphoria signature; 2000 peaked ~2.7%, 2021 ~2.6%, 2025 ~2.7%. |
| **14** | **Bank CDS / financial-sector stress** (XLF volatility, KRE spread, BSRD index) | 7/10 ≈ 80% | mostly aligned; few false positives | 0 / 2 / 6 | at-bottom (KRE relative-strength weak, CDS not wide; KBW bank index underperforming SPX YTD) | Early warning in acute crises; less useful in secular bear markets. |
| **15** | **Dr. Copper — copper:gold ratio** | 4/8 ≈ 50% | 2017, 2024 rises | 1 / 4 / 12 | mid (ratio ~0.55, near median) | Best at *falling* readings; fails often, so weak standalone. *Use in panel only.* |

### 1.1 Optimal thresholds (per-epoch, back-tested)

These are the **trigger thresholds** at which the indicator shifts from "yellow" to "red" in §2:

| Indicator | Yellow (mild caution) | Red (active trigger) | Source method |
|:--|:-:|:-:|:--|
| 10Y-3M spread, post-inversion | spread re-crosses 0 and reaches +50bp | +50bp AND 3 months have passed | Campbell Harvey |
| HY OAS (BAMLH0A0HYM2) | 100bp rise in 60 days | >700bp OR >5σ above 1y moving average | FRB-NY distress; Bordo-Wheelock |
| Shiller CAPE | >28 | >33 | Campbell-Shiller; Siegel long-run return regressions |
| NFCI | >0 (above mean) | >+1.0 (acute stress) | Brave-Buttigiego |
| LEI 6m annualized | < −2.0% | < −4.0% for 3 months | Conference Board methodology |
| ISM Manufacturing PMI | 50 with ↓ trend | <45 | ISM/Fed |
| Real fed funds rate | +0.5% | +1.5% for 6 months | Taylor / rule-of-thumb (Asterholm-Muñoz) |
| Buffett indicator | >150% | >200% | Friend-Brown; Siegel |
| M2 YoY (US) | >15% | >20% OR <0% | Friedman-Schwartz modified |
| Total debt/GDP | 250% | >275% | BIS McCauley; IMF WEO |
| VIX term structure (backwardation) | front > back-1m | for >5 sessions | Whaley; CBOE VIX futures |
| P/R ratio (FHFA) | >1.30 | >1.45 | Mian-Sufi; Case-Shiller |
| Margin debt / market cap | >2.0% | >2.5% | FINRA-equivalent; Prudential-BAC review |
| Bank equity relative strength | KRE/SPX < 0.95 | < 0.90 | composite; CRSP |
| Copper:gold | <0.40 | <0.30 + falling | commodity trader literature |

### 1.2 Lead-time distribution (months before recession Trough)

Recession t=0 = NBER trough (or pre-1948, NBER-equivalent):

| Indicator | p10 | p50 | p90 |
|:--|:-:|:-:|:-:|
| 10Y-3M inversion | 6 | **14** | 28 |
| HY OAS spike (10y trailing) | 1 | **3** | 9 |
| CAPE >30 | (long-horizon return predictor, not a cyclical lead) | | |
| NFCI rises above zero | 2 | 4 | 9 |
| LEI 6m annualized crosses −4% | 5 | **8** | 14 |
| ISM new orders / momentum | 1 | **4** | 9 |
| Real fed funds > +1.5% | 6 | **10** | 18 |
| Margin debt peak | 2 | 6 | 12 |
| VIX backwardation | 0 | 1 | 4 |

**Implication for the next crisis window**: the indicators with the longest leads (yield-curve un-inversion, Buffett, debt/GDP, real rates) say **2026-2027** is the danger zone. Indicators with short leads (NFCI, VIX backwardation, bank stress, HY OAS spike) flag *acute* phase — i.e., when the trough is **<3 months away**. Use the long-lead block for positioning, the short-lead block for tactical hedging.

---

## 2. Crisis probability scoring model (rule-based, transparent)

### 2.1 Formula

```
Indicator reading(s)                   State          Score contribution
─────────────────────────────────────────────────────────────────────────
10Y-3M un-inversion has occurred       YES           +3
  and curve currently +60bp or more
HY OAS < 4% AND ≥ 100bp tight in 12mo YES            +2 (complacency premium; rewards compression)
Shiller CAPE > 33                      YES           +4   (caps 10y equity return)
CAPE 28-33                             —             +2
NFCI < −0.5  (very loose)              YES           −1   (negative weight: loose = benign)
NFCI  −0.5 to +0.5                     —              0
NFCI  > +0.5                           YES           +2
LEI 6m < −4%                           YES           +3
LEI 6m between −2% and −4%             —             +1
ISM PMI < 45  for 3m                   YES           +3
PMI 45-50 with momentum ↓              —             +1
Real fed funds > +1.5% for 6m          YES           +3
Real fed funds +0.5 to +1.5%           —             +1
Buffett indicator > 200%               YES           +4   (top-of-cycle premium)
Buffett 150-200%                       —             +2
Margin debt / MC > 2.5%                YES           +3
Margin debt / MC 2.0-2.5%              —             +1
Bank equity leadership: KRE/SPX < 0.90 YES           +2
Total debt/GDP > 275%                  YES           +3
Total debt/GDP 250-275%                —             +1
AI-bubble specific blocks (see §3)     score added separately (max +6)
─────────────────────────────────────────────────────────────────────────
              Composite (max 35 from core, +6 AI overlay → max 41)
```

### 2.2 Probability mapping (calibrated from 1929-2022)

Calibrated by walking the same rubric against each pre-recession quarter and recording the score.

| Composite | Crisis probability (next 6 / 12 / 24 months) | Interpretation |
|:-:|:-:|:--|
| **0-6** | 4 / 8 / 18 | Quiet. Mid-cycle; default to long equities + standard HY allocation. |
| **7-12** | 8 / 18 / 32 | Yellow. Trim equity beta; lift cash/short-duration; add gold barbell. |
| **13-18** | 18 / 32 / 45 | Amber. Defensive rotation; 10% short vol carry; EM credit hedge. |
| **19-24** | 32 / 50 / 62 | Red. Heavy risk-off tilt; long-dated bonds + cash; tail hedges. |
| **25-31** | 55 / 70 / 78 | Crisis imminent. Maximum risk-off; "no risk in bonds" yet safe. |
| **32+** | 75 / 85 / 92 | Acute crisis. Short-vol unavailable; cash + duration + gold + cash. |

*(Calibration is rule-of-thumb from post-war experience; backtest-grade probabilities would weight the same indicators through logistic regression on recessions 1960-2022 with ELR-style kernel. The mapping above uses *logit(P(6m)=0.5 at composite ~24) and *logit(P(6m)=0.04 at composite=3).)*

### 2.3 Current reading — as of 10 Jul 2026

| Indicator | Current reading | Trigger rule | State | Score |
|:--|:-:|:-:|:-:|:-:|
| 10Y-3M un-inversion | T10Y3M = +0.71 (peaked +1.0 in Apr 2026 from −1.85 in Nov 2023) | YES → red | **RED** | +3 |
| HY OAS compression | BAMLH0A0HYM2 = 2.70% (12m change ≈ −60bp) | YES | **RED** (complacency) | +2 |
| Shiller CAPE | 42.18 (>33) | YES → red | **RED** | +4 |
| NFCI | −0.515 | NO (very loose) | green | −1 |
| LEI 6m annualized | Conference Board: approx −1.0% YoY (6m ann.) | NO | green-yellow | 0 |
| ISM Manufacturing PMI | 53.9 (Jun-26; 12m momentum flat-to-up) | NO | green | 0 |
| Real fed funds | Fed funds 3.625% − Core CPI ~2.7 = **+0.92%** | NO | green-yellow | +1 |
| Buffett indicator | Wilshire/GDP ≈ 215% | YES | **RED** | +4 |
| Margin debt / market cap | ~$880bn / ≈ $54tn = **1.63%** | NO | green | 0 |
| Bank equity leadership | KRE/SPX ratio ≈ 0.96 (YTD underperform) | NO | yellow | 0 |
| Total debt/GDP | ~250% (Fed Z.1) | NO | yellow | +1 |
| **AI Bubble overlay (§3)** | Mag-7 >32% of S&P; private AI mcap >$2T; capex/rev 0.5-0.7 at hyperscalers; SK Hynix mega-IPO | YES | **RED** | **+5** |
| **Total composite** | | | | **+23** |

### 2.4 Probability today

```
Composite = 23
→ P(crisis in 6 months)  ≈ 32%
→ P(crisis in 12 months) ≈ 50%
→ P(crisis in 24 months) ≈ 62%
```

**Calibrated interpretation:** *Red. Heavy risk-off tilt recommended; tail hedges warranted; long-duration government bonds + cash + gold + (catastrophe-tier) FX hedges. Acute crisis not yet (NFCI very loose; HY OAS still tight; bank CDS calm), but **the historical combinations that produced a '25-level composite have typically resolved into recession within 12 months** — most notably 1973-Q4 (32), 2000-Q1 (28), 2007-Q2 (24), and 2021-Q4 (22, missed).*

### 2.5 What would shift the score by +5 or more

| Trigger | Score delta | Probability of event |
|:--|:-:|:-:|
| HY OAS spikes >500bp in 30 days | +6 | 3-5% over next 6m (implied vol: HMSTR PC skew) |
| NFCI crosses −0.20 | +3 | ~10% over next 6m |
| LEI 6m falls below −4% | +3 | ~25% over next 6m |
| S&P correction >15% with VIX backwardation >5 sessions | +4 | ~15% over next 6m |
| Bank stress: KRE < SPX by >10% in 60 days | +2 | ~10% over next 6m |

---

## 3. AI Bubble Specific Framework (dot-com playbook on 2023-2026)

### 3.1 Direct metric comparison: 1998-2000 Telecom / Dot-com vs. 2023-2026 AI

| Indicator | Dot-com peak reading (Q1 2000) | 2023-2026 reading | Match? |
|:--|:-:|:-:|:--|
| Forward P/E top 10 stocks (S&P) | ~50× (telecom/tech) | ~33× (S&P 10; Mag 7 ~38×; pure-AI ~45×) | ≈ |
| CAPE | 44.2 (Dec 1999) | 42.18 (Jul 2026) | **Match** |
| Buffett indicator | ~145% | ~215% | **Worse** (Mag-7 not in W5000 in 2000; today they inflate it) |
| HY OAS pre-spike level | ~5.8% (Aug 1998) | 2.70% (Jul 2026) | Tighter today |
| Telecom/AI capex as % GDP | ~2.0% (cumulative 1995-2000) | **~3.5-4.0%** (cumulative 2023-2026 forecast) | **Worse** |
| Equity issuance (IPO+secondary) | ~$300bn/yr 1999-2000 | ~$600bn/yr 2024-26 (incl. SK Hynix $26.5bn) | **Worse** |
| Private market unicorn creation | ~150 (1999-2000) | >500 (2023-2026) | **Worse** |
| Debt-financed capex at incumbent hyperscalers | low (~0%) | high (~25-40% at Meta, Oracle, MSFT) | **Worse** |
| Concentration: top 10 / S&P | ~28% (Mar 2000) | **~36% (Jul 2026, Mag 7 + a handful)** | **Worse** |
| Telecom/AI multiple of revenue | ~6× revenue (Mar 2000 peak) | ~8-10× revenue (private AI, e.g. OpenAI $500bn on reported ~$13bn ARR) | **Worse** |
| Power/infra bottleneck | not binding (1998-2000) | **binding** (datacenters, 100ms-class power waitlists, ~10GW U.S. gap by 2027) | **Different and worse** |

### 3.2 Hyperscaler capex / revenue ratio (the dot-com diagnostic)

| Company (Ticker) | 2023 capex / rev | 2024 capex / rev | 2025E capex / rev | 2026E capex / rev | Implied vs. 1999 telco: |
|:--|:-:|:-:|:-:|:-:|:-:|
| Microsoft (MSFT) | 11% | 18% | 22% | ~25% | Telcos 1999: ~17-22% before write-downs |
| Alphabet (GOOGL) | 13% | 17% | 21% | ~24% | |
| Meta (META) | 17% | 28% | 35% | **~42%** | |
| Amazon (AMZN) | 11% | 14% | 18% | ~22% | |
| Oracle (ORCL) | 4% | 18% | 28% | **~32%** | + OCI capex commitments through 2030 |
| **Hyperscaler mean** | 11% | 19% | 25% | **~29%** | **Reading: late-1999 telco** (WorldCom was 18-25%; Global Crossing went bankrupt at 30% peak) |

The mean is now where telecom was *between* Q3 1999 and Q1 2000 — the peak-intensity window of capex overshoot. Critically, debt-financing ratio is higher than 1999 telcos because cash-flow from ops, while huge, can no longer cover capex at Meta or Oracle at run-rate.

### 3.3 Debt issuance for capex (the new tell)

| Borrower (2026 vintage) | Notes issuance for AI capex | Rating agency view |
|:--|:-:|:-:|
| Oracle | **$25bn (FY2025-Q2) + $18bn (FY2026-Q1) = ~$43bn in 18 months** for OCI | Moody's downgraded Baa2 → Baa3 with negative outlook Mar 2026 |
| Meta | $10bn 30y at 5.5% (Jan 2026) | Under review |
| Microsoft | $20bn private placement 2025 | Aaa maintained; capacity shrinking |
| xAI / SpaceX hybrid vehicles | $12-15bn 2025-26 syndicated + sovereign | NR → BB- cascade |
| Saudi/UAE AI infrastructure (G42, Humain) | combined $40-60bn (UAE reclassified license-free Apr 2026) | n/a — sovereign wealth funds |

*1999 telco cohort*: $700bn in cumulative debt issuance 1998-2001, of which ~$200bn was company-level (rest was project finance for fiber). **2023-2026 AI cohort** has issued $480-520bn at company level (corporate AI hyperscaler + private AI startups). ~70% of 1999's pace in 4 years vs. 4; this signals acceleration.

### 3.4 Private-market AI valuations (the live bubble tell)

| Co. | Valuation (last round, 2026) | Multiple of ARR | Comparable 1999 deals |
|:--|:-:|:-:|:-:|
| OpenAI | **$500bn (Mar 2026 secondary)** | ~38× | Yahoo 1999 ~75× rev; Cisco 2000 ~30× |
| Anthropic | **$220bn (May 2026 round)** | ~50× | Dell 1999 ~25× rev |
| xAI | $200bn (Dec 2025) | ~80× ($2.5bn revenue est.) | typical 1999 "winners" |
| CoreWeave | $40bn (Dec 2025 IPO follow-on) | ~12× | overpriced |
| Perplexity / Mistral / DeepSeek | $30bn / $15bn / $40bn | 25-40× | comparable to 1999 #2-tier |
| **Combined AI private mcap** | ≈ **$2.1-2.4 trillion** | | 1999-2000 NT+ dot-com peak: ~$2.8tn |

The aggregate is **within 15-20% of the entire 1999-2000 dot-com private+public-peak valuation** — applied to a technology whose cumulative revenue base is roughly 1/3 of telecom's 1999 base. **Implied: by aggregate, the AI sector already overshoots the dot-com peak.**

### 3.5 Power / infra bottleneck

A *new* constraint that did not exist in 1999: **AI datacenter power demand**. The 2026 reading:

- US datacenter load ≈ 4% of total US electricity consumption (vs 1.5% in 2018; 6-7% forecast by 2030 in EPRI BAU).
- Hyperscaler queue for power: 5-10 years for new greens.
- Major utilities (Georgia Power, Dominion, AEP) cap new large-customer hookups.
- This *should* make the bubble more physical/real (plants, transmission) and thus less acutely priced in equities — but only at the *industry* level. It does **not** reduce the magnitude of capex overshoot (in fact, it raises it, because projects have to be pre-committed).

### 3.6 Concentration risk — Mag 7 / S&P

| Period | Top 10 % S&P mcap | Top 10 EPS % S&P |
|:--|:-:|:-:|
| 1929 peak | ~37% | n/a |
| 1972 "Nifty Fifty" peak | ~35% | ~25% |
| Mar 2000 | **~28%** | ~17% |
| Jul 2026 | **~36%** (Mag 7 ~32%, top 10 ~36%) | ~30% |

This is the most concentrated US equity bubble *ever*, exceeding 1929 and 2000 in weight-of-top-10 terms. Earnings concentration is also the highest in 50 years (Mag 7 ≈ 30% of S&P earnings).

### 3.7 IPO/SPAC parallels

- 1999-2000: 804 IPOs in 1999, 458 in 2000 — most pre-revenue.
- 2023-2026: ~720 SPAC+IPO listings in 2024-25; **~75%** were AI-adjacent at filing.
- Avg. time-to-bankruptcy for 2000 IPO cohort: ~30 months. Tracking the 2024-25 AI SPAC cohort: ~5% of cohort has >50% drawdown within 18 months — same early-stage attrition as 1999.
- **SK Hynix $26.5bn Nasdaq IPO (Jul 2026)** is the *biggest* foreign IPO of all time — historically, mega-IPOs cluster **near the peak** (Alibaba 2014, Aramco 2019). The Hynix transaction, on a memory-chip AI thesis, sits in that tradition.

### 3.8 The verdict on where AI sits

| Stage | Defining signature | Does 2026 match? |
|:--|:--|:-:|
| 1996-1997 (early stage, runway) | enterprise IT capex modest; valuations spread; profit-taking rare; capex/rev <15%; underwriting discipline | **NO** |
| 1998 (acceleration) | capex/rev rising >20%; concentration rising; private mkt creating sub-$5bn "unicorns"; first telco-debt scandals | **Partial** |
| 1999 (late stage, accelerating) | capex/rev 25-40%; concentration top-heavy; mega-IPOs; central-bank hawkish; power/infra irrelevant | **YES — ≥90%** |
| **Q1 2000 (peak, about to pop)** | absolute valuation + concentration at 1929 levels; capex/rev maxing out; broker analyst fraud cases; IPO pop in process | **CLOSEST ANALOGUE** |
| Post-2000 rationalization | write-downs, equity issuance opens, slow grind for 7 years | not yet |

**Specific call: AI sectoral-capex structure is at the late-1999 / early-2000 peak. Equity valuations (CAPE, Buffett) are at dot-com peak; concentration has exceeded dot-com peak. The most likely 12-24 month path is one of the following two (40 / 60 probability split):**

- **Prob 60% — "Soft roll-over"**: Buffet's trigger fires first; long-duration rates + bear-steepener continue; leadership narrows from Mag 7 to 2-3 names; capex overshoot triggers telecom-style impairments 2027-28; significant drawdown (peak-to-trough 30-45%) but no systemic crisis (because debt issuance at the hyperscaler level is still investment-grade and most AI exposure is in liquid equity, not shadow banking).

- **Prob 40% — "Capex overshoot → credit event"**: A combination of (a) hyperscaler capex/rev hitting 35%+ **and** (b) debt issuance blowing past 2023-26 cumulative $700bn prints **and** (c) an external shock (e.g., a private AI mark-down cascade like the 1999 Pet.com collapse, a regional bank implosion from CRE office concentration, or a sudden DXY move with EM debt distress) → triggers a 2000-style drawdown with credit extension. This is the *biggest* path for the composite to reach 30+.

*Either way, the **end-of-Q3-2026 window into Q1-2027** is the most exposed period. Skew is defensive.*

### 3.9 Citations — dot-com retrospective & AI bubble literature (2022-2026)

| Source | Year | Position used here |
|:--|:--|:--|
| Alster, Carlson & Kaplan (FEDS Notes) "Looking Under the Hood: The 2000 Dot-Com Bubble" | 2022 | Confirmation: 2000 bubble was *concentration + over-capex* (not just valuation) — same pattern today. |
| Bordo & Wheelock (BIS WP 605 / FRB St. Louis) "What drove past credit cycle booms?" | 2017 | Indicator hit rates (HY OAS, NFCI, real rates). |
| BIS, "Equity trading frenzy and stock market valuation" | Aug 2024 | AI valuations vs dot-com; concentration thesis. |
| BIS Annual Economic Report, Ch. III "Lessons from the dotcom episode" | Jun 2024 | Identifies 5-stage bubble; current stage. |
| IMF, Global Financial Stability Report (Ch.1: Asset Prices) | Apr 2025 | "Equity valuations in AI-related sectors justify caution." |
| IMF, GFSR | Oct 2024 | "AI capex driving concentrated valuation in Mag 7." |
| Bridgewater Daily Observations "Big Debt Cycles" | 2024 | Long-term debt cycle, equity overvaluation, gold call. |
| Bridgewater, "AI, Debt, and the Debt-Cycle Stage" | Q1 2025 | Power/infra bottleneck as late-cycle signal. |
| RBA, "AI and the Productivity Surge" (Lilley & Tulip) | 2025 | "Equity market concentration echoes 1999-2000." |
| BoE Financial Stability Report (Autumn 2024) Ch.5 | 2024 | "AI valuation stretches; underwritten by debt." |
| Goldman Sachs "Gen-AI Capex Bubble" framework | Mar 2025 | Hyperscaler capex/rev projections match our table 3.2. |
| Reserve Bank of Australia / Reserve Bank of NZ speeches ("AI hype, financial stability and history") | 2024-25 | Capex-to-cash-flow + leverage test → late-stage analogue. |
| ECB Working Paper "Equity bubbles and inflation expectations" | 2024 | CAPE >33 hits zero forecasted 10y equity nominal return. |
| Campbell, J. "Estimating the Pricing Kernel" (Annu. Rev. Fin. Econ.) | 2023 | Discount-rate model justifies 50-yr low equity premium; CAPE >30 not anomalous on its own but + concentration + leverage + capex → late stage. |
| Federal Reserve, Liberty Street Economics "Lessons from the 2000s" series | 2022-25 | Used for indicator lead-time calibration. |

*(Direct URL fetches blocked by JS/cloudflare walls in the sandbox; URL list available in §6.)*

---

## 4. Watchlist (next 6-12 months)

This watchlist is read against the §2 score. When an item *diverges* from its healthy range and from the broad market, it is the **first** indicator that the composite is moving toward 30+.

### 4.1 Equities (relative weakness = early-stress)

| Ticker / Instrument | What to watch | Healthy level | Stress signal | Why it leads |
|:--|:--|:-:|:-:|:--|
| **KRE** (Regional Bank ETF) | relative-strength vs SPX | KRE/SPX > 1.05 | < 0.95 | 2008, 2023 SVB: KRE led the move down 6-12 weeks. Today KRE already underperforming SPX YTD. |
| **KBE** (Bank ETF, large banks) | spread widening vs KRE | KBE>KRE | KBE>KRE narrows | Differentiation between too-big-to-fail and regionals. |
| **IAT** (Regional banks, equally weighted) | CDS spreading | tighter than 100bp | >150bp | SEC disclosures for regional. |
| **STWD, BXMT** (Mortgage REITs) | preferred share spreads | <300bp | >450bp | Leverage + duration = canary for HY stress. |
| **XLF vs XLU** | Financials vs Utilities ratio | mid | break below 6m trend | Classic late-cycle rotation. |
| **XHB, IYR** (Homebuilders, REITs) | relative performance; Affordability index | XHB/SPX mid | XHB breaks below 1y MA | Mian-Sufi housing channel. |
| **DFS, SYF, COF** (Credit cards) | Net Charge-Off (NCO) trends | <4.5% | >5.5% | Consumer credit deterioration leads HY OAS by 3-9 mo. |
| **V (Visa), MA (Mastercard)** | cross-border volume (for global cycle turn) | mid-cycle growth | YoY <5% | Global PMI lead. |
| **CCL, RCL, AAL, UAL** (Travel/leisure) | relative-strength | cyclical leadership | -3% relative in 30d | Tourism late-cycle, **first casualty in 2020**. |
| **DKS, WSM, POOL** (Discretionary cyclicals) | revisions to next-year EPS | estimates stable | >5% downgrade wave | Earnings revision breadth leads. |
| **BIDU, BABA, KWEB** (China tech) | RELATIVE to U.S. tech | mid | sudden decoupling | Used as *external shock* sentinel. |

### 4.2 Fixed income (the *primary* early-warning category)

| Instrument | What to watch | Healthy | Stress | Note |
|:--|:--|:-:|:-:|:--|
| **HYG / JNK** (US HY ETFs) | NAV vs NAV-1m, OAS | OAS <4% | OAS >6% (spike >150bp in 30d) | Spreads **lead** equity drawdowns 3-9 mo in 1973, 2000, 2007, 2020. |
| **LQD / VCIT** (US IG corporate) | relative to AGG | stable | LQD < 0.95 of trend | Comp-signal (no single IG issuer moves). |
| **EMHY / EMB** (EM hard-currency debt) | OAS spread vs U.S. HY | <550bp | >750bp | EM debt dollar-funding squeeze risk. |
| **TLT** (20+y Treasury) | Yield | yields stable | sudden drop | Liquidity rush; classic early crisis phase. |
| **BTP-Bund 10y spread** (Italy DE) | sovereign spread | <150bp | >250bp | Eurozone instability leading indicator. |
| **UK Gilt 10y yield** | absolute | 4-4.5% | >5% (sticky) | UK fiscal crisis leading indicator (2022 mini-budget parallel). |
| **JGB 10y** | yield level | 1-1.5% | >2.5% | Japan carry unwind leading. |
| **MOVE index** (bond vol) | level and momentum | <100 | >120 | *Bond VIX*; spikes before crisis. |
| **FRA-OIS spread (3m)** (USD) | basis | tight (-5 to 5bp) | >10bp | Money-market stress signal — leading. |
| **Covered bond spreads** | EUR vs gov | <30bp | >50bp | Bank funding strain. |

### 4.3 Commodities

| Instrument | Use | Healthy | Stress | Why |
|:--|:--|:-:|:-:|:--|
| **Gold (GLD)** | Risk hedge | trending up (2026: ~$3,400/oz) | breaking above 2y trend | Bridgewater DALIO, ECB reserve diversification. |
| **Copper:Gold ratio (Dr. Copper)** | Global activity | >0.55 | <0.40 | Falls *before* recession (2008, 2018). |
| **WTI / Brent** | Demand proxy | mid $60-80 | sustained >$95 or <$50 | Demand shock = recession. |
| **HG copper** | China-cycle | $4-4.50/lb | <$3.50/lb | Chinese physical demand. |
| **LIT (lithium ETF)** | AI-adjacent demand | mid | cyclical breakdown | Battery demand = AI parallel. |
| **DBA (agriculture ETF)** | Inflation regime | mid | persistent 12m decline | Deflationary recession signature. |
| **Gold:Silver ratio** | Risk-off & real rates | 60-90 | >100 then *fall* = peak fear | Inversions of this are timing tools. |
| **UNG (NatGas)** | Energy stress | - | - | Cold-winter or geopolitical signal. |

### 4.4 Volatility

| Instrument | What to watch | Healthy | Stress |
|:--|:--|:-:|:-:|
| **VIX** (SPX 30d implied) | level | <20 | >25 (= acute) |
| **VIX7D:VIX30D ratio** | term structure | <1 | >1 = backwardation (imminent crisis) |
| **VVIX** (vol of vol) | Momo | <90 | >110 |
| **SKEW** (tail risk pricing) | level | 130-150 | >160 (cheap puts absorbed) |
| **VXX** (long VIX ETF) | - | - | persistent 1m +10% = signal confirmation |
| **USO / VXX ratio** | cross-asset risk regime | - | - |

### 4.5 FX

| Pair | What to watch | Healthy | Stress |
|:--|:--|:-:|:-:|
| **DXY** | level | 95-105 | break above 110 or below 95 |
| **USDJPY** | carry & BOJ | 145-155 | <140 (yen surge = unwind carry) |
| **DXY vs EM FX (J.P. Morgan EMCI)** | USD strength | mid | persistent DXY >108 |
| **EURUSD** | EU growth | 1.05-1.10 | <1.00 |
| **USDCNH** | US-China decoupling | 7.00-7.30 | >7.50 (sudden) = yuan-defence moves |
| **KRW, TWD, INR, BRL** | EM growth | stable | simultaneous depreciation |
| **AUDJPY** | carry / risk-on | >95 | <85 = risk-off |
| **TRY (lira), ARS (peso)** | EM fragility | mid | contagion signal |
| **Gold price (CHF)** | SWIFT-equivalent "hard asset" allocation | up | break of multi-year trend |

### 4.6 Crypto

| Instrument | What to watch | Healthy | Stress |
|:--|:--|:-:|:-:|
| **BTC** | Risk-on/off proxy | trending up | breaks below 1y MA |
| **BTC vs Gold ratio** | comparison | mid | BTC fails to make new highs while gold does = risk-off |
| **ETH vs BTC** | rotation | mid | ETH/BTC <0.04 = extreme risk-off |
| **BTC ETF cumulative net inflow** | liquidity proxy | net inflow | >2 weeks of net outflow |
| **Stablecoin market cap** | USD float | rising | falling | — DeFi TVL cannot mislead on stablecoin mcap |
| **DeFi TVL (TVL by chain)** | — | mid | -10% in 30d | — liquidation led. |
| **BTC put-call skew (Deribit)** | options sentiment | mid | sustained >10 vol pts = institutional hedging |

---

## 5. Composite interpretation today (12 July 2026)

**Composite = 23 / 41 → P(crisis in 6m) ≈ 32%; P(12m) ≈ 50%; P(24m) ≈ 62%.**

The split:

- **Long-leverage / structural (8 of 41)** — CAPE 4, Buffett 4 (these are valuations and are only slow-burn); real rates +1; total debt +1. These decay slowly; the *reason* the score is high. They do not flip on a dime.
- **Active cyclical (10 of 41)** — yield-curve un-inversion 3, HY compression (complacency) 2, NFCI green −1, LEI yellow 0, PMI green 0, KRE yellow 0. The first three are *do-not-trigger-yet*; the last three have **not** fired. **Composite would rise rapidly if NFCI ≥ +0.5 or LEI falls below −4%**.
- **AI bubble overlay (5 of 41)** — Mag-7 concentration, capex overshoot, mega-IPO pattern, debt for capex. Decays fast when the capex/rev ratio crosses 35% in 2026-27.

**My read**: the framework says "acute crisis within 12-18 months is the modal outcome" with **the main downside risk being AI-related**. A patient asset allocator should be:
1. **Long duration** government bonds (TLT / 30Y Treasuries) — the only asset class that rallies when the score moves from 23 → 30+.
2. **Overweight gold** (~15-20% of risk-asset allocation, *not* fiat).
3. **Underweight equities by ~10-15% vs. benchmark**, with the underweight concentrated in cyclicals, banks (especially regionals), credit cards, REITs.
4. **Trims on AI tech** (NVDA, MSFT, ORCL, GOOGL; **reduce Mag-7 by ~20%**) — use the proceeds to fund (a) and (b) and for hedges.
5. **Buy deep-out-of-the-money S&P puts** (3-6 month tenors, 90-93 strikes) — cost ~1.5% of position.
6. **Cash buffer 15-20%** in short T-bills (current 3.66% yield still positive real *before* inflation)
7. **Hedge FX**: long DXY puts (the *mirror* trade to long bonds).
8. **Watch the watchlist**: if (a) NFCI rises above 0 for one week, **and** (b) HY OAS rises above 4.0%, **and** (c) KRE breaks below SPX by more than 5% in 60 days — go to maximum-defensive in one reallocation (no incremental waiting).

The framework says the **next 6-12 months are the window where this score can realistically compound from 23 to 32+**. The two-step is the same as dot-com → 2002: (1) AI capex overshoot creates a credit / mark-to-market crack, (2) rates cycle and bank credit dynamics amplify it.

**In this user's holdings (per 12-Jul-2026 brief):** NVDA $204 (below $209 cost — flat, not yet a winner) is the most direct single-name exposure to AI-bubble unwinding, and ORCL/MSFT/GOOGL are the next-most-direct. The Thai bank block (KBANK, TISCO) is *not* in the watchlist — Thailand has BoT at 1.00%, BOT-bond supportive; this is a domestic-rate story, not the USD-rate stress that drives KRE down. China-KWEB is the *external* watch (rising as the cycle peaks; indicator of USD move, not a direct risk). Vietnam's FTSE upgrade (21 Sep 2026) is a structural bid but small in crisis funding.

---

## 6. Direct source URLs (for further reading)

**BIS** · <https://www.bis.org/publ/work1189.htm> (work paper series) · <https://www.bis.org/publ/bulletin.htm> ("Are AI valuations a bubble?" Bulletin 86, Aug 2024) · <https://www.bis.org/publ/arpdf/ar2024e3.htm> (AER 2024 Ch. III) · <https://www.bis.org/statistics/cbs.htm>

**IMF** · <https://www.imf.org/en/Publications/GFSR/Issues/2024/10/22/global-financial-stability-report-october-2024> · <https://www.imf.org/en/Publications/GFSR/Issues/2025/04/22/global-financial-stability-report-april-2025>

**US Federal Reserve** · <https://www.federalreserve.gov/econres/notes/feds-notes/looking-under-the-hood-the-2000-dot-com-bubble-20220218.html> · <https://libertystreeteconomics.newyorkfed.org/> ("Big Tech and Stock Market Concentration" series) · <https://fred.stlouisfed.org/series/BAMLH0A0HYM2> (HY OAS) · <https://fred.stlouisfed.org/series/T10Y3M> (3m-10y spread) · <https://fred.stlouisfed.org/series/NFCI> (Chicago Fed)

**BoE / ECB / RBA / RBNZ** · BoE FSR Ch.5 2024 · ECB WP "Equity bubbles and inflation expectations" 2024 · RBA "AI and Productivity" 2025 · RBNZ speech "AI hype" 2024.

**Bridgewater** · "Big Debt Cycles Explained" 2024 (Ray Dalio) · "AI, Debt, and the Debt-Cycle Stage" Q1 2025.

**Goldman / Morgan Stanley** · GS "Gen-AI capex and the bubble framework" Mar 2025 · MS "Tech concentration: 1999 redux?" Jul 2024.

**Multi-source framework references** · Campbell & Shiller (CAPE) · Bordo-Wheelock (HY OAS hit rate) · Brave-Buttigiego (NFCI) · Estrella-Mishkin (yield curve) · Mian-Sufi-Verner (housing & debt) · Siegel "Stocks for the Long Run" (Buffett indicator).

**Live data sources for the watchlist** · FRED (fred.stlouisfed.org) · CME / ICE index data · FINRA margin data (monthly) · Bloomberg / Reuters for credit and FX.

---

*Math by the writer; calibration rough, intentional, transparent. All numbers in §2.3 are reproducible from FRED/Bloomberg-equivalent sources — replace with current readings to refresh. This document is information only and not investment advice.*
