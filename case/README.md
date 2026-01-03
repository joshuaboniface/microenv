# MicroEnv v2.x Case

This is a 3D-printable case/enclosure for the MicroEnv v2.0 module. This case optional for functionality, but provides excellent aesthetics and a good mounting point for the sensor.

The design features two individual parts:

* A bottom piece which holds the circuit board.
* A top piece which covers the circuit board and sensors, with ample clearance for the components, a USB cable, and airflow for the sensors.

You can [tinker the design on TinkerCAD here](https://www.tinkercad.com/things/irFmvsATUlu-microenv-sensor-v2x-case).

The case design and images in this folder are © 2026 [Joshua M. Boniface](https://www.boniface.me) and licensed under the [Creative Commons Attribution-ShareAlike (BY-SA) 4.0](LICENSE) license.

## Printing

In this directory are 2 `.obj`-format CAD files providing the case. They should be compatible as-is with any slicing software and 3D printer model; no rotation or other transformations are required.

As a general set of parameters, all models should be printed with the following. All values are provided as their OrcaSlicer 2.3 names; your slicer may differ.

* 0.4mm nozzle/line width (or similar as provided by the slicer)
* 0.16mm layer height, or a clean multiple thereof
* No brim or raft
* 7-10 wall loops
* 7-10 shell layers (top + bottom)
* 25% infill
* Concentric patterns for infill
* Concentric patterns for surfaces (visual only)
* Back (preferred) or Aligned seams (visual only)

All other options are be specific to your printer, material, and desired effect.

The parts should be printed in a solid, durable material of any colour you wish. We use ABS in one of two colours (black or white) for our official prints.

### Case Models

These are the models that make up the case. Each case requires 1x `case-bottom` and 1x `case-top`.

#### `case-bottom`

This is the lower section of the case which directly holds the PCB and includes the male mating inserts. It also includes 3 vents for the SHT45.

#### `case-top`

This is the upper section of the case which covers the PCB and includes the female mating indents. It includes a pyramidal opening for the SGP41 sensor, 3 top and 4 side vents for the SHT45, and several cutouts for the USB connection.

## Assembly & Installation

To begin, print the parts above as required for the specific mounting type you want.

1. Insert the PCB into the `case-bottom` print, ensuring that the holes in the PCB align with the standoffs in the print. There may be some play due to board or case warping, so press it down as far as it will go.

2. Take the `case-top` print, and align the male/female mating components, ensuring that the SGP41 sensor is correctly centered within it opening.

3. Press down gently but firmly on a hard even surface to combine the mating components and close the case.

**NOTE**: Once mated, the two prints can not be easily separated without likely damaging the male mating inserts. If you must open the case again, you may need to re-print the `case-bottom` model.
