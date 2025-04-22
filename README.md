
# ORB Trader – Intraday Trading Bot 🇮🇳📈

A powerful intraday trading bot built with Zerodha Kite API, powered by Python and intelligent signal filtering.

## 🔥 Features
- Real-time live paper trading
- ORB + EMA + MACD + RSI + VWAP strategy
- Dynamic stop-loss using ATR
- Trailing stop-loss (breakeven at 50%, lock 20% profit at 80%)
- Live trade logging to CSV
- 30-minute paper testing mode
- Streamlit-based performance dashboard
- GitHub-ready and modular structure

## 🧠 Strategy Logic
- Entry allowed if **any 2 of 4 conditions** are met:
  - Price breakout with EMA support
  - MACD crossover
  - VWAP confirmation
  - Volume spike
- RSI between 35–70
- ATR-based SL:
  - 1.0× for high ATR
  - 0.7× for low ATR

## 📦 Folder Structure
```
orb_trader_v4/
├── live_paper_trader.py       # Real-time trading logic
├── strategy.py                # Core indicators + logic
├── dashboard.py               # Streamlit dashboard
├── run.py                     # Offline backtesting
├── mock_data/                 # For testing strategy on past data
├── utils/kite_session.py      # Login handler
├── trades_log.csv             # Generated trade logs (auto-ignored)
```

## 🚀 Quick Start
```bash
cd orb_trader_v4
python live_paper_trader.py
```

## 📊 View Dashboard
```bash
streamlit run dashboard.py
```

## ⚠️ Important
- `tokens.json` is ignored — contains sensitive credentials.
- Always test in paper mode before going live!

## 👤 Author
Maintained by [@intradayAIboat](https://github.com/intradayAIboat)

---

This is a learning and experimentation project. Use it wisely and always with risk management in place 💡📈
