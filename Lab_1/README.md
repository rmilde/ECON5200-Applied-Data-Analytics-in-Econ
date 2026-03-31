# Global Purchasing Power Parity Analysis

## Objective

This project applies the Big Mac Index—a measure of "burgernomics"—to empirically test the Law of One Price and assess real exchange rate deviations across global currencies.

## Methodology

- Constructed a structured dataset from The Economist's 2015 Big Mac Index using Python dictionaries
- Calculated implied purchasing power parity (PPP) exchange rates based on Big Mac prices across countries
- Computed percentage currency valuation against the US Dollar as the benchmark
- Identified currencies trading at significant premiums or discounts relative to PPP equilibrium

## Key Findings

The analysis reveals substantial deviations from purchasing power parity across major economies:

- The **Norwegian Krone** exhibits significant overvaluation at approximately 32% above its PPP-implied rate, suggesting potential arbitrage opportunities or structural factors such as high domestic costs and strong commodity exports
- The **Russian Ruble** demonstrates severe undervaluation at over 60% below PPP, likely reflecting macroeconomic instability, geopolitical risk premia, and capital flight pressures during the 2015 period

These findings illustrate that real-world exchange rates frequently diverge from theoretical PPP predictions due to transaction costs, non-tradable goods, and country-specific economic conditions.

## Tools Used

Python, Pandas
