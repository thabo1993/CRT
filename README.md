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
