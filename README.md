# Machine Learning and Single-Cell Multi-Omics Analysis of Lipid Metabolism in Prostate Cancer

### 🧬 Overview
This repository contains data, code, and analysis scripts for the study:

**"Integrative Machine Learning and Single-Cell Multi-Omics Analysis Reveals Lipid Metabolism–Related Signatures Driving Prostate Cancer Progression."**

This project explores how lipid metabolism contributes to prostate cancer (PCa) development, heterogeneity, and prognosis using a combination of **multi-omics**, **single-cell RNA sequencing (scRNA-seq)**, and **machine learning** approaches.


### 📚 Background
Lipid metabolic reprogramming is a hallmark of prostate cancer and plays a crucial role in tumor growth, androgen receptor (AR) signaling, and therapeutic resistance.  
Using integrative bioinformatics and computational modeling, this project identifies **key lipid metabolism–related genes** and develops **machine learning–based prognostic models** to predict clinical outcomes and identify potential therapeutic targets.


### ⚙️ Methods Summary

- **Datasets:**
  - TCGA-PRAD (The Cancer Genome Atlas, Prostate Adenocarcinoma)
  - GEO single-cell dataset: **GSE206962**
  - Validation datasets from **PCaDB** and other external cohorts
  - Proteomic data from **The Human Protein Atlas**

- **Analytical Workflow:**
  1. **Data preprocessing:** Quality control, normalization, and filtering using R (`Seurat`, `DESeq2`)
  2. **Single-cell analysis:** Clustering, cell-type annotation, and gene module scoring (`UCell`, `AUCell`, `AddModuleScore`, `ssGSEA`)
  3. **Dimensionality reduction:** PCA, t-SNE, and UMAP visualization
  4. **Machine learning:** LASSO-Cox and Regularized Cox modeling for prognostic gene identification (`glmnet`)
  5. **Functional enrichment:** GO, KEGG, and GSEA analysis (`clusterProfiler`)
  6. **Spatial transcriptomics:** Visualization of fatty acid biosynthesis and β-oxidation activity
  7. **Model validation:** ROC curve, Kaplan–Meier survival, and nomogram construction (`rms` package)

---

### 🧠 Key Findings

- Identified hub genes **HMGCR, MVK, STARD3, FADS1, and APOE** as central regulators of lipid metabolism in prostate cancer.  
- Single-cell analysis revealed strong **heterogeneity of lipid metabolic activity** among epithelial and endothelial subpopulations.  
- Machine learning established a **29-gene prognostic signature** that stratified patients by survival risk.  
- Spatial transcriptomics showed regional enrichment of lipid synthesis and oxidation pathways.  
- Results support lipid metabolism as a potential **therapeutic target** and **biomarker source** in prostate cancer.



### 🧩 Repository Structure

├── data/
│ ├── TCGA_PRAD_expression.csv
│ ├── GSE206962_scRNAseq/
│ └── PCaDB_validation/
├── scripts/
│ ├── preprocessing.R
│ ├── singlecell_analysis.R
│ ├── machine_learning_model.R
│ ├── enrichment_analysis.R
│ └── visualization.R
├── figures/
│ ├── UMAP_clusters.png
│ ├── KaplanMeier_survival.png
│ └── Spatial_transcriptomics.png
├── results/
│ ├── prognostic_model_coefficients.csv
│ ├── DEG_list.csv
│ └── pathway_enrichment.xlsx
├── LICENSE
└── README.md
