# Trading Quant Bot - Michael

Advanced real-time price tracking, prediction, and analysis for trading assets.

## Quick Start

```bash
python main.py
```

Choose:
- **Option 1**: Interactive Streamlit dashboard (web app)
- **Option 2**: Command line analysis

## File Description

- `main.py` - Main program (dashboard + command line)
- `README.md` - This file

## Environment Setup

1. **Install dependencies:**
   ```bash
   pip install streamlit plotly numpy pandas requests
   ```

2. **Add XMeta API credentials** (in `main.py`):
   ```python
   XMETA_API_KEY = "Enter API"
   XMETA_TOKEN = "Enter TOKEN if available"
   XMETA_USER_ID = "USER_ID"
   ```

3. **Run:**
   ```bash
   python main.py
   ```

## Main Features

- **Real-time XMeta price tracking** (API integration)
- **Monte Carlo simulation** to predict prices for the next 30 days
- **Risk metrics:**
  - Annualized volatility
  - Sharpe ratio
  - Value-at-Risk (VaR, 95%)
- **Price alert emails** when price crosses $60 or $70
- **Historical price logging** (CSV file)
- **Interactive charts** (Plotly)
- **Streamlit dashboard** for visualization and analysis

## Analysis & Functions

- **Technical indicators:**
  - Simple/Exponential Moving Average (SMA, EMA)
  - Relative Strength Index (RSI)
  - MACD indicator
  - Bollinger Bands
  - ATR-like volatility
- **Advanced analysis:**
  - Correlation and beta with benchmark (CSV upload supported)
  - Seasonality detection
  - Market regime detection (volatility-based)
  - Scenario analysis (shock simulation)
- **Prediction features:**
  - Monte Carlo simulation (1000 runs, 30 days)
  - Forecast mean and confidence intervals (5%, 95%)

## Dashboard

Option 1 will open in your browser: `http://localhost:8501`

## FAQ

- **API failure**: Please add valid XMeta credentials in `main.py`
- **Browser does not open automatically**: Please visit `http://localhost:8501` manually
- **Email alerts**: Uses Gmail app password (can be modified in code)
- **Slow loading**: May be due to API timeout or network issues

## Notes

- Will automatically create `xmeta_price_log.csv` for historical data logging
- All analysis and indicators are computed locally in Python, no external services required
- Command line and dashboard modes share the same codebase

---
**Author:** Ziming Pang
