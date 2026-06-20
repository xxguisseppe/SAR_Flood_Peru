# SAR Flood Mapping in Northern Peru

This repository contains a Google Earth Engine workflow for mapping flood-affected areas in northern Peru during the 2017 Coastal El Nino event. The project uses Sentinel-1 Synthetic Aperture Radar (SAR) imagery and Otsu thresholding to identify inundated areas before and after the flood event.

## Overview

Flood mapping is an important application of remote sensing for disaster risk assessment, emergency response, and environmental monitoring. SAR imagery is especially useful for flood detection because radar data can be acquired independently of daylight and most cloud conditions.

This project demonstrates a reproducible geospatial workflow for detecting flood extent from Sentinel-1 GRD imagery in Google Earth Engine.

## Study Context

In 2017, the northern coast of Peru was strongly affected by the Coastal El Nino event, which caused intense rainfall, river overflow, landslides, and flooding across several regions. This repository focuses on flood detection in the Chulucanas District, Piura, Peru.

## Objective

The objective is to detect and map flood-affected areas using SAR imagery and threshold-based image classification.

The workflow addresses:

- Where flood-affected areas were detected.
- How Sentinel-1 SAR data can support flood mapping under cloudy conditions.
- How Otsu thresholding can be applied to SAR backscatter values.
- How remote sensing workflows can support disaster risk analysis.

## Data and Platform

- Platform: Google Earth Engine
- Sensor: Sentinel-1 GRD
- Polarization: VV
- Orbit pass: Descending
- Spatial scale: 10 m
- Ancillary data: HydroSHEDS DEM for slope masking

## Methodology

1. Define the study area and threshold calibration area.
2. Filter Sentinel-1 GRD imagery by orbit, polarization, resolution, date, and study area.
3. Select pre-flood and post-flood image periods.
4. Apply focal mean smoothing to reduce SAR speckle.
5. Compute SAR backscatter histograms.
6. Estimate water thresholds using the Otsu method.
7. Generate pre-flood and post-flood water masks.
8. Derive the flood mask from post-flood water expansion.
9. Apply post-processing using connectivity filtering and slope masking.
10. Calculate flooded area in square metres, hectares, and square kilometres.
11. Export raster and vector flood extent outputs.

## Repository Structure

```text
SAR_Flood_Peru/
|-- Active_Remote_SE/       # Additional SAR remote sensing workflow folder
|-- flood_area_otsu.js      # Google Earth Engine flood mapping script
|-- LICENSE                 # Project license
`-- README.md               # Project documentation
```

## How to Use

1. Open `flood_area_otsu.js` in the Google Earth Engine Code Editor.
2. Replace the private Google Earth Engine assets at the top of the script with your own study area assets.
3. Review or adjust the pre-flood and post-flood date ranges.
4. Run the script in Google Earth Engine.
5. Inspect the flood mask and exported raster/vector outputs.

## Outputs

The script exports:

- A raster flood extent image to Google Drive.
- A vector flood extent shapefile to Google Drive.
- Flooded area statistics printed in square metres, hectares, and square kilometres.

## Skills Demonstrated

- Sentinel-1 SAR flood mapping
- Google Earth Engine scripting
- Otsu thresholding
- SAR preprocessing and speckle reduction
- Flood mask post-processing
- Raster and vector geospatial export
- Disaster risk and environmental analysis

## Limitations

- The script currently depends on private Google Earth Engine assets for the study area and threshold calibration area.
- Users must replace those assets with their own accessible geometries before running the workflow.
- Flood detection results depend on the selected dates, polarization, orbit pass, threshold calibration area, and post-processing parameters.

## Author

Guisseppe A. Vasquez Villano

## License

This project is distributed under the license included in the `LICENSE` file.
