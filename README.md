# US Equity Portfolio Optimization & Risk-Adjusted Performance Analysis

A quantitative investment and risk-management study evaluating an actively managed **£10,000, 10-stock US equity portfolio** over a two-month investment horizon (September 1 – November 1, 2025). Grounded in **Modern Portfolio Theory (MPT)**, the **Capital Asset Pricing Model (CAPM)**, and **Gordon Growth Model (GGM)** valuation, this project demonstrates how combining high-beta growth equities with defensive, low-correlation holdings balances portfolio variance while capturing asymmetric upside.

> **Repository Artifacts:**
> * [`US_Equity_Portfolio_Analysis_Report.pdf`](US_Equity_Portfolio_Analysis_Report.pdf) — Full 13-page analytical report covering theoretical framework, variance-covariance risk modeling, CAPM attribution, and equity valuation.
> * [`Portfolio_Allocation_and_Trade_Ledger.xlsx`](Portfolio_Allocation_and_Trade_Ledger.xlsx) — Initial capital allocation, share quantities, and entry-price execution schedule across all 10 securities.

---

## Executive Summary & Headline Metrics

| Performance Metric | Portfolio Result | Benchmark / Reference |
| :--- | :--- | :--- |
| **Initial Capital Allocated** | £10,000.42 | Strict 25% max single-stock cap |
| **Final Portfolio Value** | £13,405.53 | Valued at October 31, 2025 close |
| **Total Realized Profit** | **+£3,405.11** | Reported in domestic currency (GBP) |
| **Portfolio Return ($E(R_p)$)** | **+34.05%** | vs. S&P 500 2-month proxy (+1.01%) |
| **CAPM Required Return** | 1.12% | $R_f = 0.79\%$, $R_m = 1.01\%$, $\beta_p = 1.50$ |
| **Jensen's Alpha ($\alpha_p$)** | **+32.93%** | Risk-adjusted excess return over CAPM |
| **Sharpe Ratio ($S$)** | **1.66** | Based on diversified volatility ($\sigma_p = 20.00\%$) |
| **Treynor Ratio ($T$)** | **0.22** | Excess return per unit of systematic risk ($\beta_p$) |

---

## Portfolio Construction & Risk Mandate
Constructed during a period of late-2025 macroeconomic transition—characterized by US Federal Reserve rate cuts (3.75%–4.00%), persistent inflation (3.0%), and global trade uncertainty—the portfolio followed a three-sleeve allocation discipline with a maximum position limit of **25% per security**:

1. **High-Beta Growth & Secular Momentum:** Targeted AI/semiconductor and clean-energy upside through **Micron Technology (MU)**, **Lithium Americas Corp. (LAC, $\beta = 3.45$)**, and **PLUG Power (PLUG)**.
2. **Core Quality & Industrial Compounders:** Anchored the portfolio with established earnings power via **Microsoft Corp. (MSFT, $\beta = 1.05$)**, **Caterpillar (CAT)**, **Uber Technologies (UBER)**, and **Quantum Corp (QMCO)**.
3. **Defensive & Low-Correlation Hedges:** Incorporated **Pfizer (PFE)**, **Duolingo (DUOL)**, and **GameStop (GME)**—utilizing low pairwise correlations (such as **GME–MSFT at 0.05**) to dampen systemic downside exposure.

---

## Trade Execution & Performance Attribution (Sep 1 – Nov 1, 2025)

| Company | Ticker | Shares | Entry Price (£) | Exit Price (£) | Initial Allocation (£) | Weight ($w_i$) | Final Value (£) | Profit / Loss (£) | Return ($R_i$) |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Micron Technology** | `MU` | 12 | £88.10 | £170.11 | £1,057.20 | 10.57% | £2,041.32 | +£984.12 | **+93.09%** |
| **Lithium Americas** | `LAC` | 420 | £2.21 | £4.18 | £928.20 | 9.28% | £1,755.60 | +£827.40 | **+89.14%** |
| **PLUG Power** | `PLUG` | 800 | £1.16 | £2.04 | £928.00 | 9.28% | £1,632.00 | +£704.00 | **+75.86%** |
| **Caterpillar** | `CAT` | 3 | £310.08 | £438.84 | £930.24 | 9.30% | £1,316.52 | +£386.28 | **+41.52%** |
| **Quantum Corp** | `QMCO` | 250 | £5.50 | £7.18 | £1,375.00 | 13.75% | £1,795.00 | +£420.00 | **+30.55%** |
| **Uber Technologies** | `UBER` | 8 | £69.38 | £73.36 | £555.04 | 5.55% | £586.88 | +£31.84 | **+5.74%** |
| **Microsoft Corp.** | `MSFT` | 3 | £375.00 | £393.65 | £1,125.00 | 11.25% | £1,180.95 | +£55.95 | **+4.97%** |
| **Pfizer** | `PFE` | 49 | £18.22 | £18.74 | £892.78 | 8.93% | £918.26 | +£25.48 | **+2.85%** |
| **GameStop** | `GME` | 80 | £16.58 | £16.95 | £1,326.40 | 13.26% | £1,356.00 | +£29.60 | **+2.23%** |
| **Duolingo** | `DUOL` | 4 | £220.64 | £205.75 | £882.56 | 8.82% | £823.00 | -£59.56 | **-6.75%** |
| **Total Portfolio** | — | — | — | — | **£10,000.42** | **100.00%** | **£13,405.53** | **+£3,405.11** | **+34.05%** |


---

## Quantitative Methodology

1. **Mean-Variance Portfolio Optimization:**
   Evaluated total portfolio risk across all 100 variance-covariance pairs ($\sigma_p^2 = \sum_{i=1}^{10} \sum_{j=1}^{10} w_i w_j \sigma_i \sigma_j \rho_{ij}$), confirming that pairing high-volatility holdings ($\sigma_{\text{LAC}} = 0.0620$, $\sigma_{\text{PLUG}} = 0.0550$) with low-volatility stocks ($\sigma_{\text{MSFT}} = 0.0150$, $\sigma_{\text{PFE}} = 0.0180$) contained diversified portfolio volatility at $\sigma_p = 20.00\%$.
2. **CAPM & Risk-Adjusted Performance Attribution:**
   Evaluated realized return ($R_p = 34.05\%$) against the Capital Allocation Line (CAL) and two-month market proxies ($R_f = 0.79\%$ T-Bill proxy; $R_m = 1.01\%$ S&P 500 proxy) using **Jensen's Alpha**, the **Sharpe Ratio**, and the **Treynor Ratio**.
3. **Relative & Intrinsic Equity Valuation:**
   * **Relative Valuation:** Contrasted Microsoft's large-cap earnings stability ($P/E = 35\times$, $\beta = 1.05$) with Lithium Americas' high-beta growth profile ($P/E = 55\times$, $\beta = 3.45$).
   * **Gordon Growth Model (GGM):** Tested dividend-discount valuation ($P_0 = D_1 / (r - g)$) on MSFT using an annualized CAPM cost of equity ($r = 9\%$, $g = 6\%$), illustrating why dividend-based models systematically undervalue reinvestment-driven AI/tech compounders.

---

## Key Conclusions & Strategic Recommendations
* **Concentrated Alpha with Broad Hit Rate:** Nine of the ten positions closed in positive territory; three high-conviction growth holdings (`MU`, `LAC`, `PLUG`) generated **73.8%** of total profit (+£2,515.52), while position sizing limited the sole loss (`DUOL`) to -0.60% of initial capital.
* **Post-Rally Risk Rebalancing:** Following substantial two-month appreciation in `LAC` (+89.14%) and `PLUG` (+75.86%), partial profit-taking is recommended to lock in alpha and prevent high-beta concentration drift.
* **Defensive Core Retention:** Maintain core exposure to cash-generative quality equities (`MSFT`, `MU`) alongside low-correlation hedges (`GME`, `QMCO`) to protect capital against interest-rate and trade-policy volatility.

---

## Repository Contents

| File | Description |
| :--- | :--- |
| `README.md` | Project overview, trade execution ledger, quantitative methodology, and findings |
| `Portfolio_Allocation_and_Trade_Ledger.xlsx` | Initial share counts, entry prices, and GBP capital allocation spreadsheet |
| `US_Equity_Portfolio_Analysis_Report.pdf` | Full analytical report with mathematical proofs, CAPM metrics, and references |

## Tools & Frameworks
Microsoft Excel, Modern Portfolio Theory (MPT), CAPM, Gordon Growth Model (GGM), Quantitative Risk & Performance Attribution.
