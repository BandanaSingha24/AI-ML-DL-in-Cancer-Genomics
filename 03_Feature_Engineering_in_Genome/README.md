# BRCA1 Gene Mutation Analysis and AI Classification

This repository contains my practice work in bioinformatics, focusing on analyzing the BRCA1 gene to identify mutations and using machine learning for genomic sequence classification.

## Bioinformatics Methodology

The analysis follows this scientific step-by-step pipeline:

### 1. Data Acquisition & Pre-processing

* **Action:** Loaded the reference (normal) and mutated DNA sequences.
* **Result:** Data cleaned and formatted for comparative analysis.

### 2. Sequence Encoding (Label/Integer Encoding)

* **Action:** Performed initial **Sequence Encoding** to convert DNA characters (A, T, C, G) into numeric values.
* **Result:** Successfully converted raw sequence data into a numeric representation.

### 3. K-mer Generation

* **Action:** Decomposed the encoded sequences into **K-mers** to extract overlapping fragments for pattern recognition.
* **Result:** Created structured sequence fragments for systematic analysis.

### 4. Mutation Identification

* **Action:** Performed sequence alignment to identify variations between reference and mutated DNA.
* **Result:** Detected a significant **Deletion** mutation in the BRCA1 gene.

### 5. Protein Translation & Functional Impact

* **Action:** Translated the sequences into amino acid chains to evaluate biological function.
* **Result:** Identified severe truncation (2362 vs. 116 amino acids), confirming functional impairment.

### 6. One-Hot Encoding

* **Action:** Applied **One-Hot Encoding** to process the sequences into a high-dimensional binary format.
* **Result:** Transformed numeric data into a machine-readable binary vector.

### 7. Mutation Matrix Generation

* **Action:** Compiled the encoded data into a structured **Mutation Matrix**.
* **Result:** Generated a matrix of shape (7088, 2) to represent the structural impact of the mutation.

### 8. Machine Learning Classification

* **Action:** Utilized a `RandomForestClassifier` to build an AI model.
* **Result:** The model learned to distinguish between normal and mutated DNA with an accuracy of ~56%.

## Learning Outcomes

Through this practice, I have gained hands-on experience in:

* **Handling** genomic datasets and K-mer analysis.
* **Executing** multi-stage Encoding (Sequence & One-Hot) and Matrix generation.
* **Integrating** machine learning workflows with biological data.
