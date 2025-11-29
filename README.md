                                          ######Differential Gene Expression Analysis of PLCG2 Variants in Alzheimer’s Disease######

**Description**

This project investigates differential gene expression patterns associated with risk and protective PLCG2 variants in Alzheimer’s disease using raw RNA count data. The workflow uses R for data preprocessing, normalization, statistical testing, and visualization of variant-specific transcriptional changes.

**Workflow Overview**

     1. Data Preparation and Filtering (R Script)

Load raw RNA count data and rename sample columns for consistency.

Filter out genes with low expression (<100 total reads) to reduce noise.

Construct metadata describing sample genotypes (WT, KO, risk, protective).

     2. Differential Expression Analysis (R Script)

Use DESeq2 for normalization and model fitting.

Perform contrast analysis comparing PLCG2 risk vs. protective variants.

Generate MA plots and extract significantly upregulated and downregulated genes.

**Datasets Used**

GSE308813_20240829_LB_rna_counts_only.csv
(Source: NCBI, Accession: GSE308813) — Raw RNA count matrix for samples carrying various PLCG2 genotypes.

**Packages Used**

R Environment

R.utils – Data handling

tidyverse – Data manipulation and plotting

DESeq2 – Differential expression analysis

**Key Results**

regulated_genes.csv – Significantly upregulated and downregulated genes in risk vs. protective PLCG2 variants

Differential expression of genes between protective and risk variants.png – MA plot visualization

Files in This Repository

differential_expression_analysis.R – Main R script for preprocessing, differential expression testing, and visualization

**Important Notes**

Gene filtering improves statistical robustness by removing low-count noise.

DESeq2 normalization accounts for library size, dispersion, and sample variability.

Analysis highlights molecular differences between PLCG2 risk and protective variants relevant to Alzheimer’s disease research.

Script includes detailed comments to ensure reproducibility.
