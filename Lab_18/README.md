# Fraud Detection Model Evaluation — Metrics that Matter

## Objective
Evaluate the performance of a logistic regression fraud detection model on a highly imbalanced dataset using metrics that better capture real-world decision quality than accuracy alone.

## Methodology
- Utilized the Kaggle Credit Card Fraud Detection dataset (284,807 transactions; 0.172% fraud rate)
- Trained a logistic regression classifier on PCA-transformed features (V1–V28), transaction amount, and binary fraud labels
- Assessed model performance using confusion matrices, Precision, Recall, and F1-score
- Generated ROC and Precision-Recall curves to evaluate discrimination under class imbalance
- Compared default (0.5) and optimized probability thresholds, selecting the F1-maximizing cutoff
- Incorporated a business constraint (maximum 500 daily investigations) to determine a practical operating threshold

## Key Findings
- Demonstrated the accuracy paradox: a naive model achieved 99.83% accuracy while failing to detect any fraud
- Logistic regression showed strong discriminatory power, with high ROC-AUC and meaningful PR-AUC for the minority class
- The optimal decision threshold differed materially from 0.5, significantly improving recall without excessive false positives
- Applying operational constraints enabled selection of a threshold aligned with real-world investigative capacity
