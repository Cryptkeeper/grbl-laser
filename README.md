# grbl-laser
A patch to Autodesk's Fusion 360 [Grbl Laser](https://cam.autodesk.com/hsmposts?p=grbl_laser) post processor which implements the ```onPower``` function, ensuring the laser cutter turns on and off between moves instead of remaining always on and creating burn streaks.

## Usage
- Ensure you have [Git installed](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
- Clone this repository using `git clone https://github.com/Cryptkeeper/grbl-laser`
- Download a copy of Autodesk's Fusion 360 [Grbl Laser](https://cam.autodesk.com/hsmposts?p=grbl_laser) post processor. Move it into the cloned `grbl-laser` directory and rename it to `grbl laser copy.cps`
- Run `git apply grbl-laser.patch` to apply the patch
- If successful, your patched copy will be named `grbl laser.cps`

Copy this file to your Autodesk's `Fusion 360 CAM/Posts/` directory.