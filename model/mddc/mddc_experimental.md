---
layout: default
title: A description of experiments related to monocyte derived DCs in the context of A. fumigatus
---

## Table of Contents  
*  [_In vitro_ time-series RNAseq data from monocyte derived dendritic cells exposed to _A. fumigatus_ conidia (Experiment DCcocultAF).](titledccocultaf)
    1. [Description](#briefdescriptiondccocultaf)  
    2. [Data availability](#dataavailabilitydccocultaf)
<figure>
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbdee7c1b2cfe0661e5620/download?contentDisposition=inline" width="200" height="150"/>
</figure>


## __In vitro__ time-series RNAseq data from monocyte derived dendritic cells exposed to A. fumigatus conidia (Experiment DCcocultAF).

<a name="briefdescriptiondccocultaf"/>
### Description
Monocyte derived dendritic cells from six different human donors (IL-4/GM-CSF differentiated) were exposed to _Aspergillus fumigatus_ conidia with cell:conidia ratio=1:1 for 0, 2, 4, 6, 8 hours. Purity of dendritic cells was confirmed by flow cytometry using CD14-/Cd1a+/HLA+/CD83+.  


<a name="dataavailabilitydccocultaf"/>

### Data Availability
<a name="dat"/>
All data associated with the monocyte derived dendritic cells lives in the [Dendritic Cell Module collection](https://data.nutritionallungimmunity.org/#collection/5d69826fef2e2603553c5677) in our Girder Instance. In particular, in the Girder Instance, the following can be found.
#### [FASTQ files](https://data.nutritionallungimmunity.org/#collection/5d69826fef2e2603553c5677/folder/5d70041def2e2603553c567f)
Contains raw FASTQ files from two different runs on different days. **For analysis, samples that correspond to the same donor were merged together.** Files are named in the standard Illumina convention. The sample name D[donor number][timepoint] identifies the origin of the sample and how long the DCs were cocultured for.
#### [Experimental Notebooks](https://data.nutritionallungimmunity.org/#collection/5d69826fef2e2603553c5677/folder/5d939b55ef2e2603553c56bd)
Contains laboratory notebooks of the protocols utilized for differentiating monocytes to dendritic cells, as well as clinical data related to the samples (age, sex, blood type, etc.)

To see how the data was preprocessed, head to the <a href="{{ site.baseurl }}{% link model/mddc/mddc_bioinformatics.md %}">bioinformatics section for DCs (Experiment DCcocultAF)</a>.
