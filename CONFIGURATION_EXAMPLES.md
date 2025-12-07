# Strategy Configuration Examples

This document provides pre-configured settings for different market conditions, trading styles, and risk profiles.

---

## Scalping Strategy Configurations

### 🟢 Configuration 1: Conservative Scalping (Beginners)
**Best for:** New traders, low-risk appetite, learning phase

```
Timeframe: 15m
Pair: BTCUSDT

Risk Management:
- Risk Per Trade: 0.5%
- Risk/Reward Ratio: 2.5:1
- Use ATR for SL: Yes
- ATR Multiplier: 2.0
- Fixed Stop Loss: 1.5%

Scalping Settings:
- Scalping Mode: Conservative
- Use Time Filter: Yes

EMA Settings:
- Very Fast EMA: 5
- Fast EMA: 8
- Medium EMA: 21
- Slow EMA: 50

RSI Settings:
- RSI Length: 14
- RSI Overbought: 70
- RSI Oversold: 30

MACD Settings:
- MACD Fast: 12
- MACD Slow: 26
- MACD Signal: 9

Volume Settings:
- Volume Spike Multiplier: 2.0
- Volume MA Length: 20

Trend Filter:
- Use HTF Filter: Yes
- Higher Timeframe: 1H
```

**Expected Results:**
- Win Rate: 50-60%
- Trades per Week: 5-10
- Max Drawdown: <10%

---

### 🟡 Configuration 2: Moderate Scalping (Intermediate)
**Best for:** Experienced traders, balanced approach

```
Timeframe: 5m
Pair: ETHUSDT or BTCUSDT

Risk Management:
- Risk Per Trade: 1.0%
- Risk/Reward Ratio: 2.0:1
- Use ATR for SL: Yes
- ATR Multiplier: 1.5
- Fixed Stop Loss: 2.0%

Scalping Settings:
- Scalping Mode: Moderate
- Use Time Filter: Yes

EMA Settings:
- Very Fast EMA: 5
- Fast EMA: 8
- Medium EMA: 21
- Slow EMA: 50

RSI Settings:
- RSI Length: 14
- RSI Overbought: 70
- RSI Oversold: 30

MACD Settings:
- MACD Fast: 12
- MACD Slow: 26
- MACD Signal: 9

Volume Settings:
- Volume Spike Multiplier: 1.5
- Volume MA Length: 20

Trend Filter:
- Use HTF Filter: Yes
- Higher Timeframe: 15m
```

**Expected Results:**
- Win Rate: 45-55%
- Trades per Week: 15-25
- Max Drawdown: <15%

---

### 🔴 Configuration 3: Aggressive Scalping (Advanced)
**Best for:** Professional traders, high-frequency trading

```
Timeframe: 1m or 3m
Pair: BTCUSDT (highest liquidity)

Risk Management:
- Risk Per Trade: 1.5%
- Risk/Reward Ratio: 1.5:1
- Use ATR for SL: Yes
- ATR Multiplier: 1.0
- Fixed Stop Loss: 2.5%

Scalping Settings:
- Scalping Mode: Aggressive
- Use Time Filter: Yes

EMA Settings:
- Very Fast EMA: 3
- Fast EMA: 5
- Medium EMA: 13
- Slow EMA: 34

RSI Settings:
- RSI Length: 9
- RSI Overbought: 75
- RSI Oversold: 25

MACD Settings:
- MACD Fast: 8
- MACD Slow: 17
- MACD Signal: 6

Volume Settings:
- Volume Spike Multiplier: 1.3
- Volume MA Length: 14

Trend Filter:
- Use HTF Filter: Yes
- Higher Timeframe: 15m
```

**Expected Results:**
- Win Rate: 40-50%
- Trades per Week: 40-80
- Max Drawdown: <20%

---

## Higher Timeframe Strategy Configurations

### 🌙 Configuration 1: Conservative Swing Trading
**Best for:** Part-time traders, lower stress, multi-week positions

```
Timeframe: 1D (Daily)
Pair: Any major crypto

Risk Management:
- Risk Per Trade: 1.5%
- Risk/Reward Ratio: 4.0:1
- Use Partial TP: Yes
- Partial TP %: 50%
- Partial TP Ratio: 2.0

Moving Averages:
- EMA 20: 20
- EMA 50: 50
- EMA 100: 100
- EMA 200: 200

Trend Strength:
- ADX Length: 14
- ADX Threshold: 30 (stricter)

Volatility:
- ATR Length: 14
- ATR Multiplier SL: 2.5
- BB Length: 20
- BB StdDev: 2.0

Momentum:
- RSI Length: 14
- Stochastic Length: 14
- Stochastic %K: 3
- Stochastic %D: 3

Volume Analysis:
- Volume MA Length: 20
- Use Volume Confirmation: Yes

Multi-Timeframe:
- Use Multi TF: Yes
- HTF1: Weekly
- HTF2: Monthly
```

**Expected Results:**
- Win Rate: 40-50%
- Trades per Month: 2-4
- Max Drawdown: <25%

---

### 🌍 Configuration 2: Moderate Swing Trading
**Best for:** Regular monitoring, balanced risk/reward

```
Timeframe: 4H (4-Hour)
Pair: BTC, ETH, SOL, BNB

Risk Management:
- Risk Per Trade: 2.0%
- Risk/Reward Ratio: 3.0:1
- Use Partial TP: Yes
- Partial TP %: 50%
- Partial TP Ratio: 1.5

Moving Averages:
- EMA 20: 20
- EMA 50: 50
- EMA 100: 100
- EMA 200: 200

Trend Strength:
- ADX Length: 14
- ADX Threshold: 25

Volatility:
- ATR Length: 14
- ATR Multiplier SL: 2.0
- BB Length: 20
- BB StdDev: 2.0

Momentum:
- RSI Length: 14
- Stochastic Length: 14
- Stochastic %K: 3
- Stochastic %D: 3

Volume Analysis:
- Volume MA Length: 20
- Use Volume Confirmation: Yes

Multi-Timeframe:
- Use Multi TF: Yes
- HTF1: Daily
- HTF2: Weekly
```

**Expected Results:**
- Win Rate: 45-55%
- Trades per Week: 2-5
- Max Drawdown: <20%

---

### ⚡ Configuration 3: Aggressive Position Trading
**Best for:** Full-time traders, larger positions, active management

```
Timeframe: 4H
Pair: High volatility altcoins

Risk Management:
- Risk Per Trade: 3.0%
- Risk/Reward Ratio: 2.5:1
- Use Partial TP: Yes
- Partial TP %: 60%
- Partial TP Ratio: 1.2

Moving Averages:
- EMA 20: 20
- EMA 50: 50
- EMA 100: 100
- EMA 200: 200

Trend Strength:
- ADX Length: 14
- ADX Threshold: 20 (more trades)

Volatility:
- ATR Length: 14
- ATR Multiplier SL: 1.5
- BB Length: 20
- BB StdDev: 2.0

Momentum:
- RSI Length: 14
- Stochastic Length: 14
- Stochastic %K: 3
- Stochastic %D: 3

Volume Analysis:
- Volume MA Length: 20
- Use Volume Confirmation: Yes

Multi-Timeframe:
- Use Multi TF: Yes
- HTF1: Daily
- HTF2: Weekly
```

**Expected Results:**
- Win Rate: 45-55%
- Trades per Week: 5-10
- Max Drawdown: <30%

---

## Market Condition Adjustments

### 📈 Strong Trending Market (Bull Run)
**Adjustments for both strategies:**

```
Scalping:
- Reduce min confirmations (more aggressive)
- Disable time filter if volume is consistently high
- Decrease stop loss slightly (trends are smoother)
- Focus more on long positions

Higher Timeframe:
- Decrease ADX threshold (20-22)
- Can increase risk per trade (+0.5%)
- Reduce R:R ratio slightly (2.5:1 instead of 3:1)
- Use trailing stops more aggressively
```

---

### 📉 Bearish Trending Market
**Adjustments for both strategies:**

```
Scalping:
- Increase confirmations (more selective)
- Focus on short positions
- Increase stop loss buffer
- Use stricter volume filters

Higher Timeframe:
- Increase ADX threshold (28-30)
- Focus on short setups
- Consider reducing risk per trade (-0.5%)
- Tighter trailing stops
```

---

### 〰️ Ranging/Choppy Market
**Adjustments for both strategies:**

```
Scalping:
- Switch to Conservative mode
- Increase all confirmation requirements
- Consider pausing trading
- Wait for clear trend to emerge

Higher Timeframe:
- Increase ADX threshold significantly (30+)
- Reduce trading frequency
- Wait for strong breakouts
- Consider sitting out until trend forms
```

---

### 💥 High Volatility Period
**Adjustments for both strategies:**

```
Scalping:
- Increase ATR multiplier (+0.5)
- Reduce position size (-25%)
- More conservative mode
- Wider stops

Higher Timeframe:
- Increase ATR multiplier (+0.5 to +1.0)
- Reduce risk per trade (-0.5% to -1.0%)
- Increase R:R ratio (+0.5)
- More selective entries
```

---

### 😴 Low Volatility Period
**Adjustments for both strategies:**

```
Scalping:
- Consider moving to higher timeframe
- Reduce trading frequency
- May need tighter stops
- Consider switching strategies

Higher Timeframe:
- Continue as normal (less affected)
- Can slightly decrease ATR multiplier
- May see fewer signals (normal)
- Patience is key
```

---

## Pair-Specific Optimizations

### Bitcoin (BTCUSDT)
```
Scalping:
- Standard settings work well
- Best timeframes: 5m, 15m
- High liquidity allows tighter spreads

Higher Timeframe:
- Excellent for swing trading
- Best timeframes: 4H, 1D
- Very reliable trend following
```

### Ethereum (ETHUSDT)
```
Scalping:
- Similar to BTC but slightly higher volatility
- Consider +0.2 ATR multiplier
- Best timeframes: 5m, 15m

Higher Timeframe:
- Great for swing trading
- Can be more volatile than BTC
- Best timeframes: 4H, 1D
```

### Altcoins (SOL, BNB, ADA, etc.)
```
Scalping:
- Increase ATR multiplier to 2.0+
- Use Conservative mode
- Best timeframes: 15m, 30m
- Require stronger volume confirmation

Higher Timeframe:
- Higher risk/higher reward
- Increase risk/reward ratio to 3.5-4.0
- Reduce position size
- Best timeframes: 4H, 1D
- More selective with entries
```

---

## Testing Checklist

Before going live with any configuration:

- [ ] Backtest on at least 6 months of data
- [ ] Test on different market conditions
- [ ] Verify win rate meets expectations
- [ ] Check max drawdown is acceptable
- [ ] Confirm profit factor > 1.5
- [ ] Paper trade for 2-4 weeks
- [ ] Review every trade in journal
- [ ] Ensure you understand all parameters
- [ ] Have emergency exit plan
- [ ] Start with minimum position size

---

## When to Switch Configurations

**Switch to more conservative:**
- After 3+ consecutive losses
- During major news events
- When volatility spikes unexpectedly
- If drawdown exceeds 10% (scalping) or 15% (swing)
- During learning phase

**Switch to more aggressive:**
- After 5+ consecutive wins
- When market conditions are ideal
- Only if you're experienced
- When risk tolerance allows
- After proper testing

**Switch strategies entirely:**
- When market regime changes (trending to ranging)
- When current strategy underperforms for 2+ weeks
- When volatility changes dramatically
- When your schedule changes (scalping ↔ swing)

---

## Final Notes

1. **No configuration is perfect** - all require adjustment
2. **Market conditions change** - stay flexible
3. **Track everything** - data drives improvement
4. **Start conservative** - can always increase risk later
5. **Be patient** - good setups take time
6. **Risk management first** - profits follow

Remember: The best configuration is one that:
- Matches your risk tolerance
- Fits your schedule
- Works in current market conditions
- You can execute consistently
- Has been properly tested

Happy trading! 📊🚀
