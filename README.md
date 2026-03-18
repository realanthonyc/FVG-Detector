# FVG Detector

The **FVG Detector** is a TradingView Pine Script indicator that automatically identifies and highlights **Fair Value Gaps (FVGs)**. These are key price imbalances widely used by Smart Money Concepts (SMC) traders.

## How it works

An FVG is a 3-candle pattern with a gap between the 1st and 3rd candle's wicks:
- **Bullish FVG:** Gap between the 1st candle's high and 3rd candle's low.
- **Bearish FVG:** Gap between the 1st candle's low and 3rd candle's high.

The script scans for this pattern and draws a box. It includes an adjustable `Min Gap Size (%)` filter to ignore insignificant gaps based on the middle candle's body size.

## How to read the chart

The script visually plots:
- **Green Box:** Bullish FVG (buyers overpowered sellers).
- **Red Box:** Bearish FVG (sellers overpowered buyers).
- **Middle Line:** Marks the 50% midpoint of the gap, known as **Consequent Encroachment (CE)**.

Colors, box width, and the number of historical FVGs kept on the chart are customizable.

## Practical Usage & Trading Ideas

FVGs represent market inefficiencies that price typically seeks to rebalance.
1. **Magnets for Price:** Price frequently returns to "fill" the FVG. **Note: The timing of this fill varies.** It may happen on the very next bar, several bars later, or sometimes much later in the session.
   - **Partial Fill:** Price enters the gap but doesn't close it entirely. Bouncing from inside the FVG (especially at the 50% CE level) indicates aggressive trend continuation.
   - **Full Fill:** Price completely trades through the entire gap. The imbalance is considered resolved, and price may either resume the trend or reverse.
2. **Support/Resistance:** Bullish FVGs act as support in uptrends; Bearish FVGs act as resistance in downtrends.
3. **The 50% Level (CE):** Consequent Encroachment is a crucial institutional reaction zone. A strong bounce off the CE line confirms trend strength, while breaking past it often leads to a full gap fill.
4. **Consecutive FVGs (Liquidity Voids):** Multiple FVGs in a row signify high momentum and form a larger "Liquidity Void". While each box is drawn individually on lower timeframes, they functionally act as **one massive gap block** on higher timeframes. Traders often measure from the start of the first FVG to the end of the last FVG, using Fibonacci tools to locate the optimal entry (like the 50% CE of the entire void) within that combined block.
5. **Confluence:** Best used alongside Order Blocks, liquidity sweeps, or Fibonacci levels.
