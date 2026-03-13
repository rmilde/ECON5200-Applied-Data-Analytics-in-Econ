# The Architecture of Dimensionality: Hedonic Pricing & the FWL Theorem

## Objective
Implement a multivariate hedonic pricing model and empirically validate the Frisch-Waugh-Lovell (FWL) theorem by demonstrating how partialling-out procedures recover the exact ceteris paribus coefficient from a full OLS specification.

## Methodology
- Ingested and prepared a cross-sectional dataset of 2026 California real estate characteristics.
- Estimated a baseline multivariate OLS hedonic pricing model explaining `Sale_Price` using structural housing attributes and geographic proximity variables.
- Identified potential omitted variable bias by estimating restricted models excluding proximity to major tech hubs.
- Manually implemented the Frisch-Waugh-Lovell procedure by:
  - Regressing the target regressor on control variables to obtain residualized variation.
  - Regressing the dependent variable on the same controls to isolate its unexplained component.
  - Estimating the coefficient using the residual-on-residual regression to partial out shared covariance.
- Verified that the manually computed coefficient matched the coefficient from the full multivariate OLS model.

## Key Findings
The restricted specification exhibited substantial omitted variable bias: excluding proximity to tech hubs incorrectly attributed price variation to the physical age of the property. Applying the FWL decomposition removed the shared covariance between regressors, producing a coefficient identical to the multivariate OLS estimate. This empirically demonstrates how the FWL theorem operationalizes the ceteris paribus interpretation by isolating the independent variation of the regressor of interest.
