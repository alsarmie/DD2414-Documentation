# MAVROS Setup


## RPL MAVROS Wrappers

**TO DO:**
**Need to push/link our RPL repo from the NUC and provide some usage instructions**

Then move this section further down on this page.


## MAVROS Links

MAVROS usage is well documented and your priority should be to follow
the official links / resources, especially as functionalities are updated.

 * [PX4 MAVROS](https://dev.px4.io/master/en/ros/mavros_installation.html)
 * [MAVROS Github](https://github.com/mavlink/mavros/tree/master/mavros)
 * [MAVROS ROS Wiki](http://wiki.ros.org/mavros)

## Initial Installation

On the drone's companion computer (the NUC), install the ROS Noetic version of
MAVROS, per the Binary installation instructions at
[MAVROS Binary Installation](https://github.com/mavlink/mavros/tree/master/mavros#binary-installation-deb).
At the time of writing this, the installation instructions are for ROS Kinetic,
but the NUC should be running Ubuntu 20.04, so instead install the Noetic version with:

`sudo apt-get install ros-noetic-mavros ros-noetic-mavros-extras`

and follow the instructions for dependency installation.

### Test the Installation

With the Pixhawk connected to the NUC, you should be able to
test for successful installation by launching:

`roslaunch mavros px4.launch fcu_url:=/dev/ttyUSB0:57600`

Or, if reading from the microUSB port on the Pixhawk:

`roslaunch mavros px4.launch fcu_url:=/dev/ttyACM0:57600`


And listen to some relevant topics, e.g.:

 * `rostopic echo /mavros/local_position/pose`
 * `rostopic echo /mavros/distance_sensor/hrlv_ez4_pub`
 * `rostopic echo /mavros/px4flow/raw/optical_flow_rad`


## Message Rate Adjustment

It was necessary to change the rates at which messages come in.
These are all added to `/ROMFS/px4fmu_common/init.d/rcS` in our version of
[PX4 firmware](https://github.com/alsarm/PX4-Autopilot),
so it runs on Pixhawk boot.
If you are not running our version, you will need to change them
in QGroundControl every time the Pixhawk boots or make changes like
those we have made to  `/ROMFS/px4fmu_common/init.d/rcS`.

The commands to change these message rates include, but are not limited to:

 * `mavlink stream -r 500 -s POSITION_TARGET_LOCAL_NED -d /dev/ttyS1`
 * `mavlink stream -r 500 -s LOCAL_POSITION_NED -d /dev/ttyS1`
 * `mavlink stream -r 500 -s GLOBAL_POSITION_INT -d /dev/ttyS1`
 * `mavlink stream -r 500 -s ATTITUDE -d /dev/ttyS1`
 * `mavlink stream -r 500 -s ATTITUDE_QUATERNION -d /dev/ttyS1`
 * `mavlink stream -r 500 -s ATTITUDE_TARGET -d /dev/ttyS1`
 * `mavlink stream -r 500 -s SERVO_OUTPUT_RAW_0 -d /dev/ttyS1`
 * `mavlink stream -r 500 -s RC_CHANNELS -d /dev/ttyS1`
 * `mavlink stream -r 500 -s OPTICAL_FLOW_RAD -d /dev/ttyS1`
 * `mavlink stream -r 500 -s DISTANCE_SENSOR -d /dev/ttyS1`
