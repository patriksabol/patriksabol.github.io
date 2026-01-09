---
layout: page
title: Foundation Model for Geospatial Analysis
description: EU-funded HPC project developing AI foundation models for geospatial data
img: assets/img/projects/ffplus.jpg
importance: 2
category: geospatial
---

Leading the development of a comprehensive foundation model for geospatial analysis, funded by Fortisimo Plus (FFplus) - a European initiative promoting HPC adoption by SMEs.

## Project Overview

This project leverages EuroHPC supercomputing resources (MareNostrum-5) to build a scalable AI foundation model that serves as the backbone for multiple downstream geospatial tasks, enhancing European SME competitiveness in AI-driven geospatial technologies.

**Client:** Geodeticca Vision (FFplus Innovation Study)
**Funding:** European Union - Fortisimo Plus Initiative
**Infrastructure:** MareNostrum-5 Supercomputer

## Technical Achievements

### Model Architecture
- Vision Transformer-based foundation model
- Masked Autoencoder (MAE) pre-training approach
- Comparison of backbone architectures: DINOv2, GVFM
- Multi-scale feature extraction for diverse geospatial tasks

### High-Performance Computing
- Distributed training on HPC infrastructure (MareNostrum-5)
- SLURM batch script optimization
- Singularity container deployment
- Efficient data pipeline for 17 European countries' datasets

### Foundation Model Applications
- Building footprint extraction
- Land cover classification
- Infrastructure mapping
- Change detection

## Technical Stack

- **Framework**: PyTorch, PyTorch Lightning
- **Infrastructure**: MareNostrum-5 HPC, SLURM
- **Containerization**: Singularity
- **Data Processing**: GDAL, Geopandas, Shapely
- **Monitoring**: Weights & Biases (Wandb), MLflow

## Key Innovations

- **Semi-supervised Learning**: Achieved significant cost reduction in labeling requirements
- **Transfer Learning**: Foundation model adapts to various downstream tasks with minimal fine-tuning
- **Scale**: Processing massive datasets covering multiple European countries
- **Efficiency**: Optimized training workflows reducing time-to-model by 60%

## Impact

The CARTOGRAPHER platform and foundation model enable cost-effective geospatial analysis for SMEs across Europe, democratizing access to advanced AI capabilities previously available only to large organizations with extensive computational resources.
