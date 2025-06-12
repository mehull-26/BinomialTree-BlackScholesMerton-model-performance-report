# Comparative Analysis of European Option Pricing  
### Using the Binomial Tree Model & Black-Scholes Model

This project explores and compares two foundational models for pricing **European options**:

- **Binomial Tree Model** (step-based, discrete-time)
- **Black-Scholes-Merton Model** (closed-form, continuous-time)

It includes model implementation, sensitivity analysis, convergence checks, and real-world validation using **AAPL** options data via `yfinance`.

---

## Features

### Implemented:
- Binomial Tree pricing (with variable step size)
- Black-Scholes pricing (with Greeks)
- **Sensitivity analysis** for:
  - Volatility
  - Time to maturity
  - Strike price
  - Risk-free interest rate
- **Convergence analysis** of Binomial Tree → Black-Scholes
- **Real market comparison** using AAPL options (via yfinance)
- Outlier detection with volatility/time diagnostics
- Visualizations of pricing and model errors

---

## Insights
- Black-Scholes is computationally fast and accurate under typical conditions.
- Binomial Tree converges to Black-Scholes as steps increase.
- Both models can fail in edge cases: ultra-low/high IV, short expiry, illiquid strikes.
- Real data shows outliers which reveal practical model limits.

---

## Requirements

```bash
pip install numpy pandas matplotlib scipy yfinance datetime
```

> This project assumes European-style options. For American options, the Binomial Tree model can be extended, but the Black-Scholes model is not applicable without modification.


