# Upscaling Sea Surface Height

You can start with a simple structure and as you progress you can refine it to contain more components. [Here](https://cookiecutter-data-science.drivendata.org/#directory-structure) is an example of a more elaborate structure for a data science project.

## One-line Description

Use a neural network to increase Sea Surface Height data resolution of coarse scale measurements.

## Collaborators

| Name                | Location   | Role                |
|---------------------|------------|---------------------|
| Lara Schlumbom      | Bigelow    | Participant |
| Pedro Walfir       | Bigelow    | Participant         |
| Yifei Hang       | Bigelow    | Participant         |

## Planning

* Initial idea: "short description"
* Ideation Presentation: [Project Pitch](https://docs.google.com/presentation/d/1MG32LTh15YH1vHQdv_7U-SAyclAFcNLs-xWWvf0eZ8g/edit#slide=id.g2f660589f1f_28_0)
* Slack channel: ohw24_proj_upssh_us
* Final presentation: [Project Presentation](https://docs.google.com/presentation/d/1Z9WfwqM1KbRRhXcNXrDurZ-Vts_iLjF75h0j9Lux4_o/edit#slide=id.p)

## Background

mention: why increase resolution (importance of resolving finer scale phenomena); intro on neural networks; how can neural networks be applied to this

## Goals

Find a suitable neural network arhitecture for increasing sea surface height data resolution and apply that to lower resolution satellite measurements.

## Datasets

**1. GLORYS12V1 Absolute Dynamic Topography**

  We used the GLORYS12V1 product from the CMEMS global ocean eddy-resolving reanalysis, with a horizontal resolution of 1/12°, for training the model. That data can be accessed [here](https://data.marine.copernicus.eu/product/GLOBAL_MULTIYEAR_PHY_001_030/description).
   
**2. AVISO Absolute Dynamic Topography**

   The DUACS delayed-time altimeter gridded maps of sea surface height distributed by the Copernicus Climate Change Service were used as a reference for the lower resolution grid. This data has horizontal spatial resolution of 1/4° and can be accessed through [this link](https://data.marine.copernicus.eu/product/SEALEVEL_GLO_PHY_CLIMATE_L4_MY_008_057/description).

**3. SWOT Level 3 Absolute Dynamic Topography**

   The Surface Water and Ocean Topography Satellite (SWOT) Level 3 data was used for selecting the region in which to validate the model. That data can be accessed [here](https://www.aviso.altimetry.fr/en/data/products/sea-surface-height-products/global/swot-l3-ocean-products.html).

**4. SWOT Level 4 Absolute Dynamic Topography**

   The SWOT Level 4 data was used for validating the model trained on GLORYS data. That data can be accessed through [this link](https://www.aviso.altimetry.fr/en/data/products/sea-surface-height-products/global/experimental-multimission-gridded-l4-sea-level-heights-and-velocities-with-swot.html).

## Workflow/Roadmap



## Results/Findings



## Lessons Learned



## References

Höhlein, K., Kern, M., Hewson, T., & Westermann, R. (2020). A comparative study of convolutional neural network models for wind field downscaling. Meteorological Applications, 27(6), e1961.

Zhang, Z., Liu, Q., & Wang, Y. (2018). Road extraction by deep residual u-net. IEEE Geoscience and Remote Sensing Letters, 15(5), 749-753.


