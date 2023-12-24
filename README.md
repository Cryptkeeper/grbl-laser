# Unmaintained Project
An updated fork of this patch is available via [JanUlrich/grbl-laser](https://github.com/JanUlrich/grbl-laser).

# grbl-laser
Quality of life patches to Autodesk's Fusion 360 [Grbl Laser](https://cam.autodesk.com/hsmposts?p=grbl_laser) post processor. Designed for use with the [SainSmart Genmitsu CNC Router 3018-PRO](https://www.sainsmart.com/collections/genmitsu-cnc/products/sainsmart-genmitsu-cnc-router-3018-pro-diy-kit) machine and firmware on [Grbl](https://github.com/gnea/grbl/wiki) version 1.1 (with no 1.1 exclusive features used).

## Changes
- Implements the `onPower` function, ensuring the laser cutter is turned on and off between moves instead of remaining always on and creating burn streaks.
- `throughPower`, `etchPower` and `vaporizePower` properties are now multipliers of the newly added `maxPowerLevel` property. This reduces the usage of firmware dependent [magic numbers](https://en.wikipedia.org/wiki/Magic_number_(programming)) and simplifies scale adjustments.
- Adds `throughPassCount` which enables duplicating through cutting operations (with optional comment header).

## Usage
- Ensure you have [Git installed](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
- Clone this repository using `git clone https://github.com/Cryptkeeper/grbl-laser`
- Download a copy of Autodesk's Fusion 360 [Grbl Laser](https://cam.autodesk.com/hsmposts?p=grbl_laser) post processor. Move it into the cloned `grbl-laser` directory and rename it to `grbl laser copy.cps`
- Run `git apply grbl-laser.patch` to apply the patch
- If successful, your patched copy will be named `grbl laser.cps`

Copy this file to your Autodesk's `Fusion 360 CAM/Posts/` directory.
