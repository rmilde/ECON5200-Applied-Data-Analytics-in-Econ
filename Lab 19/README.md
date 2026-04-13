## Tree-Based Models — Random Forests

### Objective
Evaluate the performance and interpretability of tree-based models versus linear benchmarks on the California Housing dataset.

### Methodology
- Compared Decision Tree, Ridge Regression, and Random Forest (20,640 observations, 8 features)
- Tuned Random Forest using GridSearchCV (n_estimators, max_depth, max_features)
- Evaluated models using out-of-sample R² and cross-validation
- Compared feature importance: MDI vs permutation
- Benchmarked classification performance (RF vs logistic regression) using AUC
- Built an interactive dashboard with Plotly + ipywidgets to explore performance and feature importance

### Key Findings
- Random Forest outperformed benchmarks (R² = [YOUR VALUE] vs Ridge = [YOUR VALUE])
- Performance gains plateaued beyond ~200 trees
- MDI overstated importance of certain features; permutation provided more reliable rankings
- Random Forest achieved higher AUC than logistic regression due to nonlinear modeling
- max_features plays a key role in the bias–variance tradeoff
