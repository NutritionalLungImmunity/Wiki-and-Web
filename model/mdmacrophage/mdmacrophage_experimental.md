---
layout: default
title: A description of the monocyte derived macrophage behaviour and all associated data.
---

<figure>
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce407c1b2cfe0661e562f/download?contentDisposition=inline" width="200" height="150"/>
</figure>

## Table of Contents  
*  [_In vitro_ time-series RNAseq data from monocyte derived macrophages exposed to _A. fumigatus_ conidia (Experiment McocultAF).](#titlemcocultaf)
    1. [Description](#briefdescriptionmcocultaf)  
    2. [Data availability](#dataavailabilitymcocultaf)

<a name="titlemcocultaf">

## __In vitro__ time-series RNAseq data from monocyte derived macrophages exposed to A. fumigatus conidia.

<a name="briefdescriptionmcocultaf">
### Description
Monocyte derived macrophages from six different human donors (M-CSF differentiated) were exposed to _Aspergillus fumigatus_ conidia with cell:conidia ratio=1:1 for 0, 2, 4, 6, 8 hours. Purity of macrophages was confirmed by flow cytometry using surface markers CD14+/CD68+/CD163+.

<a name="dataavailabilitydccocultafmcocultaf">
### Data Availability
All data associated with the monocyte derived macrophages lives in the [Dendritic Cell Module collection](https://data.nutritionallungimmunity.org/#collection/5d41dcf7ef2e26236e2bb3ef) in our Girder Instance. In particular, in the Girder Instance, the following can be found.


#### [FASTQ files](https://data.nutritionallungimmunity.org/#collection/5d41dcf7ef2e26236e2bb3ef/folder/5d41de08ef2e26236e2bb3f2)
Contains raw FASTQ files from two different runs on different days. **For analysis, samples that correspond to the same donor were merged together.** Files are named in the standard Illumina convention. The sample name D[donor number][timepoint] identifies the origin of the sample and how long the DCs were cocultured for.
#### [Experimental Notebooks](https://data.nutritionallungimmunity.org/#collection/5d69826fef2e2603553c5677/folder/5d939b55ef2e2603553c56bd)
Contains laboratory notebooks of the protocols utilized for differentiating monocytes to dendritic cells, as well as clinical data related to the samples (age, sex, blood type, etc.)

To see how the data was preprocessed, head to the <a href="{{ site.baseurl }}{% link model/mdmacrophage/mdmacrophage_bioinformatics.md %}">bioinformatics section for macrophages (Experiment McocultAF)</a>.
