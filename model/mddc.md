---
layout: default
title: A description of the monocyte derived dendritic cell behaviour and all associated data.
---
<figure>
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbdee7c1b2cfe0661e5620/download?contentDisposition=inline" width="200" height="150"/>
</figure>

# Bioinformatics

## __In vitro__ time-series RNAseq data from monocyte derived dendritic cells exposed to A. fumigatus conidia.
### Description
Monocyte derived dendritic cells from six different human donors (IL-4/GM-CSF differentiated) were exposed to _Aspergillus fumigatus_ conidia with cell:conidia ratio=1:1 for 0, 2, 4, 6, 8 hours. Purity of dendritic cells was confirmed by flow cytometry using CD14-/Cd1a+/HLA+/CD83+.  

### Data Availability
All data associated with the monocyte derived dendritic cells lives in the [Dendritic Cell Module collection](https://data.nutritionallungimmunity.org/#collection/5d69826fef2e2603553c5677) in our Girder Instance. In particular, in the Girder Instance, the following can be found.

#### [FASTQ files](https://data.nutritionallungimmunity.org/#collection/5d69826fef2e2603553c5677/folder/5d70041def2e2603553c567f)
Contains raw FASTQ files from two different runs on different days. **For analysis, samples that correspond to the same donor were merged together.** Files are named in the standard Illumina convention. The sample name D[donor number][timepoint] identifies the origin of the sample and how long the DCs were cocultured for.
#### [Experimental Notebooks](https://data.nutritionallungimmunity.org/#collection/5d69826fef2e2603553c5677/folder/5d939b55ef2e2603553c56bd)
Contains laboratory notebooks of the protocols utilized for differentiating monocytes to dendritic cells, as well as clinical data related to the samples (age, sex, blood type, etc.)
#### [Processed Data](https://data.nutritionallungimmunity.org/#collection/5d69826fef2e2603553c5677/folder/5d939bcdef2e2603553c56c7)
Contains post-processed data such as aligned read counts and quality control after alignment trimming.

### Code Availability
Scripts for preprocessing and analysis of the data for DCs can be found in the following Github repositories:

#### [Preprocessing pipeline Github repository](https://github.com/NutritionalLungImmunity/NLI_response_to_Aspergillus_fumigatus_omics_data_analysis/DCvsM_response_to_AF_preprocessing)
Contains code for a [Nextflow](https://www.nextflow.io/) pipeline for preprocessing of data and alignment of reads against the GRCh38 reference genome version 96.
#### [Differential Expression Github Repository](https://github.com/NutritionalLungImmunity/NLI_response_to_Aspergillus_fumigatus_omics_data_analysis/DCvsM_response_to_AF_analysis)
Contains R scripts for performing differential expression analysis of DCs exposed to A. fumigatus and control DCs using [DESeq2](https://bioconductor.org/packages/release/bioc/html/DESeq2.html).



# Mathematical model



# Relevant literature
