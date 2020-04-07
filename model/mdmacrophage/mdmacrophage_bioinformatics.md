---
title: Nutritional Lung Immunity
subtitle: A description of the monocyte derived macrophages bioinformatics pipelines.
layout: page
show_sidebar: false
menubar: example_menu
tabs: mdmacrophage_tabs
toc: true
---


<a name="titlemcocultaf">
## __In vitro__ time-series RNAseq data from monocyte derived macrophages exposed to A. fumigatus conidia (Experiment McocultAF).

<a name="briefdescriptionmcocultaf">
Description: Monocyte derived macrophages from six different human donors (M-CSF differentiated) were exposed to _Aspergillus fumigatus_ conidia with cell:conidia ratio=1:1 for 0, 2, 4, 6, 8 hours. Purity of macrophages was confirmed by flow cytometry using surface markers CD14+/CD68+/CD163+.

### Preprocessing pipeline
The FASTQ files were aligned using a custom [Nextflow](https://www.nextflow.io/) pipeline for preprocessing of data and alignment of reads against the GRCh38 reference genome version 96.  An overview of the pipeline is below. Click on the image to be taken to the Github repository containing the Nextflow pipeline.


<figure >
<a href="https://github.com/NutritionalLungImmunity/NLI_response_to_Aspergillus_fumigatus_omics_data_analysis/tree/master/DCvsM_response_to_AF_preprocessing/star_pipeline">
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5e0e4292c1b2cfe0661e5643/download?contentDisposition=inline" />
</a>
</figure>

#### [Differential Expression Github Repository](https://github.com/NutritionalLungImmunity/NLI_response_to_Aspergillus_fumigatus_omics_data_analysis/DCvsM_response_to_AF_analysis)
Contains R scripts for performing differential expression analysis of macrophagess exposed to A. fumigatus and control DCs using [DESeq2](https://bioconductor.org/packages/release/bioc/html/DESeq2.html).

<a name ="processeddatamcocultaf">
### [Processed Data](https://data.nutritionallungimmunity.org/#collection/5d69826fef2e2603553c5677/folder/5d939bcdef2e2603553c56c7)
Contains post-processed data such as aligned read counts and quality control after alignment trimming.
