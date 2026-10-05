# WEEK 6 — DIGITAL FABRICATION: LASER CUTTING & 3D PRINTING

## Segment 1 — Laser Cutting & Vector Engraving

### 1. Laboratory Safety & Strict Protocols
Operating high-energy CO₂ lasers requires strict adherence to thermal, electrical, and optical safety standards:
- **Exhaust Ventilation**: Active blower system extracting smoke and acrylic fumes.
- **Water Chiller**: Continuous cooling circulation for the 150W CO₂ laser tube.
- **Air-Assist**: High-pressure lower blowing to prevent flare-ups and move debris.
- **Material Verification**: 2 mm Transparent Acrylic (PVC/chlorine plastics strictly prohibited).

### 2. Machine Details & Technical Specifications
- **Make & Model**: FORGE 1490 CO₂ Laser Cutter
- **Bed Area**: 1300 × 900 mm
- **Laser Tube Power**: 150 W
- **Control Software**: RDWorks
- **Workpiece**: 2 mm Transparent Acrylic (50 × 50 mm blank)

### 3. Selected Design & Vector Workflow
- **Graphic**: “FIRE IN THE HOLE!!” flame character graphic.
- **Image-to-DXF Vector Conversion**: Traced raster contours to closed vector paths, scaled to 45 × 45 mm, and separated into Laser Scan (engraving) and Laser Cut (outline) layers.
- **Parameters**: 100 mm/s speed, 30% min/max power, single pass. Simulated time: 1 min 14.3 s (laser light time: 28.38 s).

> **Laser Cutting takeaway:**  
> Digital fabrication quality is determined during vector preparation. Clean geometry, closed paths, and calibrated power settings produce crisp physical results.

---

## Segment 2 — 3D Printing & Additive Manufacturing

### 1. Additive vs. Subtractive Manufacturing
Unlike subtractive CNC machining which struggles with internal undercuts and organic geometries, **Fused Deposition Modeling (FDM)** constructs complex objects layer by layer directly from an STL polygon surface mesh.

### 2. Machine Specifications & Slicing
- **Printer**: Bambu Lab H2S CoreXY High-Speed 3D Printer (340 × 320 × 340 mm build volume, 0.4 mm hardened-steel nozzle)
- **Material**: 1.75 mm White PLA Filament
- **Slicer**: Bambu Studio

### 3. Selected Model & Slicer Parameters
- **Model**: Organic Toothless Dragon STL (45.7 × 98.7 × 16.2 mm envelope)
- **Settings**:
  - Layer Height: 0.20 mm
  - Nozzle Temperature: 220 °C | Bed Temperature: 55 °C
  - Infill: 15% Gyroid (for multi-directional mechanical strength)
  - Wall Loops: 2 | Print Speed: 200 mm/s
  - Total Print Time: 37 min 47 s
  - Filament Used: 8.62 g total (8.50 g model + 0.11 g support)

> **3D Printing takeaway:**  
> Additive manufacturing removes conventional geometric constraints. Smart orientation and minimal support usage make complex organic prototyping fast and sustainable.

---

## Week 6 Summary

From digital vector lines to high-energy laser beams, and from 3D meshes to layer-by-layer extrusion — digital fabrication turns imagination into physical reality.
