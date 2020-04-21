---
title: Nutritional Lung Immunity
subtitle: A description of mathematical models related to the monocyte derived macrophages.
layout: page
show_sidebar: false
menubar: example_menu
tabs: mdmacrophage_tabs
toc: true
---

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQ7A_8RVpvcs5nGXfv8Z1cpbMmXgQNWPf_wV0_xkRU-d5o7QHlyDDgu2BORifCbUmxyz3dqkIJaU7_t/embed?start=false&loop=false&delayms=3000&slide=4" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

## Modeling iron handling by monocyte derived macrophages challenged by _A. fumigatus_
Iron is essential for all living organisms. A characteristic immune response to infections is the sequestration of iron by macrophages to keep it away from pathogens. We have created a generalized Boolean model of how monocyte derived activate an iron metabolism program after sensing _A. fumigatus_ based on the transcriptomics data (see the Bioinformatics section) as well as the literature.

### Wiring diagram
<figure>
<img  src="https://data.nutritionallungimmunity.org/api/v1/file/5dbc2b6eef2e2603553c5a0a/download?contentDisposition=inline" width="600" />
</figure>


The code for the implementation of the intracellular model, as well as a more thorough description can be found [here](https://github.com/NutritionalLungImmunity/NLI_macrophage_iron_regulation).

<a name="macrophageliterature"></a>
## Bibliography

{% bibliography --query @*[keywords ~= macrophage_response_to_AF] %}
{% bibliography --query @*[keywords ~= macrophage_model] %}
