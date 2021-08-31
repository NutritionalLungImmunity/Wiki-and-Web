---
layout: page
title: Multiscale model of nutritional immunity in invasive pulmonary aspergillosis
show_sidebar: false
---


# Multiscale model of nutritional immunity in invasive pulmonary aspergillosis
The purpose of the work is to develop a multiscale computational model to simulate the invasion of the human lungs by spores of the opportunistic fungus _Aspergillus fumigatus_. In particular, we explore the role of **nutritional immunity** in clearing  infection, with a focus on iron. This project is currently funded by The National Institutes of Health and The National Science Foundation of the United States of America (see <a href="{{ site.baseurl }}{% link funding/index.md %}"> funding section </a>). The team includes members from [The Center for Quantitative Medicine at UConn Health](https://health.uconn.edu/laubenbacher/), [The Jackson Laboratory for Genomic Medicine](https://www.jax.org/about-us/locations/farmington), [UF Health](https://ufhealth.org/), and [Kitware](https://www.kitware.com/).


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

Agents behave according to a set of rules that are derived from literature and _de novo_ experiments. For example, the monocyte derived macrophages respond to the sensing of _A. fumigatus_ and respond accordingly to the output of an intracellular [Generalized Boolean Network](https://en.wikipedia.org/wiki/Boolean_network) (GBN). The GBN is built from a combination of literature results and analysis of a transcriptomics dataset generated as part of this project.

Importantly, we are implementing the model in an innovative modularized framework to make the model extendable and customizable by the community.

## Transparent model building and information management

Multiscale mathematical modeling of disease brings together a wide array of scientists with various backgrounds. As a result, a diverse set of data, code, and tools are utilized in the model building effort, all of which needs to be freely available and understandable to enable collaboration and replication. To this end, we have invested in creating a comprehensive information management system to empower various information consumers including bench scientists, modeling and simulation experts, and internal lab members to find the information they need to use and extend our models.

### Modular software design

The major innovation that the modeling design implements is the separation of multiscale dynamics and components into individual “modules.” The full set of biological, chemical, and physical behaviors remains encoded within the model but the software architecture is such that each module is a unique collection of code packaged with its own computational environment. The goal of such structure is to remove any interdependence between modules so that a modeler interested in extending or modifying the model can do so without changing the parts of the model that are outside the scope of the desired changes.


## News
* (May 18, 2021) Many of our research faculty personnel contributed to a recent publication, [“A Modular Computational Framework for Medical Digital Twins”](https://www.pnas.org/content/118/20/e20242871). This paper presents a modular software design that will help implement precision medicine in the form of medical digital twins which are computational models of disease processes calibrated to individual patients.
* (Mar 12, 2021) Dr. Reinhard Laubenbacher, co-authored an article, [Using Digital Twins in Viral Infection](https://doi.org/10.1126/science.abf3370), in Science Magazine along with Drs. James P. Sluka, and James A. Glazier.
* Dr. Reinhard Laubenbacher and Ms. Bandita Adhikari present at the [annual meeting of the Society for Mathematical Biology in Montreal](http://www.smb2019.org/).
* Dr. Reinhard Laubenbacher and Dr. Luis Sordo Vieira developed methods of control of intracellular networks using computational algebra. See the [BiorXiv preprint](https://www.biorxiv.org/content/10.1101/682989v1)!

## Team Leads

<figure>
    <a href="https://facultydirectory.uchc.edu/profile?profileId=Laubenbacher-Reinhard">
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5d7262b3ef2e2603553c5696/download?contentDisposition=inline" alt='missing' width="120" height="160" />
    </a>
    <figcaption>
        Dr. Reinhard Laubenbacher<br>
        Laboratory for Systems Medicine<br>
        UF Health
    </figcaption>
</figure>


<figure>
    <a href="https://pulmonary.medicine.ufl.edu/about-us/faculty/borna-mehrad-md/">
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5d7262b2ef2e2603553c5693/download?contentDisposition=inline" alt='missing' width="120" height="180" />
    </a>
    <figcaption>
        Dr. Borna Mehrad<br>
        UF Health
    </figcaption>
</figure>

<figure>
    <a href="https://www.kitware.com/will-schroeder/">
    <img  src="https://data.nutritionallungimmunity.org/api/v1/file/5d7262b3ef2e2603553c5699/download?contentDisposition=inline" alt='missing' width="120" height="120" />
    </a>
    <figcaption>
        Dr. William Schroeder<br>
        Kitware
    </figcaption>
</figure>




## Funding

- [National Instute of Biomedical Imaging and Bioengineering U01EB024501](https://projectreporter.nih.gov/project_info_description.cfm?aid=9567990), Modular design of multiscale models, with an application to the innate immune response to fungal respiratory pathogens.
- [National Institute of Allergy and Infectious Diseases 1R01AI135128](https://projectreporter.nih.gov/project_info_description.cfm?projectnumber=1R01AI135128-01), Multi scale modeling of the battle our iron in invasive lung infection.
- [National Science Foundation EAGER #1750183](https://nsf.gov/awardsearch/showAward?AWD_ID=1750183&HistoricalAwards=false), Modular design of multiscale models, with an application to the innate immune response to fungal respiratory pathogens.

### Contact
- [Dr. Reinhard Laubenbacher](mailto:Reinhard.Laubenbacher@medicine.ufl.edu)
- [Dr. Borna Mehrad](mailto:Millie.Ramos@medicine.ufl.edu)
