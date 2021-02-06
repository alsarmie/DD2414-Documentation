## Mechanical design considerations.
---

The main objective of this project was to improve the existing drone platforms, with the following specs:

<center>

  | Exisitng Drone Specs              | Quadcopter | Hexacopter |
  | --------------------------------- | ---------- | ---------- |
  | Wheelbase (mm)                    | 260        | 290        |
  | Prop size (mm) \*                 | 153        | 127        |
  | Max width (mm)                    | 370        | 420        |
  | Occupancy sphere radius           | 207        | 209        |
  | Empty Mass (g)                    | 760        | 1376       |
  | Full Mass (TX2, 4000mAh LiPo)     | 1328       | 2026       |
  | Number Propellers                 | 4          | 6          |
  | Minimum Thrust Ratio ( \_ : 1 )   | 2          | 2          |
  | Minimum Thrust per motor (g)      | 664        | 676        |
  | \* Hexacopter uses three blade propellers |    |            |

</center>

Starting with the frame, we decided upon a X body, as it is symmetric (pitch & roll), strong, compact and simple. Its natural symmetry  is better for balancing flying forces. Considering as well the biggest element the drone carries (Intel NUC), the ideal dimensions were reduced to the following diagram.

<p align="center">
<kbd>
  <img src="../../img/dimension_diagram.png" width=450>
  </kbd>
</p>

<center>

| Element                  | Size(mm) |
| ------------------------ | -------- |
| Wheelbase                | 380      |
| Propeller                | 204      |
| Drone Occupancy Radius   | 292      |
| Drone Occupancy Diameter | 584      |
| Clearance                | 124      |

</center>

To determine the type of motors and size of the propellers, we took an estimate of the total mass that the drone had to lift, taking the following considerations:

<center>

| Expected Mass Calculations - Fully Loaded |||
| ----------------------------------------- |||
| Component                                 | Component Mass (g) | Count |
| Frame with landing gear                   | 710  | 1 |
| NUC                                       | 226  | 1 |
| TX2                                       | 174  | 0 |
| LiPo Battery (4000 mAh)                   | 392  | 0 |
| LiPo Battery (8500 mAh)                   | 672  | 1 |
| RealSense D435i                           | 72   | 2 |
| RealSense D455                            | 120  | 0 |
| RealSense L515                            | 100  | 1 |
| SunnySky X2216-7 1250 KV III              | 69   | 4 |
| Low Level Hardware                        | 445  | 1 |
| Total                                     | 2573 | N/A |

</center>

Ideally we want to have a hovering lift force equal to the weight of the drone, that is a thrust ratio of 2:1. Hence, the maximum thrust we need to generate is 5146 g.

<center>

| Thrust Calculations          ||
| ---------------------------- ||
| Expected mass (g)            | 2573 |
| Thrust ratio ( \_ : 1 )      | 2 |
| Required Thrust (g)          | 5146 |
| Motor Count                  | 4 |
| Minimum thrust per motor (g) | 1287 |

</center>

For the actual drone frame, we chose the [Q380](https://www.rcnhobby.com/se/hmf-totem-q380-380mm-fpv-4-axel-mini-quadcopter-frame-kit.html) X frame due to the following useful features:

  + Complies with the 380-400 mm wheelbase size requirement
  + Glass filled nylon arms for increased strength and durability
  + Lightweight arm design
  + Integrated PDB for easy wiring and tidy installation
  + Increased internal space for additional electronics/equipment
  + Additional mounting holes for frame upgrades
  + Arguably the arm design allows for better CG


## Landing Gear Design

As sudden drops and crashes are commonplace in drone research,
it was desirable to have some level of shock absorption in the landing gear.
This is to help protect the more critical components from damage during a crash landing.

To accomplish this, we designed and 3D printed custom landing gear with magnetic shock absorption.
We split the landing gear into two primary components and embedded repelling magnets in each component.
The lower component, which contacts the ground,
is able to slide relative to the upper component,
which connects rigidly to the drone frame.


With a tensile force 1.3 kg per magnet and 12 magnets pairs (3 per leg x 4 legs),
the landing gear provides up to 31.2 kg of repelling force upon a crash.

This can be seen below in the gif demonstrating a static drop
test from 50 cm on a hard tile floor.


<p align="center">
  <kbd>
    <img src="../../img/fall_50cm.gif" width=450>
  </kbd>
</p>


Assembly and all components of the landing gear can be found at [Assembly - Landing Gear](../assembly/landing_gear.md)
