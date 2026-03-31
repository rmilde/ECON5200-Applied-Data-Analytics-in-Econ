# Recovering Experimental Truths via Propensity Score Matching

## Objective  
Demonstrate how Propensity Score Matching corrects selection bias in observational data and recovers the true experimental treatment effect.

## Data  
Observational subset of the Lalonde dataset (1986 job training study), a benchmark in causal inference for evaluating non-experimental estimators against known experimental results.

## Methodology  
- Modeled treatment assignment using logistic regression on pre-treatment covariates.  
- Estimated individual propensity scores to summarize selection mechanisms.  
- Applied nearest-neighbor matching to construct balanced treatment and control groups.  
- Implemented using Python, Pandas, and Scikit-Learn.

## Key Findings  

**In my CPS-based observational sample (n = 614):**
- Naive difference in means: **–$635** (selection bias present but modest).  
- Matched estimate: **≈ +$1,850**, closely recovering the experimental benchmark (~+$1,800).

**In the more extreme PSID comparison often cited in the literature:**
- Naive estimate: **≈ –$15,204**, illustrating severe observational failure without adjustment.

**Conclusion:** When selection into treatment is explicitly modeled, matching estimators can restore experimental credibility to observational data.
