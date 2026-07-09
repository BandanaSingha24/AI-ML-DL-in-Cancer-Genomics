# 01. Python Foundation for Cancer Genomics
This module focuses on building a strong foundation in Python and Data Science libraries to analyze and visualize cancer genomic datasets, specifically targeting breast cancer.

## 🛠️ Tech Stack & Core Libraries
* **Google Colab:** Cloud-based development environment.
* **NumPy:** Numerical computations and multi-dimensional array handling.
* **Pandas:** Loading, cleaning, and filtering large TCGA expression matrices.
* **Matplotlib & Seaborn:** Statistical data visualization and plotting profiles.
* **Biopythan:** Biological computation, sequence transcription & translation and remote NCBI BLAST quarying

## 💻 Implemented Logics & Functions
### 1. Data Processing
* `pd.read_csv()` & `df.head()`: Loaded and inspected the structural dimensions of the Breast Cancer (TCGA) dataset.
* `df.sort_values()`: Filtered and identified highly expressed oncogenes.
* `df.corr()`: Generated a correlation matrix to identify overlapping genetic expressions.

### 2. Genomic Visualization
* `sns.histplot(kde=True)`: Plotted the distribution curve of the `rs_MMP11` gene expression.
* `sns.scatterplot()`: Mapped the direct expression correlation between `rs_FOXA1` and `rs_AGR2`.
* `sns.heatmap()`: Constructed an annotated grid (`cmap='coolwarm'`) to visualize co-expression networks among top 10 cancer genes.
### 3. Biopython Basics & Sequence Analysis (NCBI Workflow)
* **`from Bio.Seq import Seq`**: Performed DNA sequence transcription and translation to identify the correct protein sequence from the Open Reading Frame (ORF).
* **`from Bio.Blast import NCBIWWW`**: Executed a live remote NCBI BLAST search using a customized **PAM30 matrix** optimized for short peptide sequences (`MKIVMLSLKLYL`).
* **`from Bio.Blast import NCBIXML`**: Parsed the resulting XML data to extract top matching protein alignments and analyzed their statistical significance based on E-values.


## 📊 Key Research Insights
* **MMP11 Biomarker:** High expression of `rs_MMP11` correlates directly with tumor progression and potential metastasis pathways.
* **FOXA1-AGR2 Co-expression:** Strong positive correlation detected, serving as a significant indicator for Luminal breast cancer subtypes.
