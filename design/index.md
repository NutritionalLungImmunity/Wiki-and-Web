---
layout: page
title: Software Design
subtitle: Principles of software design for multiscale model of nutritional lung immunity to A. fumigatus
show_sidebar: false
---

## Modular software design
The major innovation that the modeling design implements is the separation of multiscale dynamics and components into individual “modules.” The full set of biological, chemical, and physical behaviors remains encoded within the model but the software architecture is such that each module is a unique collection of code packaged with its own computational environment, capable of running on a separate process. The modules then communicate by mutating a shared state variable that exists within memory. The effect of such structure is to remove any interdependence between modules so that a modeler interested in extending or modifying the model can do so without changing the parts of the model that are outside the scope of the desired changes, For example, the aspergillus module contains code that supports aspergillus data initialization and update, but if an improved or tangential model is created to replace the existing model, only the aspergillus module will need to be edited. In comparison, a more conventional software structure would require the understanding and ability to modify a macrophage module equivalent to avoid breaking the code. Therefore, we can have a robust platform which can work with different programming languages and it will be easy to “plug in” or “unplug” a module as long as the modules read and write data in a similar way. For more information, refer to our [publication](https://www.pnas.org/content/118/20/e2024287118) and [documentation](https://nutritionallungimmunity.github.io/nlisim/).

<img src="https://data.nutritionallungimmunity.org/api/v1/file/5db9a799ef2e2603553c5950/download?contentDisposition=inline" alt='missing' width="1000"     height="500" />
