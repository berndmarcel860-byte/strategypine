# Professional Crypto Trading Strategies for TradingView

This repository contains two professional Pine Script strategies designed for cryptocurrency futures trading, optimized for different timeframes and trading styles.

## 📊 Strategies Overview

### 1. Crypto Scalping Strategy (`crypto_scalping_strategy.pine`)
**Best for:** 1m, 5m, 15m, 30m timeframes  
**Trading Style:** Fast-paced scalping with multiple quick trades  
**Risk Profile:** Lower risk per trade, higher frequency

### 2. Crypto Swing/Higher Timeframe Strategy (`crypto_swing_strategy.pine`)
**Best for:** 4H, 1D, 1W timeframes  
**Trading Style:** Swing trading with position holding for days/weeks  
**Risk Profile:** Higher risk per trade, lower frequency, better risk/reward

---

## 🎯 Scalping Strategy Features

### Core Indicators
- **Multiple EMAs** (Very Fast: 5, Fast: 8, Medium: 21, Slow: 50)
- **RSI** (14 period) with dynamic zones
- **MACD** (12, 26, 9) for momentum confirmation
- **Volume Analysis** with spike detection
- **ATR-based** dynamic stop loss

### Entry Conditions
The strategy uses a confirmation system requiring multiple signals:
- **Aggressive Mode:** 3+ confirmations
- **Moderate Mode:** 4+ confirmations  
- **Conservative Mode:** 5+ confirmations

**Long Entry Signals:**
- Fast EMAs aligned bullish (5 > 8 > 21)
- Price above medium EMA
- RSI in favorable zone (40-70)
- MACD bullish crossover
- Volume spike confirmation
- Positive momentum
- Optional: Bullish candlestick patterns
- Higher timeframe trend confirmation

**Short Entry Signals:**
- Fast EMAs aligned bearish (5 < 8 < 21)
- Price below medium EMA
- RSI in favorable zone (30-60)
- MACD bearish crossover
- Volume spike confirmation
- Negative momentum
- Optional: Bearish candlestick patterns
- Higher timeframe trend confirmation

### Risk Management
- **Customizable risk per trade** (0.1% - 5%)
- **Risk/Reward ratio** (1:1 to 1:5)
- **ATR-based or fixed percentage stop loss**
- **Dynamic position sizing** based on account equity
- **Emergency exit conditions** on trend reversal
- **Time filter** to avoid low liquidity hours (0-4 UTC)

### Visual Features
- Color-coded EMA lines
- Entry signal markers (triangles)
- Trend background coloring
- Real-time dashboard with:
  - Current mode and signal count
  - RSI value
  - Higher timeframe trend
  - Volume status
  - Position status
  - Risk/reward ratio
  - ATR value

---

## 📈 Higher Timeframe Strategy Features

### Core Indicators
- **EMAs** (20, 50, 100, 200) for trend identification
- **ADX** (14) for trend strength measurement
- **Bollinger Bands** (20, 2.0) for volatility
- **RSI & Stochastic** for momentum
- **MACD** for trend confirmation
- **Volume Profile** analysis
- **Multi-timeframe** analysis (Daily & Weekly)

### Advanced Features
1. **Trend Strength Filter** - Only trades in strong trends (ADX > 25)
2. **Market Structure Analysis** - Identifies higher highs/lows and lower highs/lows
3. **Support/Resistance** - Automatic swing point detection
4. **Multi-Timeframe Confirmation** - Aligns with higher timeframe trends
5. **Volatility Analysis** - BB expansion/contraction detection

### Entry Conditions
**Long Entry Requirements:**
- Bullish EMA alignment (20 > 50 > 100)
- Strong uptrend (ADX > 25, +DI > -DI)
- Bullish momentum (RSI > 50, Stochastic bullish)
- MACD bullish or Stochastic confirmation
- Volume confirmation (buying pressure)
- Higher timeframes bullish (Daily & Weekly)
- Price near support or above BB middle

**Short Entry Requirements:**
- Bearish EMA alignment (20 < 50 < 100)
- Strong downtrend (ADX > 25, -DI > +DI)
- Bearish momentum (RSI < 50, Stochastic bearish)
- MACD bearish or Stochastic confirmation
- Volume confirmation (selling pressure)
- Higher timeframes bearish (Daily & Weekly)
- Price near resistance or below BB middle

### Position Management
- **Partial Take Profit** system (50% at 1.5R, 50% at 3R)
- **ATR-based stop loss** (2x ATR default)
- **Trailing stop** using EMA 20 when in profit
- **Trend reversal exit** on EMA 50 break
- **Dynamic risk/reward** (1.5:1 to 10:1)

### Visual Features
- All major EMAs plotted
- Bollinger Bands with fill
- Support/Resistance levels
- Entry signal markers
- Trend background coloring
- Comprehensive dashboard showing:
  - Current timeframe
  - Trend direction and strength
  - ADX value
  - RSI value
  - Higher timeframe alignment
  - Volume status
  - Volatility state
  - Market structure
  - Position and P&L
  - Risk/reward ratio

---

## 🚀 How to Use

### Installation
1. Open [TradingView](https://www.tradingview.com)
2. Open the Pine Editor (Alt + E)
3. Copy the entire content of either strategy file
4. Paste into Pine Editor
5. Click "Add to Chart"

### Recommended Settings

#### For Scalping Strategy:
```
Timeframe: 5m or 15m
Asset: BTC/USDT, ETH/USDT (high liquidity pairs)
Mode: Start with "Moderate", adjust based on results
Risk per Trade: 1%
Risk/Reward: 2:1
Use ATR for SL: Yes
Use Time Filter: Yes
Use HTF Filter: Yes (15m chart)
```

#### For Higher Timeframe Strategy:
```
Timeframe: 4H or 1D
Asset: Any major crypto futures
Risk per Trade: 2%
Risk/Reward: 3:1
Use Partial TP: Yes
HTF1: Daily (if on 4H), Weekly (if on Daily)
HTF2: Weekly (if on 4H), Monthly (if on Daily)
ADX Threshold: 25
Volume Confirmation: Yes
```

### Optimization Tips

1. **Backtesting:**
   - Test on at least 6-12 months of data
   - Adjust parameters based on specific pairs
   - Consider different market conditions (trending vs ranging)

2. **Risk Management:**
   - Never risk more than 1-2% per trade for scalping
   - Can risk 2-3% for higher timeframe swings
   - Adjust position size based on volatility

3. **Market Conditions:**
   - Scalping works best in trending markets with high liquidity
   - Higher timeframe strategy excels in strong trends
   - Reduce trading during major consolidation periods

4. **Time Filter (Scalping):**
   - Avoid trading during low liquidity hours (0-4 UTC typically)
   - Best results during Asian, European, and US sessions overlap
   - Consider exchange-specific volume patterns

5. **Alerts:**
   - Set up TradingView alerts for entry signals
   - Configure alerts for emergency exits
   - Use mobile app for real-time notifications

---

## ⚙️ Strategy Parameters

### Scalping Strategy Parameters

| Parameter | Default | Range | Description |
|-----------|---------|-------|-------------|
| Risk Per Trade | 1.0% | 0.1-5.0% | Percentage of equity to risk |
| Risk/Reward Ratio | 2.0 | 1.0-5.0 | Take profit distance multiplier |
| Scalping Mode | Moderate | Conservative/Moderate/Aggressive | Signal confirmation level |
| Fast EMA | 8 | 1+ | Fast moving average |
| Medium EMA | 21 | 1+ | Medium moving average |
| Slow EMA | 50 | 1+ | Slow moving average |
| RSI Length | 14 | 1+ | RSI calculation period |
| MACD Fast | 12 | 1+ | MACD fast length |
| MACD Slow | 26 | 1+ | MACD slow length |
| Volume Multiplier | 1.5 | 1.0-5.0 | Volume spike threshold |
| ATR Multiplier | 1.5 | 0.5-5.0 | Stop loss distance |

### Higher Timeframe Parameters

| Parameter | Default | Range | Description |
|-----------|---------|-------|-------------|
| Risk Per Trade | 2.0% | 0.5-10.0% | Percentage of equity to risk |
| Risk/Reward Ratio | 3.0 | 1.5-10.0 | Take profit distance multiplier |
| Partial TP % | 50% | 10-90% | Percentage of position to close at first TP |
| EMA 20/50/100/200 | Standard | 1+ | Moving average periods |
| ADX Length | 14 | 1+ | ADX calculation period |
| ADX Threshold | 25 | 10-50 | Minimum trend strength |
| ATR Multiplier | 2.0 | 1.0-5.0 | Stop loss distance |
| BB Length | 20 | 1+ | Bollinger Bands period |
| BB StdDev | 2.0 | 0.5-5.0 | Bollinger Bands standard deviation |
| RSI Length | 14 | 1+ | RSI calculation period |

---

## 📊 Performance Metrics to Monitor

### Key Metrics
- **Win Rate:** Target 45-55% for scalping, 40-50% for swing
- **Profit Factor:** Target >1.5
- **Average R:R:** Should match or exceed set ratio
- **Max Drawdown:** Keep under 20% for scalping, 30% for swing
- **Sharpe Ratio:** Target >1.0

### Regular Review
- Review performance weekly for scalping strategy
- Review performance monthly for higher timeframe strategy
- Adjust parameters if market conditions change significantly
- Keep trading journal to track what works

---

## ⚠️ Risk Disclaimer

**IMPORTANT:** These strategies are for educational purposes only. Cryptocurrency trading involves substantial risk of loss.

- Past performance does not guarantee future results
- Always use proper risk management
- Never trade with money you can't afford to lose
- Start with small position sizes
- Test thoroughly on paper trading first
- Consider market conditions and your risk tolerance
- Consult with a financial advisor before trading

---

## 🔧 Troubleshooting

### Common Issues

1. **Too many signals:**
   - Increase confirmation requirements
   - Enable higher timeframe filter
   - Increase ADX threshold (HTF strategy)

2. **Too few signals:**
   - Decrease confirmation requirements
   - Disable some filters temporarily
   - Check if market is ranging (strategies work best in trends)

3. **High drawdown:**
   - Reduce risk per trade
   - Increase stop loss multiplier
   - Add more confirmations
   - Trade only in direction of higher timeframe trend

4. **Strategy not executing:**
   - Check if time filter is blocking trades
   - Verify all indicators are calculating correctly
   - Ensure sufficient bar history loaded

---

## 📝 Version History

### v1.0.0 (Current)
- Initial release
- Scalping strategy for lower timeframes
- Higher timeframe swing strategy
- Multi-indicator confirmation system
- Advanced risk management
- Visual dashboard
- Alert system

---

## 🤝 Contributing

Feel free to fork this repository and submit pull requests with improvements. Suggestions for enhancements are welcome!

---

## 📧 Support

For questions or issues:
- Open an issue on GitHub
- Review TradingView Pine Script documentation
- Join trading communities for strategy discussion

---

## 📚 Additional Resources

- [TradingView Pine Script Documentation](https://www.tradingview.com/pine-script-docs/)
- [Pine Script Reference Manual](https://www.tradingview.com/pine-script-reference/)
- Community forums for strategy optimization
- Backtesting best practices guides

---

**Happy Trading! 🚀📈**

Remember: The best strategy is one that fits your trading style, risk tolerance, and time commitment. Always practice proper risk management and stay disciplined!