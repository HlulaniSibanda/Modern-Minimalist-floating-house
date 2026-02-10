# Structural Analysis: Beverly Hills Modern Residence

![Beverly Hills project](https://github.com/user-attachments/assets/4da58436-257d-4218-94f0-6e21b3750922)

## Project Overview
This repository contains the structural analysis and design documentation for a luxury modern residence located in Beverly Hills, California. The project features a two-story cantilevered steel structure situated on a hillside terrain.

The primary engineering challenge was to achieve a minimalist architectural aesthetic—characterized by 3-meter cantilevered balconies and floor-to-ceiling glass facades—while maintaining structural integrity in a high-seismic zone (Seismic Design Category E).

## Structural Systems

### Gravity System
* **Primary Framing:** ASTM A992 (Grade 50) / S355 Structural Steel W-Sections.
* **Floor System:** Lightweight Composite Metal Deck on W12 secondary purlins to reduce dead load and minimize long-term deflection.
* **Cantilevers:** 3-meter overhangs supported by continuous back-span beams anchored to shear walls and internal columns.
* **Roof:** W24x62 steel beams supporting a lightweight steel deck assembly to eliminate column supports at the cantilever tip.

### Lateral System
* **Seismic Force Resisting System:** Special Steel Moment Frames (SMF) in the longitudinal direction and Reinforced Concrete Shear Walls in the transverse direction.
* **Foundation:** Deep foundation system consisting of 400mm diameter drilled concrete piers (caissons) interconnected by grade beams to resist slope instability and seismic uplift.

<img width="1333" height="583" alt="01 3D overview" src="https://github.com/user-attachments/assets/812d1609-1c4d-49e4-be22-70ba88ee42e3" />

## Design Criteria & Codes

The structure was modeled and analyzed in accordance with the following codes and standards:

* **Building Code:** International Building Code (IBC) 2021 / CBC 2022
* **Design Standard:** ASCE 7-16 (Minimum Design Loads for Buildings)
* **Steel Design:** AISC 360-16 (Specification for Structural Steel Buildings)
* **Concrete Design:** ACI 318-19 (Building Code Requirements for Structural Concrete)

### Loading Parameters
| Load Type | Value | Notes |
| :--- | :--- | :--- |
| **Dead Load (Floor)** | 3.6 kPa | Lightweight Composite Deck |
| **Dead Load (Roof)** | 1.5 kPa | Metal Deck + Insulation + Waterproofing |
| **Live Load (Residential)** | 1.92 kPa (40 psf) | ASCE 7-16 Table 4.3-1 |
| **Live Load (Balcony)** | 4.79 kPa (100 psf) | Required for occupancy > 100 sq ft |
| **Seismic Base Shear** | 670 kN | Calculated based on site soil class and mass |

## Modeling & Analysis Methodology

The structural model was developed using **Autodesk Robot Structural Analysis Professional 2026**.

### 1. Geometry and Connectivity
The structure utilizes a rigid grid system to ensure load path continuity. All steel connections were modeled as:
* **Moment Connections:** Fully Fixed (Releases: None) for cantilever back-spans.
* **Shear Connections:** Pinned releases for secondary infill beams.
* **Diaphragm Action:** Modeled using rigid links and finite element mesh intersections to simulate the composite action of the floor deck.

<img width="1052" height="731" alt="FEA model" src="https://github.com/user-attachments/assets/996aa6f0-e830-4a81-b592-c1e1e008506c" />

### 2. Deflection Optimization
Initial analysis using a 450mm solid concrete slab resulted in excessive deflection (>30mm) at the cantilever tip due to self-weight.

**Optimization Strategy:**
1.  Replaced solid concrete slab with a 150mm composite metal deck system.
2.   increased cantilever beam depth to W24x62 to maximize Moment of Inertia ($I_x$).
3.  Designed a 2:1 back-span ratio (6m back-span for 3m cantilever) to counter-balance the overhang.

**Final Result:**
* **Maximum Tip Deflection:** 3.3 mm
* **Span/Deflection Ratio:** L/491 (Exceeds the L/480 limit required for glazing).

<img width="1312" height="757" alt="image" src="https://github.com/user-attachments/assets/5da7ab35-742f-44ed-b348-c12093a3e8a9" />

### 3. Seismic Performance
A modal response spectrum analysis was performed to verify drift limits.
* **Drift Check:** Inter-story drift limited to 2.0% of story height.
* **Base Shear:** 670 kN distributed to shear walls and moment frames.

<img width="1570" height="782" alt="image" src="https://github.com/user-attachments/assets/f689ccbe-abb9-44e0-a848-ff8390cf7851" />

## Repository Contents

* `/calc_package`:
  * <img width="650" height="672" alt="Seismic base shear calculations" src="https://github.com/user-attachments/assets/dbab083c-1857-4727-8854-761a0c3ec9bf" />
  *<img width="942" height="682" alt="Beam Design" src="https://github.com/user-attachments/assets/d8221001-3ce8-4951-a7ee-a0b6a53962fe" />

### Drawings

  ### Foundation plan:
  
  <img width="815" height="678" alt="02 Foundation plan" src="https://github.com/user-attachments/assets/a44c6533-99a9-4adb-a64b-9a1ad5d0d363" />
  
  ### Column foundation connection:
  
  <img width="986" height="655" alt="03 Column base connection" src="https://github.com/user-attachments/assets/ea5a398e-af51-4f02-943b-9c7a56d036ec" />
  
  ### Side elevation:
  
  <img width="712" height="542" alt="04 Side elevation" src="https://github.com/user-attachments/assets/d69ac37d-e6ea-4741-921f-3d330c330030" />
  
  ### Ground floor framing:
  
  <img width="828" height="660" alt="05 Ground floor framing" src="https://github.com/user-attachments/assets/c7b47156-a605-4ea9-a85a-e78950b351fa" />
  
  ### First floor framing:
  
  <img width="870" height="655" alt="06 First floor framing" src="https://github.com/user-attachments/assets/e65cf463-b1b3-4fbc-8e01-0b58cf8e59b2" />


## Disclaimer
This project is a design portfolio demonstration. While based on real-world codes and engineering principles, it is for illustrative purposes.

---

**Tools Used:** Autodesk Robot Structural Analysis, Revit, Excel
