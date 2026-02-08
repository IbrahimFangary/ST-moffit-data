# Spatial Transcriptomics of the Preoptic Region in Mouse Hypothalamus:
## Methodological Approach

Ibrahim Fangary  
August 31st, 2024  
:contentReference[oaicite:0]{index=0}

---

## Introduction

• Using spatial transcriptomics data from Moffitt et al. (2018).  
• The data was generated using multiplexed error-robust fluorescence in situ hybridization (MERFISH).  
• Investigate spatial gene expression in the hypothalamic preoptic region of mice.  
• Analyze excitatory, inhibitory, and hybrid neural subpopulations.  
:contentReference[oaicite:1]{index=1}

---

## Methods

• Using scanpy package in python for preprocessing, clustering, and visualizing single-cell gene expression data.  
• Squidpy to spatial analysis of the dataset including neighborhood enrichment analysis and visualization of spatial data  
• The analysis consists of 4 parts  
• Data preparation  
• Preprocessing and clustering  
• Cell type identification  
• Spatial distribution of neural subpopulation  
:contentReference[oaicite:2]{index=2}

---

## Data Preparation

• utilizing jupyter notebook with Python kernel.  
• Using pandas package to handle and prepare the data.  
• Building Anndata dataframe for further analysis with scanpy.  
:contentReference[oaicite:3]{index=3}

---

## Data Preparation

• Subsetting the required Bregma section in animal 1.  
• Removing ‘Ambiguous’ cell class as identified in Moffitt et al. (2018).  
• Removing empty cells and unexpressed genes.  
• Final dataset: 28,317 cells across five Bregma sections (-0.04 mm, -0.09 mm, -0.14 mm, -0.19 mm, and -0.24 mm) and 155 genes.  
:contentReference[oaicite:4]{index=4}

---

## preprocessing and clustering

• Building a Simple Preprocessing and Clustering Function  
• The data was normalized to total count and log transformed  
• Calculating PCA, neighbors and Leiden for dimensionally reduction and clustering  
• Calculate UMAP to project the high-dimensional data  
:contentReference[oaicite:5]{index=5}

---

## Results

• Visualization of all clusters identified in each approach (PP and clustering on combined tissue and each tissue separately) to see if there any cluster specific for certain tissue.  
• Ploting umap of combined tissue once and each tissue separately  
:contentReference[oaicite:6]{index=6}

---

## Cell types identification

• Differential gene expression analysis across clusters identified marker genes for each clusters  
• Those marker genes was used to assign each cluster cell types  
• database PanglaoDB was used to identify cell types based on highly Differential expression genes.  
:contentReference[oaicite:7]{index=7}

---

## Cell types identification

tissue sections -0.19mm Combined tissue sections

• Ploting heatmap with dendogram to identify excitatory, inhibitory and hybrid clusters based on expression of Slc17a6, Slc17a7 and Gad1  
• After assigning cell types the Oligodendrocytes (OD) were not identified in tissue sections - 0.19mm  
:contentReference[oaicite:8]{index=8}

---

## Results

1

• Utilizing seaborn package to plot heatmap  
• similar trends in cell type assignment. Except Oligodendrocytes (OD) that were not identified in separate tissue  
• clusters were similar in Astrocyte, Endothelial, Ependymal, Inhibitory and Microglia  
• large portion of cells was identified as inhibitory in the case of combined tissue sections but identified as hybrid in the case of separate tissue.  
• The clusters of case of combined tissue sections stated cells heterogeneity more effectively and explored more cell types than separate tissue  
:contentReference[oaicite:9]{index=9}

---

## Spatial distribution of neural subpopulation

• Subsetting the inhibitory, excitatory and hybrid clusters and re-cluster them  
• Re-assigning the new identified clusters based on expression of Slc17a6, Slc17a7 and Gad1  
• Using the Squidpy package in python to Perform neighborhood enrichment analysis  
• Using squidpy to compare the spatial distribution of these genes with the newly identified clusters  
:contentReference[oaicite:10]{index=10}

---

## Spatial distribution of neural subpopulation

• Using squidpy for  
• Calculating neighborhood graph  
• Neighborhood Enrichment Calculation  
• Plotting the Neighborhood Enrichment Heatmap  
:contentReference[oaicite:11]{index=11}

---

## Results

• most of clusters exhibited strong spatial neighborhood relations, except for clusters 9 and 17 showeing the lowest spatial scores  
:contentReference[oaicite:12]{index=12}

---

## re-assigning the I, E and H clusters

• Each cluster was assigned to a cell type based on the expression of markers such as Slc17a6, Slc17a7, and Gad1  
• identifying 10 inhibitory subpopulations, 8 excitatory subpopulations, and 1 hybrid subpopulation  
:contentReference[oaicite:13]{index=13}

---

## Spatial distribution of neural subpopulation

• Using squidpy for  
• Calculating Spatial Neighbors  
• Computing Spatial Autocorrelation  
• Plotting scatter plot of distribution of each gene  
• Using matplotlib package in python for handling and visualization of plots  
:contentReference[oaicite:14]{index=14}

---

## Results

• The plot is inverted  
• The distribution of Slc17a6 was predominantly localized in the PVT and FX regions  
• Gad1 expression was mainly concentrated in the BST region  
:contentReference[oaicite:15]{index=15}

---

## Spatial distribution of neural subpopulation

• clusters E4, E7, and I8 were widely dispersed consistent with their lower spatial neighboring scores  
• clusters E1, E2, I1, and I3 exhibited more localized patterns  
:contentReference[oaicite:16]{index=16}

---

## Conclusion

• Combined tissue section clustering reveals greater heterogeneity.  
• Identified additional neural subtypes not detected in individual sections  
• Spatial context is crucial for understanding the organization of neural populations.  
:contentReference[oaicite:17]{index=17}

---

Thank you  
:contentReference[oaicite:18]{index=18}

# 🧠 Spatial Transcriptomics – Yalla Bioinformatics Hiring Task

This repository contains my submission for the **Yalla Bioinformatics Hiring Task**, focused on spatial transcriptomics analysis of the **preoptic region in the mouse hypothalamus**.

## Repository Contents

- `data preparation.ipynb`  
  Preprocessing and loading spatial transcriptomics data.

- `exploration and comparing.ipynb`  
  Initial data exploration and comparison of clustering annotations.

- `spatial analysis of neural cluster.ipynb`  
  In-depth analysis of neural clusters across tissue sections.

- `spatial domains prediction SpaGCN.ipynb`  
  Prediction of spatial domains using the SpaGCN algorithm.

- `Spatial Transcriptomics of the Preoptic Region in Mouse Hypothalamus.pdf`  
  A PDF report summarizing the data workflow, results, and biological insights.
