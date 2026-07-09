
# 🧬 AI/ML & Deep Learning in Cancer Genomics

Welcome to Module 1 of my Computational Oncology pipeline. This section focuses on processing large-scale clinical metadata from the TCGA-BRCA (Breast Invasive Carcinoma) cohort to make it ready for downstream multi-omics integration and machine learning survival analysis.

---

## 🛠️ Module 1: Clinical Data Preprocessing Pipeline

### **Step 1: Data Integration & Merging**
* **Process:** Merged two separate complex clinical datasets containing patient-specific core diagnostics and sample-specific clinical tumor markers.
* **Method:** Performed an inner merge on the unique identifier `PATIENT_ID`.
* **Result:** Successfully unified the data into a single master dataframe consisting of **2,509 patient rows** and **36 clinical features**.

---

### **Step 2: Missing Value Identification**
* **Process:** Analyzed the complete dataset to map out missing values across columns before introducing any modeling bias.
* **Method:** Used custom filtering logic to isolate columns with missing values (`missing_info > 0`).
* **Result:** Identified major gaps in clinical features (e.g., `CELLULARITY` missing 592 rows, `CHEMOTHERAPY` missing 529 rows, and `RFS_MONTHS` missing 121 rows) that required systematic treatment.

---

### **Step 3: Automated Strategic Imputation**
* **Process:** Handled missing data logically using domain-specific knowledge instead of blind row deletion to prevent data loss.
* **Method:** 
  * Automatically segregated categorical (text) and numerical (numeric) datatypes.
  * Forced strict numeric conversion using `pd.to_numeric(..., errors='coerce')` to capture data format anomalies.
  * Imputed categorical missing values with an **`'Unknown'`** flag to preserve clinical variation.
  * Imputed numerical columns using the **`Median`** statistical value of each respective feature.
* **Result:** Successfully cleaned the entire dataset. **Total remaining missing values: 0**.

---

### **Step 4: Clinical Feature Engineering & Label Encoding**
* **Process:** Transformed core molecular bio-markers into machine-readable mathematical inputs.
* **Method:** Map-encoded the three main breast cancer diagnostic receptors: Estrogen Receptor (`ER_STATUS`), Progesterone Receptor (`PR_STATUS`), and Human Epidermal Growth Factor Receptor 2 (`HER2_STATUS`).
* **Mapping Logic:** `{'Positive': 1, 'Negative': 0, 'Unknown': 0}`
* **Result:** Created a binary receptor matrix highlighting molecular subtype features (e.g., identifying Luminal ER+/PR+/HER2- patient profiles).

---

### **Step 5: One-Hot Encoding & Train-Test Splitting**
* **Process:** Prepared non-binary categorical variables (like `CELLULARITY` and `CHEMOTHERAPY`) for regression algorithms and split the matrix into isolated subsets.
* **Method:** Applied `pd.get_dummies()` to create balanced multi-column binary features and executed an 80/20 train-test split via `sklearn`.
* **Result:** Expand features to **11 highly-optimized clinical inputs** and isolated:
  * **Training Set:** 2,007 patient profiles (for supervised pattern learning).
  * **Testing Set:** 502 patient profiles (saved as a hidden exam dataset for validation).
