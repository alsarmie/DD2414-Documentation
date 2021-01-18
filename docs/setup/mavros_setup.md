# MAVROS Setup

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
**NOTE: Only follow this section if attempting to use the FTDI cable to connect the Pixhawk to the NUC.
See [PX4 Companion Computer Hardware Setup](https://docs.px4.io/master/en/companion_computer/pixhawk_companion.html#hardware-setup).
If flying with usb, change the [`CBRK_USB_CHK`](https://docs.px4.io/master/en/advanced_config/parameter_reference.html#CBRK_USB_CHK) parameter to `197848` and you can use the microUSB port on the Pixhawk 4 to connect to the NUC.**

When using the FTDI cable,
it was necessary to change the rates at which messages come in.
These are all added to `/ROMFS/px4fmu_common/init.d-posix/rcS` in our version of
[PX4 firmware](https://github.com/alsarm/PX4-Autopilot),
so it runs on Pixhawk boot.
If you are not running our version, you will need to change them
in QGroundControl every time the Pixhawk boots or make changes like
those we have made to  `/ROMFS/px4fmu_common/init.d-posix/rcS`.

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


## RPL MAVROS Wrappers

The ROS nodes required to run when flying are contained in
[dd2414_ros_companion_pc](https://github.com/alsarm/dd2414_ros_companion_pc).
Follow the instructions in the repo for setup.

 * [`uav.launch`](https://github.com/alsarm/dd2414_ros_companion_pc/blob/main/src/rpl/launch/uav.launch)
   is the launch file that you use.
 * Set up a config folder like [`awesome_drone/`](https://github.com/alsarm/dd2414_ros_companion_pc/tree/main/src/rpl/config/awesome_drone) that `uav.launch` will call
   * You shouldn't need to change much if anything in here
 * [`distance_sensor_override.py`](https://github.com/alsarm/dd2414_ros_companion_pc/blob/main/src/rpl/src/distance_sensor_override.py) is the 'fake mocap' that uses the distance sensro (TeraRanger) for z-axis estimates, but maps them through the MoCap position estimate topic
   * This was created because of z-axis drift issues when using the distance sensor directly with the Pixhawk.
     * This, we think, is because PX4 swaps to the barometer during periods of uncertainty when using the distance sensor and it is doesn't do this when using 'external vision'