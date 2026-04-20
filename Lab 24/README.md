## Causal ML — DML and Causal Forests for Policy Evaluation

### Objective  
Estimate the causal effect of 401(k) eligibility on net financial assets and evaluate treatment effect heterogeneity using modern causal machine learning methods.

### Methodology  
- Fixed a broken manual DML implementation (data leakage, missing treatment residualization, incorrect formula)  
- Validated by recovering true ATE (= 5.0) in simulation  
- Estimated ATE using DoubleML with Random Forests and 5-fold cross-fitting  
- Performed sensitivity analysis for unobserved confounding  
- Estimated CATEs via CausalForestDML  
- Compared subgroup DML vs. individual-level heterogeneity from causal forests  

### Key Findings  
- Positive and robust ATE of 401(k) eligibility on net financial assets  
- DML provides stable, policy-relevant estimates  
- Causal Forests reveal finer heterogeneity but with higher uncertainty  
