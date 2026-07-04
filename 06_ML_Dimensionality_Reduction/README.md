# TCGA BRCA mRNA Dimensionality Reduction

## Project Overview
The primary objective of this project is to analyze high-dimensional mRNA gene expression data from the **TCGA Breast Invasive Carcinoma (BRCA)** dataset. We have employed advanced dimensionality reduction techniques, specifically **PCA** and **UMAP**, to simplify and visualize the complex genomic landscape.

## Data Source
* **Dataset:** TCGA PanCancer Atlas (mRNA Expression, RSEM-normalized).
* **Platform:** [cBioPortal](https://www.cbioportal.org/)

## Methodology & Steps

### 1. Data Preprocessing
* **Cleaning:** Handled missing values and structured the gene expression matrix for analysis.
* **Standardization:** Applied `StandardScaler` to normalize the data, ensuring all genes contribute equally to the model.

### 2. PCA (Principal Component Analysis)
* **Objective:** Reduced the feature space from thousands of genes to 50 Principal Components.
* **Result:** Successfully preserved the main variance of the dataset while filtering out technical noise.

### 3. UMAP Projection
* **Objective:** Projecting the reduced PCA output into a 2D space for visualization.
* **Result:** Created an intuitive visual plot where patient clusters are clearly observable.

## Key Results
* Successfully reduced the dataset from **5,131 features** to a **2D visualization**.
* This analysis provides a robust foundation for identifying potential cancer subtypes and patient clusters.
