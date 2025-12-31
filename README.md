# Market Meet — Portfolio Optimization

Portfolio optimizer built for the CFM 101 competition at the University of Waterloo.

## What It Does

Constructs an optimized stock portfolio that tracks a blended **S&P 500 + TSX** benchmark. The goal was to minimize tracking error while adhering to competition constraints (market cap requirements, sector limits, position sizing).

## How It Works

1. **Stock filtering** — Filters tickers by volume, market cap, and data availability
2. **Benchmark construction** — Creates a 50/50 blend of S&P 500 and TSX returns
3. **Covariance-based optimization** — Uses `scipy.optimize.minimize` to find weights that minimize tracking error variance
4. **Constraint handling** — Enforces position limits, sector caps, and market cap diversity requirements

## Results

- **Tracking error:** 0.49% during the competition
- **Benchmark:** S&P 500 + TSX average

![Screenshot 1](graphresults)
![Screenshot 2](tableresults)

## Tech Stack

- Python
- pandas, numpy
- scipy (optimization)
- yfinance (market data)

## Team

Built by Shayan Jalali, Krish Suryavanshi, and Paul Reddy for CFM 101 (Fall 2025).
