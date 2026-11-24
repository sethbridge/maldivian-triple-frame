# Maldivian Triple Frame - SolidCraft Design Review

## Overview
The **Maldivian Triple Frame** is a parametric 3D CAD design created in SolidCraft for a triple-panel display frame. It's designed to hold three paintings or artworks side-by-side within a unified frame structure.

## Key Specifications

### Overall Dimensions
- **Total Width**: 1,204.91 mm (47.5 in)
- **Total Height**: 554.04 mm (21.8 in)
- **Frame Depth**: 12.7 mm (0.5 in)
- **Frame Height (Z)**: 38.1 mm (1.5 in)

### Panel Configuration
- **Number of Panels**: 3 (left, center, right)
- **Painting Width**: 300.04 mm (11.8 in)
- **Painting Height**: 401.64 mm (15.8 in)
- **Glass Thickness**: 3.175 mm (1/8 in)
- **Painting Depth**: 17.46 mm (11/16 in)

### Frame Details
- **Frame Middle Width**: 76.2 mm (3 in) - dividers between panels
- **Gap Between Panels**: 1.59 mm (1/16 in)
- **Painting Overlap**: 6.35 mm (1/4 in)
- **Bevel Angle**: 10 degrees
- **Bevel Depth**: 44.45 mm (1.75 in)

## Structure

### Bodies
The design consists of **4 separate bodies**:

1. **OuterFrame** (Outer container)
   - Volume: 4,885,393 mm³
   - Surface Area: 512,902 mm²
   - Bounding Box: 1,204.9 × 554.0 × 38.1 mm
   - 10 faces, closed solid

2. **Center Panel**
   - Volume: 2,062,100 mm³
   - Dimensions: 376.2 × 477.8 × 38.1 mm
   - Holds the center painting

3. **Right Panel**
   - Volume: 2,062,100 mm³
   - Positioned offset to the right
   - Mirrors center panel geometry

4. **Left Panel**
   - Volume: 2,062,100 mm³
   - Positioned offset to the left
   - Mirrors center panel geometry

### Design Features (Timeline)
- **Sketch1**: Base profile sketch (38 curves, 8 profiles, solved)
- **Extrude1**: Initial extrusion of base frame
- **Extrude2**: Second extrusion for frame structure
- **Chamfer1**: Beveled edges (10° angle)
- **RectangularPattern1**: Rectangular pattern for panel repetition
- **Mirror1**: Mirror feature to create left/right symmetry
- **Sketch2**: Additional detail sketch (14 curves, 3 profiles, visible)
- **Extrude3**: Final extrusion for frame details

## Parameters (24 user parameters)

All parameters use Imperial units (inches) with derived metric conversions:

| Parameter | Value | Expression |
|-----------|-------|-----------|
| paint_w | 300.04 mm | 11 13/16" |
| paint_h | 401.64 mm | 15 13/16" |
| glass_thick | 3.175 mm | 1/8" |
| frame_mid_w | 76.2 mm | 3" |
| frame_depth | 12.7 mm | 1/2" |
| gap_between | 1.59 mm | 1/16" |
| frame_z | 38.1 mm | 1.5" |
| bevel_depth | 12.7 mm | 1/2" |
| bevel_angle | 0.1745 rad | 10° |
| painting_overlap | 6.35 mm | 1/4" |
| paint_d | 17.46 mm | 11/16" |
| **Derived Parameters** | | |
| total_w | 1,204.91 mm | paint_w * 3 + frame_mid_w * 4 |
| total_h | 554.04 mm | paint_h + frame_mid_w * 2 |

## Design Methodology

The frame uses a **parametric-driven approach**:
- All dimensions are defined by parent parameters
- The three panels are created using rectangular pattern and mirror operations
- Beveled edges (chamfer) add professional finishing
- Fully constrained sketches (DOF = 0) ensure dimensional stability

## Use Cases

This design is suitable for:
- Display frames for art galleries or exhibitions
- Multi-panel artwork presentation
- Parametric design portfolio demonstration
- CAD template for custom frames

## Export-Ready

The design is fully modeled and ready for:
- CNC manufacturing
- 3D printing (with material adjustments)
- Rendering and visualization
- Further customization via parameter adjustment
