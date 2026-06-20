# SAR Flood Mapping in Northern Peru

This repository contains a remote sensing workflow for detecting flood-affected areas in northern Peru during the 2017 Coastal El Niño event. The project uses Synthetic Aperture Radar (SAR) data and threshold-based classification methods to identify inundated areas.

The workflow was developed as an applied Earth observation exercise focused on flood detection in a province in northern Peru affected by the *Fenómeno del Niño Costero 2017*.

---

## Project Overview

Flood mapping is an important application of remote sensing for disaster risk assessment, emergency response, and environmental monitoring. SAR imagery is particularly useful for flood detection because radar sensors can acquire information independently of cloud cover and daylight conditions.

This project explores the use of SAR-based methods to detect flooded areas and estimate the spatial extent of inundation during an extreme rainfall and flooding event in Peru.

---

## Study Context

In 2017, the northern coast of Peru was strongly affected by the *Fenómeno del Niño Costero*, which produced intense rainfall, river overflow, landslides, and flooding across several regions.

This repository focuses on detecting flood-affected areas using radar remote sensing and image classification methods.

---

## Objective

The main objective of this project is to detect and map flood-affected areas in northern Peru using SAR imagery.

The workflow aims to answer:

- Where were flood-affected areas detected?
- How can SAR data support flood mapping under cloudy conditions?
- How can threshold-based classification methods be applied to flood detection?
- How can remote sensing workflows support disaster risk analysis?

---

## Methods

The repository includes scripts and/or workflows related to:

1. SAR data preparation
2. Pre-processing of radar imagery
3. Flood detection using image thresholding
4. Application of the Otsu thresholding method
5. Flood area extraction
6. Export of flood classification outputs

The folder `Flood_Area_OTSU` suggests the use of the Otsu thresholding method to identify flooded areas from SAR-derived information.

---

## Repository Structure

```text
SAR_Flood_Peru/
├── Active_Remote_SE/     # SAR remote sensing processing workflow
├── Flood_Area_OTSU/      # Flood area detection using Otsu thresholding
├── LICENSE               # Project license
└── README.md             # Project documentation
