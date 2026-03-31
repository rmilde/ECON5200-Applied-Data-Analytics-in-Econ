# AI Capex Diagnostic Modeling

## Objective
Evaluate and correct structural violations in an OLS regression model predicting AI software revenue, with a focus on identifying heteroscedasticity and multicollinearity to ensure statistically reliable inference.

## Methodology
- Constructed an OLS regression model linking AI software revenue to capital expenditure and deployment metrics  
- Performed residual diagnostics to detect heteroscedasticity, including visual inspection of variance patterns across fitted values  
- Assessed multicollinearity using Variance Inflation Factor (VIF) analysis  
- Identified instability in error variance at higher capital expenditure tiers  
- Applied HC3 robust standard errors to correct biased inference under heteroscedasticity  
- Compared naive OLS results with heteroscedasticity-consistent estimates to evaluate changes in statistical significance  

## Key Findings
The baseline OLS model exhibited pronounced heteroscedasticity, particularly at elevated capital expenditure levels, leading to downward-biased standard errors and overstated statistical significance. After applying HC3 corrections, standard errors widened materially, reducing false confidence in several predictors. This adjustment clarified that only a subset of deployment metrics retained true explanatory power, underscoring the importance of robust inference in high-variance AI investment environments.
