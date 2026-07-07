# AI & Machine Learning in Cancer Genomics

This project focuses on classifying cancer subtypes using advanced machine learning models (Random Forest, SVM, and XGBoost) applied to genomic datasets.

## Project Workflow
1. **Data Pre-processing:** Dimensionality reduction using UMAP to visualize distinct cancer clusters.
2. **Model Training:** Training Random Forest, SVM, and XGBoost classifiers.
3. **Evaluation:** Comprehensive performance analysis using Confusion Matrices, ROC-AUC, and classification metrics.

## Model Performance Summary

| Model | Precision | Recall | F1-Score |
| :--- | :--- | :--- | :--- |
| **Random Forest** | 0.9883 | 0.9882 | 0.9882 |
| **SVM** | 0.9950 | 0.9949 | 0.9949 |
| **XGBoost** | 0.9800 | 0.9797 | 0.9798 |

* **ROC-AUC Score:** Consistently ~0.99 across all models.

## Key Insights
* **SVM** emerged as the top-performing model with the highest F1-Score (0.9949).
* **Feature Importance:** Both UMAP1 and UMAP2 dimensions were found to be critical for classification, with SVM and XGBoost showing strong reliance on UMAP1.

## Conclusion
The high F1-Scores and ROC-AUC values validate that the selected machine learning models are highly reliable for clinical-grade cancer subtype classification.

## Requirements
* Python 3.x
* Scikit-learn
* XGBoost
* Pandas, Matplotlib, Seaborn

