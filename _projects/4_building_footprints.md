---
layout: page
title: Building Footprint Extraction
description: Deep learning pipeline for topologically clean building vector extraction
img: assets/img/projects/buildings.jpg
importance: 4
category: geospatial
---

Development and implementation of an advanced deep learning pipeline for extracting building footprints and other infrastructure features from orthophotos, with a focus on generating topologically clean vector outputs.

## Project Overview

This project tackles the complex problem of automatically extracting building footprints from aerial imagery while ensuring the output vectors are topologically correct—essential for GIS applications and urban planning.

**Client:** Geodeticca Vision
**Application Domain**: Urban mapping, cadastral updates, infrastructure planning

## Technical Challenge

Extracting building footprints from aerial imagery involves several challenges:

- **Raster-to-Vector Conversion**: Traditional segmentation produces rasters; we need clean vectors
- **Off-Nadir Displacement**: Aerial imagery captured at angles causes visible rooftops to be displaced from actual ground footprints
- **Topological Quality**: Outputs must be valid polygons without overlaps, gaps, or self-intersections
- **Scale Variation**: Buildings range from small sheds to large industrial complexes

## Solution Architecture

### Deep Learning Pipeline

1. **Semantic Segmentation**: Initial building detection using U-Net/DeepLabv3+ architectures
2. **Polygonization**: Advanced vectorization preserving geometric accuracy
3. **Footprint Rectification**: ML-based correction of off-nadir displacement
4. **Topology Cleaning**: Post-processing to ensure valid GIS-ready outputs

### Footprint Rectification Innovation

The system addresses a unique challenge in aerial photogrammetry: when buildings are photographed at an angle, the visible rooftop appears displaced from where the building actually stands on the ground. Our ML model learns this displacement pattern and corrects it automatically.

### Technical Components

- **Backbone Networks**: ResNet, EfficientNet for feature extraction
- **Segmentation Heads**: Multi-scale prediction for various building sizes
- **Vector Refinement**: Graph-based topology cleaning algorithms
- **Quality Assurance**: Automated validation of output geometries

## Technical Stack

- **Deep Learning**: PyTorch, segmentation_models.pytorch
- **Geospatial Processing**: GDAL, Shapely, Geopandas, QGIS
- **Vector Operations**: PostGIS, topology validation libraries
- **Deployment**: Docker, FastAPI for serving predictions

## Dataset & Training

- **Data Sources**: Aerial orthophotos from various European regions
- **Labeling**: Custom annotation workflows using QGIS
- **Augmentation**: Rotation, scaling, color jittering to handle diverse imagery
- **Training Infrastructure**: Cloud-based GPU clusters

## Results & Impact

The system produces high-quality building footprint vectors suitable for:
- Cadastral database updates
- Urban planning and development
- 3D city model generation
- Infrastructure monitoring
- Emergency response mapping

Achieved significant time savings compared to manual digitization while maintaining high geometric accuracy and topological correctness required for professional GIS workflows.
