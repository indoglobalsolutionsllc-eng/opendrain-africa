# OpenDrain-Africa

## Project Version
OpenDrain-Africa v1.0

## Project Purpose
OpenDrain-Africa is an open-source GeoAI model designed to detect visible open roadside drainage channels from very high-resolution RGB aerial imagery.

The model is intended to support humanitarian mapping, flood preparedness, infrastructure assessment, disaster-risk reduction, and open mapping.

## Initial Geographic Focus
Abeokuta, Ogun State, Nigeria.

The model is intended to expand to additional African cities as additional validated training data becomes available.

## Target Feature
Visible open constructed roadside drainage channels.

The model will not infer drainage infrastructure that cannot be visually confirmed from aerial imagery.

## AI Task
Semantic Segmentation

## Framework
PyTorch

## Input
3-band RGB GeoTIFF aerial imagery.

Bands:
- Red
- Green
- Blue

## fAIr Chip Size
256 x 256 pixels

## Classes
0 = background  
1 = open_drain

## Output
GeoJSON Polygon features representing visible open drainage channels.

## Model Deployment
ONNX

## Training and Validation
Spatial split

Default validation ratio: 0.20

Default split seed: 42

## License
Apache License 2.0

SPDX Identifier: Apache-2.0

## Workflow
RGB aerial imagery  
→ GeoTIFF chips  
→ human-validated drainage labels  
→ semantic-segmentation training  
→ drainage probability mask  
→ vectorization  
→ GeoJSON polygons  
→ HOT fAIr

## Version 1 Scope
Version 1 detects one feature only:

Visible open roadside drainage.

Future versions may include other drainage and flood-related infrastructure.

## Known Initial Limitations
Performance may be affected by:

- Vegetation covering drainage
- Heavy shadows
- Covered drainage systems
- Poor image resolution
- Water, roads, or shadows that resemble drainage
- Geographic differences between training locations
- Image quality and capture conditions