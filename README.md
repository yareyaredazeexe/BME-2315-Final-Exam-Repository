# **Module 3 — Evading Apoptosis in Breast Cancer (BRCA)**

### **Team Members:**

Hazel Miranda and Michael Dornic

---

## **📌 Project Title**

**Understanding Gene Dysregulation in the Hallmark “Evading Apoptosis” in Breast Cancer**

---

## **📘 Project Overview**

This module investigates how breast cancer (BRCA) tumors alter apoptosis pathways using RNA-Seq gene expression data from TCGA. We focused on four key apoptosis-related genes (TP53, BCL2, BAX, BAK) and used dimensionality reduction and clustering to evaluate whether gene expression patterns reflect dysregulation of apoptotic mechanisms.

The analysis combines:

* High-dimensional RNA-seq data processing
* Dimensionality reduction using UMAP
* Unsupervised clustering using K-means
* Visualization of gene-expression gradients
* Biological interpretation of apoptosis pathway behavior

---

## **📂 Files in This Folder**

This module folder contains:

### **1. `Module_3.ipynb`**

Your full Jupyter Notebook including:

* Background on apoptosis as a cancer hallmark
* Dataset description and preprocessing
* UMAP dimensionality reduction
* Expression visualizations for TP53, BCL2, BAX, and BAK
* K-means clustering and evaluation metrics
* Conclusions, limitations, and future directions

### **2. `Module_3.pdf`**

A PDF export of the notebook for ease of viewing and submission.

### **3. `GSE62944_subsample_log2TPM.csv`**

A subsampled RNA-seq matrix containing:

* log₂(TPM + 1) normalized expression values
* Highly variable protein-coding genes
* BRCA tumor samples only

### **4. `GSE62944_metadata.csv`**

A metadata file containing:

* Tumor subtype
* Patient age and stage
* Receptor information
* Survival data

> Note: All data files are publicly available and fully de-identified.

---

## **🧬 Dataset Summary**

The dataset includes RNA-Seq gene expression values paired with clinical metadata for TCGA BRCA samples.

* **Expression Data:** log₂(TPM + 1) normalized transcript counts
* **Metadata:** age, subtype, stage, survival, clinical variables
* **Focus Genes:** TP53, BCL2, BAX, BAK — core regulators of mitochondrial apoptosis

These genes were chosen for their critical involvement in cell-death signaling and their known dysregulation in breast cancer.

---

## **🖥️ Methods Summary**

### **Data Processing Steps**

1. Load expression and metadata

2. Merge datasets by TCGA sample barcodes  
3. Extract apoptosis-related genes  
4. Prepare data for dimensionality reduction and clustering  

### **UMAP Dimensionality Reduction**

We used UMAP to visualize global gene-expression structure.

* `n_neighbors = 10`
* `min_dist = 0.15`

UMAP allowed us to visualize patterns, gradients, and subtle subclusters in BRCA tumors.

### **K-Means Clustering**

K-means clustering was performed for **k = 2–8**, evaluated with:

* Silhouette score  
* Calinski-Harabasz score  
* Davies-Bouldin score  

### **Gene-Expression Visualization**

We plotted UMAP coordinates colored by expression levels of:

* **TP53**
* **BCL2**
* **BAX**
* **BAK**

These plots helped reveal the distribution and variability of apoptotic signaling across tumors.

---

## **📈 Key Findings**

* **BCL2** displayed a strong expression gradient across the embedding, matching known biological variation in BRCA subtypes.  
* A small distinct expression pattern emerged for **CASP8**, suggesting a subgroup with altered extrinsic apoptosis signaling.  
* UMAP revealed one dominant cluster with smaller subclusters, consistent with BRCA’s heterogeneity.  
* Clustering metrics consistently supported **k = 2**, indicating two broad expression groupings.

---

## **🔍 Validation**

We validated our approach through:

* **Cluster metrics** — Silhouette, Calinski-Harabasz, and Davies-Bouldin scores all agreed that **k = 2** was optimal.  
* **Biological consistency** — Known expression behaviors (variable TP53, subtype-dependent BCL2) matched our observed gradients.  
* **UMAP stability** — Key structures persisted across embeddings with different seeds.  

These checks confirmed that our analysis captured meaningful and reproducible patterns.

---

## **📌 Conclusions**

* Apoptosis-related genes contribute significant variation across BRCA tumors.  
* Differences in BCL2 and CASP8 expression suggest distinct apoptotic profiles among tumor subsets.  
* The hallmark “Evading Apoptosis” is active but highly heterogeneous in BRCA.

---

## **⚖️ Ethical Implications**

* All TCGA datasets used are **public and fully de-identified**, ensuring ethical use.  
* Computational analysis reduces reliance on wet-lab experiments and avoids additional human or animal sampling.  
* Interpretations must remain cautious — gene expression alone cannot determine treatment decisions without additional evidence.

---

## **⚠️ Limitations**

* Only a small apoptosis gene panel was analyzed.  
* The dataset was subsampled, limiting detail and statistical resolution.  
* UMAP is stochastic and may show slight variation across runs.  
* K-means assumes spherical clusters, which may not reflect true tumor biology.

---

## **🚀 Future Work**

* Expand analysis to the full **Hallmark Apoptosis** gene set.  
* Compare apoptosis signaling across additional cancer types.  
* Integrate mutation data (e.g., TP53) and copy-number variation.  
* Perform survival analysis based on apoptosis gene expression.  
* Validate dimensionality-reduction results using PCA or t-SNE.

---
