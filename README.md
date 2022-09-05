# Differential-Gene-Expression-Analysis-of-Single-Cell-RNAseq-data
An analysis of head and neck tumour single cell RNA sequencing data from NCBI database.

The steps involved were-

1. Integrate the data from two datasets- GSE164690, GSE103322. A tutorial from scvi tools was used for this (https://docs.scvi-tools.org/en/0.12.2/user_guide/notebooks/harmonization.html)

2. Using scanpy.pp.neighbors nearest neighbor cells (according to gene expression) were determined. scanpy.tl.leiden was used to perform clustering of similar cells. Parameters of this function can determine the total number of clusters in the end result. scanpy.tl.umap was used to plot a 2D representation (UMAP) of the clustering made by leiden.
 
3. Using scanpy.pl.rank_genes_groups common genes for every cluster were determined, and HUman Protein Atlas was used to find the corresponding cell type then, and the UMAP plotted in previous step was annotated according to the cell type.

4. scanpy.pl.rank_genes_groups_heatmap was used to plot a heatmap displaying the expression of different genes in every cell-type cluster in the UMAP.
