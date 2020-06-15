---
layout: page
title: Information management
subtitle: A description of the model, the workflow of model building, and associated data.
show_sidebar: false
toc: true
bibliography: references.bib
---



## Information Management

This project is highly interdisciplinary and complex, with many digital artifacts and data to track, so we've built an information management system in order to track and store all of the pieces. That information management system is rooted in this website, which then provides links out to other resources appropriate for storing the artifacts, e.g. GitHub for code repositories and Girder for digital assets.

<object type="image/svg+xml" data="/media/svgs/whole_alveolus.svg" >
<!-- fallback image in CSS -->
<img src="/media/svgs/whole_alveolus.svg" width="186" height="235"/>
</object>


## Information Consumers Example Use Cases

The diversity of scientists that is needed in the building of the multiscale mathematical model is also reflected by the diversity of consumers of the multiscale mathematical model. We spell out 3 use cases that we have in mind to support with our Information Management system.

1. Bench scientist: We expect that most of our users would be scientists that enter the project by reading a publication or hearing a presentation related to the multiscale mathematical model. Such user might be interested in running simulations, in which case we would refer them to the web-based tool we are developing for running the model without any installation or looking through the low-level details. Alternatively, the user might be interested in an experimental dataset that was used to generate the rules of an individual cell in the overall model implementation. Such an user would then navigate to this <a href="{{ site.baseurl }}{% link model/index.md %}"> section </a> which provides references to all the data generated from experiments as well as the accompanying experimental notebooks.

2. Scientists hoping to expand/adapt our modeling platform: Our goal is to build a computational infrastructure that can be used to model how the immune system responds to _A. fumigatus_. A user might be interested in modifying or expand our current multiscale model and running simulations to see how their adaption differs from ours and/or contribute their independent model of a cell type we have not implemented as of yet. For that user, it might be of interest to read the implementation details of the overall 3D computational model, as well as a guide to the API on how to extend the model. We envision that such an user would be most interested in this <a href="{{ site.baseurl }}{% link design/index.md %}"> section </a>.

3. Internal lab members: Long term projects in computational projects in academia are challenged by a high turnover of trainees that come into the project. Moreover, in the building of multiscale modeling, team members might be working on individual components in parallel. Our hope is to provide a central repository where a new lab member can find all of the pieces that have been used in the process of the project and get them up to speed. For example, a new member might be in charge of preprocessing data of a cell type not previously analyzed. For the sake of consistency and efficiency, the new lab member can then refer to the bioinformatics column in the table provided in this <a href="{{ site.baseurl }}{% link model/index.md %}"> section </a> where they can find scripts utilized for the analysis of previously generated data.


## Data associated with the model building effort

The overall model building process can be described as a pipeline going from experimental work to computational analysis of the experimental data, to mathematical modeling, to the implementation and incorporation of a version of the mathematical model into the 3D agent-based model. For example, monocyte derived macrophages, which are known to play a crucial role in iron-handling during infection, are included as agents in the 3D agent-based model. To derive the rules of a monocyte derived macrophage, we built a generalized boolean network (GBN) model from a combination of literature and experiments. All the experimental data that was used to derive rules in the GBN can be found in the experimental section in the table below.

<a name="datatable">
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
      <td><a href ="/model/mdmacrophage/">
      <div><img src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce407c1b2cfe0661e562f/download?contentDisposition=inline" height="auto" width="36" alt="Monocyte Derived Macrophages">Monocyte derived macrophages</div></a>
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
      <td><a href ="/model/mddc/">
      <div><img src="https://data.nutritionallungimmunity.org/api/v1/file/5dfbdee7c1b2cfe0661e5620/download?contentDisposition=inline" height="auto" width="36" alt="Monocyte Derived Dendritic Cells">Monocyte Derived Dendritic Cells</div></a></td>
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