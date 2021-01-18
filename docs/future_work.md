# Future Work

As this project was completed over a limited time frame,
this design should be considered as the first iteration
for the new KTH RPL CAS-UAV drone platform.

As such, there are a few potential areas for improvement
that should be considered as priorities during the second iteration.
These include:

 * TeraRanger I2C booting
 * Z axis drift with local positioning
 * Flying with USB


## TeraRanger I2C booting

The TerarRanger Evo Mini (our choice of distance sensor)
has an issue where it inconsistently fails to be recognized
by the PX4 code when the Pixhawk boots.
This may be a low level I2C driver issue.

A work around is to reboot the Pixhawk until the distance sensor
is recognized, but this is not a feasible long term solution.

This issue may be resolved in future PX4 releases, as it is
not an issue for all TeraRanger sensors.


## Z axis drift with local positioning

When flying with the distance sensor as the primary source of height data used by the EKF,
[`EKF2_HGT_MODE`](https://docs.px4.io/v1.9.0/en/advanced_config/parameter_reference.html#EKF2_HGT_MODE)
set to `2`, the EKF often switches to barometer for altitude readings.
This causes the z-axis estimate of the position to diverge.

A successful workaround of mapping the distance sensor values through the MoCap
topic was discussed in [MAVROS Setup - ROS Wrappers](setup/mavros_setup.md#rpl-mavros-wrappers).
However, this is not a feasible long term solution.


This issue may be resolved in future PX4 releases, as it is
a commonly discussed issue for those working with indoor flight
on the PX4 forums.


## Flying with USB

As mentioned in [MAVROS Setup - FTDI vs USB](setup/mavros_setup.md#ftdi-vs-usb), we chose to "fly with USB"
rather than with an FTDI cable.
This was not a design choice, but rather was because of issues we were facing
with mavlink / mavros message rates when using the FTDI cable.

Properly setting up the FTDI cable and flying with it rather than with USB
is the recommended configuration in the PX4 documentation.
See [Companion Computer for Pixhawk Series](https://docs.px4.io/master/en/companion_computer/pixhawk_companion.html)
for further details.