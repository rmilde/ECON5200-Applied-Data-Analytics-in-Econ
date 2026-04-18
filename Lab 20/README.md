## Time Series Diagnostics & Advanced Decomposition

### Objective
Build a diagnosis-first framework for time series decomposition and inference with correct specification, structural break detection, and dependence-aware uncertainty.

### Methodology
- Corrected STL mis-specification by applying log transform to multiplicative data  
- Fixed Augmented Dickey-Fuller test by using appropriate regression specification  
- Applied MSTL to capture multiple seasonalities (daily and weekly cycles)  
- Implemented moving block bootstrap for trend confidence intervals  
- Detected structural breaks using PELT and tested stationarity by regime  
- Built reusable `decompose.py` module for decomposition and diagnostics  

### Key Findings
- GDP behaves as a non-stationary I(1) process with structural breaks  
- Decomposition results are highly sensitive to model specification  
- MSTL reduces seasonal leakage into trend estimates  
- Structural breaks materially affect stationarity conclusions  
- Block bootstrap reveals significant uncertainty in trend estimates  
