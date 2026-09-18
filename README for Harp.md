# Laser Harp

A 1:1 wooden harp model designed to work as a laser-based interactive
instrument.

The physical harp is a non-playable wooden model and does not use
traditional strings. Instead, laser beams are positioned along the upper
curve of the harp to represent the strings. These virtual strings can
later be detected using LDR sensors, allowing an interrupted laser beam
to trigger a corresponding musical note.

This repository contains the parametric CAD design of the laser mounting
system used to position and adjust the laser modules.

## Project Overview

The main objective of the mechanical design is to provide a simple way
to mount and align the laser modules along the harp's upper curve.

The laser mount is designed around two basic adjustments:

1.  **Laser adjustment**\
    The laser module is inserted into a slot in the mount. The slot is
    sized around the laser module so that friction holds it in position
    while still allowing the laser to be manually adjusted.

2.  **Mount adjustment**\
    The complete mounting block can be moved between the two walls of
    the harp structure. Friction keeps the block in place while allowing
    its position to be changed when aligning the laser with the
    corresponding LDR.

This gives the laser system adjustment in two directions without
requiring a separate mechanical adjustment mechanism.

## Design Concept

The physical arrangement is based on the following concept:

``` text
Wooden Harp
     |
     v
Laser Mount
     |
     v
Laser Beam
     |
     v
LDR Sensor
     |
     v
Note Trigger
```

The CAD work in this repository currently focuses on the first part of
this system: the laser mounting mechanism.

## Laser Mount

The mounting block is a small parametric structure designed to hold a
cylindrical laser module.

The slot is dimensioned according to the laser module being used. The
laser can be pushed into the slot and held by friction. This also allows
its position to be adjusted manually when required.

The mounting block itself fits between the two supporting walls of the
harp. It can be repositioned along the structure to align the laser beam
with the required sensor position.

### Main design requirements

-   Friction-fit laser mounting
-   Manual laser adjustment
-   Manual adjustment of the complete mount
-   Simple geometry
-   Parametric dimensions
-   Easy adaptation to different laser module sizes
-   Easy reproduction for multiple laser positions

## Onshape Document

The primary parametric CAD model is maintained in Onshape.

[Open the Onshape CAD
document](https://cad.onshape.com/documents/89cf6b00cf7b795ae2f5dd3b/w/717d53ea8ababa12619c551d/e/7e3aa22e7690729a05d70ef4?renderMode=0&rightPanel=variableTablePanel&uiState=6aad9599c5c327812b27e8ca)

The Onshape document is the main source for the parametric model,
including the feature history and variable table.

## Onshape Model

The primary parametric CAD model is maintained in Onshape.

[Open the Onshape CAD
model](https://cad.onshape.com/documents/89cf6b00cf7b795ae2f5dd3b/w/717d53ea8ababa12619c551d/e/7e3aa22e7690729a05d70ef4?renderMode=0&rightPanel=variableTablePanel&uiState=6aad9599c5c327812b27e8ca)

The Onshape document is the main source for the parametric design,
including the feature history and variables. The GitHub repository is
intended to store exported CAD files, documentation, images, and project
information.

## Parametric Design

The model is created parametrically in Onshape.

The main dimensions are controlled using variables so that the design
can be adapted without rebuilding the entire part. If a different laser
module or different harp dimensions are used, the relevant variables can
be changed and the model will update accordingly.

### Current Variables

  Variable               Value Description
  ----------------- ---------- ----------------------------------------
  `Width`                19 mm Overall width of the mounting block
  `Length`               19 mm Overall length of the mounting block
  `Slot_Width`        10.75 mm Width of the laser mounting slot
  `Slot_diameter`      14.5 mm Reference diameter of the laser module
  `Fillet`                1 mm Edge fillet size
  `Ears_Length`          19 mm Length of the mounting ears
  `Ears_Width`            2 mm Width/thickness of the mounting ears
  `Ears_Height`           6 mm Height of the mounting ears

These values represent the current version of the design. They can be
changed according to the actual hardware and dimensions of the harp
structure.

## Design Intent

The design is intentionally kept simple.

Rather than using screws, hinges, or dedicated adjustment mechanisms,
the current concept uses friction to hold both the laser and the
mounting block.

This makes the system easier to assemble and allows the laser position
to be adjusted by hand during installation and alignment.

The design also allows multiple identical mounts to be used along the
upper curve of the harp.

## CAD Workflow

The model was developed using Onshape with a parametric approach.

The general workflow is:

1.  Define the master variables.
2.  Create the main mounting geometry.
3.  Create the laser slot.
4.  Create the mounting ears.
5.  Apply the required fillets.
6.  Check the fit against the laser module dimensions.
7.  Adjust the variables if the hardware or mounting dimensions change.

## Current Project Status

### Completed

-   1:1 wooden harp model
-   Dedicated gap for the virtual laser strings
-   Parametric laser mounting design
-   Friction-fit laser slot
-   Adjustable laser position
-   Adjustable mounting-block position
-   Onshape CAD model

### Next Steps

-   Install the laser modules
-   Position the LDR sensors
-   Align individual laser beams with the sensors
-   Integrate the electronics
-   Map laser interruptions to musical notes
-   Complete the interactive harp system

## Recommended File Structure

``` text
Laser-Harp/
|
├── CAD/
|   └── Laser_Mount/
|
├── Images/
|   ├── harp_model.jpg
|   └── laser_mount.jpg
|
└── README.md
```

The exact CAD file format can be added according to the intended
workflow. If the model is maintained directly in Onshape, the repository
can also contain the Onshape document link or exported CAD files.

## CAD File Format

There is an important distinction between a CAD geometry file and a
parametric CAD model.

The Onshape document is the best place to preserve the actual parametric
design, because it contains the feature history, sketches, variables,
and relationships used to build the model. Exporting the model from
Onshape does **not** preserve that feature history or parametric
structure.

For the GitHub repository, the recommended exports are:

  -----------------------------------------------------------------------
  File                                Purpose
  ----------------------------------- -----------------------------------
  `.step`                             General-purpose CAD exchange and
                                      reference

  `.x_t`                              Parasolid model; useful for CAD
                                      systems that support Parasolid

  `.stl`                              3D-printing / mesh representation

  Onshape link                        Primary parametric model
  -----------------------------------------------------------------------

If you want someone else to continue editing the actual parametric
model, share the Onshape document rather than relying on a STEP, STL, or
Parasolid export. Onshape supports exporting to STEP, Parasolid, STL and
other formats, but its documentation notes that exported data does not
contain the original feature history. citeturn0search0turn0search2

### Recommended approach

Keep these two levels separate:

``` text
GitHub
|
├── README.md
├── CAD/
|   ├── Laser_Mount.step
|   ├── Laser_Mount.x_t
|   └── Laser_Mount.stl
|
└── Images/

Primary Parametric Source
|
└── Onshape Document
    ├── Feature history
    ├── Variables
    ├── Sketches
    └── Parametric relationships
```

This way, GitHub contains portable CAD files and documentation, while
Onshape remains the editable parametric master model.

## Fit and Manufacturing Notes

The dimensions listed above are specific to the current design and
should not be treated as universal dimensions.

Before manufacturing or assembling the mount, verify:

-   Actual laser module diameter
-   Slot dimensions
-   Required friction fit
-   Distance between the harp walls
-   Harp wall thickness
-   Required laser position
-   LDR position and alignment

Depending on the material and manufacturing process, small dimensional
adjustments may be required to achieve the desired friction fit.

## Project Direction

The overall project explores a physical recreation of a harp where the
traditional strings are replaced by light-based interaction.

The wooden structure maintains the form and proportions of a
conventional harp, while the laser beams represent the strings. The
mechanical design described in this repository provides the adjustable
mounting system required to position those virtual strings accurately.

Further development will focus on the sensor system, electronics, and
interaction between the laser beams and the musical output.
