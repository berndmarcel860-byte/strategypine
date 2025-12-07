# Quick Start Guide

## 5-Minute Setup for Crypto Futures Trading

### Step 1: Choose Your Strategy

**Are you a day trader or scalper?**
→ Use `crypto_scalping_strategy.pine` on 5m-15m charts

**Do you prefer swing trading?**
→ Use `crypto_swing_strategy.pine` on 4H-1D charts

### Step 2: Import to TradingView

1. Open [TradingView](https://www.tradingview.com)
2. Open any crypto futures chart (e.g., BINANCE:BTCUSDT.P)
3. Press `Alt + E` to open Pine Editor
4. Copy entire content of your chosen strategy file
5. Paste into Pine Editor
6. Click "Add to Chart"

### Step 3: Initial Configuration

#### For Scalping (5m-15m charts):
```
Strategy Settings → Properties:
- Initial Capital: $10,000 (or your actual capital)
- Base Currency: USDT
- Order Size: 100% of equity
- Commission: 0.075%
- Slippage: 10 ticks

Strategy Settings → Inputs:
- Risk Per Trade: 1%
- Risk/Reward Ratio: 2:1
- Scalping Mode: Moderate
- Use ATR for SL: ✓ Yes
- Use Time Filter: ✓ Yes
- Use HTF Filter: ✓ Yes
- Higher Timeframe: 15m (if on 5m), 1H (if on 15m)
```

#### For Higher Timeframe (4H-1D charts):
```
Strategy Settings → Properties:
- Initial Capital: $10,000 (or your actual capital)
- Base Currency: USDT
- Order Size: 50% of equity
- Commission: 0.075%
- Slippage: 20 ticks

Strategy Settings → Inputs:
- Risk Per Trade: 2%
- Risk/Reward Ratio: 3:1
- Use Partial TP: ✓ Yes
- Partial TP %: 50%
- ADX Threshold: 25
- Use Multi-TF: ✓ Yes
- HTF1: Daily (if on 4H), Weekly (if on 1D)
- HTF2: Weekly (if on 4H), Monthly (if on 1D)
```

### Step 4: Backtest

1. Right-click chart → Strategy Tester
2. View performance metrics:
   - Net Profit should be positive
   - Win Rate around 45-55%
   - Profit Factor > 1.5
   - Max Drawdown < 20%
3. If results are poor, adjust parameters

### Step 5: Set Up Alerts

1. Click "Create Alert" button
2. Select your strategy
3. Choose condition:
   - "Long Entry Signal" for buy alerts
   - "Short Entry Signal" for sell alerts
4. Configure notification (email, SMS, webhook)
5. Click "Create"

### Step 6: Paper Trade First

**CRITICAL:** Never trade real money immediately!

1. Use TradingView's paper trading feature
2. Trade for at least 2-4 weeks
3. Track your results
4. Adjust strategy parameters if needed
5. Only then consider live trading

---

## Recommended Trading Pairs

### High Liquidity (Best for Scalping):
- BTCUSDT (Bitcoin)
- ETHUSDT (Ethereum)
- BNBUSDT (Binance Coin)
- SOLUSDT (Solana)

### Good for Higher Timeframes:
- All above pairs plus:
- ADAUSDT (Cardano)
- AVAXUSDT (Avalanche)
- MATICUSDT (Polygon)
- DOTUSDT (Polkadot)

---

## Daily Routine

### For Scalpers (30-60 min sessions):
1. Check higher timeframe trend (1H/4H)
2. Wait for trend alignment
3. Monitor 5m/15m chart for entry signals
4. Set alerts and let strategy work
5. Review trades at end of session

### For Swing Traders (15-30 min daily):
1. Check weekly/daily trends
2. Review open positions
3. Adjust stops if needed
4. Look for new setups
5. Set alerts and wait

---

## First Week Checklist

- [ ] Strategy imported and configured
- [ ] Backtested on 3+ months of data
- [ ] Alert system set up
- [ ] Paper trading account ready
- [ ] Risk management rules defined
- [ ] Trading journal started
- [ ] Stop loss always enabled
- [ ] Position sizing calculated
- [ ] Trading hours defined
- [ ] Review process scheduled

---

## Red Flags to Avoid Trading

❌ Major news events (FOMC, CPI, etc.)  
❌ Extremely low volume periods  
❌ Market-wide flash crashes  
❌ Exchange maintenance windows  
❌ Personal emotional distress  
❌ Consecutive losing streak (take break)  
❌ Ranging/choppy markets (for trend strategies)  

---

## Quick Parameter Adjustments

### If too many signals:
- Increase min confirmations (scalping mode)
- Increase ADX threshold (HTF)
- Enable all filters
- Increase stop loss size

### If too few signals:
- Decrease min confirmations
- Decrease ADX threshold
- Reduce some filters
- Check market is trending

### If win rate too low:
- Increase confirmation requirements
- Add higher timeframe filter
- Increase take profit target
- Review trade quality

### If drawdown too high:
- Reduce risk per trade
- Increase stop loss distance
- Trade less frequently
- Focus on higher quality setups

---

## Emergency Actions

**If losing more than 5% in one day:**
1. STOP trading immediately
2. Review all open positions
3. Check if stops are in place
4. Take break for 24 hours
5. Review what went wrong
6. Adjust strategy before resuming

**If strategy stops working:**
1. Check if market regime changed
2. Review recent market conditions
3. Verify all settings are correct
4. Consider parameter optimization
5. May need to sit out until trend returns

---

## Support & Resources

- **TradingView Pine Script Docs:** https://www.tradingview.com/pine-script-docs/
- **Pine Script Reference:** https://www.tradingview.com/pine-script-reference/
- **Strategy Tester Guide:** https://www.tradingview.com/support/solutions/43000481029/
- **Trading Communities:** Reddit r/algotrading, TradingView chat

---

## Remember

✅ Start small  
✅ Use stop losses always  
✅ Paper trade first  
✅ Keep a journal  
✅ Stay disciplined  
✅ Manage risk strictly  
✅ Be patient  
✅ Continuous learning  

**Success in trading = Strategy + Discipline + Risk Management**

Good luck! 🚀
