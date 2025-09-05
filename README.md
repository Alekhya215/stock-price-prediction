# 📈 Stock Price Prediction using LSTM

## Overview
This project predicts the **next day's closing price** of a stock using an LSTM (Long Short-Term Memory) neural network.  
Data is pulled from **Yahoo Finance** via the `yfinance` Python package.

> ⚠️ Educational project: This is **not** financial advice, and the model is not guaranteed to generalize to unseen market conditions.

## Features
- Fetch historical OHLCV data with `yfinance`
- Create technical features (MA20, MA50)
- Scale features using `MinMaxScaler`
- Convert series to sequences (lookback window)
- Train an **LSTM** model in TensorFlow/Keras
- Plot **Actual vs Predicted** prices
- Save trained model and plot to disk

## Tech Stack
- Python
- NumPy, Pandas, Matplotlib, Scikit-learn
- TensorFlow/Keras
- yfinance
- Jupyter Notebook

## Dataset
- Default Ticker: `AAPL` (Apple Inc.) — changeable in notebook
- Default Period: 2015-01-01 to 2023-12-31 — changeable

## How to Run
1. Create and activate a virtual environment (recommended):
   ```bash
   # Windows (PowerShell)
   python -m venv .venv
   .venv\Scripts\Activate.ps1

   # macOS / Linux
   python3 -m venv .venv
   source .venv/bin/activate
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch Jupyter and open the notebook:
   ```bash
   jupyter notebook stock_predictor.ipynb
   ```

4. Run the notebook cells top-to-bottom. Replace the `TICKER` variable to try other stocks (e.g., `MSFT`, `TSLA`).

## Repo Structure
```
stock-price-prediction/
├─ stock_predictor.ipynb      # main notebook
├─ requirements.txt
├─ README.md
├─ .gitignore
├─ images/
│  └─ (result_plot.png saved here after training)
└─ LICENSE
```

## Future Improvements
- Add RSI, MACD, Bollinger Bands
- Compare LSTM vs GRU vs Transformer
- Hyperparameter tuning (window size, layers, dropout)
- Streamlit app for interactive predictions
- Add train/val/test split with walk-forward validation

## License
Released under the MIT License. See `LICENSE` for details.

---
*Starter created on: 2025-09-05*
