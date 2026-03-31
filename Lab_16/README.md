# High-Dimensional GDP Growth Forecasting with Regularized Regression

## Objective
Forecast 5-year average GDP per capita growth across 120+ countries using a high-dimensional set of World Development Indicators, while diagnosing overfitting and improving out-of-sample performance via regularization.

## Methodology
- Collected 35+ World Development Indicators (WDI) via the World Bank API (2013–2019), spanning macroeconomic, infrastructure, health, education, and governance domains.
- Constructed a high-dimensional feature matrix (~50 predictors) and split data into training and test sets for out-of-sample evaluation.
- Estimated a baseline OLS model to diagnose overfitting in a setting with correlated predictors and a moderate p/n ratio.
- Applied feature standardization using `StandardScaler` to ensure comparability across variables.
- Implemented Ridge and Lasso regression with cross-validated λ selection using `RidgeCV` and `LassoCV`.
- Visualized coefficient shrinkage and selection dynamics using the Lasso regularization path.

## Key Findings
- The OLS model exhibited severe overfitting, with high in-sample fit but negative out-of-sample performance.
- Ridge regression delivered the strongest predictive performance, effectively stabilizing estimates in the presence of multicollinearity.
- Lasso achieved comparable out-of-sample accuracy while selecting a substantially smaller subset of predictors, highlighting the role of conditional predictive redundancy.
- Results underscore the bias–variance tradeoff and demonstrate that variable exclusion under Lasso reflects correlation structure rather than absence of economic relevance.
