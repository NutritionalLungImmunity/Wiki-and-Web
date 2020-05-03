---
title: Nutritional Lung Immunity
subtitle: A description of the monocyte derived dendritic cell bioinformatics pipelines.
layout: page
show_sidebar: false
menubar: example_menu
tabs: mddc_tabs
toc: true
---
<object type="image/svg+xml" data="/media/mddcs/bioinformatics.svg" >
<!-- fallback image in CSS -->
<img src="/media/mddcs/bioinformatics.svg" width="186" height="235"/>
</object>



    <!-- alt="Workflow for bioinformatics analysis of dendritic cells"/>-->

## __In vitro__ time-series RNAseq data from monocyte derived dendritic cells exposed to A. fumigatus conidia (Experiment DCcocultAF).
Description: Monocyte derived dendritic cells from six different human donors (IL-4/GM-CSF differentiated) were exposed to _Aspergillus fumigatus_ conidia with cell:conidia ratio=1:1 for 0, 2, 4, 6, 8 hours. Purity of dendritic cells was confirmed by flow cytometry using CD14-/Cd1a+/HLA+/CD83+. For more details, go to the <a href="{{ site.baseurl }}{% link model/mddc/mddc_experimental.md %}"> experimental section for monocyte derived DCs and see the section for (Experiment DCcocultAF).

### Preprocessing pipeline
The FASTQ files were aligned using a custom [Nextflow](https://www.nextflow.io/) pipeline for preprocessing of data and alignment of reads against the GRCh38 reference genome version 96.  An overview of the pipeline is below. Click on the image to be taken to the Github repository containing the Nextflow pipeline.


#### Postprocessing analysis


#### [Differential Expression Github Repository](https://github.com/NutritionalLungImmunity/NLI_response_to_Aspergillus_fumigatus_omics_data_analysis/DCvsM_response_to_AF_analysis)
Contains R scripts for performing differential expression analysis of DCs exposed to A. fumigatus and control DCs using [DESeq2](https://bioconductor.org/packages/release/bioc/html/DESeq2.html).

#### [Processed Data](https://data.nutritionallungimmunity.org/#collection/5d69826fef2e2603553c5677/folder/5d939bcdef2e2603553c56c7)
Contains post-processed data such as aligned read counts and quality control after alignment trimming.


### References

#### Preprocessing tools
{% bibliography --query @*[keywords ~= bioinformatics_pipeline_macrophages_dcs_preprocessing] %}

#### Postprocessing tools
{% bibliography --query @*[keywords ~= bioinformatics_pipeline_macrophages_dcs_postprocessing] %}
