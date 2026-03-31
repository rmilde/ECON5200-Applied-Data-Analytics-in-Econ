# Econ 5200 – Assignment 3  
## Causal Inference & Bias Correction

This project applies modern causal inference methods to simulated and observational datasets. The objective is to understand bias, sampling uncertainty, and causal estimation in non-experimental settings.

---

## Phase 1 – Manual Bootstrap

- Simulated skewed driver tip data
- Built a manual bootstrap engine (10,000 resamples)
- Estimated median sampling distribution
- Constructed 95% percentile confidence intervals
- Demonstrated asymmetry vs parametric inference

---

## Phase 2 – A/B Test & Permutation Test

- Simulated experimental delivery-time data
- Generated observed difference in means
- Constructed a fully manual permutation test (5,000 shuffles)
- Computed empirical p-value

---

## Phase 3 – Propensity Score Matching

Using observational SwiftPass data:

- Computed Naive Simple Difference in Means (SDO)
- Estimated Propensity Scores via Logistic Regression
- Performed 1:1 Nearest-Neighbor Matching
- Estimated Average Treatment Effect on the Treated (ATT)
- Compared causal ATT to biased naive SDO

---

## Phase 4 – Covariate Balance (Love Plot)

- Calculated Standardized Mean Differences (SMD)
- Visualized balance before and after matching
- Verified bias reduction (|SMD| < 0.1 threshold)

---

## Key Concepts

- Bootstrap inference  
- Permutation testing  
- Selection bias  
- Propensity Score Matching  
- ATT estimation  
- Covariate balance diagnostics  

---

## Tools

- pandas  
- numpy  
- scikit-learn  
- scipy  
- seaborn  
- matplotlib  

---

This assignment demonstrates applied econometric techniques for causal inference in both experimental and observational settings.
