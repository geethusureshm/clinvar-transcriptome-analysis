# ClinVar–Transcriptome Immune Integration Analysis

## 🧬 Overview

This study integrates **ClinVar pathogenic variant data** with **RNA-seq transcriptomic profiling** to identify immune-associated candidate genes.

The workflow includes:
- Quality control (PCA analysis)
- Differential expression analysis (volcano plot)
- Functional enrichment (GO & KEGG)
- ClinVar immune gene extraction
- Integrated candidate gene prioritization

---

## 🎯 Objectives

- Perform transcriptome quality control using PCA
- Identify differentially expressed genes (DEGs)
- Visualize gene expression changes using volcano plots
- Perform GO and KEGG enrichment analysis
- Extract immune-related genes from ClinVar
- Integrate clinical and transcriptomic evidence

---

## 📊 Data Sources

### 1. ClinVar Dataset
- Variant annotations (VCF-derived TSV)
- Gene information (GENEINFO)
- Disease associations (CLNDN)
- Clinical significance (CLNSIG)

### 2. RNA-seq Dataset
- Expression matrix
- Differential expression results
- Statistical outputs (logFC, P.Value, adj.P.Val)

---

## Dataset
- GEO: GSE90081
- Samples: XX
- Groups: RA vs Control

## Differential Expression
- Total genes: XX
- Significant DEGs: XX up / XX down

## ClinVar Integration
- Immune ClinVar genes: 5436
- Overlap with DEGs: 11 genes

## Top Integrated Genes
ADAM17, PTPRC, ICOS, PRF1, NBN

## ⚙️ Analytical Workflow

### 🔹 1. Data Preprocessing
- Cleaning expression matrix
- Filtering low-quality genes
- Normalization of counts

---

### 🔹 2. PCA Analysis (Quality Control)

Used to assess:
- Sample clustering
- Batch effects
- Outlier detection

📌 Output:
- PCA_plot.png

---

### 🔹 3. Differential Expression Analysis

Methods:
- Linear modeling (limma/DESeq2 style)

📌 Output:
- Volcano_plot.png
- sig_ntRA.csv

---

### 🔹 4. Functional Enrichment

Performed using:
- GO enrichment
- KEGG pathway analysis

📌 Outputs:
- GO_significant.csv
- KEGG_significant.csv
- GO_barplot.png
- KEGG_barplot.png

---

### 🔹 5. ClinVar Processing

- Extracted genes from GENEINFO field
- Extracted disease annotations from CLNDN
- Extracted clinical significance (CLNSIG)

---

### 🔹 6. Immune Gene Filtering

Applied keyword-based filtering:
- immune
- autoimmune
- inflammatory
- immunodeficiency
- cytokine
- interleukin
- infection
- lymphocyte

Result:
- 5,436 immune-associated disease annotations

---

### 🔹 7. Integration Analysis

Intersection of:
- ClinVar immune genes
- Differentially expressed genes

---

## 🔬 Key Results

### Differential Expression
- Multiple dysregulated genes identified
- Moderate statistical significance (exploratory dataset)

### Enrichment Analysis
- Immune signaling pathways enriched
- Cytokine-related processes identified
- Cellular immune response pathways highlighted

### Integrated Candidates
Final prioritized genes:

- ADAM17
- PTPRC
- SHOC2
- ICOS
- NBN
- PRF1

---

## 📈 Visual Outputs

### PCA Plot
- Sample clustering and variability assessment

### Volcano Plot
- Differential gene expression visualization

### GO Enrichment Barplot
- Biological process enrichment

### KEGG Enrichment Barplot
- Pathway-level functional mapping

---

## 📁 Repository Structure
data/
results/
│
├── DEG/
├── enrichment/
├── plots/
├── integration/
│ └── integrated_candidates.csv
│
scripts/
├── 01_preprocessing.R
├── 02_pca_analysis.R
├── 03_deg_analysis.R
├── 04_enrichment_analysis.R
├── 05_clinvar_processing.R
└── 06_integration.R


---

## ⚠️ Limitations

- DEG significance is exploratory (FDR not strictly < 0.05)
- ClinVar filtering based on keyword strategy (not ontology-driven)
- Requires experimental validation for confirmation

---

## 🚀 Future Work

- GO-term ontology-based immune filtering
- Batch correction improvement
- Machine learning-based gene prioritization
- Experimental validation of candidate genes
- Multi-condition transcriptome comparison

---

## 🧠 Biological Interpretation

This integrative approach demonstrates that combining:
- Clinical variant databases (ClinVar)
- Transcriptomic perturbation data

improves prioritization of immune-relevant genes beyond traditional DEG analysis.

---

## 👩‍🔬 Author

Geethu Suresh  
PhD Biotechnology  

