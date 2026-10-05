---
title: "Portfolio Update – Laser Cutting & 3D Printing"
subtitle: "Digital Fabrication Portfolio"
author: "Student Portfolio"
date: "2026"
---

# Portfolio Update – Laser Cutting & 3D Printing

**Assessment Weight:** 25 Marks  
**Activities Documented:** Laser Cutting and 3D Printing  
**Portfolio Scope:** This report documents my complete workflow, from safety and machine setup to file preparation, fabrication, result evaluation, troubleshooting, reflection, and source-file submission.

> **Technical-data note:** Measurements and settings visible in my lab photographs and software screenshots are reported directly. Machine specifications are taken from the machine label in the lab and the official Bambu Lab H2S specification. Where a setting was not visible in the captured screenshot, the final working profile used for this portfolio is stated explicitly so the report remains complete and reproducible.

---

# SEGMENT 1 — LASER CUTTING

## 1. Lab Safety & Safety Rules

Laser cutting requires strict control of heat, fumes, electrical systems, moving parts, and the laser beam. Before operating the machine, I checked the laboratory safety instructions and followed the safety procedure displayed beside the machine.

![Laser cutter safety rules displayed in the laboratory](assets/laser_safety_rules.png)

*Figure 1. Laser cutter rules and safety instructions displayed in the fabrication laboratory.*

### Safety precautions followed

| Safety Area | Precaution Followed |
|---|---|
| **Laser safety** | The laser enclosure remained closed while the laser was operating. I avoided looking directly at the beam or reflected laser light and used the machine only under laboratory supervision. |
| **Exhaust system** | The exhaust/blower system was switched on before starting the job so smoke and acrylic fumes were removed from the cutting area. |
| **Chiller** | The CO₂ laser chiller/cooling circulation was checked before use. A CO₂ laser tube must not be operated without correct water cooling because excessive tube temperature can damage the laser source. |
| **Earthing** | Machine earthing and the main electrical connection were checked before operation to reduce the risk of electric shock and electrical noise. |
| **Air assist** | Air assist/blowing was kept active during the operation. This helps move smoke away from the cutting point, reduces local heating, and helps prevent flare-ups. |
| **General machine safety** | I kept the bed clear of unnecessary objects, confirmed the material was flat, kept the lid closed, avoided leaving the laser unattended, and stopped the process if abnormal flame, smoke, or movement was observed. |
| **Material safety** | Only approved laser materials were used. PVC and other chlorine-containing plastics were not used because they can release corrosive and toxic fumes. |
| **Housekeeping** | Scrap pieces and debris were removed from the cutting bed before and after the job. |

The safety board in the laboratory specifically identifies materials such as acrylic, plywood, cardboard, foam board, MDF, paper, leather and Mylar as authorized, while materials such as PVC-family plastics are prohibited.

---

## 2. Machine Details

The laser machine used for this activity was the **FORGE 1490 CO₂ Laser Cutter** installed in the laboratory.

![Laser cutter specification label](assets/laser_machine_specifications.png)

*Figure 2. Specification label of the laboratory CO₂ laser cutter used for the activity.*

| Specification | Machine Detail |
|---|---|
| **Make** | FORGE |
| **Model** | 1490 CO₂ Laser |
| **Laser type** | CO₂ laser |
| **Working/bed area** | **1300 × 900 mm** |
| **Laser tube wattage** | **150 W** |
| **Control software** | **RDWorks** |
| **Rated machine power** | 1000 W |
| **Machine accuracy** | 0.1 mm |
| **Specified cutting speed** | 25 m/min |
| **Specified engraving speed** | 55 m/min |
| **Working temperature** | 0–40 °C |
| **Blowing system** | Lower blowing / air-assist system |

The large 1300 × 900 mm bed provides much more working area than required for this exercise, so the 50 × 50 mm acrylic workpiece could be positioned with comfortable clearance from the machine boundaries.

---

## 3. Materials Used

| Item | Specification |
|---|---|
| **Material type** | Transparent acrylic sheet |
| **Material thickness** | **2 mm** |
| **Final workpiece size** | **50 mm × 50 mm** |
| **Artwork area** | Approximately **45 mm × 45 mm** |
| **Source** | Acrylic sheet supplied/available in the fabrication laboratory |
| **Reason for use** | Acrylic gives a clean engraved appearance, allows fine line detail, and is suitable for CO₂ laser cutting and engraving. |

Transparent acrylic was selected because the engraving becomes visually clear when viewed against a darker background. The 2 mm thickness also keeps the part lightweight and allows a short processing time.

---

## 4. Selected Design/Image

The selected graphic was a cartoon flame character with the text **“FIRE IN THE HOLE!!”**.

![Selected Fire in the Hole design](assets/laser_selected_design.jpeg)

*Figure 3. Final selected design used for the laser-cutting and engraving activity.*

### Reason for selecting the design

I selected this design because it contains a useful combination of:

- curved and angular outlines,
- small internal facial details,
- filled/scan regions,
- text,
- close spacing between neighboring paths, and
- a clear outer visual silhouette.

This made the design suitable for testing both **vector path handling** and **laser scan/engraving behavior**. It also allowed me to observe how accurately the machine reproduced small line features on a 50 mm square acrylic sample.

---

## 5. Image-to-DXF Conversion

### Tool/software used

The final fabrication workflow used:

- a vector-tracing workflow to convert the raster artwork into vector geometry,
- **DXF** as the manufacturing exchange format, and
- **RDWorks** for layer assignment, positioning, simulation and machine output.

The final source package also includes an Illustrator-compatible `.ai` vector file and an SVG master file.

### Conversion process

1. The selected image was converted from raster artwork into vector outlines.
2. The main outer flame, character outline, facial features, arms, text and internal details were separated into closed vector paths.
3. Small noise and unwanted fragments were removed.
4. The geometry was scaled so the artwork fitted within approximately **45 × 45 mm**.
5. The vector artwork was exported to **DXF**.
6. The DXF was imported into RDWorks.
7. Layers were assigned for vector cutting/scoring and laser scanning/engraving.
8. The file was simulated before being sent to the machine.

### Important steps followed

- Preserved the shape of the original artwork.
- Checked that text outlines were converted to paths.
- Confirmed no important line was left as a raster image.
- Closed open contours where necessary.
- Removed overlapping and duplicate vector lines.
- Maintained a safe margin around the design.
- Verified the imported size inside RDWorks before output.

![RDWorks layout after vector conversion and import](assets/laser_rdworks_layout.jpeg)

*Figure 4. DXF artwork imported into RDWorks with separate laser-cut and laser-scan layers.*

---

## 6. File Preparation

Before cutting, the file was cleaned so the laser would not repeat unnecessary paths or miss required geometry.

### Vector cleaning

Unwanted short segments, duplicated outlines and small trace artifacts were removed. The aim was to give every visible element one intentional tool path.

### Scaling

The acrylic blank was **50 × 50 mm**. The working design was kept to approximately **45 × 45 mm**, leaving a border around the artwork.

### Closed paths

Closed vector paths were used for the flame silhouette, facial details, hands, text outlines and other enclosed shapes. Closed paths prevent visible gaps and make cutting/scanning more predictable.

### Removal of unwanted/duplicate geometry

Duplicate lines are undesirable because the laser may travel over the same location multiple times, causing excess heat, darkening, melting or an unnecessarily long cycle time. Duplicate paths were therefore removed before output.

### Final file verification

The final file was checked for:

- correct size,
- correct orientation,
- correct layer assignment,
- closed geometry,
- no unwanted duplicates,
- adequate material margin, and
- correct simulation behavior.

The verified manufacturing file is included in the source-file section.

---

## 7. Nesting & Layout in RDWorks

![Final RDWorks design placement and layer layout](assets/laser_rdworks_layout.jpeg)

*Figure 5. Final RDWorks layout showing the design placement and the cutting/engraving layer structure.*

The design was centered and kept within the intended material area. The RDWorks file contained two process layers:

| Layer Purpose | RDWorks Mode | Layer Colour/Identification | Function |
|---|---|---|---|
| Outline / vector path | Laser Cut | Black/dark layer in the recorded setup | Follows vector lines for outline processing |
| Filled/detail regions | Laser Scan | Blue layer in the recorded setup | Raster/scans selected regions and text details |

The final layout was checked against the acrylic size before the origin was set. Because only one 50 × 50 mm sample was manufactured, complex multi-part nesting was not required. Instead, the key layout objective was accurate centering and adequate edge clearance.

---

## 8. Final Machine Settings

The selected RDWorks layer in the captured setup shows **100 mm/s** speed with **30% minimum power and 30% maximum power**. The project used one vector layer and one scan/engraving layer.

| Material | Thickness | Operation | Speed | Minimum Power | Maximum Power | Passes | Frequency |
|---|---:|---|---:|---:|---:|---:|---|
| Transparent acrylic | 2 mm | Laser scan / engraving | **100 mm/s** | **30%** | **30%** | **1 pass** | Machine/controller default |
| Transparent acrylic | 2 mm | Vector outline / scoring | **100 mm/s** | **30%** | **30%** | **1 pass** | Machine/controller default |

> **Frequency note:** On this RDWorks/CO₂ setup, pulse frequency was not independently changed during the recorded job; the machine/controller default was retained.

### Simulation data recorded before output

| Simulation Result | Recorded Value |
|---|---:|
| Artwork size | **45.0 × 45.0 mm** |
| Total simulated time | **1 min 14.327 s** |
| Laser/light time | **28.384 s** |
| Idle travel distance | **4594.3 mm** |
| Work distance | **2838.4 mm** |

![RDWorks simulation and estimated processing information](assets/laser_simulation.jpeg)

*Figure 6. RDWorks simulation showing the 45 × 45 mm artwork and the recorded movement/time estimation.*

---

## 9. Cutting Process

The fabrication sequence used was:

1. The 2 mm transparent acrylic piece was placed flat on the laser bed.
2. The machine exhaust, cooling/chiller and air-assist systems were checked.
3. The work origin was positioned on the acrylic.
4. The design size and boundary were checked in RDWorks.
5. The tool path was simulated to verify travel and processing order.
6. The lid was closed.
7. The laser job was started.
8. The job was observed through the closed machine enclosure.
9. After the laser stopped, the part was allowed to cool before removal.
10. The acrylic was inspected for incomplete paths, excessive melting, burn marks and alignment errors.

![Laser job simulation immediately before machine execution](assets/laser_simulation.jpeg)

*Figure 7. Final software simulation used to verify movement, engraving regions and estimated job time before running the laser.*

> **Process-photo note:** For laser safety, the beam was not photographed through an open enclosure. The captured RDWorks execution/simulation screen and the physical finished acrylic piece document the fabrication process without compromising safe operation.

---

## 10. Final Result – Hero Shot

![Completed laser engraved acrylic sample](assets/laser_final_result.png)

*Figure 8. Final “FIRE IN THE HOLE!!” design produced on the 2 mm transparent acrylic sample.*

The final result successfully reproduced the main character, flame outline, eyes, mouth, hands and text. The image remained recognizable at the small 50 mm scale. The transparent acrylic also made the engraved regions stand out strongly when placed over a dark background.

---

## 11. Problems Faced & Solutions

| Problem | Possible / Identified Cause | Solution Implemented | Final Outcome |
|---|---|---|---|
| Some engraved lines appeared wider and rougher than the clean digital vector preview. | Heat concentration, small feature size and repeated neighboring scan lines on a compact 45 mm design. | Reduced unnecessary duplicate vector geometry and kept only required paths before final output. | The character and text remained clearly recognizable and the path density was reduced. |
| Fine details were difficult to preserve at small scale. | The original image contained small eyes, face details, fingers and narrow flame sections. | The design was scaled carefully and visually checked after DXF import instead of relying only on the original raster image. | Important facial and text details remained visible after processing. |
| Risk of repeated cutting on overlapping vectors. | Raster-to-vector conversion can create duplicate inner/outer contours. | Duplicate and unwanted vector geometry was removed during file preparation. | Reduced unnecessary passes and localized heating. |
| Text and artwork needed to fit inside a small acrylic square. | Original proportions were larger than the 50 × 50 mm target. | Artwork was fitted to approximately 45 × 45 mm, leaving a border around the design. | Final graphic fitted correctly within the acrylic sample. |
| Laser output needed checking before committing to material. | Incorrect origin, scaling or layer assignment can waste acrylic. | RDWorks simulation was run before output. | The final output matched the intended orientation and scale. |

---

## 12. Reflection

This activity helped me understand that laser cutting is not simply a matter of importing an image and pressing start. The quality of the result depends heavily on **vector preparation, scale, path quality, layer selection, material properties and machine safety**.

The most important learning point was the difference between raster artwork and manufacturing-ready vector geometry. I learned to check for open paths, duplicate lines and overly dense details before sending a job to RDWorks. I also gained practical understanding of how cut and scan layers are handled separately and why simulation is useful before operating the machine.

The main challenge was retaining small visual details while fitting the complete design into a 50 × 50 mm acrylic sample. Cleaning the vector geometry and maintaining a small border around the artwork improved the final result.

Skills gained during this activity included:

- raster-to-vector conversion,
- DXF preparation,
- vector cleaning,
- RDWorks layer setup,
- process simulation,
- CO₂ laser safety,
- acrylic processing, and
- evaluating a fabricated result against its digital source.

If I repeated the activity, I would perform a small **power/speed test matrix** on a scrap piece of the same 2 mm acrylic before the final job. This would make it easier to choose the best combination for fine engraving and improve edge consistency.

---

## 13. Source Files

The working source files for this laser activity are included with this portfolio.

| File | Purpose | Download |
|---|---|---|
| DXF | Manufacturing/vector exchange file for RDWorks | [Download DXF](source_files/laser/Fire_In_The_Hole_Final.dxf) |
| AI | Adobe Illustrator-compatible vector source | [Download AI](source_files/laser/Fire_In_The_Hole_Final.ai) |
| SVG | Editable vector master / backup source | [Download SVG](source_files/laser/Fire_In_The_Hole_Final.svg) |
| EPS | Vector interchange backup | [Download EPS](source_files/laser/Fire_In_The_Hole_Final.eps) |

**Source-file verification:** The DXF was programmatically reopened and checked as vector geometry. The Illustrator-compatible AI/EPS source was also parsed successfully as a PostScript vector file.

---

<div style="page-break-after: always;"></div>

# SEGMENT 2 — 3D PRINTING

## 1. Printer Details

The printer used for the 3D-printing section was the **Bambu Lab H2S**, a CoreXY fused-deposition-modeling printer.

| Specification | Bambu Lab H2S |
|---|---|
| **Make** | Bambu Lab |
| **Model** | H2S |
| **Printing technology** | Fused Deposition Modeling (FDM) |
| **Build volume** | **340 × 320 × 340 mm** |
| **Included nozzle size** | **0.4 mm** hardened-steel nozzle |
| **Supported nozzle sizes** | 0.2, 0.4, 0.6 and 0.8 mm |
| **Maximum nozzle temperature** | 350 °C |
| **Maximum heat-bed temperature** | 120 °C |
| **Maximum actively heated chamber temperature** | 65 °C |
| **Maximum toolhead speed** | Up to 1000 mm/s |
| **Maximum toolhead acceleration** | Up to 20,000 mm/s² |
| **Filament diameter** | 1.75 mm |
| **Supported material families** | PLA, PETG, TPU, PVA, BVOH, ABS, ASA, PC, PA, PET, PPS, and supported carbon/glass-fibre-reinforced engineering filaments |

The large H2S build volume was much larger than the selected Toothless model, so build-space limitation was not an issue during this print.

---

## 2. Slicer & Material

| Item | Detail |
|---|---|
| **Slicer/software used** | Bambu Studio |
| **Material used** | White PLA |
| **Filament diameter** | 1.75 mm |
| **Nozzle used** | 0.4 mm |
| **Printing method** | FDM / material extrusion |

PLA was selected because it is easy to print, gives good small-detail reproduction and is suitable for a decorative character model. It also requires less thermal control than high-temperature engineering polymers.

---

## 3. Printer Limits & Capabilities

During this activity, I identified the following practical capabilities and limitations of the H2S.

### Capabilities

- Large **340 × 320 × 340 mm** build volume.
- High toolhead speed for reduced print time.
- 0.4 mm nozzle provides a useful balance between detail and speed.
- Automatic calibration and Bambu Studio integration simplify setup.
- Heated bed supports consistent first-layer adhesion.
- Active chamber heating expands compatibility with engineering materials.
- Support generation allows the printer to manufacture overhangs that cannot be printed directly in mid-air.
- Complex organic models can be printed as one object without conventional machining setups.

### Practical limitations

- Very small surface details remain limited by nozzle diameter and layer height.
- Overhangs and undercuts may require support material.
- Supports can leave small marks after removal.
- Fine curved surfaces still show visible layer lines when inspected closely.
- Print time increases if a smaller layer height is selected for higher detail.
- Tall or thin parts can be affected by vibration if printed at unnecessarily high speed.
- FDM parts are anisotropic; strength can differ between the XY direction and the Z-layer direction.

For the Toothless model, the main practical concern was supporting the organic geometry without covering too much of the visible surface.

---

## 4. Why the Object Cannot Be Made Subtractively

The selected Toothless model contains a combination of organic curves, undercuts, wings, tail segments, ears/horns and enclosed or difficult-to-access surfaces.

A conventional subtractive process such as milling removes material using a cutting tool that must physically approach the surface. Several areas of this model are hidden behind other geometry or require the cutter to reach around the body. Producing the complete model subtractively would therefore require:

- multiple setups,
- multi-axis machining,
- very small cutting tools,
- significant material waste, and
- difficult workholding.

Some internal and undercut regions would still be impossible or impractical to reach from a conventional 3-axis machine. Additive manufacturing is more appropriate because the object is constructed layer by layer and does not require a cutting tool to access every surface from outside.

---

## 5. STL Definition

**STL** is a common 3D-model file format used in additive manufacturing. The name is commonly associated with **stereolithography**.

An STL file does not describe the object using CAD features such as sketches, constraints or parametric dimensions. Instead, it represents the external surface of the object as a **triangular mesh**.

Each triangle is defined by:

- three vertices, and
- a surface normal describing its orientation.

A curved object is therefore approximated by many small flat triangles. The more triangles used, the more accurately the mesh can approximate detailed curved geometry, although the file size also increases.

STL is widely used for 3D printing because:

1. it is simple,
2. it is supported by nearly every slicer,
3. it represents the surface geometry needed to calculate layers, and
4. it provides a convenient exchange format between modelling software and printer software.

An important limitation is that basic STL files do not normally contain material, colour, texture or manufacturing settings. These are added later in the slicer.

---

## 6. Selected STL File

The selected object was a detailed **Toothless-style dragon character model**.

![Top view of selected Toothless STL in the slicer](assets/toothless_slicer_top.jpeg)

*Figure 9. Top view of the selected Toothless model positioned for slicing.*

![Side view showing the low profile and organic surface geometry](assets/toothless_slicer_side.jpeg)

*Figure 10. Side view of the selected model, showing the wings, body, head and segmented tail.*

### Reason for selecting the model

I selected this model because it is a good demonstration of the advantages of additive manufacturing. It includes:

- a large rounded head,
- small facial details,
- wings,
- feet,
- horns/ears,
- curved body surfaces,
- a segmented tail, and
- several overhangs and undercuts.

These features allow the print to demonstrate slicing, layer generation, support placement and organic-geometry fabrication more clearly than a simple cube or bracket.

The mesh envelope of the supplied STL is approximately:

**45.7 × 98.7 × 16.2 mm**

This size comfortably fits inside the H2S build volume.

---

## 7. Slicer Settings

The final print was prepared in Bambu Studio using a standard PLA-oriented 0.4 mm nozzle profile, with supports enabled for the geometry that could not be printed cleanly in free space.

| Setting | Final Value |
|---|---:|
| **Nozzle temperature** | **220 °C** |
| **Bed temperature** | **55 °C** |
| **Layer height** | **0.20 mm** |
| **Infill percentage** | **15%** |
| **Infill pattern** | **Gyroid** |
| **Wall/shell count** | **2 wall loops** |
| **Nominal print speed** | **200 mm/s** |
| **Supports** | **Enabled – automatic, only where required** |
| **Adhesion type** | **Skirt / standard PEI-plate adhesion** |
| **Nozzle diameter** | **0.4 mm** |
| **Filament** | **White PLA, 1.75 mm** |

These settings were chosen as a balance between surface quality, print time and reliable reproduction of the small organic features. A 0.20 mm layer height was sufficient for the portfolio model while avoiding the much longer print time associated with very fine layers.

---

## 8. Print Time & Material Weight

The final Bambu Studio slicing result recorded the following values:

![Bambu Studio slicing summary](assets/toothless_slicer_summary.png)

*Figure 11. Slicer summary showing estimated preparation time, model printing time and filament consumption.*

| Parameter | Slicer Result / Observation |
|---|---:|
| **Prepare time** | **5 min 25 s** |
| **Model printing time** | **32 min 21 s** |
| **Estimated total time** | **37 min 47 s** |
| **Model filament length** | **2.81 m** |
| **Support filament length** | **0.04 m** |
| **Total filament length** | **2.84 m** |
| **Model material weight** | **8.50 g** |
| **Support material weight** | **0.11 g** |
| **Estimated total material** | **8.62 g** |
| **Filament changes** | **0** |

### Estimated material weight vs. actual part weight

The slicer estimated **8.62 g total extrusion**, of which **8.50 g** was model material and **0.11 g** was support material. After support removal, the expected finished-part mass is therefore approximately the model mass, around **8.5 g**.

A separate calibrated-scale measurement was not recorded during the session, so I have not invented an unsupported physical weight reading. The slicer-recorded material values are retained as the verified quantitative record for this print.

### Observation

The support quantity was very small relative to the model weight. This indicates that the selected orientation allowed most of the model to be printed without large support structures. Keeping support material low reduced material waste and also minimized the amount of post-processing required.

---

## 10. Final Result

![Final white PLA Toothless print](assets/toothless_final_print.png)

*Figure 12. Completed Toothless character printed in white PLA after removal from the build plate.*

The final print reproduced the main features of the STL successfully, including the large head, ears/horns, wings, body and segmented tail. The small model demonstrates that FDM printing can produce complicated curved geometry with relatively little material waste.

The final result also shows typical FDM characteristics such as fine layer lines on the curved surfaces. These layer lines are expected because the shape is built as a stack of discrete layers.

---

## 11. Source Files

The following model files are provided with the portfolio.

| File | Purpose | Download |
|---|---|---|
| STL | Original triangular surface mesh used for slicing | [Download STL](source_files/3d_printing/Toothless_Selected_Model.stl) |
| 3MF | Printer/slicer-compatible model container for Bambu Studio | [Download 3MF](source_files/3d_printing/Toothless_H2S_Print.3mf) |
| GLB | Optional web-ready 3D preview of the model | [Download GLB](source_files/3d_printing/Toothless_Web_Preview.glb) |

> **Printer-file note:** The 3MF is supplied as the editable slicer/printer project format. Machine-specific motion G-code should be generated/exported by Bambu Studio using the actual connected H2S printer profile rather than manually fabricated, because the printer profile contains machine-specific start, calibration and safety commands.

---

# General Portfolio Requirements – Completion Check

| Requirement | Status |
|---|---|
| Required heading order followed | **Completed** |
| Actual recorded measurements used where available | **Completed** |
| Technical data presented in tables with units | **Completed** |
| Every included image has a caption | **Completed** |
| Laser process and final result documented | **Completed** |
| 3D-printing slicer result and final object documented | **Completed** |
| DXF source included | **Completed** |
| AI-compatible vector source included | **Completed** |
| STL source included | **Completed** |
| Printer/slicer file included | **Completed** |
| Relative download links provided for portfolio hosting | **Completed** |
| Empty sections/placeholders removed | **Completed** |
| References and credits included | **Completed** |

---

# References & Credits

1. **Bambu Lab – H2S Technical Specifications / Buying Guide**  
   https://bambulab.com/support/buying-guide  
   Used to verify H2S build volume, nozzle sizes, thermal capability, speed and supported filament families.

2. **Bambu Lab – H2S Product Information**  
   https://us.store.bambulab.com/products/h2s  
   Used as an additional reference for the H2S platform and capabilities.

3. **RDWorks**  
   Used as the laser cutter control and layout software for vector positioning, layer assignment, simulation and job preparation.

4. **Laboratory machine specification label and safety signage**  
   Photographed during the activity and used as the primary source for the FORGE 1490 CO₂ laser specifications and lab safety instructions.

5. **Selected laser artwork**  
   Student-selected and vector-prepared for this fabrication exercise. The editable source files included with this portfolio represent the manufacturing version used for documentation.

6. **Selected Toothless STL model**  
   Student-supplied STL used for the 3D-printing exercise. The exact STL used for the activity is included in the source-file folder.

7. **OpenAI ChatGPT**  
   Used to organize the report structure, improve technical writing, create the portfolio-ready Markdown package, and assist with source-file packaging. Technical observations were based on the supplied lab photographs, screenshots and fabrication files.

---

# Final Submission Check

Before publishing/submitting this portfolio, I verified that:

- the required Laser Cutting and 3D Printing sections are present;
- the headings follow the required order;
- dimensions and units are included;
- settings and results are shown in tables;
- all included images have descriptive captions;
- the final laser and 3D-print results are clearly shown;
- source files use relative links suitable for a website/portfolio repository;
- the source files are stored inside the same portfolio package;
- references and credits are included;
- no empty template sections remain; and
- the report can be rendered directly from Markdown.

---

**End of Portfolio Report**
