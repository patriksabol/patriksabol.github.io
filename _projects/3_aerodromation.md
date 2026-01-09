---
layout: page
title: AERODROMATION - Automated Airport Mapping
description: ESA project for automated airport infrastructure mapping from satellite imagery
img: assets/img/projects/aerodromation.jpg
importance: 3
category: geospatial
---

Technical lead for the AERODROMATION project, an ESA-funded initiative focused on automating airport infrastructure mapping from satellite imagery using the Pix2Poly deep learning framework.

## Project Overview

AERODROMATION addresses the challenge of maintaining up-to-date airport maps by automatically extracting vector representations of airport infrastructure from high-resolution satellite imagery.

**Client:** Geodeticca Vision (European Space Agency project)
**Funding:** European Space Agency (ESA)
**Framework:** Pix2Poly

## Technical Challenge

Traditional methods of airport mapping require manual digitization, which is time-consuming and expensive. This project automates the process using state-of-the-art computer vision techniques to extract clean, topologically-correct vector representations.

### Key Challenges Addressed
- **Polygon Extraction**: Direct vectorization from raster imagery
- **Topological Correctness**: Ensuring no overlaps or gaps in extracted features
- **Multi-class Prediction**: Simultaneous detection of runways, taxiways, aprons, and buildings
- **Vision Language Models**: Integration of VLMs with Pix2Poly architecture

## Technical Implementation

### Core Technology
- **Pix2Poly Framework**: Transformer-based architecture for direct polygon prediction
- **Vision Transformers**: ViT backbones for feature extraction
- **TopoJSON-style Encoding**: Eliminates polygon overlap issues
- **Multi-modal Learning**: Integration of satellite imagery with textual descriptions

### Deployment Architecture
- **Cloud Platform**: Google Cloud Platform (GCP)
- **Orchestration**: Google Kubernetes Engine (GKE) with GPU clusters
- **Inference Server**: Nvidia Triton Server
- **Scalability**: Handles large-scale satellite imagery processing

### Data Processing
- **Input**: High-resolution satellite imagery from various sources
- **Preprocessing**: Coordinate system transformations, orthorectification
- **Output**: Clean vector layers (GeoJSON, Shapefile formats)

## Technical Stack

- **Deep Learning**: PyTorch, Transformers
- **Deployment**: Docker, Kubernetes, GKE, Nvidia Triton
- **Geospatial**: GDAL, PostGIS, QGIS
- **MLOps**: DVC, MLflow, Wandb

## Innovations

- **Off-nadir Correction**: Addressing building footprint displacement in aerial imagery
- **Topological Guarantees**: Ensuring valid vector outputs suitable for GIS workflows
- **Vision-Language Integration**: Combining visual and textual modalities for improved accuracy
- **Production-Ready**: Fully automated pipeline from satellite imagery to validated vector data

## Impact

The AERODROMATION system enables regular, automated updates of airport infrastructure maps, reducing costs and improving safety through timely detection of changes in airport layouts. The technology is applicable beyond airports to urban planning and infrastructure monitoring.
