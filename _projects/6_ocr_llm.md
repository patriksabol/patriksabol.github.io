---
layout: page
title: OCR with LLM Post-Correction
description: Advanced OCR system enhanced with Large Language Models for geospatial text extraction
img: assets/img/projects/ocr.jpg
importance: 6
category: geospatial
---

Development of an advanced Optical Character Recognition (OCR) system for extracting text from geospatial imagery, enhanced with Large Language Model (LLM) post-processing for improved accuracy and context-aware corrections.

## Project Overview

Traditional OCR systems struggle with challenging conditions common in geospatial imagery: varying fonts, rotations, perspective distortions, and partial occlusions. This project combines state-of-the-art OCR with LLM-based correction to achieve superior results.

**Client:** Geodeticca Vision
**Application**: Automated map digitization, cadastral data extraction, infrastructure labeling

## Technical Innovation

### Two-Stage Architecture

**Stage 1: OCR Detection & Recognition**
- Text detection in challenging conditions (rotation, perspective, low quality)
- Multi-language support (primarily European languages)
- Specialized handling of map-specific text (coordinates, place names, measurements)

**Stage 2: LLM Post-Correction**
- Context-aware error correction using Large Language Models
- Geospatial domain knowledge integration
- Disambiguation of uncertain characters based on semantic context
- Standardization of place names and addresses

## Why LLMs for OCR Correction?

Traditional OCR makes character-level errors without understanding context:
- "Košice" might be read as "Kos1ce" or "Kosice"
- Street numbers like "123" could become "1Z3"
- Coordinate values need specific formatting

LLMs understand geospatial context and can:
- Correct errors based on known place names
- Validate coordinate formats
- Fix common OCR confusions (0/O, 1/I/l, 5/S)
- Maintain semantic consistency across document

## Technical Stack

### OCR Components
- **Detection**: EAST, CRAFT text detection models
- **Recognition**: TrOCR, EasyOCR, Tesseract
- **Preprocessing**: OpenCV for image enhancement

### LLM Integration
- **Models**: GPT-4, Claude, fine-tuned open-source LLMs
- **Prompt Engineering**: Domain-specific prompts for geospatial context
- **Validation**: Rule-based checks combined with LLM suggestions
- **API Integration**: Efficient batching and caching strategies

### Geospatial Processing
- **Coordinate Systems**: Recognition and validation of various projections
- **Gazetteer Integration**: Cross-referencing with official place name databases
- **Map Metadata**: Extraction of scale, legend, and orientation information

## Workflow

1. **Image Preprocessing**: Enhancement, rotation correction, binarization
2. **Text Detection**: Locate text regions in imagery
3. **OCR Recognition**: Extract raw text with confidence scores
4. **LLM Correction**: Context-aware refinement of uncertain extractions
5. **Validation**: Cross-check against geospatial databases
6. **Structured Output**: Export to GIS-compatible formats with attributes

## Applications

### Cadastral Map Digitization
- Extracting parcel numbers, owner information
- Reading area measurements and boundary descriptions
- Digitizing historical maps

### Infrastructure Mapping
- Road names and numbers
- Utility labels (power lines, pipelines)
- Building addresses and identifiers

### Topographic Map Processing
- Elevation labels
- Place names and features
- Coordinate grids and scale bars

## Results & Impact

The LLM-enhanced OCR system achieves:
- **Character-level accuracy**: 98%+ (vs. 92% for standard OCR)
- **Semantic accuracy**: 99%+ for validated geospatial entities
- **Processing speed**: 100+ map sheets per hour
- **Cost savings**: 80% reduction vs. manual transcription

The system enables rapid digitization of legacy maps and automated extraction of text from modern geospatial imagery, unlocking valuable data previously trapped in raster formats.
