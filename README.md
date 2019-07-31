# Transcriptomics of Bronchoalveolar Lavage Cells Identifies New Molecular Endotypes of Sarcoidosis
We have conducted RNAseq analysis of the BAL samples from sarcoidosis patients recruited by the GRADS study. This repository contains supplementary information files and the analytical codes for our study. 

## Supervised Analysis

### Gene Lists
Under the Supervised_Analysis/gene_lists folder, we provide the list of associated genes identified for each given clinical trait. There are three types of association tests as follows:
* spearman test for continuous/ordinal clinical traits. Files are named as TraitName_spearman_fdr0.05.txt.
* wilcoxon rank sum test for binary clinical traits. Files are named as TraitName_wilcoxon_fdr0.05.txt.
* wilcoxon rank sum test to compare between 8 clinical phenotype groups with Non-acute Stage I, untreated, between the 4 SCADDING stages and SCADDING Stage I, and between the PFT% predicted high (>80%) and low (50% - 80%) groups. Since there are no genes with FDR<0.05 for most of these comparisons, we provide the list of genes with nominal p value<0.05 and fold change>2 or < -2. Files are named as DEGs_TraitName_pvalue0.05_FC2.0.txt. 

The file names have the format of traitname_testname_fdr0.05.txt. These files are tab delimited text files that can be open in many programs, including Excel, R, and so on. The content in the files is self-explaned.

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



