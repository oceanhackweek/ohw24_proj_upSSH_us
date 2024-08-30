# Upscaling Sea Surface Height

This repository provides the code for accessing altimetry and model data, as well as the U-Net neural network implementation used to upscale altimetry data from 1/4 to 1/12 degrees.

## Collaborators

* Lara Schlumbom      
* Pedro Walfir      
* Yifei Hang      

## Additional Informations

* Ideation Presentation: [Project Pitch](https://docs.google.com/presentation/d/1MG32LTh15YH1vHQdv_7U-SAyclAFcNLs-xWWvf0eZ8g/edit#slide=id.g2f660589f1f_28_0)
* Slack channel: ohw24_proj_upssh_us
* Final presentation: [Project Presentation](https://docs.google.com/presentation/d/1Z9WfwqM1KbRRhXcNXrDurZ-Vts_iLjF75h0j9Lux4_o/edit#slide=id.p)

## Background

Traditional altimetry products, with a resolution of 1/4°, fail to capture the fine-scale motions in the ocean. The recently launched SWOT satellite addresses this limitation by providing sea surface height (SSH) measurements at a much finer resolution of 1 km. However, its coverage is restricted to narrow swaths, limiting its utility for global ocean monitoring.

Neural networks, particularly convolutional architectures like U-Net, have proven to be powerful tools in this context. By learning complex patterns from high-resolution model outputs, these networks can significantly enhance the resolution of SSH data from classical altimetry, bridging the gap between coarse measurements and the detailed dynamics observed in the ocean. In our project, we leverage a U-Net trained on GLORYS12V1 model outputs to upscale SSH data from 1/4° to 1/12°. This approach not only provides ocean scientists with more detailed information but also demonstrates the transformative potential of neural networks in advancing our understanding of ocean dynamics.


## Goals

Find a suitable neural network arhitecture for increasing sea surface height data resolution and apply that to lower resolution satellite measurements.

## Datasets

**GLORYS12v1 Absolute Dynamic Topography**

  We used the [GLORYS12v1 product](https://data.marine.copernicus.eu/product/GLOBAL_MULTIYEAR_PHY_001_030/description) from the CMEMS global ocean eddy-resolving reanalysis, with a horizontal resolution of 1/12°, for training the model.
   
**AVISO Absolute Dynamic Topography**

   The [DUACS delayed-time altimeter](https://data.marine.copernicus.eu/product/SEALEVEL_GLO_PHY_CLIMATE_L4_MY_008_057/description) gridded maps of sea surface height distributed by the Copernicus Climate Change Service were used as a reference for the lower resolution grid. This data has horizontal spatial resolution of 1/4°.

**SWOT Level 3 Absolute Dynamic Topography**

   The [Surface Water and Ocean Topography Satellite (SWOT) Level 3 data](https://www.aviso.altimetry.fr/en/data/products/sea-surface-height-products/global/swot-l3-ocean-products.html) was used for selecting the region in which to validate the model.

**SWOT Level 4 Absolute Dynamic Topography**

   The [SWOT Level 4 data](https://www.aviso.altimetry.fr/en/data/products/sea-surface-height-products/global/experimental-multimission-gridded-l4-sea-level-heights-and-velocities-with-swot.html) was used for validating the model trained on GLORYS data.

## Workflow/Roadmap

1. Get GLORYS and AVISO data
2. Downscale GLORYS data to AVISO resolution
3. Find a neural network architeture to work with
4. Restructure U-Net architecture to fit the input and output dimensions of our data
5. Run the model and compare output to original GLORYS data
6. Get SWOT data and select validation region
7. Interpolate SWOT data to AVISO and GLORYS resolution
8. Validate upscaled altimetry output with SWOT data

## Results/Findings


## References

Höhlein, K., Kern, M., Hewson, T., & Westermann, R. (2020). A comparative study of convolutional neural network models for wind field downscaling. Meteorological Applications, 27(6), e1961.

Zhang, Z., Liu, Q., & Wang, Y. (2018). Road extraction by deep residual u-net. IEEE Geoscience and Remote Sensing Letters, 15(5), 749-753.


