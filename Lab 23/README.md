## FedSpeak 2.0 — NLP Pipeline for Central Bank Communications

### Objective
Develop a domain-aware NLP framework to extract, quantify, and evaluate the predictive signal embedded in central bank communications for monetary policy decisions.

### Methodology
- Diagnosed and corrected pipeline flaws in tokenization, sentiment specification, and feature construction  
- Replaced naive preprocessing with NLTK tokenization and adopted the Loughran-McDonald financial sentiment dictionary  
- Tuned TF-IDF vectorization (min_df / max_df) to improve signal-to-noise ratio  
- Generated semantic document embeddings using a sentence-transformers model (all-MiniLM-L6-v2)  
- Compared TF-IDF and embedding-based representations across clustering quality and predictive performance  
- Built reusable `fomc_sentiment.py` module for preprocessing, sentiment scoring, and feature generation  

### Key Findings
- Domain-specific preprocessing materially improves sentiment signal extraction from policy text  
- Embedding-based representations capture deeper semantic structure, while TF-IDF remains more interpretable  
- Model performance varies by representation, highlighting a tradeoff between interpretability and predictive accuracy  
- Central bank communications contain statistically meaningful information for forecasting rate decisions  
