**Seurat R Code Readme**

This repository contains R code for performing data analysis using the Seurat package on 20k Mixture of NSCLC DTCs from 7 donors (Single Cell Gene Expression Dataset) obtained through 10X genomics platform. The code provided demonstrates various steps in a typical analysis workflow, including data loading, quality control, filtering, normalization, identification of highly variable features, scaling, dimensionality reduction, clustering, and visualization using Seurat.

**Installation**

The following packages were installed:
Seurat,
SeuratDisk,
tidyverse


**Usage**

Load the NSCLC dataset: The code reads the input data from an h5 file using the Read10X_h5() function. 

Initialize the Seurat object: The code creates a Seurat object using the CreateSeuratObject() function, providing the count matrix (cts) and project name. 

Quality Control (QC): This section performs QC on the data, including checking the percentage of mitochondrial reads, visualizing QC metrics using violin plots and scatter plots.

Filtering: The code filters out cells based on specified criteria, including the number of expressed features (nFeature_RNA) and the percentage of mitochondrial reads.

Normalization: This section performs data normalization using the NormalizeData() function. Two options are provided: log-normalization with a scale factor of 10,000 or the default method.

Identifying highly variable features: The code identifies highly variable features using the FindVariableFeatures() function and visualizes them using a feature plot.

Scaling: This section scales the data using the ScaleData() function.

Dimensionality reduction: The code performs principal component analysis (PCA) using the RunPCA() function and visualizes the PCA results using various plots. It also includes an elbow plot to determine the appropriate number of dimensions to retain.

Clustering: This section performs clustering analysis using the FindNeighbors() and FindClusters() functions. The code assigns cluster identities and visualizes the clusters using dimensionality reduction plots.

Non-linear dimensionality reduction: The code performs uniform manifold approximation and projection (UMAP) using the RunUMAP() function and visualizes the results.


**References**

Seurat: https://satijalab.org/seurat/
SeuratDisk: https://satijalab.org/seurat-disk/
