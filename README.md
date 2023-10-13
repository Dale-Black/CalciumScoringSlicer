# CalciumScoringSlicer

CalciumScoringSlicer is a 3D Slicer plugin for calculating coronary artery calcium scores from CT images using different quantification algorithms. See the [documentation](https://glassnotebook.io/r/7uus7O8aIcLsGebjQFqxU/docs/(00)%20Getting%20Started.jl) for more details.

## Features
```mermaid
graph TB
    classDef unique1 fill:#f9d71c,stroke:#333,stroke-width:2px;
    classDef unique2 fill:#8cd9f5,stroke:#333,stroke-width:2px;
    A["Overview: Four Different CAC Quantification Methods"]
    A --> AgatstonRegime
    A --> CalciumMassRegime
    subgraph AgatstonRegime["Agatston Scoring Regime"]
        B["Agatston Scoring"]
        E["Spatially Weighted Calcium Scoring"]
    end
    subgraph CalciumMassRegime["Calcium Mass Quantification Regime"]
        C["Volume Fraction Calcium Mass"]
        D["Integrated Calcium Mass"]
    end
    class B,C,D,E unique2;
```
- Handles scan calibration and voxel spacing information
- Easy to use GUI

## Installation

WIP

## Usage

The general workflow is:

1. Load DICOM Data
2. Create segmentation and segment the parts you need
3. Enter algorithm specific module from CalciumScoring category from dropdown menu
4. Select corresponding required and optional inputs (input volume, segmentation, etc.)
5. Press score button

### Algorithms
The main algorithms available are:
- `Agatston()`: Traditional Agatston scoring
- `VolumeFraction()`: Volume fraction calcium mass
- `Integrated()`: Integrated calcium mass
- `SpatiallyWeighted()`: Spatially weighted calcium scoring
