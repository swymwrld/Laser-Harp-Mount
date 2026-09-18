# 🎵 Laser Harp - Parametric Laser Mount

![CAD](https://img.shields.io/badge/CAD-Onshape-blue?logo=onshape)
![Hardware](https://img.shields.io/badge/Hardware-Laser_Harp-orange)

A 1:1 wooden harp model designed to work as a laser-based interactive instrument. 
This repository contains the parametric CAD design of the laser mounting system used to position and adjust the laser modules.

## 🌟 Project Overview
The physical harp is a non-playable wooden model that replaces traditional strings with laser beams. When a player "plucks" the virtual string, they interrupt the laser beam, triggering an LDR sensor to play a musical note.

The core challenge in this system is precisely mounting and aligning the lasers with the sensors below.

### The Mechanism
The laser mount is designed around two friction-based adjustments (eliminating the need for complex screws or hinges):
1. **Laser adjustment**: The laser module slides into a slot dimensioned for a tight friction fit, allowing it to be aimed by hand.
2. **Mount adjustment**: The complete mounting block slides between the two walls of the harp's upper curve, holding its position via friction.

## 🛠️ The CAD Model (Onshape)

The primary parametric CAD model is maintained in Onshape.
👉 **[Open the Onshape CAD Document](https://cad.onshape.com/documents/89cf6b00cf7b795ae2f5dd3b/w/717d53ea8ababa12619c551d/e/7e3aa22e7690729a05d70ef4?renderMode=0&rightPanel=variableTablePanel&uiState=6aad9599c5c327812b27e8ca)**

### Screenshots
*(Visuals of the Parametric Laser Mount)*
<p align="center">
  <img src="Images/Screenshot%202026-09-19%20012310.png" width="30%">
  <img src="Images/Screenshot%202026-09-19%20012324.png" width="30%">
  <img src="Images/Screenshot%202026-09-19%20012350.png" width="30%">
</p>

### Parametric Variables
The model is fully parametric. If a different laser module or harp dimension is used, you only need to change these variables in Onshape and the geometry will update automatically:

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

## 🚀 Current Status & Next Steps

**Completed:**
- [x] 1:1 wooden harp model constructed.
- [x] Parametric friction-fit laser mounting designed in Onshape.
- [x] Adjustable positioning mechanics finalized.

**Next Steps:**
- [ ] Install the laser modules and LDR sensors.
- [ ] Align individual laser beams with the sensors.
- [ ] Integrate the electronics (Arduino/Microcontroller).
- [ ] Map laser interruptions to MIDI musical notes.

## 📂 Repository Structure

While Onshape holds the parametric *master* file (including feature history), this GitHub repository is used to store the exported portable files and documentation.

```text
Laser-Harp-Mount/
├── README.md
├── CAD/ (Recommended for .step, .stl, .x_t exports)
└── Images/
```

### Fit and Manufacturing Notes
Before 3D printing or machining the mount, verify the actual laser module diameter and harp wall thickness. Depending on your material and printer tolerances, small dimensional adjustments to the variables may be required to achieve the perfect friction fit.
