### PX4 Software installation and build
---

The software version we are using for the current drone is based on release 1.11.2. You can clone the repo [here](https://github.com/alsarm/PX4-Autopilot.git).

Make sure to update your system before.

```bash
$ sudo apt-get update && upgrade
```

Install ninja build:

```bash
$ sudo apt-get install -y ninja-build
```

In the folder of preference, run the following :

```bash
$ git clone https://github.com/alsarm/PX4-Autopilot.git
```

Navigate inside the repo into the 'Tools' folder:

```bash
$ cd PX4-Autopilot/Tools/setup
```


Execute the 'ubuntu.sh' script, this will take some minutes to complete:

```bash
$ ./ubuntu.sh
```

If installation fails, you may need to check the Ubuntu Software tab in Software & Updates to verify that you have Community-maintained source checked.

To compile  the software, you will need to have an ARM GNU compiler version <9.3.1. Version 7.3.1 works pretty well. The setup script from previous step will install the compiler at

```bash
~/opt/gcc-arm-none-eabi-9-2020-q2-update
```

The easiest way to use version 7.3.1 is to download the corresponding files from [here](https://developer.arm.com/-/media/Files/downloads/gnu-rm/7-2018q2/gcc-arm-none-eabi-7-2018-q2-update-linux.tar.bz2?revision=bc2c96c0-14b5-4bb4-9f18-bceb4050fee7?product=GNU%20Arm%20Embedded%20Toolchain,64-bit,,Linux,7-2018-q2-update). Uncompress the .tar file and move it to '~/opt/' , then change the name of the folder to 'gcc-arm-none-eabi-9-2020-q2-update' (just remember to back up the previous folder). Other methods to setup the compiler could be through symbolic links.

Once the script finishes, you can check everything works by compiling the software. But before, you need to change to the 'release/1.11' branch:
```bash
~PX4-Autopilot$git checkout release/1.11
Branch 'release/1.11' set up to track remote branch 'release/1.11' from 'origin'.
Switched to a new branch 'release/1.11'

~PX4-Autopilot$make px4_fmu-v5_default
```

Alternatively you can directly upload to the PX4 by adding the option 'upload'

```bash
~PX4-Autopilot$make px4_fmu-v5_default upload
```

If you are prompted regarding some files not being in the recommended version, type 'y' and continue with the build.

---

### QGroundControl Install

To install QGroundControl, please refer to the very comprehensive guide provided by [them](https://docs.qgroundcontrol.com/master/en/getting_started/download_and_install.html)

---

### Debugging FMU

It may be useful to debug the PX4 via the NSH terminal. For that reason, you can use a FTDI cable to connect to the debug port, as described [here](https://docs.px4.io/master/en/flight_controller/snapdragon_flight_advanced.html#over-ftdi).

You can check how to connect the FTDI cable to the PX4 [here](/parts/cabling/).
