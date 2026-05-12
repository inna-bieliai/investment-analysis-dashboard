# 📊 Investment Analysis Dashboard
## 10 Tech Companies · January 2019 – December 2025

An end-to-end data analysis project that examines 7 years of daily stock 
price data for 10 major tech companies and classifies each company by 
investor risk profile using 10 quantitative financial metrics.

🔗 **[Open Live Dashboard](https://inna-bieliai.github.io/investment-analysis-dashboard/)**

---

## 📌 Project goal

Build a data-driven classification system that helps match companies to 
investor types — Aggressive, Balanced, or Conservative — based on real 
historical data and the CAPM financial model.

---

## 🏢 Companies analyzed

| Ticker | Company | Investor type |
|--------|---------|--------------|
| NVDA | NVIDIA | Aggressive |
| AMD | Advanced Micro Devices | Aggressive |
| MU | Micron Technology | Aggressive |
| TSLA | Tesla | Aggressive |
| TSM | Taiwan Semiconductor | Balanced |
| AAPL | Apple | Balanced |
| MSFT | Microsoft | Balanced |
| AMZN | Amazon | Balanced |
| BA | Boeing | No fit |
| ADBE | Adobe | No fit |

---

## 📐 Metrics calculated

| Metric | What it means in plain language |
|--------|--------------------------------|
| **Annual Return** | How much you would have earned on average per year |
| **Volatility** | How wildly the price swings — lower = more stable |
| **Sharpe Ratio** | Return per unit of risk — higher is better |
| **Sortino Ratio** | Like Sharpe, but only penalizes for losses |
| **Max Drawdown** | The worst loss from peak to bottom during the period |
| **Beta (β)** | How sensitive the stock is to market movements |
| **Correlation** | How closely the stock follows the S&P 500 |
| **Alpha (CAPM)** | How much the stock beat market expectations |
| **P/E Ratio** | How expensive the stock is relative to earnings |
| **Dividend Yield** | Annual cash payment as % of stock price |

---

## 🔍 Key findings

- **NVDA** — highest return (+70.9%) and best Sharpe ratio (1.30)
- **TSLA** — explosive growth (+65.0%) but highest volatility (64.5%)
- **BA (Boeing)** — worst drawdown (−78.4%) with near-zero return (+5.2%)
- **BA and ADBE** — only companies with negative Alpha (underperformed expectations)
- **MSFT and AAPL** — most stable profiles, suitable for Balanced investors

---

## 🗂️ Investor classification

| Company | Conservative | Balanced | Aggressive |
|---------|:-----------:|:--------:|:----------:|
| NVDA | ❌ | ⚠️ | ✅ |
| AMD | ❌ | ⚠️ | ✅ |
| TSM | ❌ | ✅ | ✅ |
| MU | ❌ | ✅ | ✅ |
| BA | ❌ | ❌ | ❌ |
| ADBE | ❌ | ❌ | ❌ |
| AAPL | ❌ | ✅ | ✅ |
| MSFT | ✅ | ✅ | ⚠️ |
| TSLA | ❌ | ❌ | ✅ |
| AMZN | ❌ | ✅ | ⚠️ |

✅ Suitable · ⚠️ May be risky · ❌ Not suitable

---
### Why BA and ADBE don't fit any investor profile

**Boeing (BA)** and **Adobe (ADBE)** were excluded from all three investor 
categories because they failed on multiple criteria simultaneously:

| | BA (Boeing) | ADBE (Adobe) |
|-|------------|--------------|
| Annual Return | +5.2% | +12.9% |
| Max Drawdown | −78.4% | −60.0% |
| Sharpe Ratio | 0.03 | 0.26 |
| Alpha (CAPM) | −17.6% | −6.4% |
| Verdict | ❌ | ❌ |

**The problem in plain language:**

- **BA** delivered almost no return (+5.2%/year) while taking on enormous risk 
  (−78.4% max drawdown). An investor in Boeing lost more than 3/4 of their 
  investment at the worst point — and barely recovered. The Sharpe ratio of 
  0.03 means the return was essentially zero relative to risk.

- **ADBE** showed moderate return but negative Alpha — meaning it 
  underperformed what the market would predict given its risk level. 
  A passive S&P 500 index fund would have delivered better 
  risk-adjusted results.

Both companies also have negative Alpha, which means they destroyed value 
relative to market expectations — a key disqualifier in this analysis.

> A stock that fits no investor profile is not necessarily a "bad company" —
> it simply means that during this specific period (2019–2025), the 
> risk/reward ratio did not justify inclusion in any of the three profiles.

## 🛠️ Tools used

- **Google Sheets** — data collection, cleaning, metric calculations
- **Google Finance** — daily closing price data via GOOGLEFINANCE()
- **CAPM model** — Alpha and expected return calculations
- **HTML / JavaScript / Chart.js** — interactive dashboard

---

## 📊 Dashboard features

Fully interactive — filter by company, investor type, or metric:
1. Risk vs Return scatter plot (bubble size = Sharpe ratio)
2. Alpha comparison — who beat market expectations
3. Dynamic metric switcher — compare any of 9 metrics
4. Heatmap — all companies × all metrics at a glance
5. Sharpe vs Sortino comparison
6. Investor classification table

---

## 📝 Methodology note

Annual Return = arithmetic mean of daily log-returns × 252 trading days.
Standard practice in quantitative finance. Differs slightly from CAGR 
due to volatility drag, especially for high-volatility stocks (NVDA, TSLA).

---

*Project by Inna Bieliai · Data Analysis Portfolio · 2026*
