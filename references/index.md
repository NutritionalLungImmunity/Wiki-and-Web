---
layout: page
title: References
subtitle: Works cited in the project
show_sidebar: true
toc: true
---


## Review papers

{% bibliography --query @*[keywords ~= review_innate_immunity] %}
{% bibliography --query @*[keywords ~= review_neutrophils] %}
{% bibliography --query @*[keywords ~= signaling_reviews] %}



## Bioinformatic tools





### Statistical tools

{% bibliography --query @*[keywords ~= statisticaltools] %}

### Preprocessing tools used in comparison between DCs and Macrophages response to A. fumigatus
{% bibliography --query @*[keywords ~= bioinformatics_pipeline_macrophages_dcs_preprocessing] %}

### Postprocessing tools used in comparison between DCs and Macrophages response to A. fumigatus
{% bibliography --query @*[keywords ~= bioinformatics_pipeline_macrophages_dcs_postprocessing] %}


## Papers about interactions of cells with A. fumigatus

### Epithelial cells
{% bibliography --query @*[keywords ~= Epithelial_cells_response_to_af] %}


### Dendritic cells


#### Specific to Aspergillus fumigatus
{% bibliography --query @*[keywords ~= DC_response_to_AF] %}



### Macrophages


#### Specific to Aspergillus fumigatus
{% bibliography --query @*[keywords ~= macrophage_response_to_AF] %}


### Neutrophils

#### Specific to Aspergillus fumigatus
{% bibliography --query @*[keywords ~= Neutrophils_response_to_AF] %}
