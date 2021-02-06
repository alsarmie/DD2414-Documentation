## Design Overview
---

The main objective of this project was to improve the existing drone platforms.


  + *Previous working quadcopter*

<p align="center">
<kbd>
  <img src="https://drive.google.com/uc?export=view&id=1S6N-BE8nQSU5emsR-n_m0tD9OuC-3pNb" width=500>
  </kbd>
</p>

  + *Previous working hexacopter*

<p align="center">
  <kbd>
    <img src="https://drive.google.com/uc?export=view&id=1Fe6wwjZy6Nwv8JpEMQuKM2kAXpSoLfZj" width=300>
  </kbd>
</p>

 In order to design the new drone, we first required to take into consideration the space limitations on which the previous drones operated and their current specs. In this case, as an indoor drone, it was desirable to be able to pass through doors (800 mm wide) with enough clearance. Given this constrain, we then required to choose the type of frame, motors and propellers that could meet the following requirements:

### Primary Design Objectives

 * Isotropic quadcopter
 * Longer flight time (10+ minutes)
 * 600 mm maximum blade tip-to-tip distance
 * Stable flight (designed for indoor mapping & SLAM, not for racing)
 * Heavier & more configurable payloads (3 Intel RealSense cameras & a NUC)
 * Serviceable design for easier maintenance

### Additional Design Objectives

 * Better motor/propeller pairing
    * Larger propellers -> lower motor RPM for same thrust → more efficient & less noise
 * Better weight distribution
    * Keep center of mass close to the center of the drone in all directions
 * Better cable management
    * Ability to tell where cables go and easily change cables/components out
 * Parts that break, rather than bend
    * Broken 3D printed parts can be quickly replaced
 * Shock absorption for landing gear
    * Protect sensitive components during hard landings
 * MoCap reflectors
    * For ground truth localization in certain environments
 * Propeller guards
    * Withstand collisions with doorways, walls, etc.

### Mandatory Hardware

 * 1 Flight Control Unit - PX4 Flight Stack
 * 1 Intel NUC computer
 * 3 RealSense cameras (RGB-D): 1 LIDAR (L515) + 2 Stereo (D435i)
 * 1 TeraRanger distance sensor, 1 Optical Flow sensor
 * 1 Y-PWR Hotswap board
 * DC/DC converters


### Perception Sensor Layout

With three RealSense cameras
(1 [L515 LiDAR Camera](https://www.intelrealsense.com/lidar-camera-l515/)
and 2 [D435i Stereo Cameras](https://www.intelrealsense.com/depth-camera-d435i/)),
this drone is designed to provide:

 * A 154 degree RGB field of view (FOV)
 * A 176 degree depth FOV
 * 22 degrees of RGB overlap *
 * 33 degrees of depth overlap *
 * 40+ degree height FOV from all sensors


**Between the L515 LiDAR Camera and each D435i stereo camera.*
