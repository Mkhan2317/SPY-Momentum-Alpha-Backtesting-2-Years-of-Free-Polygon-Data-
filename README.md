
# 📈 Intraday Momentum Strategy for S&P 500 ETF (SPY)

This repository contains a **fully implemented and backtested Jupyter Notebook** of an **intraday momentum trading strategy** for the S&P 500 ETF (**SPY**), inspired by the research paper:

> **Beat the Market: An Effective Intraday Momentum Strategy for S&P 500 ETF (SPY)**  
> [SSRN Link](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4824172)

The strategy seeks to **capitalize on short-term price trends** that emerge during the trading session due to supply-demand imbalances.  
Unlike traditional models that focus on the final minutes of trading, this approach **dynamically initiates positions** in response to abnormal intraday market imbalances, integrating techniques from active day traders.  
A key component is the use of **dynamic trailing stops** to limit downside risk while preserving upside potential.

---

## 🚀 Key Highlights
- **Data Source:** [Polygon.io](https://polygon.io/)  
- **Timeframe:** May 2022 – April 2024 (minute & daily bars)  
- **Implementation:** Single Jupyter Notebook (end-to-end workflow)  
- **Performance:**  
  - **Total Return:** 42%  
  - **Annualized Return:** 34.6%  
  - **Sharpe Ratio:** 2.36  
  - **Max Drawdown:** 6%  
  - **Alpha:** 29.55% (β = 0.11)

---

## 📊 Strategy Logic
1. **Data Fetching**  
   - Minute-level SPY data, daily data, and dividend data via Polygon.io API  
   - Automatic rate-limit handling for free-tier accounts  

2. **Signal Generation**  
   - Volatility-adjusted breakout levels (Upper Band, Lower Band)  
   - VWAP confirmation filter to reduce false signals  

3. **Position Sizing**  
   - Volatility-targeted position scaling  
   - Leverage capped at 4x  

4. **Risk Management**  
   - Dynamic trailing stops  
   - Trade frequency control (e.g., every 30 minutes)  
   - Commission and slippage modeling  

5. **Performance Analysis**  
   - Equity curve vs. Buy & Hold SPY  
   - Sharpe ratio, alpha/beta, drawdowns, and hit ratios  
   - Regression analysis against SPY returns  

---

## 📂 Repository Structure
```

├── Intraday\_Momentum\_SPY.ipynb    # Main notebook with all code, analysis, and results
├── docs/
│   └── strategy\_performance.png   # Sample performance chart
└── README.md

````

---

## 📈 Sample Results

### Equity Curve
![Strategy Performance Chart](docs/strategy_performance.png)

### Key Metrics
| Metric                    | Value   |
|---------------------------|---------|
| Total Return (%)          | 42.0    |
| Annualized Return (%)     | 34.6    |
| Annualized Volatility (%) | 13.6    |
| Sharpe Ratio              | 2.36    |
| Hit Ratio (%)             | 50.0    |
| Max Drawdown (%)          | 6.0     |
| Alpha (%)                 | 29.55   |
| Beta                      | 0.11    |

---

## 🛠 How to Run
1. **Clone this repository**  
```bash
git clone https://github.com/Mkhan2317/SPY-Momentum-Alpha-Backtesting-2-Years-of-Free-Polygon-Data-
cd Intraday-Momentum-SPY
````

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

*(Alternatively, run in Google Colab — see below)*

3. **Set your Polygon.io API Key**
   Inside the notebook:

```python
API_KEY = "YOUR_API_KEY"
```

4. **Run all cells** in `Intraday_Momentum_SPY.ipynb`

---

## 📦 Google Colab

You can run this notebook directly in Google Colab without local setup:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Mkhan2317/Intraday-Momentum-SPY/blob/main/Intraday_Momentum_SPY.ipynb)

---

## 🔍 References

* **Paper:** [Beat the Market: An Effective Intraday Momentum Strategy for S\&P 500 ETF (SPY)](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4824172)
* **Data Source:** [Polygon.io](https://polygon.io/)

---

## ⚠️ Disclaimer

This project is for **educational and research purposes only**. It is **not** financial advice. Trading involves substantial risk and is not suitable for all investors.

---

## 📬 Contact

If you have questions or would like to collaborate:

* **Email:** [mkhan37@stevens.edu](mailto:mkhan37@stevens.edu)
* **LinkedIn:** [Amir Khan](https://linkedin.com/in/amirkhan2317)
* **Portfolio:** [mkhan2317.github.io](https://mkhan2317.github.io/)


---


