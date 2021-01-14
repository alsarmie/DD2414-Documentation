# MoCap Setup

## Existing Setup Documentation

These instructions have been taken directly from the KTH RPL CAS-UAV public pages, found at
[Setting up MOCAP for PixRacer Drones](https://www.kth.se/social/group/cas-rpl-uav-public/page/how-to-set-up-mocap-for-pixracer-drones-2/).
[Jan '21]


These instructions are specific to the motion capture (MoCap) system at the RPL Drone Lab.


## Safety first

By personal experience, we now know that it is unwise to experiment with the
drones without protective gear. In fact, it is probably unwise to do so with
protective gear. The motors are racing motors and are way more powerful than
normal multicopter motors. Therefore

 1. NEVER unsafe the drone unless it's in the protective cage, OR you are
    wearing protective gear and are alone in the workshop. This is to protect
    others (and yourself) from rogue drones.
 2. See 1.
 3. PWM_AUX_REV is a dangerous setting. Don't touch it.


## Components

You should have:

 * MOCAP system for 11 000 euros (cameras + Windows computer + Motive)
 * Drone with or without on-board co-computer, but a co-computer _is_ required
  to feed the MOCAP data into the flight control unit (FCU)

## MOCAP

Calibrate the MOCAP system using the wand supplied with the MOCAP system. Just
go wave the wand around with the calibration process started on the MOCAP
computer. It will tell you when it's done.

Calibrate the ground plane of the MOCAP system using the "calibration square",
which is in fact not a square but a triangleish shape. Put it in the center of
the capture volume, and align its axes. Know that the longer side is the Z
axis, and the shorter side is the X axis. One of them will be negated, I forget
which. I think it's the X axis. This is nothing to worry about because you can
then flip the coordinate system in the ground plane settings, which you will
have to anyway. Note that the rotations are accumulative; it's not a setting,
but a transformation that you add. So if you rotate 90° about X, and
then again -- you've actually rotated 180° about X in total.

Double check the orientation of the FCU in QGroundControl. Just do it. It's under the "Sensors" heading.

It is important to know that when you create a rigid body in the MOCAP system,
the current orientation of that rigid body will be its "unit orientation", and
so when you inevitably need to align the body frame to the frame of the MOCAP
system, do it before creating the body (or recreate it afterwards.)

DO NOT trust the axes labels in Motive. They are not indicative of which
direction is positive for each dimension. It's a lot easier to do this
alignment later, using RViz.

Enable the Data Streaming in Motive, found somewhere in the menus. It will send
its data to a multicast IP address, and that's great. Don't change it. NOTE that Motive sometimes sets the broadcasting device to "loopback", this effectively disables the MOCAP data broadcasting. We don't know why it keeps doing that.

## ROS
So, on the co-computer, install and run `mavros`, and `mavros_extras`. Edit the
configuration of mavros to include the `mocap_pose_estimate` plugin.

Also install `mocap_optitrack` and run it. You should be able to see your rigid
body in the TF tree (in RViz).