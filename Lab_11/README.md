# Data Wrangling & Engineering Pipeline

## Objective
Design and implement a reproducible data preparation pipeline that engineers structural features and addresses missingness in a high-noise dataset to enable reliable downstream econometric modeling.

## Methodology
- Ingested and audited the `messy_hr_economics.csv` dataset to identify structural inconsistencies and missingness patterns.
- Visualized and diagnosed missing data mechanisms using **missingness mapping** to assess whether observations were Missing at Random (MAR).
- Engineered model-ready variables through categorical encoding and feature restructuring.
- Prevented **perfect multicollinearity** (Dummy Variable Trap) by omitting a reference category when constructing dummy variables.
- Reduced dimensionality of high-cardinality geographic variables using **target encoding** to retain predictive signal while controlling model complexity.
- Constructed a cleaned, analysis-ready dataset suitable for econometric estimation in `statsmodels`.

## Key Findings
The pipeline successfully transformed a structurally noisy dataset into a model-ready format. Missingness patterns were consistent with a MAR structure, enabling defensible imputation strategies. Multicollinearity risks were mitigated through careful dummy variable design, and high-cardinality location features were efficiently compressed via target encoding, preserving informational value while improving model tractability.
