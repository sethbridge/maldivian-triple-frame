# Design Notes - Maldivian Triple-Frame

## Project Vision

Create a gallery-quality triple-frame system for displaying three paintings of Maldives ocean scenes. The design integrates:

1. **Cultural Elements** – Maldivian geometric patterns, ocean/coral motifs
2. **Mathematical Harmony** – Golden ratio throughout all proportions
3. **Practical Engineering** – Recessed glass, beveled edges, parametric flexibility
4. **Visual Sophistication** – Layered frame hierarchy with refined aesthetics

## Design Philosophy

### Golden Ratio Basis
All frame proportions follow φ (1.618), creating natural visual harmony:
- Viewers perceive golden ratio proportions as inherently balanced
- Each border layer is φ times smaller than the previous
- Results in elegant, gallery-ready appearance without seeming over-designed

### Layered Visual Hierarchy
Three frame layers create depth and visual interest:
1. **Outer Border** (185.4 mm) – Dominant frame presence
2. **Mid Border** (114.5 mm) – Secondary visual layer
3. **Fine Detail** (70.8 mm) – Accent layer with beveled edges

This hierarchy guides the eye through the frame into the artwork.

### Recessed Glass Integration
- Glass sits 5mm inset from frame surface
- Creates shadow line emphasizing each painting
- 1mm tolerance gap prevents glass-to-wood contact
- Professional gallery finish

### Beveled Edges (5°)
- 5-degree chamfers on all outer borders
- Creates elegant shadow line
- Sophistication without ostentation
- Light-catching surface adds visual depth

## Maldivian Design Elements (Future Implementation)

Planned decorative additions:
1. **Geometric Inlays** – Islamic-inspired star patterns in corner medallions
2. **Wave Motifs** – Ocean-inspired undulating patterns on frame edges
3. **Coral Elements** – Textured cylindrical elements representing reef structures
4. **Border Patterns** – Triangular geometric inlay cuts at frame borders
5. **Traditional Elements** – Concentric circles and cross-hatched patterns

Implementation approach:
- Create parametric sketch profiles for each element
- Use extrude/cut operations to inlay patterns 1-2mm deep
- Apply to corner blocks and frame edges
- Enhance with wood staining or inlay materials

## Structural Decisions

### Why Recessed Glass?
- Glass floating on top appears cheap/temporary
- Recessed integration looks permanent and professional
- Protects glass edges from damage
- Creates cohesive single-piece aesthetic

### Why Three Layers?
- Single flat border looks plain
- Two layers insufficient visual depth
- Three layers create balanced hierarchy
- Matches golden ratio hierarchy perfectly

### Why This Size Range?
- Outer (185.4 mm) – Substantial enough for inlay patterns
- Mid (114.5 mm) – Accent layer, visual transition
- Fine (70.8 mm) – Detail layer, beveled edge emphasis
- Gaps (114.5 mm) – Breathing room, natural spacing

### Why Beveled, Not Filleted?
- Bevels create defined shadow lines
- Filleted edges too soft for gallery aesthetic
- 5-degree angle: shallow enough for elegance, defined enough for visual impact
- Easier to manufacture than complex curves

## Parametric Architecture

All 13 parameters are interconnected:
- Change `paint_w` → entire frame auto-scales
- Change `frame_z` → `bevel_depth` can auto-scale
- Change `num_paintings` → `total_w` recalculates
- All golden ratio relationships preserved

This enables:
- Quick design iterations
- Easy customization for client needs
- Scalability to different painting sizes
- Manufacturing precision

## Material Characteristics

**Recommended Woods** (by aesthetic):

1. **Sapele** – Warm golden-orange tones, medium hardness, excellent workability
   - Best for: Tropical/ocean aesthetic
   - Finish: Oil or matte lacquer

2. **Mahogany** – Rich reddish-brown, medium hardness, beautiful grain
   - Best for: Luxury/traditional aesthetic
   - Finish: Satin lacquer or wax

3. **Walnut** – Deep brown/chocolate tones, hard, fine grain
   - Best for: Contemporary/sophisticated aesthetic
   - Finish: Matte lacquer or oil

4. **Maple** – Light blonde, fine grain, very hard
   - Best for: Minimalist/modern aesthetic
   - Finish: Clear matte or satin lacquer

**Glass Specification**:
- 4mm tempered low-iron glass
- UV-protective coating (optional)
- Anti-reflective coating (optional for paintings)
- 1mm tolerance gap in frame recess

## Manufacturing Considerations

### CNC Routing
- Export frame geometry as STEP file
- Use 3D CAM software for beveled edges
- Glass recession can be cut as one operation per painting area

### Hand Fabrication
- Frame can be constructed from solid wood or laminated boards
- Beveled edges created with router or hand plane
- Glass recesses routed or milled
- Hand-inlay decorative elements possible

### Assembly
- Glass panels sit in prepared recesses
- Light backing plate (veneer or hardboard) behind glass
- Painting mounted to backing
- Frame sealed with wood filler or sealant

## Future Development

Potential enhancements:
1. **Decorative Inlays** – Add Maldivian geometric patterns
2. **Maldé Elements** – Coral/wave textures from 3D modeling
3. **LED Backlighting** – Accent lighting integrated into frame
4. **Modular Variants** – 2-painting, 4-painting versions
5. **Material Variants** – Metals (bronze, copper) accents
6. **Glass Options** – Textured glass, frosted edges, tinted glass

## Design Validation

Golden ratio validation:
- ✓ Layer widths: 185.4 → 114.5 → 70.8 mm (each ÷ 1.618)
- ✓ Frame depth: 43.7 mm (consistent with ratio progression)
- ✓ Frame height: 26.9 mm (consistent with ratio progression)
- ✓ Gap spacing: 114.5 mm (equals frame_mid_w)
- ✓ Bevel depth: 13.45 mm (frame_z ÷ 2, maintains proportion)

Aesthetic validation:
- ✓ Layered borders create visual hierarchy
- ✓ Beveled edges add sophistication
- ✓ Recessed glass maintains clean lines
- ✓ Golden ratio creates natural balance
- ✓ Proportions feel intentional, not arbitrary

---

**Design Status**: Parametric foundation complete. Ready for geometry creation and decorative element integration.
