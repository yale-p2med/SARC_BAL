# Transcriptomics of Bronchoalveolar Lavage Cells Identifies New Molecular Endotypes of Sarcoidosis
We have conducted RNAseq analysis of the BAL samples from sarcoidosis patients recruited by the GRADS study. This repository contains supplementary information files and the analytical codes for our study. 

## Supervised Analysis
Under the Supervised_Analysis folder, we provide one file for each given clinical trait that contains its significant (FDR<0.05) associated genes identified by the supervised analysis. The file names have the format of traitname_testname_fdr0.05.txt. These files are tab delimited text files that can be open in many programs, including Excel, R, and so on. The content in the files is self-explaned.

## Supplementary Information Files
Under the supplment folder, we provide the following supplementary files.

1. Supervised analysis results:

- lists of identified genes for the clinicla traits.

- pathway enrichment analysis using GeneGO MetaCore for each gene list.

2. Unsupervised analysis results including the list of genes in each identified gene modules and their corresponding pathway enrichment analysis results.

- list of genes in each identified gene module.

- pathway enrichment analysis using GeneGO MetaCore for each gene module.

3. RDS files that contains the all the data. These files can be directly loaded into R so that readers do not have to write their own codes to load in the data.

2. Supplementary figures and tables.

## R codes for the analysis
Under the Rcodes folder, we provide the R codes that generate the figures in our manuscript.



