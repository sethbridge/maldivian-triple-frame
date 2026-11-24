# Parametric Design Reference

## All Parameters

### Core Painting Dimensions
```
paint_w = 299.9 mm        # Painting width (11 13/16")
paint_h = 402 mm          # Painting height (15 13/16")
num_paintings = 3         # Number of paintings in frame
```

### Frame Border Widths (Golden Ratio Hierarchy)
```
frame_base_w = 185.4 mm   # Outer border width (paint_w ÷ 1.618)
frame_mid_w = 114.5 mm    # Mid-layer width (paint_w ÷ 2.618)
frame_fine_w = 70.8 mm    # Fine detail width (paint_w ÷ 4.236)
```

### Frame Depth & Thickness
```
frame_depth = 43.7 mm     # Total frame depth (paint_w ÷ 6.86)
frame_z = 26.9 mm         # Frame height/Z-thickness (paint_w ÷ 11.14)
```

### Glass & Bevel
```
glass_thick = 4 mm        # Glass panel thickness
bevel_depth = 13.45 mm    # 5° bevel recession depth (frame_z ÷ 2)
```

### Spacing
```
gap_between = 114.5 mm    # Space between paintings (= frame_mid_w)
```

### Calculated Dimensions (Auto-computed)
```
total_w = paint_w * 3 + gap_between * 4 + frame_base_w * 2
        = 1,728.5 mm      # Total assembly width

total_h = paint_h + frame_base_w * 2
        = 772.8 mm        # Total assembly height
```

## Golden Ratio Relationships

All frame proportions follow φ (1.618):

| Layer | Width (mm) | Relationship | Ratio |
|-------|-----------|--------------|-------|
| Outer | 185.4 | paint_w ÷ 1.618 | 1.0 |
| Mid | 114.5 | paint_w ÷ 2.618 | 0.618 |
| Fine | 70.8 | paint_w ÷ 4.236 | 0.382 |

Each layer is φ times smaller than the previous.

## Modification Guide

### Change Painting Size
To use different painting dimensions:
```
paint_w = [new width in mm]
paint_h = [new height in mm]
```
All frame proportions auto-scale via golden ratio calculations.

### Change Number of Paintings
```
num_paintings = [new count]
```
Adjust `total_w` formula to: `paint_w * num_paintings + gap_between * (num_paintings + 1) + frame_base_w * 2`

### Adjust Frame Thickness
```
frame_z = [new thickness in mm]
bevel_depth = frame_z / 2    # Keeps bevel proportional
```

### Adjust Glass Thickness
```
glass_thick = [new thickness in mm]
```
No other parameters affected.

### Adjust Bevel Angle
```
bevel_depth = [new depth in mm]
```
Current: 13.45 mm for 5° chamfer

## Usage in SolidCraft

All parameters are expressions that can be referenced in:
- Sketch dimensions: `sketch.dimension` with `value: "paint_w / 2"`
- Feature fields: `solid.box` with `length: "paint_w"`
- Extrude distances: `solid.extrude` with `distance: "frame_z"`

Example sketch dimension:
```
{
  "command": "sketch.dimension",
  "params": {
    "entities": ["l1"],
    "value": "frame_base_w - frame_mid_w"
  }
}
```

## Parameter Values Summary

| Name | Value | Unit | Formula/Source |
|------|-------|------|-----------------|
| paint_w | 299.9 | mm | Base measurement |
| paint_h | 402 | mm | Base measurement |
| glass_thick | 4 | mm | Standard glass |
| frame_base_w | 185.4 | mm | paint_w ÷ φ |
| frame_mid_w | 114.5 | mm | paint_w ÷ φ² |
| frame_fine_w | 70.8 | mm | paint_w ÷ φ³ |
| frame_depth | 43.7 | mm | paint_w ÷ φ⁴ |
| gap_between | 114.5 | mm | = frame_mid_w |
| frame_z | 26.9 | mm | paint_w ÷ φ⁵ |
| bevel_depth | 13.45 | mm | frame_z ÷ 2 |
| total_w | 1,728.5 | mm | Calculated |
| total_h | 772.8 | mm | Calculated |
| num_paintings | 3 | count | Design spec |

---

**Note**: φ (phi) = 1.618... (golden ratio)
