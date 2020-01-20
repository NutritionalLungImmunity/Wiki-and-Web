---
layout: page
title: Model Building & Information Management
subtitle: A description of the model, the workflow of model building, and associated data.
show_sidebar: false
toc: true
---

## An overview of invasive pulmonary aspergillosis
<figure class="center">
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce32bc1b2cfe0661e5629/download?contentDisposition=inline" width="700" height="500"/>
</figure>
The average human inhales hundreds of spores of the _A. fumigatus_ fungus on a daily basis. Despite of this, the vast majority of immunocompetent patients are able to clear the fungus without any seeming effects. A small number of spores are capable of reaching the alveolar sac, where resident macrophages and epithelial cells quickly mount an immune response recruiting various other cells from the circulation such as dendritic cells (DCs), monocyte derived macrophages, and neutrophils. A weakened immune system (e.g. neutropenia) presents a window of opportunity for the fungus to start germinating and breach the epithelial layer, getting into the circulation and causing a systemic infection. Thus, the immune system must act quickly and efficiently to clear the fungus.

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

<figure>
<img  src="https://data.nutritionallungimmunity.org/api/v1/file/5e0f99d4c1b2cfe0661e564d/download?contentDisposition=inline" width="400" height="250"/>
<figcaption>A summary of our experimental pipeline for monocyte-derived macrophages.</figcaption>
</figure>

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

## Information Management

This project is highly interdisciplinary and complex, with many digital artifacts and data to track, so we've built an information management system in order to track and store all of the pieces. That information management system is rooted in this website, which then provides links out to other resources appropriate for storing the artifacts, e.g. GitHub for code repositories and Girder for digital assets.


## Information Consumers Example Use Cases

The diversity of scientists that is needed in the building of the multiscale mathematical model is also reflected by the diversity of consumers of the multiscale mathematical model. We spell out 3 use cases that we have in mind to support with our Information Management system.

1. Bench scientist: We expect that most of our users would be scientists that enter the project by reading a publication or hearing a presentation related to the multiscale mathematical model. Such user might be interested in running simulations, in which case we would refer them to the web-based tool we are developing for running the model without any installation or looking through the low-level details. Alternatively, the user might be interested in an experimental dataset that was used to generate the rules of an individual cell in the overall model implementation. Such an user would then navigate to this <a href="{{ site.baseurl }}{% link model/index.md %}"> section </a> which provides references to all the data generated from experiments as well as the accompanying experimental notebooks.

2. Scientists hoping to expand/adapt our modeling platform: Our goal is to build a computational infrastructure that can be used to model how the immune system responds to _A. fumigatus_. A user might be interested in modifying or expand our current multiscale model and running simulations to see how their adaption differs from ours and/or contribute their independent model of a cell type we have not implemented as of yet. For that user, it might be of interest to read the implementation details of the overall 3D computational model, as well as a guide to the API on how to extend the model. We envision that such an user would be most interested in this <a href="{{ site.baseurl }}{% link design/index.md %}"> section </a>.

3. Internal lab members: Long term projects in computational projects in academia are challenged by a high turnover of trainees that come into the project. Moreover, in the building of multiscale modeling, team members might be working on individual components in parallel. Our hope is to provide a central repository where a new lab member can find all of the pieces that have been used in the process of the project and get them up to speed. For example, a new member might be in charge of preprocessing data of a cell type not previously analyzed. For the sake of consistency and efficiency, the new lab member can then refer to the bioinformatics column in the table provided in this <a href="{{ site.baseurl }}{% link model/index.md %}"> section </a> where they can find scripts utilized for the analysis of previously generated data.


## Data associated with the model building effort

The overall model building process can be described as a pipeline going from experimental work to computational analysis of the experimental data, to mathematical modeling, to the implementation and incorporation of a version of the mathematical model into the 3D agent-based model. For example, monocyte derived macrophages, which are known to play a crucial role in iron-handling during infection, are included as agents in the 3D agent-based model. To derive the rules of a monocyte derived macrophage, we built a generalized boolean network (GBN) model from a combination of literature and experiments. All the experimental data that was used to derive rules in the GBN can be found in the experimental section in the table below.

<table class="models-table header-column" style="width:100%">
  <thead>
    <tr>
      <th class="has-text-centered"></th>
      <th class="has-text-centered">Experimental data</th>
      <th class="has-text-centered">Bioinformatics</th>
      <th class="has-text-centered">Mathematical models</th>
    </tr>
  </thead>
  <tbody>

    <!-- INTRACELLULAR SCALE -->
    <tr>
      <th class="has-text-centered"></th>
      <th class="has-text-centered" colspan="3"> Intracellular Scale</th>
    </tr>

    <tr>
      <td>
      <div><img src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce407c1b2cfe0661e562f/download?contentDisposition=inline" height="auto" width="36" alt="Monocyte Derived Macrophages">Monocyte derived macrophages</div>
      </td>
      <td>
        <div  style="font-size: 24px;">
        <a href="{{ site.baseurl }}{% link model/mdmacrophage/mdmacrophage_experimental.md %}">
          <i class="fa fa-dna" ></i><i class="fa fa-clipboard-check" ></i>
             </a>
        </div>
      </td>
      <td>

          <div  style="font-size: 24px;">
          <a href="{{ site.baseurl }}{% link model/mdmacrophage/mdmacrophage_bioinformatics.md %}">
          <i class="fa fa-dna" ></i><i class="fab fa-github"></i>

          </a>
          </div>
      </td>
      <td>
        <div style="font-size: 24px;">
          <a href="{{ site.baseurl }}{% link model/mdmacrophage/mdmacrophage_mathematical.md %}">
          <i class="fab fa-github"></i>
          </a>
        </div>
      </td>
    </tr>

    <tr>
      <td>
      <div><img src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbdee7c1b2cfe0661e5620/download?contentDisposition=inline" height="auto" width="36" alt="Monocyte Derived Dendritic Cells">Monocyte Derived Dendritic Cells</div></td>
      <td>
        <div style="font-size: 24px;">
          <a href="{{ site.baseurl }}{% link model/mddc/mddc_experimental.md %}">
          <i class="fa fa-dna" ></i><i class="fa fa-clipboard-check" ></i>


          </a>
        </div>
      </td>
      <td>
        <div style="font-size: 24px;">

          <a href="{{ site.baseurl }}{% link model/mddc/mddc_bioinformatics.md %}">
          <i class="fa fa-dna" ></i><i class="fab fa-github"></i>

          </a>
        </div>
      </td>
      <td>
        <div style="font-size: 24px;">
          <a href="{{ site.baseurl }}{% link model/mddc/mddc_mathematical.md %}">

          <i class="fa fa-wrench"></i>

          </a>

        </div>
      </td>
    </tr>

    <tr>
      <td><div><img src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce335c1b2cfe0661e562c/download?contentDisposition=inline" height="auto" width="36" alt="Aspergillus fumigatus"><em>Aspergillus fumigatus</em></div></td>
      <td>
        <div style="font-size: 24px;">
        <i class="fa fa-wrench"></i>

        </div>
      </td>
      <td>
        <div style="font-size: 24px;">
        <i class="fa fa-wrench"></i>

        </div>
      </td>
      <td>
        <div style="font-size: 24px;">
        <i class="fa fa-wrench"></i>
        </div>
      </td>
    </tr>

    <tr>
      <td><div><img src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbdfeac1b2cfe0661e5626/download?contentDisposition=inline" height="auto" width="36" alt="Alveolar epithelial cells"><em>Alveolar epithelial cells</em></div></td>      
      <td>
              <div style="font-size: 24px;">
              <i class="fa fa-wrench"></i>

              </div>
            </td>
            <td>
              <div style="font-size: 24px;">
              <i class="fa fa-wrench"></i>

              </div>
            </td>
            <td>
              <div style="font-size: 24px;">
              <i class="fa fa-wrench"></i>
              </div>
            </td>
    </tr>

    <tr>
      <td> <div><img src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbdf5ec1b2cfe0661e5623/download?contentDisposition=inline" height="auto" width="36" alt="Alveolar macrophages"><em>Alveolar macrophages</em></div></td>   
      <td>
              <div style="font-size: 24px;">
              <i class="fa fa-wrench"></i>

              </div>
            </td>
            <td>
              <div style="font-size: 24px;">
              <i class="fa fa-wrench"></i>

              </div>
            </td>
            <td>
              <div style="font-size: 24px;">
              <i class="fa fa-wrench"></i>
              </div>
            </td>
    </tr>
    <tr>
    <td> <div><img src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbd8edc1b2cfe0661e561d/download?contentDisposition=inline" height="auto" width="36" alt="Neutrophils"><em>Neutrophil</em></div></td>   
    <td>
            <div style="font-size: 24px;">
            <i class="fa fa-wrench"></i>

            </div>
          </td>
          <td>
            <div style="font-size: 24px;">
            <i class="fa fa-wrench"></i>

            </div>
          </td>
          <td>
            <div style="font-size: 24px;">
            <i class="fa fa-wrench"></i>
            </div>
          </td>

    </tr>

    <!-- TISSUE SCALE -->
    <tr>
      <th class="has-text-centered"></th>
      <th class="has-text-centered" colspan="3"> Tissue Scale</th>
    </tr>

    <tr>
      <td><div><img src="https://data.nutritionallungimmunity.org/api/v1/file/5d7262b2ef2e2603553c5690/download?contentDisposition=inline" height="auto" width="36" alt="Geometry">Geometry</div>
      </td>
      <td>
      <div style="font-size: 24px;">
      <i class="fa fa-wrench"></i>

      </div>
      </td>
      <td>
      <div style="font-size: 24px;">
      <i class="fa fa-wrench"></i>
      </div>
      </td>
      <td>
        <div style="font-size: 24px;">
          <a href="{{ site.baseurl }}{% link model/Geometry/Geometry.md %}"><i class="fab fa-github"></i></a>
        </div>
      </td>
    </tr>

    <!-- WHOLE-BODY SCALE -->
    <tr>
      <th class="has-text-centered"></th>
      <th class="has-text-centered" colspan="3"> Whole-body Scale</th>
    </tr>

    <tr>
    <td><div><img src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbccd9c1b2cfe0661e561a/download?contentDisposition=inline" height="auto" width="36" alt="Liver">Liver</div>
    </td>
      <td>

      <div style="font-size: 24px;">
      <i class="fa fa-wrench"></i></div>
      </td>
      <td>
      <div style="font-size: 24px;">
      <i class="fa fa-wrench"></i></div>
      </td>
      <td>
      <div style="font-size: 24px;">
      <i class="fa fa-wrench"></i>
        </div>
      </td>
    </tr>
  </tbody>
</table>

## Bridging the scales


## Bibliography

### Overview of innate immunity to invasive pulmonary aspergillosis

__ Add bibliography__







####  Acknowledgements of figures.

Many of the individual figures were generated by the scientific illustration team at [The Jackson Laboratory](https://www.jax.org).
