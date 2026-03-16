# 📈 LSTM-Based Portfolio Optimization (Research Repository)

## 📌 Project Overview
This repository contains the core research and algorithmic implementation for the paper: *"Deep Learning Applications in Building Optimal Portfolio Models for the Vietnamese Stock Market"*. 

🏆 **First Prize Winner at the 26th National Euréka Scientific Research Competition (2024).**

This project focuses on architecting a custom Long Short-Term Memory (LSTM) neural network that integrates SMA20/SMA50 technical crossovers to forecast asset returns. The model dynamically optimizes a portfolio of 50 high-performing stocks on the Ho Chi Minh City Stock Exchange (HOSE) over the 2018–2023 period.

*(Note: This repository contains the model research and training pipeline. The production-ready interactive web application can be found in my [Streamlit App Repository](#) - **Insert your App Repo link here later**).*

## 🗂️ Repository Structure
* `notebooks/`: 
  * `01_lstm_portfolio_optimization.ipynb`: The complete pipeline including data fetching (via `vnstock`), EDA, LSTM model architecture (TensorFlow/Keras), and comprehensive backtesting using `Backtrader` and `PyFolio`.

## 🚀 Key Technologies
* **Deep Learning:** TensorFlow, Keras, SciKeras
* **Algorithmic Trading & Backtesting:** Backtrader, PyFolio, QuantStats
* **Data Processing:** Pandas, NumPy, VNStock API
 Consistently lower maximum drawdowns during volatile market regimes.

## ⚙️ How to Run
1. Clone this repository:
```bash
git clone [https://github.com/HuyLe3011/LSTM-Portfolio-Research.git](https://github.com/HuyLe3011/LSTM-Portfolio-Research.git)
```

2. Install the strict dependencies required for the backtesting environment:
```bash
pip install -r requirements.txt
```

3. Open the `notebooks/` directory and execute the Jupyter notebook to reproduce the training and backtesting results.

## ⚠️ Known Limitations & Future Work
While the model demonstrates strong out-of-sample performance, it was developed under academic constraints. Future iterations will address the following real-world market dynamics:

* **Survivorship Bias:** The current dataset consists of the top 50 highly liquid HOSE stocks over the 2018–2023 period. Future work will utilize Point-in-Time (PiT) data, including delisted entities, to prevent the inflation of risk-adjusted returns.
* **Market Friction & Slippage:** The backtest assumes standard transaction costs but does not fully account for market impact during high-turnover rebalancing. I plan to integrate a Transaction Cost Penalty directly into the Deep Learning loss function.
* **Regime Shift Overfitting:** To prevent model decay during macroeconomic shifts, future pipelines will replace the static train/test split with Walk-Forward Validation and Hidden Markov Models (HMM) for dynamic regime detection.
