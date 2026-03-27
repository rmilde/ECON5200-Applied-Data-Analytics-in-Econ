# NY Fed Yield Curve Recession Model Replication

## Objective
Replicate the Federal Reserve Bank of New York’s yield curve–based recession probability model using a logistic regression framework to forecast NBER recessions 12 months ahead.

## Methodology
- Collected macroeconomic time series from FRED: 10Y–3M Treasury yield spread (T10Y3M) and NBER recession indicator (USREC)
- Resampled daily yield data to monthly frequency and applied a 12-month lag structure
- Estimated both a Linear Probability Model (LPM) and a logistic regression model for comparison
- Implemented time-series-aware validation techniques
- Used a logit specification to compute odds ratios and 95% confidence intervals
- Generated a time series of predicted recession probabilities

## Key Findings
- The Linear Probability Model produced invalid predictions outside the \[0,1\] range, confirming its unsuitability for probability estimation
- The logistic model correctly imposed a bounded S-curve and yielded interpretable probability estimates
- The yield spread exhibited a statistically significant relationship with future recessions via the estimated odds ratio
- The model signaled elevated recession risk during the 2022–2024 yield curve inversion, despite no realized NBER recession, highlighting limitations in real-time predictive performance
