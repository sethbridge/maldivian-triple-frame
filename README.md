# Maldivian Triple-Frame

A parametric wooden frame design for displaying three ocean paintings with Maldivian design influences. Built with SolidCraft using golden ratio proportions throughout.

## Overview

This project creates a sophisticated triple-frame system designed to display three paintings (11 13/16" × 15 13/16") of Maldives ocean scenes. The frame features:

- **Golden Ratio Proportions** – All dimensions follow φ (1.618) relationships
- **Layered Borders** – Outer, mid, and fine-detail frame layers with visual hierarchy
- **Recessed Glass** – 4mm glass panels integrated flush into frame apertures
- **Beveled Edges** – 5-degree chamfers on frame borders for gallery-quality finish
- **Parametric Design** – All dimensions linked and scalable
- **Cultural Elements** – Inspired by Maldivian geometric patterns and ocean themes

## Specifications

### Painting Dimensions
- Width: 299.9 mm (11 13/16")
- Height: 402 mm (15 13/16")
- Quantity: 3

### Frame Parameters (Golden Ratio)
- **Outer Border** (`frame_base_w`): 185.4 mm (paint_w ÷ 1.618)
- **Mid Border** (`frame_mid_w`): 114.5 mm (paint_w ÷ 2.618)
- **Fine Detail** (`frame_fine_w`): 70.8 mm (paint_w ÷ 4.236)
- **Gap Between Paintings** (`gap_between`): 114.5 mm
- **Frame Thickness** (`frame_z`): 26.9 mm
- **Glass Thickness** (`glass_thick`): 4 mm
- **Bevel Depth** (`bevel_depth`): 13.45 mm (5° angle)

### Assembly Dimensions
- **Total Width**: 1,728.5 mm
- **Total Height**: 772.8 mm
- **Total Depth**: 65.07 mm (beveled profile)

### Materials & Mass
- **Wood Frame**: ~48 kg
- **Glass Panels**: ~1.84 kg (3 × 4mm)
- **Total Assembly**: ~50.3 kg

### Recommended Wood Species
- **Sapele** – Warm golden tones, tropical aesthetic
- **Mahogany** – Rich reddish-brown, luxury appearance
- **Walnut** – Sophisticated dark grain, contemporary
- **Maple** – Light, minimalist modern style

## Files

- `maldivian_parameters_foundation.sc` – SolidCraft design file with parametric foundation (13 linked parameters, no geometry)
- `README.md` – This file
- `DESIGN_NOTES.md` – Detailed design documentation
- `PARAMETERS.md` – Complete parameter reference

## Development

The design is fully parameterized in SolidCraft. To build from the foundation:

1. Open `maldivian_parameters_foundation.sc` in SolidCraft
2. All 13 parameters are pre-defined with golden ratio values
3. Create sketches and features using parametric dimensions
4. Modify `paint_w`, `paint_h`, or other base parameters to auto-scale entire frame

## Golden Ratio Architecture

Every dimension follows φ (1.618):
- Layer widths decrease: 185.4 → 114.5 → 70.8 mm (each ÷ φ)
- Frame depth: 43.7 mm (paint_w ÷ φ²)
- Frame height: 26.9 mm (paint_w ÷ φ³)
- Gap spacing: 114.5 mm (frame_mid_w)

Result: Harmonious proportions that naturally feel balanced and elegant.

## Usage

This is a design template ready for:
- **CAD Refinement** – Add Maldivian geometric inlays and decorative elements
- **Manufacturing** – Export to STEP/STL for CNC cutting and production
- **Customization** – Adjust parameters for different painting sizes
- **Material Selection** – Choose wood species and finishes

## License

MIT License - Free to use, modify, and distribute

---

**Design Approach**: Parametric, golden ratio-based, gallery-ready frame system inspired by Maldivian ocean and traditional design elements.
