## Unsupervised Learning — Clustering & Dimensionality Reduction

### Objective
Develop a robust clustering framework for customer segmentation, emphasizing proper preprocessing, reproducibility, and reliable low-dimensional representation.

### Methodology
- Diagnosed and corrected a flawed K-Means pipeline by enforcing feature standardization, proper parameterization, and reproducibility controls  
- Rebuilt pipeline as: StandardScaler → :contentReference[oaicite:0]{index=0} → :contentReference[oaicite:1]{index=1} visualization  
- Applied clustering to synthetic customer behavioral data to identify distinct segments  
- Compared linear (PCA) and nonlinear (:contentReference[oaicite:2]{index=2}) embedding methods for cluster separability  
- Developed reusable `clustering_utils.py` module for pipeline execution, K selection, and visualization  

### Key Findings
- Proper standardization is critical for meaningful distance-based clustering outcomes  
- Cluster structure stabilizes at moderate K, with diminishing marginal improvement beyond that point  
- PCA provides interpretable global structure, while UMAP yields tighter local cluster separation  
- Results highlight the sensitivity of unsupervised learning outcomes to preprocessing and representation choices  
