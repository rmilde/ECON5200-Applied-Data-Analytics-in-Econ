## Lab 6: The Architecture of Bias

**Objective**  
Analyzed how the Data Generating Process (DGP) and sampling decisions introduce bias in machine learning systems, with a focus on variance, covariate shift, and experimental integrity.

**Tech Stack**  
Python · pandas · numpy · scipy (Chi-Square tests) · scikit-learn

**Methodology**  
1. **Simple Random Sampling (SRS):**  
   Manually simulated SRS on the Titanic dataset to illustrate how small or unrepresentative samples inflate variance and sampling error.
2. **Stratified Sampling:**  
   Applied stratified sampling (via `sklearn`) to preserve class proportions and eliminate covariate shift between training and target populations.
3. **Sample Ratio Mismatch (SRM) Audit:**  
   Performed a Chi-Square–based forensic check to detect deviations between expected and observed treatment/control splits, identifying potential engineering or logging failures in A/B tests.

**Key Takeaways**  
- Sampling is part of the model: poor sampling can bias results even with correct estimators.  
- Stratification reduces variance and guards against distributional drift.  
- SRM tests are critical diagnostics for validating experimental pipelines.

---

### Theory: Survivorship Bias & Ghost Data

Analyzing only successful Unicorn startups (e.g., those featured on TechCrunch) induces **Survivorship Bias** because the sample conditions on success. Failed, stagnant, or never-funded startups are excluded, leading to upwardly biased inferences about growth rates, funding strategies, or founder characteristics.

To correct this using a **Heckman Selection Model**, the required **Ghost Data** is **selection-equation information** on *all startups that could have appeared* but did not—specifically:
- Data on non-Unicorn and failed startups (outcomes unobserved in the main equation), and  
- An exclusion variable affecting the probability of being featured or surviving (e.g., media exposure, VC network access) but not directly affecting post-success outcomes.

This ghost data allows modeling the selection process and correcting bias in outcome estimates.
