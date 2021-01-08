## Flight Considerations
---
For the drone to be useful for indoor navigation a long flight time (within reason) is desired. For this project, the aim was to achieve a ~10 minute flight with the following considerations were estimated:

With 4000mAh LiPo battery:

 + Expected weight of ~2 kg.
 + ~ 500 g thrust@hover/motor -> 7.4 A draw (ideally).
 + ~ 40 A draw from all motors + ~3A draw from normal NUC operation + 20% safety factor.
  > Estimated flight time is = (4 A/ 40 A) * 60 min/hr =  6 min

Although, this battery does not deliver the necessary flight time, it was useful to test the drone at earlier stages without hardware modifications. Once the drone was stable at flight, we moved into a larger battery.

With 8000mAh LiPo battery:

+ Expected weight of ~2 kg.
+ ~ 500 g thrust@hover/motor -> 7.4 A draw (ideally).
+ ~ 50 A draw from all motors + ~3A draw from normal NUC operation + 20% safety factor.
 > Estimated flight time is = (8 A/ 50 A) * 60 min/hr =  9.6 min


---

With the final iteration of the drone, the following holds:

 + Drone weight with 3 cameras, flight controller, sensors and NUC is currently at 2.5 kg
 + 8500 mAh battery is used to achieve a 12:44 minute flight.
 + Power consumption increased (due to weight increase) to ~80 Amps.
 + Despite the consumption, the battery is never depleted lower than 3.3 V per cell ( for a 4S battery). The recommended limit by the manufacturer to avoid damage to the battery is 3.2 V.
 + Power consumption for the NUC with all 3 RealSense cameras working never exceeds 5 A, with an average of 3.3 A.

> Current flight time is = 12:44 min

 *All the flight times that were measured in the flight tests were considering a static hovering, so expect the flight time to vary slightly if performing more dynamic movements.*

 ---
## General considerations when handling the batteries:

 > :material-battery-alert: **Never allow the voltage per cell drop below 3.2 V under load (flying)**

 > :material-fire: **Wait for the battery to cool down before charging**

 > :material-ev-station: **Balance-charge the batteries at 1C to avoid overcharging or damage**

 > :material-blood-bag: **Keep batteries inside protective bags**
