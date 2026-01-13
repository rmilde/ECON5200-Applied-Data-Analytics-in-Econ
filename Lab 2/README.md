# The Illusion of Growth & The Composition Effect

## Objective

This lab builds a reproducible Python data pipeline to interrogate long‑run U.S. wage growth using live data from the Federal Reserve (FRED). The goal is to distinguish **nominal gains** from **real purchasing power**, identify statistical distortions during the COVID‑19 period, and correct for **composition bias** to assess whether observed wage growth reflects true labor‑market improvement.

## Methodology

**Data ingestion via FRED API**
Using `fredapi`, the pipeline programmatically retrieves official macroeconomic series directly from the Federal Reserve, ensuring transparency and reproducibility.

1. **Nominal vs. Real Wages**

   * Fetched nominal average hourly earnings (AHETPI).
   * Combined with CPI data to deflate nominal wages and compute **real wages**.
   * Plotted long‑run time series to compare nominal growth against inflation‑adjusted purchasing power.

2. **Anomaly Detection: The 2020 Pandemic Spike**

   * Visual inspection and time‑series comparison revealed an abrupt rise in measured wages during 2020.
   * This spike contradicted economic intuition given the simultaneous collapse in employment.

3. **Composition Effect Correction (ECI)**

   * Retrieved the Employment Cost Index (ECIWAG), which holds the occupational mix constant.
   * Rebased series to a common index to compare growth paths.
   * Demonstrated that, once composition is fixed, wage growth remains smooth—confirming the 2020 spike as a statistical artifact rather than a true surge in labor demand.

## Key Findings — *The Pandemic Paradox*

* **The Money Illusion:** Over roughly five decades, nominal wages rose steadily, but real wages remained largely flat—highlighting the erosion of purchasing power after inflation.
* **The Pandemic Paradox:** The apparent wage “boom” in 2020 was driven by low‑wage workers disproportionately exiting the labor force, mechanically raising the average wage.
* **Reality Check via ECI:** When controlling for workforce composition using the Employment Cost Index, the spike disappears. Wage growth during the pandemic was **stable, not explosive**.

**Conclusion:** Without correcting for inflation and composition bias, standard wage statistics can mislead. Proper deflation and fixed‑composition measures reveal a far more sobering picture of long‑run wage growth.
