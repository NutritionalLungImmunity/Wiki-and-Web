---
layout: default
title: A description of the model, the workflow of model building, and associated data.
---

# Table of Contents  
1. [An overview of invasive pulmonary aspergillosis](#overview)
2. [Focusing on nutritional immunity](#nutritionalimmunity)  
3. [Our approach](#approach)
4. [Data associated with with the model building effort.](#datadiagram)
5. [Bridging the scales](#bridgingthescales)
<a name="overview">

# An overview of invasive pulmonary aspergillosis
<figure class="center">
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce32bc1b2cfe0661e5629/download?contentDisposition=inline" width="700" height="500"/>
</figure>


<b>High level description of IPA.</b>
<a name="lungimmunity">
# Focusing on nutritional immunity
<b>Describe the focus on iron</b>
<a name="approach">

# Our approach

## Agent-based modeling

We are building a 3D agent-based model of the innate immune response to _invasive pulmonary aspergillosis_ with a focus on the "battle over iron" that occurs in the alveolar space between the host and the fungus. [Agent-based modeling](https://en.wikipedia.org/wiki/Agent-based_model) aims to model how autonomous individuals interact with each other and their computational environment. For us, the individual agents are:

1. Alveolar macrophages.
1. Monocyte derived macrophages.
1. Monocyte derived dendritic cells (DCs).
1. Neutrophils.
1. Epithelial cells.
1. _A. fumigatus_

Agents behave according to a set of rules that are derived from literature and _de novo_ experiments. For example, the monocyte derived macrophages respond to the sensing of _A. fumigatus_ and respond accordingly to the output of an intracellular [Generalized Boolean Network](https://en.wikipedia.org/wiki/Boolean_network) (GBN). The GBN is built from a combination of literature results and analysis of a transcriptomics dataset generated as part of this project.


### Calibrating the model with experimental data

In order to build the 3D agent based model, we have performed several _in vivo_ and _in vitro_ experiments.

For example, we co-cultured monocyte derived macrophages with _A. fumigatus_ in a time-series and extracted mRNA for RNA sequencing. We used the transcriptomic data for the calibration of the intracellular model of macrophages. We also performed other protein-level assays such as ELISA and blot assays to calibrate parameters related to extracellular behavior. For the purpose of transparency, all experimental data that was generated with the goal of calibrating the 3D model can be found on this website.

<figure>
<img  src="https://data.nutritionallungimmunity.org/api/v1/file/5e0f99d4c1b2cfe0661e564d/download?contentDisposition=inline" width="400" height="250"/>
<figcaption>A summary of our experimental pipeline for monocyte-derived macrophages.</figcaption>
</figure>

### How we build features of the model

 We provide an example from our own project to describe how the research process proceeds within our interdisciplinary research group.

__Example Goal:__ Implement a model of the iron-handling behavior of an immune cell in response to _A. fumigatus_

  To answer this question, the following steps could be taken:
  1. An experimentalist might perform a co-cultured experiment of an immune cell type with _A. fumigatus_.
  2. Various experiments including transcriptomics and ELISA are used to measure transcriptional and protein-level changes.
  3. After sequencing, the data is preprocessed and analyzed by a computational biologist.
  4. Such analysis (such as differential expression analysis, pathway analysis, etc.),together with the protein-level data, is then used to enrich a preliminary intracellular mathematical model built from literature knowledge.
  5. The implementation of this individual-cell model is then incorporated into the tissue-level 3D model.

  From this example alone, we see the various data and artifacts that were required and/or generated:
  1. Experimental notebooks describing the protocol of the experiment.
  2. Raw data (e.g. RNA seq fastq files).
  3. Computational scripts analyzing the generated data.
  4. Versions of different software dependencies used in the analysis.
  5. Literature results.
  6. Implementation of mathematical model.

# Information Management

This project is highly interdisciplinary and complex, with many digital artifacts and data to track, so we've built an information management system in order to track and store all of the pieces. That information management system is rooted in this website, which then provides links out to other resources appropriate for storing the artifacts, e.g. GitHub for code repositories and Girder for digital assets.


## Information Consumers Example Use Cases

The diversity of scientists that is needed in the building of the multiscale mathematical model is also reflected by the diversity of consumers of the multiscale mathematical model. We spell out 3 use cases that we have in mind to support with our Information Management system.

1. Bench scientist: We expect that most of our users would be scientists that enter the project by reading a publication or hearing a presentation related to the multiscale mathematical model. Such user might be interested in running simulations, in which case we would refer them to the web-based tool we are developing for running the model without any installation or looking through the low-level details. Alternatively, the user might be interested in an experimental dataset that was used to generate the rules of an individual cell in the overall model implementation. Such an user would then navigate to this <a href="{{ site.baseurl }}{% link model/model.md %}"> section </a> which provides references to all the data generated from experiments as well as the accompanying experimental notebooks.

2. Scientists hoping to expand/adapt our modeling platform: Our goal is to build a computational infrastructure that can be used to model how the immune system responds to _A. fumigatus_. A user might be interested in modifying or expand our current multiscale model and running simulations to see how their adaption differs from ours and/or contribute their independent model of a cell type we have not implemented as of yet. For that user, it might be of interest to read the implementation details of the overall 3D computational model, as well as a guide to the API on how to extend the model. We envision that such an user would be most interested in this <a href="{{ site.baseurl }}{% link design/design.md %}"> section </a>.

3. Internal lab members: Long term projects in computational projects in academia are challenged by a high turnover of trainees that come into the project. Moreover, in the building of multiscale modeling, team members might be working on individual components in parallel. Our hope is to provide a central repository where a new lab member can find all of the pieces that have been used in the process of the project and get them up to speed. For example, a new member might be in charge of preprocessing data of a cell type not previously analyzed. For the sake of consistency and efficiency, the new lab member can then refer to the bioinformatics column in the table provided in this <a href="{{ site.baseurl }}{% link model/model.md %}"> section </a> where they can find scripts utilized for the analysis of previously generated data.



<a name="datadiagram">
## Data associated with the model building effort

The overall model building process can be described as a pipeline going from experimental work to computational analysis of the experimental data, to mathematical modeling, to the implementation and incorporation of a version of the mathematical model into the 3D agent-based model. For example, monocyte derived macrophages, which are known to play a crucial role in iron-handling during infection, are included as agents in the 3D agent-based model. To derive the rules of a monocyte derived macrophage, we built a generalized boolean network (GBN) model from a combination of literature and experiments. All the experimental data that was used to derive rules in the GBN can be found in the experimental section in the table below.

<table style="width:100%">
 <col align="left">
 <col align="left">
 <col align="right">
 <tr>
   <th>Experimental data  </th>
   <th>Bioinformatics</th>
   <th>Mathematical models</th>
 </tr>
 <tr>
   <td><p><b><center>Intracellular scale</center></b><a align="center" href="{{ site.baseurl }}{% link model/mdmacrophage/mdmacrophage_experimental.md %}">
       <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce407c1b2cfe0661e562f/download?contentDisposition=inline" width="50" height="30"/><u>Experimental notebooks and raw data associated with monocyte derived macrophages</u>
       </a> </p>


       <a href="{{ site.baseurl }}{% link model/mddc/mddc_experimental.md %}">
       <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbdee7c1b2cfe0661e5620/download?contentDisposition=inline" width="50" height="30"/><u>Experimental notebooks and raw data associated with monocyte DCs</u>
       </a>



        </td>
   <td><p><b><center>Intracellular scale </center></b><a align="center" href="{{ site.baseurl }}{% link model/mdmacrophage/mdmacrophage_bioinformatics.md %}">
       <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce407c1b2cfe0661e562f/download?contentDisposition=inline" width="50" height="30"/><u>Computational pipelines to analyze monocyte derived macrophage related data</u>
       </a> </p>

       <a href="{{ site.baseurl }}{% link model/mddc/mddc_bioinformatics.md %}">
       <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbdee7c1b2cfe0661e5620/download?contentDisposition=inline" width="50" height="30"/><u>Computational pipelines to analyze monocyte derived DC related data</u>
       </a>


       </td>

   <td><p><b><center>Intracellular scale</center></b><a align="center" href="{{ site.baseurl }}{% link model/mdmacrophage/mdmacrophage_mathematical.md %}">
       <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce407c1b2cfe0661e562f/download?contentDisposition=inline" width="50" height="30"/><u>Mathematical models associated with monocyte derived macrophages</u>
       </a> </p>
       <a href="{{ site.baseurl }}{% link model/mddc/mddc_mathematical.md %}">
       <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbdee7c1b2cfe0661e5620/download?contentDisposition=inline" width="50" height="30"/><u>Mathematical models associated with monocyte derived DCs </u>
       </a>
       <p>
       <a href="{{ site.baseurl }}{% link model/afumigatus/af_mathematical.md %}">
       <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce335c1b2cfe0661e562c/download?contentDisposition=inline" width="50" height="30"/><u>Mathematical models associated with <i> A. fumigatus </i> </u>
       </a>
       </p>
       <p>
       <a href="{{ site.baseurl }}{% link model/epithelium/epithelium_mathematical.md %}">
       <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbdfeac1b2cfe0661e5626/download?contentDisposition=inline" width="50" height="30"/><u>Mathematical models associated with alveolar epithelial cells </u>
       </a>
       </p>
       <p>
       <a href="{{ site.baseurl }}{% link model/neutrophil/neutrophil_mathematical.md %}">
       <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbd8edc1b2cfe0661e561d/download?contentDisposition=inline" width="50" height="30"/><u>Mathematical models associated with neutrophils </u>
       </a>
       </p>
       <p>
       <a href="{{ site.baseurl }}{% link model/alveolarmacrophage/alveolar_macrophage_mathematical.md %}">
       <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbdf5ec1b2cfe0661e5623/download?contentDisposition=inline" width="50" height="30"/><u>Mathematical models associated with alveolar macrophages </u>
       </a>
       </p>


       </td>

 </tr>
 <tr>
 <td>
 <p><b><center>Tissue scale</center></b></p>

 </td>
 <td><p><b><center>Tissue scale</center></b></p>

 </td>
 <td><p><b><center>Tissue scale</center></b></p>
 <a href="{{ site.baseurl }}{% link model/Geometry/Geometry.md %}">
  <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5d7262b2ef2e2603553c5690/download?contentDisposition=inline" width="50" height="50"/>
  <u>Files related to the generation of the geometry.</u>
  </a>


 </td>


 </tr>
 <tr>
 <td>
 <p><b><center>Whole-body scale</center></b></p>

 </td>
 <td><p><b><center>Whole-body scale</center></b></p>
 </td>

 <td><p><b><center>Whole-body scale</center></b></p>
  <a href="{{ site.baseurl }}{% link model/liver/liver_mathematical.md %}">
   <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbccd9c1b2cfe0661e561a/download?contentDisposition=inline" width="50" height="50"/>
   <u>Files related to the mathematical model of the liver</u></a>
 </td>


 </tr>
</table>

<a name="bridgingthescales">
# Bridging the scales

####  Acknowledgements of figures.

Many of the individual figures were generated by the scientific illustration team at [The Jackson Laboratory](https://www.jax.org).
