# thebaud_lung_BPD
R Notebooks for Hurskainen &amp; Mizikova et al., 2020

Raw UMI counts and associated metadata is available at the GEO accession GSE151974. Don't hesitate to contact me at david.cook [at] uottawa.ca for access to processed seurat objects or with any questions about the scripts.

A little messy at the moment, but the general ordering here is the following:

1) processing.Rmd - Demultiplexing, QC
2) differential_state_analysis.Rmd - Performs initial integration and a global DSA (though subset-specific DSA after pruning doublets is used for the paper-see below)
3) Each of the individual subset_xxx.Rmd scripts - generates major subsets, prunes doublets, DSA
4) cluster_annotations.Rmd - Brings back doublet-pruned, high-resolution clustered data from each subset into a single seurat object and manually adds cell type labels
5) cell_communication.Rmd - NicheNet analysis
