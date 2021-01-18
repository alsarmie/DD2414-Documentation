## Design Overview
---

The main objective of this project was to improve the existing drone platforms.


  + *Previous working quadcopter*
<kbd>
  <img src="https://drive.google.com/uc?export=view&id=1S6N-BE8nQSU5emsR-n_m0tD9OuC-3pNb">
</kbd>
  + *Previous working hexacopter*
  <kbd>
    <img src="https://drive.google.com/uc?export=view&id=1Fe6wwjZy6Nwv8JpEMQuKM2kAXpSoLfZj">
  </kbd>

 In order to design the new drone, we first required to take into consideration the space limitations on which the previous drones operated and their current specs. In this case, as an indoor drone, it was desirable to be able to pass through doors (800 mm wide) with enough clearance. Given this constrain, we then required to choose the type of frame, motors and propellers that could meet the following requirements:

### Primary Design Objectives

 * Isotropic quadcopter
 * Longer flight time (10+ minutes)
 * 600 mm maximum blade tip-to-tip distance
 * Stable flight
 * Heavier & more configurable payloads (3 Intel RealSense cameras & a NUC)
 * Serviceable design for easier maintenance

### Additional Design Objectives

 * Better motor/propeller pairing
 * Better weight distribution (keep center of mass close to the center of the drone)
 * Better cable management
 * Parts that break, rather than bend
 * Shock absorption for landing gear
 * MoCap reflectors
 * Propeller guards

### Mandatory Hardware

 * 1 Flight Control Unit - PX4 Flight Stack
 * 1 Intel NUC computer
 * 3 RealSense cameras (RGB-D): 1 LIDAR (L515) + 2 Stereo (D435i)
 * 1 TeraRanger distance sensor, 1 Optical Flow sensor
 * 1 Y-PWR Hotswap board
 * DC/DC converters
