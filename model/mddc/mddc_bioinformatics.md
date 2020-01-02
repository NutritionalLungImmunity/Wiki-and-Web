---
layout: default
title: A description of the monocyte derived dendritic cell bioinformatics pipeline.
---

# Table of Contents  
*  [_In vitro_ time-series RNAseq data from monocyte derived dendritic cells exposed to _A. fumigatus_ conidia. (Experiment DCcocultAF)](#invitrotransc)
    1. [Description](#briefdescriptiondccocultaf)  
    2. [Preprocessing pipeline](#preprocessingpipelinedccocultaf)
    3. [Processed data](#processeddatadccocultaf)   


<figure>
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbdee7c1b2cfe0661e5620/download?contentDisposition=inline" width="200" height="150"/>
</figure>


<a name="invitrotransc"/>
## __In vitro__ time-series RNAseq data from monocyte derived dendritic cells exposed to A. fumigatus conidia (Experiment DCcocultAF).
<a name="briefdescriptiondccocultaf"/>
Description: Monocyte derived dendritic cells from six different human donors (IL-4/GM-CSF differentiated) were exposed to _Aspergillus fumigatus_ conidia with cell:conidia ratio=1:1 for 0, 2, 4, 6, 8 hours. Purity of dendritic cells was confirmed by flow cytometry using CD14-/Cd1a+/HLA+/CD83+. For more details, go to the <a href="{{ site.baseurl }}{% link model/mddc/mddc_experimental.md %}"> experimental section for monocyte derived DCs and see the section for (Experiment DCcocultAF).


<a name ="preprocessingpipelinedccocultaf">
## Preprocessing pipeline
The FASTQ files were aligned using a custom [Nextflow](https://www.nextflow.io/) pipeline for preprocessing of data and alignment of reads against the GRCh38 reference genome version 96.  An overview of the pipeline is below:

<figure >
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5e0e4292c1b2cfe0661e5643/download?contentDisposition=inline" />
</figure>

### Code Availability
Scripts for preprocessing and analysis of the data for DCs can be found in the following Github repositories:

#### [Preprocessing pipeline Github repository](https://github.com/NutritionalLungImmunity/NLI_response_to_Aspergillus_fumigatus_omics_data_analysis/DCvsM_response_to_AF_preprocessing)
Contains code for a [Nextflow](https://www.nextflow.io/) pipeline for preprocessing of data and alignment of reads against the GRCh38 reference genome version 96.
#### [Differential Expression Github Repository](https://github.com/NutritionalLungImmunity/NLI_response_to_Aspergillus_fumigatus_omics_data_analysis/DCvsM_response_to_AF_analysis)
Contains R scripts for performing differential expression analysis of DCs exposed to A. fumigatus and control DCs using [DESeq2](https://bioconductor.org/packages/release/bioc/html/DESeq2.html).

<a name ="#processeddatadccocultaf">
### [Processed Data](https://data.nutritionallungimmunity.org/#collection/5d69826fef2e2603553c5677/folder/5d939bcdef2e2603553c56c7)
Contains post-processed data such as aligned read counts and quality control after alignment trimming.
