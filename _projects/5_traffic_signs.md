---
layout: page
title: Traffic Sign Detection & Vectorization
description: ML system for automated detection and vectorization of traffic signs in geospatial data
img: assets/img/projects/traffic_signs.jpg
importance: 5
category: geospatial
---

Design and deployment of machine learning models for automated detection and vectorization of horizontal and vertical traffic signs from aerial and ground-level imagery.

## Project Overview

This project addresses the labor-intensive task of maintaining accurate traffic sign inventories by automating both detection and precise vectorization of traffic infrastructure.

**Client:** Geodeticca Vision
**Application**: Road infrastructure mapping, traffic management systems

## Scope

### Horizontal Traffic Signs
- Lane markings
- Pedestrian crossings
- Stop lines
- Arrow indicators
- Parking bay markings

### Vertical Traffic Signs
- Regulatory signs (speed limits, stop signs)
- Warning signs
- Informational signs
- Sign position and orientation

## Technical Approach

### Detection Pipeline

**Object Detection**: YOLOv5/YOLOv8 models fine-tuned for traffic sign detection
- High precision at various scales
- Real-time inference capability
- Robust to occlusion and varying lighting

**Classification**: Multi-class classification of detected signs
- Transfer learning from ImageNet
- Custom dataset with European traffic sign standards
- High accuracy across sign categories

### Vectorization System

Beyond simple bounding boxes, the system extracts precise vector representations:

- **Polygon Extraction**: Accurate boundaries of horizontal markings
- **Position Encoding**: GPS coordinates of vertical sign locations
- **Orientation Detection**: Angle and facing direction of signs
- **GIS Integration**: Direct export to Shapefile/GeoJSON formats

## Technical Stack

- **Detection**: PyTorch, YOLOv8, Detectron2
- **Image Processing**: OpenCV, PIL
- **Geospatial**: GDAL, Geopandas, coordinate transformations
- **Deployment**: Docker containers, FastAPI endpoints
- **Data Processing**: Efficient batch processing pipelines

## Dataset Development

- **Data Collection**: Aerial orthophotos and mobile mapping imagery
- **Annotation**: Custom labeling workflows with domain expert validation
- **Classes**: 50+ distinct traffic sign and marking types
- **Augmentation**: Synthetic data generation for rare sign types

## Deployment Architecture

### Inference Service
- RESTful API for on-demand processing
- Batch processing for large-scale imagery
- GPU acceleration for real-time performance

### Output Formats
- Vector layers (Shapefile, GeoJSON)
- Attributed features (sign type, condition, GPS coordinates)
- Quality metrics and confidence scores
- Integration with GIS databases

## Applications

The system enables municipalities and transportation agencies to:

- Maintain up-to-date traffic sign inventories
- Plan road maintenance and sign replacement
- Ensure compliance with traffic regulations
- Support autonomous vehicle HD map creation
- Optimize traffic flow management

## Results

Automated processing achieves:
- 95%+ detection accuracy for standard signs
- Significant reduction in manual survey costs
- Rapid updates covering hundreds of kilometers
- Standardized, GIS-ready vector outputs
