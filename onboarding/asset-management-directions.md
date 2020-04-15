---
layout: page
title: Directions for information management aspects of the project.
subtitle: Your efforts will pay off.
show_sidebar: true
toc: true
---

## Reference and literature management

We assume that you have completed the [first steps](/onboarding/#first-steps) and you are part of the NutritionalLungImmunity Zotero group. We ask all our team members to add relevant literature to the Zotero NutritionalLungImmunity group and tag their items with a minimal set of tags. You can read about how to add Zotero tags [here](https://www.zotero.org/support/collections_and_tags). Whatever tags you add will be added to the other team members tag, assuming that you are syncing your library. Please check before adding a paper if the reference is already in the library--if so, simply add tags to the existing reference.

To have the new bibliography be included on the website, you can do one of two things. You can manually export the bib file and drop it and save it as```\_bibliography\references.bib,``` or alternatively, you can use an add-on such as [better BibTex](https://retorque.re/zotero-better-bibtex/) that automatically exports your bib file. Once you are ready to push your new bib file onto the website,  follow [these steps](#github-and-jekyll-workflow) on how to do so. We use [Jekyll Scholar](https://github.com/inukshuk/jekyll-scholar) to manage the reference on the webfront (hence why the standardized tags!). It allows you to include subset of literature on the website based on fields in the bibfile.

### Reference tags

| Tag       | Include if         |
| ------------- |:-------------:|
| Monocyte derived dendritic cell| Related to cell type |
| Dendritic cell| Related to cell type    |  
| Monocyte derived macrophage| Related to cell type      |  
| Alveolar macrophage| Related to cell type     |
| Alveolar epithelial cell| Related to cell type      |  
| Airway epithelial cell| Related to cell type     |
| Aspergillus fumigatus| Related to the fungus itself    |
| Neutrophil| Related to cell type     |  
| Innate immunity| Overview of innate immunity response |
| Software| Related to software used in the project |  
| Review paper| Reference is a review paper|
| Invasive Pulmonary Aspergillosis| Paper specific to IPA    |
| In vitro| Includes _in vitro_ data used to calibrate a model|
| In vivo| Includes _in vivo_ data used to calibrate a model|
| Multiscale modeling| Reference related to techniques of multiscale modeling|
| Preprocessing tools| Related to a tool used in the preprocessing step     |
| Bioinformatics tool|  Related to a tool used in the bionformatics analysis    |
| Our publication| Papers that cite funding related to these projects     |
| Intracellular model| Paper is used in the building of an intracellular network model in this project |
| Parameter reference| A parameter related to a model is derived from this paper  |
| Human| Includes data from humans  |
| Mouse| Includes data from mice |
| Numerical methods| Paper related to numerical method     |
| Software architecture| Paper related to software architecture    |
| Information management | Paper related to information management    |
| Transcriptomic dataset | Paper includes a transcriptomic dataset|

## Our suggested Github workflow


### Github and Jekyll workflow

## Adding assets onto Girder




Go to our [Girder instance](data.nutritionallungimmunity.org) to upload/download data. Assuming you have the appropriate permissions, you should be able to upload/download assets onto Girder. We include a brief description of some of the Girder collections to orient you, although once you go to Girder, each collection contains information that describes what is in them.


###  Overview of Girder collections


| Girder collection (non-exhaustive list) | Includes (non-exhaustively) |
| ------------- |:-------------:|
|Model dissemination| Includes project documentation, and presentation materials. |
|Experimental protocols and metadata associated to experiments| Includes experimental protocols and experimental metadata associated with various experiments related to this project|
|Monocyte derived macrophages | Includes all data related to monocyte derived macrophages, including wiring diagrams for model, experimental data for model validation, processing output for bioinformatics data related to the analysis of macrophages, etc. (see e.g the monocyte derived macrophage [subsite](/model/mdmacrophage/) to get an idea of what sort of data is associated with a monocyte derived macrophage).

Once you find the appropriate place, add the appropriate tags (#girder-asset-tags) to the asset as a markdown comment, e.g.
```[//]: <TAG>```. This will allow you to query in girder by using these tags. For example, now you can find all posters where Bandita Adhikari is first author by typing  ```"NLI:POSTER" "NLI:FIRSTAUTHOR:BanditaAdhikari"``` in the query field on Girder.

To make life easier, we made [some python scripts](https://github.com/NutritionalLungImmunity/data-management) where you can choose tags from a GUI and it will write to a file that you can copy and paste onto the information tab.

### Girder asset tags


| Tag       | Include if         |
| ------------- |:-------------:|
|NLI:POSTER| Asset is a poster |
|NLI:DOCUMENTATION| Asset is related to documentation for the project |
|NLI:SLIDES| Asset is for a presentation in slide format |
|NLI:EXP.DATA| Asset is part of an experiment related to the NLI project|
|NLI:METADATA| Asset is metadata associated to a dataset |
|NLI:EXP.PROTOCOL| Asset is metadata associated to a dataset |
|NLI:TRANSCRIPTOMICS| Asset is related to a transcriptomic experiment |
|NLI:TISSUESCALE| Asset is related to data at the tissue scale |
|NLI:INTRACELLULARSCALE| Asset is related to data at the intracellular scale |
|NLI:RESULTS|Asset presents results for an analysis or for model|
|NLI:ABSTRACT|Asset is an abstract for a presentation|
|NLI:MODEL|Asset is associated with the building of a model|
|NLI:MDMACROPHAGE|Asset is associated with the cell type|
|NLI:MDDC|Asset is associated with the cell type|
|NLI:ALVEOLARMACROPHAGE|Asset is associated with the cell type|
|NLI:NEUTROPHIL|Asset is associated with the cell type|
|NLI:ALVEOLAREPITHELIALCELL|Asset is associated with the cell type|
|NLI:ENDOTHELIALCELL|Asset is associated with the cell type|
|NLI:LABORATORYNOTEBOOK|Asset is a laboratory notebook|
|NLI:LASTAUTHOR:LuisSordoVieira|Last/Senior author(s)|
|NLI:LASTAUTHOR:ReinhardLaubenbacher|Last/Senior author(s)|
|NLI:LASTAUTHOR:BanditaAdhikari|Last/Senior author(s)|
|NLI:LASTAUTHOR:JosephMasison|Last/Senior author(s)|
|NLI:LASTAUTHOR:HenriqueDeAssis|Last/Senior author(s)|
|NLI:LASTAUTHOR:YuMei|Last/Senior author(s)|
|NLI:LASTAUTHOR:BornaMehrad|Last/Senior author(s)|
|NLI:LASTAUTHOR:MichaelGrauer|Last/Senior author(s)|
|NLI:LASTAUTHOR:WilliamSchroeder|Last/Senior author(s)|
|NLI:LASTAUTHOR:NingYang|Last/Senior author(s)|
|NLI:LASTAUTHOR:BrianHelba|Last/Senior author(s)|
|NLI:LASTAUTHOR:JonathanBeezley|Last/Senior author(s)|
|NLI:FIRSTAUTHOR:LuisSordoVieira|First author(s)|
|NLI:FIRSTAUTHOR:ReinhardLaubenbacher|First author(s)|
|NLI:FIRSTAUTHOR:BanditaAdhikari|First author(s)|
|NLI:FIRSTAUTHOR:JosephMasison|First author(s)|
|NLI:FIRSTAUTHOR:HenriqueDeAssis|First author(s)|
|NLI:FIRSTAUTHOR:YuMei|First author(s)|
|NLI:FIRSTAUTHOR:BornaMehrad|First author(s)|
|NLI:FIRSTAUTHOR:MichaelGrauer|First author(s)|
|NLI:FIRSTAUTHOR:WilliamSchroeder|First author(s)|
|NLI:FIRSTAUTHOR:NingYang|First author(s)|
|NLI:FIRSTAUTHOR:BrianHelba|First author(s)|
|NLI:FIRSTAUTHOR:JonathanBeezley|First author(s)|


#### That's not all

If you feel up to the challenge, you can also write your own python scripts to upload/download data from our Girder collection.
You can find the manual for Girder [here](https://girder.readthedocs.io/en/stable/).
