# Forecasting Architecture and the Bias-Variance Tradeoff

## Objective
To rigorously diagnose the bias-variance tradeoff in a financial forecasting context by quantifying the out-of-sample instability of a high-capacity polynomial regression model using K-Fold cross-validation.

## Methodology
- Collected and structured quarterly revenue data for NVIDIA spanning 2024–2026  
- Engineered a nonlinear feature space using a 7th-degree polynomial expansion to intentionally increase model flexibility  
- Estimated a baseline Ordinary Least Squares (OLS) regression on the expanded feature set to minimize in-sample error  
- Evaluated model performance using K-Fold Cross-Validation to obtain a robust estimate of out-of-sample Mean Squared Error (MSE)  
- Compared training error against cross-validated error to isolate variance-driven overfitting effects  
- Visualized fitted vs. predicted values to assess extrapolation behavior and structural instability  

## Key Findings
The analysis demonstrates a textbook manifestation of high-variance overfitting. While the 7th-degree polynomial model achieved near-zero training error, it failed catastrophically in out-of-sample validation, producing highly unstable and economically implausible forecasts when extrapolated. Cross-validation revealed a substantial divergence between in-sample and true predictive error, highlighting the model’s sensitivity to noise rather than signal. These results underscore the operational risk of unconstrained model complexity in financial forecasting and provide empirical justification for the adoption of regularization techniques to stabilize predictions and improve generalization.
