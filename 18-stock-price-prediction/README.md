# Stock Price Prediction (Next-Day)

Predicts AAPL's **next-day return** from lag/technical features (1/5/10-day returns, moving-average ratios, rolling volatility), converts it to an implied next-day price, and benchmarks honestly against the naive "tomorrow = today" forecast. Data: 10 years of real daily prices from Yahoo Finance (2,484 usable days; chronological 80/20 split — time series are never shuffled).

## Verified result (executed notebook)
- Naive baseline MAE: **$3.04**
- Linear Regression implied-price MAE: $3.07 · direction accuracy 48.8%
- Random Forest implied-price MAE: $3.27 · direction accuracy 49.0%

**The models did not beat the naive baseline** — and that is the real, publishable finding. Next-day stock moves are close to a random walk; any tutorial claiming 95% accuracy on this task is leaking future data.

## Design choices that keep it honest
- Target = next-day **return**, not the price level (a level model just memorises the training years' price range and collapses later)
- Features use only information available at today's close — no look-ahead
- Chronological split, naive-baseline comparison, direction accuracy reported alongside MAE

## Run it
Open `stock_price_prediction.ipynb` — it downloads the price history itself and runs end to end.

⚠️ Educational project only — **not investment advice**, and no model of this kind can predict the market.
