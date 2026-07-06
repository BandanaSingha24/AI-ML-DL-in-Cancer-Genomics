# Cancer Genomics Clustering Project

This project focuses on the computational analysis of genomic data using advanced machine learning techniques to identify cancer subgroups.

## **Project Overview**
The objective is to cluster genomic samples into distinct groups using unsupervised learning, specifically to understand breast cancer genomics (TCGA-BRCA data).

## **Workflow Steps & Results**

### **Step 1: Dimensionality Reduction (UMAP)**
* **Action**: Reduced high-dimensional genomic features into 2D space.
* **Result**: Created a clear visualization of data distribution, making it ready for clustering.

### **Step 2: K-Means Clustering**
* **Action**: Partitioned the data into 3 distinct clusters.
* **Result**: Successfully identified 3 main subgroups within the genomic samples.

### **Step 3: Hierarchical Clustering (Dendrogram)**
* **Action**: Analyzed the hierarchical structure of the data using a dendrogram.
* **Result**: Validated the 3-cluster partition through hierarchical relationships.

### **Step 4: Cluster Stability Analysis (Resampling)**
* **Action**: Performed 50 iterations of resampling-based clustering.
* **Result**: Confirmed the robustness of our 3 subgroups, demonstrating high consistency across iterations.

### **Step 5: Cluster Distribution Analysis**
* **Action**: Quantified the number of samples in each cluster.
* **Result**: Found a balanced distribution of samples (Cluster 0: 537, Cluster 1: 704, Cluster 2: 739) ready for downstream classification.

## **Conclusion**
The analysis confirms that the genomic data naturally divides into 3 stable subgroups, providing a solid foundation for further classification and clinical research.
