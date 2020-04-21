---
layout: page
title: Model Building & Information Management
subtitle: A description of the model, the workflow of model building, and associated data.
show_sidebar: false
toc: true
bibliography: references.bib
---

## An overview of invasive pulmonary aspergillosis
<figure class="center">
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce32bc1b2cfe0661e5629/download?contentDisposition=inline" width="700" height="500"/>
</figure>
The average human inhales hundreds of spores of the _A. fumigatus_ fungus on a daily basis. Despite of this, the vast majority of immunocompetent patients are able to clear the fungus without any seeming effects. A small number of spores are capable of reaching the alveolar sac, where resident macrophages and epithelial cells quickly mount an immune response recruiting various other cells from the circulation such as dendritic cells (DCs), monocyte derived macrophages, and neutrophils. A weakened immune system (e.g. neutropenia) presents a window of opportunity for the fungus to start germinating and breach the epithelial layer, getting into the circulation and causing a systemic infection. Thus, the immune system must act quickly and efficiently to clear the fungus. See e.g. {% cite parkinnateimmunityaspergillus2009 %}.

## Focusing on nutritional immunity
Although the response of the innate immune system to _A. fumigatus_ is multifaceted, the sequestration of iron (in turn starving the fungus from its needed iron) by the host's immune cells is a crucial response to reduce fungal burden. The _A. fumigatus_ mould is equipped with a sideorophore system that attempts to scavenge iron from its environment. The host immune system is equipped with various mechanisms of iron retention and scavenging. We thus focus on this __battle over iron__ that occurs in the alveolar space between the host and the fungus.

## Our approach
### Multiscale modeling
The progression of _invasive pulmonary aspergillosis_ is dependent on processes that occur at various spatiotemporal scales. For example, after the spore is inhaled into the alveolar space (tissue scale), receptors on immune cells detect the pathogen and initiate intracellular signaling processes (intracelullar scales) that result in the translation of various cytokines and chemokines. Some of these cytokines then get into the circulation and recruit other immune cells to the site of infection. For example, the cytokine interleukin-6 signals the liver (whole-body scale) to produce the hormone hepcidin which works to reduce iron export from host cells, arresting iron from pathogens. These biophysical processes take effect in ranges from milliseconds to hours. As such, the area of multiscale modeling is becoming increasingly popular for the modeling of diseases that affect multiple scales. [Multiscale modeling](https://en.wikipedia.org/wiki/Multiscale_modeling) seeks to model system behavior by modeling the events occurring at various scales and bridging them appropiately.

### Agent-based modeling

We are building a 3D agent-based model of the innate immune response to _invasive pulmonary aspergillosis_ with a focus on the "battle over iron" that occurs in the alveolar space between the host and the fungus. [Agent-based modeling](https://en.wikipedia.org/wiki/Agent-based_model) aims to model how autonomous individuals interact with each other and their computational environment. For us, the individual agents are:

1. Alveolar macrophages.
1. Monocyte derived macrophages.
1. Monocyte derived dendritic cells (DCs).
1. Neutrophils.
1. Epithelial cells.
1. _A. fumigatus_
1. Liver cells

Agents behave according to a set of rules that are derived from literature and _de novo_ experiments. For example, the monocyte derived macrophages respond to the sensing of _A. fumigatus_ and respond accordingly to the output of an intracellular [Generalized Boolean Network](https://en.wikipedia.org/wiki/Boolean_network) (GBN). The GBN is built from a combination of literature results and analysis of a transcriptomics dataset generated as part of this project.


#### Calibrating the model with experimental data

In order to build the 3D agent based model, we have performed several _in vivo_ and _in vitro_ experiments.

For example, we co-cultured monocyte derived macrophages with _A. fumigatus_ in a time-series and extracted mRNA for RNA sequencing. We used the transcriptomic data for the calibration of the intracellular model of macrophages. We also performed other protein-level assays such as ELISA and blot assays to calibrate parameters related to extracellular behavior. For the purpose of transparency, all experimental data that was generated with the goal of calibrating the 3D model can be found on this website.

<!--<figure>
<img  src="https://data.nutritionallungimmunity.org/api/v1/file/5e0f99d4c1b2cfe0661e564d/download?contentDisposition=inline" width="400" height="250"/>
<figcaption>A summary of our experimental pipeline for monocyte-derived macrophages.</figcaption>
</figure>
-->

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTS1vqMQ_UwWNYXCMbvCE2kV8xGgl0FH3M3BAsUli_LEkv3rZT2FhecCkp7sl82uaKNUsGqyHBxi1a-/embed?start=false&loop=false&delayms=60000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>


#### How we build features of the model

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

Here we provide an overview of the steps of model building for the itnracellular macrophage model.

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vS-nYyATU8HLssXjd8Nu8LlI2s-9dcMT9ZYgQbOOl-7diHiTFiJlioexE_5Eq4nGUyLvwyVX5qbqHvF/embed?start=false&loop=false&delayms=60000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>### Flow diagram of process



## Bibliography

{% bibliography --cited %}


### Overview of innate immunity to invasive pulmonary aspergillosis

####  Acknowledgements of figures.

Many of the individual figures were generated by the scientific illustration team at [The Jackson Laboratory](https://www.jax.org).
