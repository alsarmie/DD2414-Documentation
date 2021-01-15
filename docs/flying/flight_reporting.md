# Flight Reporting

After the flight, there will be a few different sources of useful flight
data that should be compiled and stored for analysis and future reference.

This includes:

 * Flight ROSBAG
 * PX4 log
 * External video
 * Flight notes

Examples of the what & how to save this flight data can be found in the [Flight tests](/tests/#flight-tests)
section of the [Weekly Updates & Tests](/tests/) page.

## Flight ROSBAG

**TO DO: Verify rosbag topics**

For each flight, you should record a [ROSBAG](http://wiki.ros.org/rosbag).
If you are unfamiliar with this process, see the [ROSBAG Tutorials](http://wiki.ros.org/rosbag/Tutorials).
Be sure to record all `mavros/` and `tf/` topics, and omit unnecessary topics,
so you can more easily replay and analyze these ROSBAGs at a later date.
Additionally, if any RealSense cameras are collecting data, the data should be also be saved in the ROSBAGs.

Since 10+ minutes the 3D camera data from three RealSense cameras will be an impractically large file,
it recommended that you record a base ROSBAG with all topics mentioned above for the duration of the flight
and additional ROSBAGs of `< 1 min` with these topics AND the `realsense/` camera topics during the periods of interest.



## PX4 Logs

The PX4 logs can be downloaded after the flight from QGroundControl and analyzed,
as described in [Flight Reporting](https://docs.px4.io/master/en/getting_started/flight_reporting.html).

**Note:** It is recommended to keep
[`SDLOG_MODE`](https://docs.px4.io/master/en/advanced_config/parameter_reference.html#SDLOG_MODE)
at it's default value of `0` so you don't record unnecessary log data.


### Flight Review

The [Flight Review](https://logs.px4.io/) tool they recommend proved very useful for us.

Follow the guidance in [Log Analysis using Flight Review](https://docs.px4.io/master/en/log/flight_review.html)
for details on how to interpret the [Flight Review](https://logs.px4.io/) results.


### ECL EKF Analysis

Another useful tool is the [ECL EKF Analysis](https://github.com/Auterion/ecl_ekf_analysis)
tool from [Auterion](https://github.com/Auterion).

This tool should already be installed in the `tools/` directory of your [PX4-Autopilot](https://github.com/PX4/PX4-Autopilot) installation.
If it isn't, you should be able to follow the installation instructions in their repo.

Process your PX4 logs using the `process_logdata_ekf.py` script from the command line, e.g:

`~$ ./PX4-Autopilot/Tools/ecl_ekf/process_logdata_ekf.py <path/to/PX4_log/filename>.ulg`

This will generate a `.pdf` report of states, values, etc. specific to the
[ECL EKF estimator](https://docs.px4.io/master/en/advanced_config/tuning_the_ecl_ekf.html)
data recorded over the duration the flight.



## External Video

You should also record an external video of each flight.
It is better if you have a dedicated camera for this,
but a cell phone can be used if not.

Recommendations:

 * Try to get most/all of the flight volume in (unobstructed) view of the camera
 * Mount/position the camera somewhere stable so it does not move
    * Handheld video will be less pleasant to watch
 * If filming through the net, stick the camera lens just inside
   the net so the net is not obstructing the camera's view
 * Ensure you have enough battery/memory capacity to record the full flight

Check out some examples of flight videos we recorded in the [Flight tests](/tests/#flight-tests)
section of the [Weekly Updates & Tests](/tests/) page.

## Flight Notes

It is recommended to jot down some notes about the flight immediately after the flight
and especially during analysis of the flight data if you are debugging some issues.
e.g:

<kbd>
   <img src="../../img/flying/flight_notes_example.png">
</kbd>

These sample notes were taken while we were performing battery life/flight duration tests,
hence the focus on power consumption.

The flight notes were also particularly useful for us when tuning the drone's PID controllers
(see [Multicopter PID Tuning Guide](https://docs.px4.io/master/en/config_mc/pid_tuning_guide_multicopter.html))
so that we could quickly & easily correspond PID parameter changes made with the resulting
performance changes in the drone's flight.

Check out some more examples of flight notes we took in the [Flight tests](/tests/#flight-tests)
section of the [Weekly Updates & Tests](/tests/) page.