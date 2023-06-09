
# Kostyrko Multiomics Analysis for Methylation EPIC and RNAseq
# Description
This repository contains a set of R scripts specifically designed for the data analysis performed in Kostyrko et al. The repository provides a set of R scripts for analyzing Methylation EPIC and RNAseq (correlation and survival analysis) used in the original paper. This respository is a resource for researchers looking to replicate or build upon the findings of Kostyrko et al.

* PMID: 37407562 PMCID: PMC10322837 DOI: 10.1038/s41467-023-39591-2
* https://pubmed.ncbi.nlm.nih.gov/37407562/
# Features
## Methylation EPIC Analysis & RNAseq Correlation: 
  + This repo is tailored to handle Methylation EPIC data and RNAseq correlation analysis as performed in the Kostyrko et al study.
  + Survival Analysis & Miscellaneous RNAseq Analysis: 
# Data
The dataset used for the Kostyrko et al study can be accessed from the GEO SuperSeries under the accession number GSE198289.
### This SuperSeries is composed of the following SubSeries:
  + GSE198289	UHRF1 is a mediator of KRAS driven oncogenesis in lung adenocarcinoma [RNA-seq]
  + GSE198446	UHRF1 is a mediator of KRAS driven oncogenesis in lung adenocarcinoma [epic_methyl]
  + GSE209923	UHRF1 is a mediator of KRAS driven oncogenesis in lung adenocarcinoma [shRNA]
  + GSE233401	UHRF1 is a mediator of KRAS driven oncogenesis in lung adenocarcinoma [CRISPR_screen]
# Minimum Requirements
  * Download and install R from here. R (3.6.2) 
  * Download the dataset from GEO SuperSeries GSE198289.
  * R packages
 
    + edgeR (3.28.1) 
    + Minfi (1.32)
    + EpiDISH (2.2.2)
    + limma package(3.42.2)
    + missMethyl (1.20.4)
    + DMRcate (2.0.7)
    + survminer (0.4.6.999) and survival (3.1.11) 
    + DGCA (1.0.2 )
    + methylGSA (1.4.9) 
## additional packages 
  <details>
  <summary>Click to expand Bioinformatics and Genomics packages!</summary>
  
  ### Genomic Data Annotation:
  1. `library(biomaRt)`: Tools for BioMart databases (like Ensembl).
  2. `library(BSgenome)`: Infrastructure for Bioconductor packages using large-scale genomic or other data.
  3. `library(org.Hs.eg.db)`: Mapping information for human genes.
  4. `library(GenomicFeatures)`: Tools for making and manipulating transcript centric annotations.
  5. `library(IlluminaHumanMethylation450kanno.ilmn12.hg19)`: Annotation data for the Illumina Human Methylation 450k array.
  6. `library(IlluminaHumanMethylationEPICanno.ilm10b4.hg19)`: Annotation data for the Illumina Human Methylation EPIC array.
  7. `library(IlluminaHumanMethylationEPICmanifest)`: Manifest file for Illumina's EPIC methylation arrays.
  8. `library(Homo.sapiens)`: Annotation data for the human genome.
  9. `library(rtracklayer)`: An interface to genome annotation files and the UCSC genome browser.

  ### Genomic Data Analysis (Omics):
  1. `library(DESeq2)`: Differential gene expression analysis based on the negative binomial distribution.
  2. `library(edgeR)`: Empirical analysis of digital gene expression data in R.
  3. `library(GenomicRanges)`: Representations and manipulations of genomic intervals and variables defined along a genome.
  4. `library(GSVA)`: Gene set variation analysis for microarray and RNA-seq data.
  5. `library(Gviz)`: Plotting data and annotation information along genomic coordinates.
  6. `library(minfi)`: Tools to analyze Illumina's methylation arrays.
  7. `library(missMethyl)`: Analyzes differential methylation in the context of GC content.
  8. `library(methylGSA)`: Gene set testing for Illumina's methylation arrays.
  9. `library(pathview)`: Plots pathway maps and overlays experimental data.
  10. `library(sva)`: Surrogate Variable Analysis: identification and adjustment for hidden confounding factors.
  11. `library(biovizBase)`: Basic graphic utilities for visualization of genomic data.
  12. `library(ggbio)`: Visualization tools for genomic data.
  13. `library(limma)`: Linear models for microarray data.
  14. `library(pathfindR)`: An R package for comprehensive identification of enriched pathways in omics data through active subnetworks
  15. `library (DGCA)`: #Differential Gene Correlation Analysis

  
  ### Genomic Data Analysis (Epigenetics):
  1. `library(EpiDISH)`: Epigenetic Dissection of Intra-Sample-Heterogeneity.
  2. `library(DMRcate)`: Detecting differentially methylated regions in CpG methylation data.
  
  ### Heatmaps and Clustering:
  1. `library(clusterProfiler)`: Statistical analysis and visualization of functional profiles for genes and gene clusters.
  2. `library(ComplexHeatmap)`: Making complex heatmaps.
  3. `library(d3heatmap)`: Interactive heatmaps.
  4. `library(dendextend)`: Extending R's dendrogram functionality.
  5. `library(dendroextras)`: Extra functions to cut, label and colour dendrogram clusters.
  6. `library(parallelDist)`: Parallel distance matrix computation.
  
  ### Visualization:
  1. `library(corrplot)`: Visualization of a correlation matrix.
  2. `library(factoextra)`: Extract and visualize the results of multivariate data analyses.
  3. `library(ggdendro)`: Create dendrograms using ggplot.
  4. `library(ggplot2)`: An implementation of the Grammar of Graphics.
  5. `library(ggplotify)`: Convert plot function call to 'ggplot' objects.
  6. `library(ggpubr)`: 'ggplot2' based publication ready plots.
  7. `library(ggpval)`: Annotate statistical significance onto 'ggplot' objects.
  8. `library(ggrepel)`: Automatically position non-overlapping text labels with 'ggplot2'.
  9. `library(gplots)`: Various R programming tools for plotting data.
  10. `library(gridExtra)`: Miscellaneous functions for "grid" graphics.
  11. `library(kableExtra)`: Build complex HTML or 'LaTeX' tables using 'kable()' and pipe syntax.
  12. `library(patchwork)`: The composer of ggplots.
  13. `library(RColorBrewer)`: ColorBrewer palettes.
  14. `library(VennDiagram)`: Generate high-resolution Venn and Euler plots.
  15. `library(Vennerable)`: Venn and Euler area-proportional diagrams.
  16. `library(wesanderson)`: Wes Anderson color palettes.
  17. `library(igraph)`: Network analysis and visualization.
  18. `library (ggbeeswarm)` # Beeswarm plots helper
  19. `library(forestplot)` # forest plot helper, mostly use in meta-analysis
  20. `library (ggridges)` # Ridgeline plots 
  21. `library(cowplot)` # functions to align plots and arrange them into complex compound figures
  
  ### Statistical Analysis:
  1. `library(FactoMineR)`: An R package for multivariate analysis.
  2. `library(fgsea)`: Fast gene set enrichment analysis.
  3. `library(MASS)`: Functions and datasets to support Venables and Ripley's MASS.
  4. `library(matrixStats)`: Functions that apply to rows and columns of matrices (and to vectors).
  5. `library(PerformanceAnalytics)`: Econometric tools for performance and risk analysis.
  6. `library(psych)`: Procedures for psychological, psychometric, and personality research.
  7. `library(survival)`: Survival analysis.
  8. `library(survminer)`: Drawing survival curves using 'ggplot2'.
  9. `library(vegan)`: Community Ecology Package.
  10. `library(scales)`: Scale functions for visualization.
  11. `library(Rtsne)`: T-distributed stochastic neighbor embedding using a Barnes-Hut implementation.
  12. `library(umap)`: Uniform Manifold Approximation and Projection.
  
  ### Data Manipulation:
  1. `library(data.table)`: Extension of `data.frame`.
  2. `library(dplyr)`: A grammar of data manipulation.
  3. `library(DT)`: A wrapper of the JavaScript library 'DataTables'.
  4. `library(forcats)`: Tools for working with categorical variables (factors).
  5. `library(plyr)`: Tools for splitting, applying and combining data.
  6. `library(reshape)`: Flexibly reshape data.
  7. `library(stringr)`: Simple, consistent wrappers for common string operations.
  8. `library(tidyr)`: Easily tidy data with 'spread()' and 'gather()' functions.

  ### Document Generation and Reporting:
  1. `library(knitr)`: A general-purpose tool for dynamic report generation in R.
  2. `library(pander)`: An R Pandoc writer.
  3. `library(stargazer)` # LATEX, HTML and ASCII tables from R statistical output
  
  ### File I/O:
  1. `library(openxlsx)`: Read, write and edit XLSX files.
  

  
</details>

## Additional public datasets

| LUAD, survival, correlations | RNAseq Counts      | Broad GDAC ( Firehose ) | [https://gdac.broadinstitute.org/runs/stddata__2016_01_28/data/LUAD/20160128/gdac.broadinstitute.org_LUAD.Merge_rnaseqv2__illuminahiseq_rnaseqv2__unc_edu__Level_3__RSEM_genes__data.Level_3.2016012800.0.0.tar.gz](https://gdac.broadinstitute.org/runs/stddata__2016_01_28/data/LUAD/20160128/gdac.broadinstitute.org_LUAD.Merge_rnaseqv2__illuminahiseq_rnaseqv2__unc_edu__Level_3__RSEM_genes__data.Level_3.2016012800.0.0.tar.gz) |
| ---------------------------- | ------------------ | ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Pathway                      | database           | MSigDB                  | [https://www.gsea-msigdb.org/gsea/msigdb](https://www.gsea-msigdb.org/gsea/msigdb)                                                                                                                                                                                                                                                                                                                                                     |
| EPIC annotation              | Probe annotations  | Bioconductor            | [https://bioconductor.org/packages/release/data/annotation/html/IlluminaHumanMethylationEPICanno.ilm10b4.hg19.html](https://bioconductor.org/packages/release/data/annotation/html/IlluminaHumanMethylationEPICanno.ilm10b4.hg19.html)                                                                                                                                                                                                 |
| TSG annotation               | Annotations        | UTHealth                | [https://bioinfo.uth.edu/TSGene/download.cgi?csrt=9609930864565957852](https://bioinfo.uth.edu/TSGene/download.cgi?csrt=9609930864565957852)                                                                                                                                                                                                                                                                                           |
| Probe Filter                 | Annotations        | github                  | [https://github.com/sirselim/illumina450k_filtering](https://github.com/sirselim/illumina450k_filtering)                                                                                                                                                                                                                                                                                                                               |
| ERV                          | Genomic annotation | UCSC genome             | [https://genome.ucsc.edu/cgi-bin/hgTables?hgta_doMainPage=1&hgta_group=rep&hgta_track=rmsk&hgta_table=rmsk](https://genome.ucsc.edu/cgi-bin/hgTables?hgta_doMainPage=1&hgta_group=rep&hgta_track=rmsk&hgta_table=rmsk)                                                                                                                                                                                                                 |
| RNAseq index                 | Genomic index      | GENCODE                 | [ftp://ftp.ebi.ac.uk/pub/databases/gencode/Gencode_human/release_37/GRCh38.primary_assembly.genome.fa.gz](ftp://ftp.ebi.ac.uk/pub/databases/gencode/Gencode_human/release_37/GRCh38.primary_assembly.genome.fa.gz)                                                                                                                                                                                                                     |
| RNAseq GTF                   | Gene Annotation    | GENCODE                 | [ftp://ftp.ebi.ac.uk/pub/databases/gencode/Gencode_human/release_37/gencode.v37.annotation.gtf.gz](ftp://ftp.ebi.ac.uk/pub/databases/gencode/Gencode_human/release_37/gencode.v37.annotation.gtf.gz)                                                                                                                                                                                                                                   |
