# The Cost of Living Crisis: A Data-Driven Analysis

## Overview
Official inflation measures are designed to capture the spending patterns of the “average” urban consumer. However, this aggregation can obscure meaningful differences in cost-of-living experiences across demographic groups. This project examines whether the headline Consumer Price Index (CPI) accurately reflects inflation faced by students, whose expenditures are heavily concentrated in tuition, housing, and food away from home.

Using publicly available price data and economic index theory, I construct a Student-Specific Price Index (SPI) and compare it to the national CPI.

---

## Research Question
**Does the official CPI understate inflation experienced by students?**

---

## Methodology
- **Data Sources:** Federal Reserve Economic Data (FRED) API  
- **Tools:** Python, pandas, matplotlib, fredapi  
- **Index Construction:**  
  - Student SPI constructed as a **Laspeyres price index**, holding expenditure weights fixed to represent a typical student consumption bundle.
  - All price series normalized to **2016 = 100** to ensure comparability.
- **Data Processing:**  
  - Monthly CPI component series aligned and cleaned.
  - Missing values handled to preserve consistent time-series comparisons.

---

## Key Findings
- Student-relevant prices (rent, food away from home, tuition-related categories) consistently grow faster than headline inflation.
- Since 2016, the Student SPI diverges from the official CPI by approximately **1.3 percentage points**.
- Core student expense categories exhibit cumulative inflation exceeding **50%**, far outpacing the national CPI.

---

## Implications
Headline inflation measures mask important distributional effects. For students, whose consumption baskets are concentrated in non-substitutable goods, official CPI significantly understates real cost-of-living pressures. These findings have implications for education affordability, financial aid policy, and the interpretation of inflation statistics in heterogeneous populations.

---

## Repository Structure
-  Econ_5200_Assignment_1.ipynb (Data collection, index construction, and analysis)
- README.md (Project overview and findings)

## Key Skills Demonstrated
- Economic index construction (Laspeyres methodology)
- API-driven data collection
- Time-series analysis
- Inflation measurement and distributional analysis
- Data visualization and reproducible research

---

## Future Extensions
- Regional student inflation comparisons
- Alternative index formulations (Paasche, chained CPI)
- Policy simulation using student-weighted inflation adjustments
