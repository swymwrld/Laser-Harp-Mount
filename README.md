# Parametric Laser Mount

![CAD](https://img.shields.io/badge/CAD-Onshape-blue?logo=onshape)
![Hardware](https://img.shields.io/badge/Hardware-3D_Printing-orange)

This repository contains the parametric CAD design for a specialized 3D-printable laser mounting block. It is specifically designed to be manufactured using TPU (Thermoplastic Polyurethane), allowing for friction-based alignment without the need for complex mechanical fasteners.

This mount was designed to be utilized as part of a laser harp system, but the CAD principles apply to any project requiring compact, adjustable laser positioning.

## Mechanical Design and Adjustability

The primary function of this mount is to securely hold a cylindrical laser module while allowing for fine-tuned alignment across two axes. The use of flexible TPU material enables friction-fit kinematics.

### Two-Axis Adjustment System
1. **X-Axis (Laser Slot)**: The inner slot is dimensioned to grip the laser module firmly. The flexibility of the TPU allows the laser to be manually tilted and translated within the slot along the x-axis.
2. **Y-Axis (Mount Base)**: The entire mounting block can be shifted along the y-axis where it is mounted. 

Together, these two friction-based adjustment axes allow the laser beam to be accurately targeted in 3D space.

## The CAD Model (Onshape)

The primary parametric CAD model is maintained natively in Onshape.
[Open the Onshape CAD Document](https://cad.onshape.com/documents/89cf6b00cf7b795ae2f5dd3b/w/717d53ea8ababa12619c551d/e/7e3aa22e7690729a05d70ef4?renderMode=0&rightPanel=variableTablePanel&uiState=6aad9599c5c327812b27e8ca)

### Visuals
<p align="center">
  <img src="Images/Screenshot%202026-09-19%20012310.png" width="30%">
  <img src="Images/Screenshot%202026-09-19%20012324.png" width="30%">
  <img src="Images/Screenshot%202026-09-19%20012350.png" width="30%">
</p>

### Parametric Variables
The model is fully parametric. If a different laser module diameter is required, simply update the variables in the Onshape document and the geometry will rebuild automatically:

| Variable | Value | Description |
|---|---|---|
| `Width` | 19 mm | Overall width of the mounting block |
| `Length` | 19 mm | Overall length of the mounting block |
| `Slot_Width` | 10.75 mm | Width of the laser mounting slot |
| `Slot_diameter` | 14.5 mm | Reference diameter of the laser module |
| `Fillet` | 1 mm | Edge fillet size |
| `Ears_Length` | 19 mm | Length of the mounting ears |
| `Ears_Width` | 2 mm | Width/thickness of the mounting ears |
| `Ears_Height` | 6 mm | Height of the mounting ears |

## Repository Structure

While Onshape holds the parametric master file (including feature history), this GitHub repository is used to store the exported portable files and documentation.

```text
Laser-Harp-Mount/
├── README.md
├── CAD/ 
│   └── Laser_Mount.step
└── Images/
```

## Manufacturing Notes

This part is specifically engineered for **3D printing with TPU filament**. 
Before printing the mount, verify the actual laser module diameter and your printer's tolerances. The flexibility of the TPU is critical for the friction-fit mechanism to function correctly; printing this in rigid materials like PLA or PETG may result in the laser not fitting or the adjustment axes being locked.
