## Time Series Forecasting — ARIMA, GARCH & Bootstrap

### Objective
Develop a rigorously specified forecasting framework for macroeconomic and financial time series, integrating proper differencing, volatility modeling, and robust uncertainty quantification.

### Methodology
- Diagnosed and corrected a misspecified ARIMA pipeline by addressing non-stationarity, incorporating seasonal structure, and validating residuals  
- Transitioned to SARIMA with appropriate differencing and seasonal terms, confirming adequacy via the :contentReference[oaicite:0]{index=0}  
- Modeled conditional volatility in equity returns using :contentReference[oaicite:1]{index=1}  
- Built a reusable `forecast_evaluation.py` module for scale-free error measurement and expanding window backtesting  
- Implemented block bootstrap forecast intervals to preserve dependence structure and avoid parametric assumptions  

### Key Findings
- Correct model specification (stationarity + seasonality) is critical for reliable ARIMA-based forecasts  
- Residual diagnostics confirm well-specified SARIMA models eliminate remaining autocorrelation  
- Equity return volatility exhibits strong persistence consistent with standard GARCH dynamics  
- Block bootstrap intervals reveal materially wider and more realistic forecast uncertainty than parametric alternatives  
