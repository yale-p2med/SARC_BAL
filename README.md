# Transcriptomics of Bronchoalveolar Lavage Cells Identifies New Molecular Endotypes of Sarcoidosis
We have conducted RNAseq analysis of the BAL samples from sarcoidosis patients recruited by the GRADS study. This repository contains supplementary information files and the analytical codes for our study. 

## Paper Supplement
Under the Paper_Supplement folder, we provide the supplement files for our paper including the following files. 
* Supplementary Table E1: `SupplTable_E1.xlsx`.

* Supplementary Table E2: `SupplTable_E2.xlsx`.

* Supplementary Table E3: `SupplTable_E3.xlsx`.

##

## Supervised Analysis

### Gene Lists
Under the `Supervised_Analysis/gene_lists` folder, we provide the list of associated genes identified for each given clinical trait. There are three types of association tests as follows:

* Spearman test for continuous/ordinal clinical traits. Files are named as TraitName_spearman_fdr0.05.txt. 

* Wilcoxon rank sum test for binary clinical traits. Files are named as TraitName_wilcoxon_fdr0.05.txt.

* Wilcoxon rank sum test to compare between 8 clinical phenotype groups with Non-acute Stage I, untreated, between the 4 SCADDING stages and SCADDING Stage I, and between the PFT% predicted high (>80%) and low (50% - 80%) groups. Since there are no genes with FDR<0.05 for most of these comparisons, we provide the list of genes with nominal p value<0.05 and fold change>2 or < -2. Files are named as DEGs_TraitName_pvalue0.05_FC2.0.txt. 

These files are tab delimited text files that can be open in many programs, including Excel, R, and so on. The content in the files is self-explained.

### Overlapped Gene Lists
Under the `Supervised_Analysis/overlap_genelists_2` folder, we provide the list of overlapped genes that are simultaneously associated with any two clinical traits. For each given pairs of clincal traits (trait1, traits), the corresponding result files include the following:

* file named `[trait1]_VS_[trait2]_all.txt`. This file has all the genes that are significantly associated with both trait1 and trait2.

* file named `[trait1]_VS_[trait2]_samedirection.txt`. This file has all the genes that are significantly associated with both trait1 and trait2 with the same direction. For example, genes that are positively associated with both traits.

* file named `[trait1]_VS_[trait2]_oppositedirection.txt`. This file has all the genes that are significantly associated with both trait1 and trait2 with the opposite direction. For example, genes that are positively associated with trait1 but negatively correlated with trait2.

* file named `[trait1]_VS_[trait2]_[dir1][dir2].txt`. This file has all the genes that are significantly associated with both trait1 and trait2 with directions described by dir1 and dir2, respectively. For example, genes that are positively associated with trait1 but negatively correlated with trait2 can be found in `[trait1]_[trait2]_posneg.txt`.

### Pathway Enrichment Analysis by MetaCore
Under the `Supervised_Analysis/pathway_enrichment_metacore` folder, we provide the pathway enrichment analysis results for the gene lists under the `Supervised_Analysis/gene_lists` folder. Each gene list was divided into positive and negative lists based on the correlation coefficient. MetaCore was applied to both lists.

##

## Unsupervised Analysis
Under the `Unsupervised_Analysis` folder, we provide the results for the unsupervised analysis that identified gene modules using WGCNA and performed patient clustering using each module separately.

### WGCNA gene modules
Under the `Unsupervised_Analysis` folder, the file `module_genelist.xls` provides the assignment of genes into the 48 gene modules identified by WGCNA. Since before we removed genes with no variation (SD=0) across the 209 samples, there are 20828 genes/transcripts in this file. The tracking_ids has the format of `gene.name_tss.id`. The other columns are self-explained.

### Pathway enrichment analysis of the gene modules

##

## Data and R codes
* FPKM matrix
* Clinical trait data
* R codes

##
