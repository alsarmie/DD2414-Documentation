# Flight Procedure

**TO DO: Add correct launch commands**


 1. Review [Flight Safety](/flying/flight_safety/) instructions
 2. Review [Flight Safety](/flying/flight_safety/) instructions again
 3. Set your QGroundControl parameter selections
    1. Especially `EKF2_HGT_MODE` (see [PX4 Parameter Reference](https://dev.px4.io/en/advanced/parameter_reference.html))
        1. Set value to `2` for using TeraRanger distance sensor readings directly for z-axis position measurements
        2. Set value to `3` for using MoCAp or TeraRanger readings mapped through the MoCap topic (see ____) for z-axis position measurements
 4. Configure relevant files such as `uav.launch`, `______`
    1. Select which RealSense cameras to use, z-axis estimate mode, etc.
 5. Safely place drone in the flying cage and reboot/prearm the Pixhawk 4
    1. You must be wearing PPE (gloves, safety glasses, ear muffs).
    2. Prearming is done with the pre-arming button.
 6. Launch all necessary ROS nodes
    1. `roslaunch ______`
 7. Verify the TeraRanger distance sensor is actively reporting
    distance values either through MAVROS or in QGroundControl
    (unless using alternative z-axis position source)
    1. If not, repeat the reboot/prearm procedure until it is.
 8. Begin recording video of flight with an external camera (w/ a view of the flight area)
 9. Begin recording a ROSBAG of all relevant topics
    1. `rosbag record ____`
 10. Arm the drone with the [Arming Gesture](https://docs.px4.io/master/en/advanced_config/prearm_arm_disarm.html#arming-gesture)
    1. Requires that the mode switch is set to Manual Mode (should be `[SA]` if you followed our [Flight Modes](/setup/flight_modes/) setup instructions)
    2. The Taranis X9D Plus is a Mode 2 transmitter (should be default)
 11. Visually verify all propellers are spinning
 12. Takeoff in Manual Mode by pushing the left throttle stick up towards a max of ~ 50% until you are ~ 1 m above ground
     1.  This requires getting a feel for how fast to accelerate based on the drone's specific configuration during this flight
 13. Switch to [Position Mode (Multicopter)](https://docs.px4.io/master/en/flight_modes/position_mc.html) by flipping the `[SA]` switch to centered position
 14. Center the throttle switch at 50% and fly based on Position Mode (Mode 2 remote) instructions
   <kbd>
      <img src="../../img/flying/position_mode.png">
   </kbd>
 15. When you are ready to land, or hear the low voltage alarm, fly above a flat landing
     spot and throttle stick down in Position Mode until the drone lands
 16. Switch to Manual Mode (`[SA]` up) and disarm with the disarming gesture
 17. Stop ROS nodes, ROSBAG recording, and external video recording
 18. Enter the flying cage (with full PPE) and fully disarm the pre-arming button
 19. Proceed to [Flight Reporting](/flying/flight_reporting/) instructions
