# Make Flood Extent and Compare to Flood Risk & Vulnerability
This repository contains the code that was used to produce results for a <a href= https://rdcu.be/dPcyu>study</a> published in <i>Natural Hazards</i>. 

<p align="center">
  <img src="/Flood_Schul.JPG" title="test" width="60%" />
</p>

## Google Earth Engine (GEE) Steps
<a href=https://code.earthengine.google.com/7a770b9cb0fbbe28ff800a779452d26a> Part I Make RF Model Inputs</a>: Get Sentinel-2 (10 m) satellite data, derives indices, join with other data (DEM, land cover, water), and export for the model. 

<a href=https://code.earthengine.google.com/6a1bf94510abb49f38af6514117bc513> Part II Run RF Model</a>: Use Part I outputs and training data to train and run RF model, output is 10-m raster classified as NotWater (0), Water (permanent) (1), and Flood (2). This classified layer is also available as a geojson file on <a href= https://zenodo.org/records/13145035>Zenodo</a>.


## Python Steps
<a href=https://github.com/rlwcomposto/Flood_Extent_Comparison_Ida_PA_2021/blob/main/PartIII.ipynb > Part III Compare Flood Area</a>: Calculate area and percent of flood extent (output of Part II) for <a href=https://www.fema.gov/flood-maps> FEMA Flood Risk Zones </a> (100-year, 500-year, Minimal Risk). Plot the area and percent of flooding that occured in each zone at the tract level. This code requires downloading data from <a href=https://hazards.fema.gov/femaportal/NFHL/searchResult>FEMA</a>.

<a href=https://github.com/rlwcomposto/Flood_Extent_Comparison_Ida_PA_2021/blob/main/PartIV.ipynb > Part IV Compare Flood Impact</a>: Plot Lorenz curves and calculate the Gini coefficient to determine distribution of flood impact. This code requires downloading vulnerability data from the <a href=https://www.atsdr.cdc.gov/placeandhealth/svi/data_documentation_download.html >CDC</a>.


## Other products
- <a href= https://rdcu.be/dPcyu>Paper</a> published in <i>Natural Hazards</i> creating novel flood extent for Hurricane Ida in southeastern Pennsylvania using satellite imagery and the Random Forest machine learning algorithm.
- Skip the paper, go straight to this <a href=https://experience.arcgis.com/experience/3d12e11db70740d28a52b29f33c9f1a7/>interactive map<a/> displaying the flood extent, roads, FEMA flood zones and more.
- Skip the map, go straight to the data and download the <a href=https://zenodo.org/records/13145035>vectorized flood extent</a> .


