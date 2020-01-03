---
layout: default
title: A description of the model, the workflow of model building, and associated data.
---

# Table of Contents  
1. [An overview of invasive pulmonary aspergillosis](#overview)
2. [Focusing on nutritional immunity](#nutritionalimmunity)  
3. [Our approach](#approach)
4. [Data associated with with the model building effort.](#datadiagram)
5. [Briding the scales](#bridgingthescales)  
<a name="overview">

# An overview of invasive pulmonary aspergillosis
<figure class="center">
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce32bc1b2cfe0661e5629/download?contentDisposition=inline" width="700" height="500"/>
</figure>

<a name="lungimmunity">
# Focusing on nutritional immunity


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

Agents behave according to a set of rules that are derived from literature and _de novo_ experiments. For example, the monocyte derived macrophages respond to the sensing of _A. fumigatus_ and respond accordingly to the output of an intracellular Generalized Boolean network (GBN). The GBN is built from a combination of literature results and a dataset generated as part of this project.

### Calibrating the model with experimental data

In order to build the 3D agent based model, we have performed several _in vivo_ and _in vitro_ experiments.

For example, we co-cultured monocyte derived macrophages with _A. fumigatus_ in a time-series and extracted mRNA for RNA sequencing. We used the transcriptomic data for the calibration of the intracellular model of macrophages. We also performed other protein-level assays to calibrate parameters related to extracellular behavior.

<figure>
<img  src="https://data.nutritionallungimmunity.org/api/v1/file/5e0f99d4c1b2cfe0661e564d/download?contentDisposition=inline" width="400" height="250"/>
</figure>


<a name="datadiagram">
# Data associated with the model building effort.
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

<a name="bridingthescales">
# Briding the scales

####  Acknowledgements of figures.

Many of the individual figures were generated by the scientific illustration team at [The Jackson Laboratory](https://www.jax.org).
