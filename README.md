# CRT AMD Distribution Indicator

This repository contains a Pine Script v5 indicator for TradingView that helps identify Candle Range Theory (CRT) setups using an AMD-style workflow: Accumulation, Manipulation, and Distribution.

## Files

- `crt_indicator.pine` — TradingView Pine Script indicator.

## What the indicator does

- Tracks a higher-timeframe candle range.
- Overlays translucent higher-timeframe candles on the lower-timeframe chart.
- Plots CRH, CRL, and 50% equilibrium levels.
- Detects accumulation inside the active CRT range.
- Flags buy-side and sell-side liquidity sweeps.
- Tracks CHoCH confirmation after manipulation.
- Detects Fair Value Gaps in premium or discount zones.
- Generates long and short distribution-phase entry signals.
- Plots entry, stop loss, and take-profit levels.
- Shows optional phase labels, FVG boxes, premium/discount zones, and a dashboard.
- Includes alert conditions for sweeps, entries, invalidation, and targets.

## Recommended timeframe pairs

| Higher Timeframe Range | Lower Timeframe Entry |
| --- | --- |
| Monthly | Daily |
| Weekly | 4H |
| Daily | 1H |
| 4H | 15m |
| 1H | 5m |
| 15m | 1m |

## CRT variants from the transcript

### Bearish CRT

- Use a bullish higher-timeframe candle as the CRT range.
- Mark its Candle Range High (CRH), Candle Range Low (CRL), and midpoint.
- Look for price to sweep above the CRH, then close back inside the range.
- Confirm bearish intent with lower-timeframe market structure, such as CHoCH.
- Prefer entries from a bearish FVG in the premium area above the midpoint.
- Main target is the CRL.

### Bullish CRT

- Use a bearish higher-timeframe candle as the CRT range.
- Mark its CRH, CRL, and midpoint.
- Look for price to sweep below the CRL, then close back inside the range.
- Confirm bullish intent with lower-timeframe market structure, such as CHoCH.
- Prefer entries from a bullish FVG in the discount area below the midpoint.
- Main target is the CRH.

### Three-candle CRT model

- Candle 1 defines the range.
- Candle 2 manipulates liquidity by sweeping one side of the range and closing back inside.
- Candle 3 provides the distribution entry and targets the opposite side of the range.

### Multi-candle AMD CRT model

- CRT does not have to complete in exactly three candles.
- The important requirement is a clear AMD sequence: Accumulation, Manipulation, then Distribution.
- Distribution can begin after manipulation is confirmed and lower-timeframe structure supports the trade idea.

### Two-candle / nested lower-timeframe CRT model

- A CRT setup can complete in fewer higher-timeframe candles when the lower-timeframe chart shows a full AMD sequence.
- The lower timeframe should still show accumulation, a liquidity sweep, CHoCH, and a valid FVG entry catalyst.

### Liquidity-run versus liquidity-sweep CRT

- CRT is useful around attacks on liquidity.
- If price sweeps a candle range level and fails to close beyond it, the setup favors reversal toward the opposite side of the range.
- If price closes beyond the swept level, the CRT reversal idea is void or weaker because the move may be a liquidity run.

### PD-array confirmation CRT

- CRT can be used to confirm whether price is respecting a PD array such as a Fair Value Gap or Order Block.
- Avoid CRT setups that require price to trade through strong opposing PD arrays near the target.

## How to use

1. Open TradingView.
2. Open the Pine Editor.
3. Copy the contents of `crt_indicator.pine` into the editor.
4. Save and add the indicator to your chart.
5. Choose the higher timeframe range and lower timeframe reference in the indicator settings.
6. Use the HTF candle overlay settings to display the higher-timeframe candle body and wick directly on the chart.
7. Adjust sweep tolerance, entry mode, and visual toggles as needed.

## Alerts

The indicator includes alert conditions for:

- CRT Manipulation Sweep Detected (Bearish)
- CRT Manipulation Sweep Detected (Bullish)
- CRT Distribution Entry Signal — Short
- CRT Distribution Entry Signal — Long
- CRT Setup Invalidated
- CRT Target (CRL/CRH) Reached

## Disclaimer

This indicator is for educational and research purposes only. It is not financial advice. Always test thoroughly and use proper risk management before making trading decisions.
