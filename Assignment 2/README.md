# Audit 02: Deconstructing Statistical Lies

This audit examines how commonly reported metrics can mislead decision-makers when data are skewed, base rates are ignored, or failures are censored. Using simulated data and manual statistical tests, we highlight three recurring statistical fallacies in product analytics, machine learning, and financial markets.  

## 1. Latency Skew and the Vanity of the Mean
**Finding:** Mean latency misrepresents performance in heavy-tailed systems.  
- Simulated latency: 98% of requests in 20–50ms; rare spikes of 1–5s.  
- Mean and standard deviation inflated by rare spikes.  
- Median and Median Absolute Deviation (MAD) remain stable.  
**Conclusion:** In skewed systems, robust statistics better reflect typical experience than traditional metrics.

## 2. False Positives and the Base Rate Fallacy
**Finding:** High model “accuracy” can be misleading in low-prevalence environments.  
- Audited a plagiarism detector claiming 98% accuracy.  
- With a 0.1% cheating rate, most flagged cases are false positives.  
- Accuracy alone is uninformative without base-rate context.  
**Conclusion:** Ignoring base rates can produce misleading or unjust outcomes in rare-event settings.

## 3. Survivorship Bias in Crypto Markets
**Finding:** Observed success overstates reality when failures are excluded.  
- Simulated 10,000 crypto token launches (Pareto distribution).  
- Top 1% by market cap (“Survivors”) appear successful.  
- Full distribution shows most tokens fail.  
**Conclusion:** Metrics based only on survivors exaggerate expected returns and hide true risks.

## Overall Takeaway
Misleading conclusions often arise from selective metrics, ignored base rates, and censored data—not bad math. Statistical rigor and understanding the data generating process are essential for truthful analysis.
