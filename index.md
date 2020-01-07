---
layout: default
---

# Multiscale model of nutritional immunity in invasive pulmonary aspergillosis
The purpose of the work is to develop a multiscale computational model to simulate the invasion of the human lungs by spores of the opportunistic fungus _Aspergillus fumigatus_. In particular, we explore the role of **nutritional immunity** in clearing  infection, with a focus on iron. This project is currently funded by The National Institutes of Health and The National Science Foundation of the United States of America (see <a href="{{ site.baseurl }}{% link funding/funding.md %}"> funding section </a>). The team includes members from [The Center for Quantitative Medicine at UConn Health](https://health.uconn.edu/laubenbacher/), [The Jackson Laboratory for Genomic Medicine](https://www.jax.org/about-us/locations/farmington), [UF Health](https://ufhealth.org/), and [Kitware](https://www.kitware.com/).


Invasive pulmonary aspergillosis (IPA) is initiated by the inhalation of spores that then reach the alveolar space. Recognition of spores by the innate immune system and epithelial cells lead to a immune response recruiting various leukocytes to the site of infection.
<figure class="center">
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dfce32bc1b2cfe0661e5629/download?contentDisposition=inline" width="700" height="500"/>
</figure>
<a name="lungimmunity">


We are building a 3D agent-based model of the innate immune response to _invasive pulmonary aspergillosis_ with a focus on the "battle over iron" that occurs in the alveolar space between the host and the fungus. [Agent-based modeling](https://en.wikipedia.org/wiki/Agent-based_model) aims to model how autonomous individuals interact with each other and their computational environment. For us, the individual agents are:

1. Alveolar macrophages.
1. Monocyte derived macrophages.
1. Monocyte derived dendritic cells (DCs).
1. Neutrophils.
1. Epithelial cells.
1. _A. fumigatus_

Agents behave according to a set of rules that are derived from literature and _de novo_ experiments. For example, the monocyte derived macrophages respond to the sensing of _A. fumigatus_ and respond accordingly to the output of an intracellular Generalized Boolean network (GBN). The GBN is built from a combination of literature results and analysis of a transcriptomics dataset generated as part of this project.

Importantly, we are implementing the model in an innovative modularized framework to make the model extendable and customizable by the community.

## Transparent model building

### Three use-cases of multi-scale model.

Multiscale mathematical modeling of disease brings together a wide array of scientists with various backgrounds. As a result, a diverse set of data is utilized in the model building effort. We provide an example from our own project to describe what we mean.

__Example Goal:__ Implement a model of the iron-handling behavior of an immune cell in response to _A. fumigatus_

  To answer this question, the following steps could be taken: An experimentalist might perform a co-cultured experiment of an immune cell type with _A. fumigatus_. Various experiments such as transcriptomics and ELISA are used to measure transcriptional and protein-level changes. After sequencing, the data is preprocessed and analyzed by a computational biologist. Such analysis (such as differential expression analysis, pathway analysis, etc.),together with the protein-level data, is then used to enrich a preliminary intracellular mathematical model built from literature knowledge. The implementation of this individual-cell model is then incorporated into the tissue-level 3D model.

  From this example alone, we see the various data that were required and/or generated:
  1. Experimental notebooks describing the protocol of the experiment.
  2. Raw data.
  3. Computational scripts analyzing the generated data.
  4. Versions of different software used in the analysis.
  5. Literature results.
  6. Implementation of mathematical model.

The diversity of scientists that is needed in the building of the multiscale mathematical model is also reflected by the diversity of consumers of the multiscale mathematical model. We spell out 3 use cases.

1. Bench scientist: We expect that most of our users would be scientists that enter the project by reading a publication or hearing a presentation related to the multiscale mathematical model. Such user might be interested in running simulations, in which case we are developing a web-based tool for running the model without any installation or looking through the low-level details. Alternatively, the user might be interested in an experimental dataset that was used to generate the rules of an individual cell in the overall model implementation. Such an user would then navigate to this <a href="{{ site.baseurl }}{% link model/model.md %}"> section </a> which provides references to all the data generated from experiments as well as the accompanying experimental notebooks.

2. Scientists hoping to expand/adapt our modeling platform: Our goal is to build a computational infrastructure that can be used to model how the immune system responds to _A. fumigatus_. A user might be interested in modifying or expand our current multiscale model and running simulations to see how their adaption differs from ours and/or contribute their independent model of a cell type we have not implemented as of yet. For that user, it might be of interest to read the implementation details of the overall 3D computational model, as well as a guide to the API on how to extend the model. We envision that such an user would be most interested in this <a href="{{ site.baseurl }}{% link design/design.md %}"> section </a>.

3. Internal lab members: Long term projects in computational projects in academia are challenged by a high turnover of trainees that come into the project. Moreover, in the building of multiscale modeling, team members might be working on individual components in parallel. Our hope is to provide a central repository where a new lab member can find all of the pieces that have been used in the process of the project and get them up to speed. For example, a new member might be in charge of preprocessing data of a cell type not previously analyzed. For the sake of consistency and efficiency, the new lab member can then refer to the bioinformatics column in the table provided in this <a href="{{ site.baseurl }}{% link model/model.md %}"> section </a> where they can find scripts utilized for the analysis of previously generated data.


### Modular software design
The major innovation that the modeling design implements is the separation of multiscale dynamics and components into individual “modules.” The full set of biological, chemical, and physical behaviors remains encoded within the model but the software architecture is such that each module is a unique collection of code packaged with its own computational environment, capable of running on a separate process. The modules then communicate by mutating a shared state variable that exists within memory. The effect of such structure is to remove any interdependence between modules so that a modeler interested in extending or modifying the model can do so without changing the parts of the model that are outside the scope of the desired changes, For example, the aspergillus module contains code that supports aspergillus data initialization and update, but if an improved or tangential model is created to replace the existing model, only the aspergillus module will need to be edited. In comparison, a more conventional software structure would require the understanding and ability to modify a macrophage module equivalent to avoid breaking the code. Therefore, we can have a robust platform which can work with different programming languages and it will be easy to “plug in” or “unplug” a module as long as the modules read and write data in a similar way. For more information, refer to the Github Wiki.

<img src="https://data.nutritionallungimmunity.org/api/v1/file/5db9a799ef2e2603553c5950/download?contentDisposition=inline" alt='missing' width="1000"     height="500" />



## News
* Dr. Reinhard Laubenbacher and Ms. Bandita Adhikari present at the [annual meeting of the Society for Mathematical Biology in Montreal](http://www.smb2019.org/).
* Dr. Reinhard Laubenbacher and Dr. Luis Sordo Vieira developed methods of control of intracellular networks using computational algebra. See the [BiorXiv preprint](https://www.biorxiv.org/content/10.1101/682989v1)!
## Team Leads
<figure>
    <a href="https://facultydirectory.uchc.edu/profile?profileId=Laubenbacher-Reinhard">
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5d7262b3ef2e2603553c5696/download?contentDisposition=inline" alt='missing' width="120" height="160" />

    </a>
    <figcaption>Dr. Reinhard Laubenbacher<br> UConn Health<br> The Jackson Laboratory</figcaption>
</figure>
<figure>
    <a href="https://pulmonary.medicine.ufl.edu/about-us/faculty/borna-mehrad-md/">


    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5d7262b2ef2e2603553c5693/download?contentDisposition=inline" alt='missing' width="120" height="180" />

    </a>

<figcaption>Dr. Borna Mehrad<br> UF Health</figcaption>
</figure>
<figure>
    <a href="https://www.kitware.com/will-schroeder/">
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5d7262b3ef2e2603553c5699/download?contentDisposition=inline" alt='missing' width="120" height="120" />

    </a>
    <figcaption>Dr. William Schroeder<br> Kitware</figcaption>
</figure>


## Funding
- [National Instute of Biomedical Imaging and Bioengineering U01EB024501](https://projectreporter.nih.gov/project_info_description.cfm?aid=9567990), Modular design of multiscale models, with an application to the innate immune response to fungal respiratory pathogens.
- [National Institute of Allergy and Infectious Diseases 1R01AI135128](https://projectreporter.nih.gov/project_info_description.cfm?projectnumber=1R01AI135128-01), Multi scale modeling of the battle our iron in invasive lung infection.
- [National Science Foundation EAGER #1750183](https://nsf.gov/awardsearch/showAward?AWD_ID=1750183&HistoricalAwards=false), Modular design of multiscale models, with an application to the innate immune response to fungal respiratory pathogens.

### Contact
- [Dr. Reinhard Laubenbacher](mailto:laubenbacher@uchc.edu)
- [Dr. Borna Mehrad](mailto:Millie.Ramos@medicine.ufl.edu)
