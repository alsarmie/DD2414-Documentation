# Cabling Summary

<p align="center">
<kbd>
  <img src="../../img/PX4.png" alt="drawing" width="200">
</kbd>
</p>

The PX4 FMU v5 requires some custom cables to interact with the sensors. Here you will find the necessary information to replicate such cables.

---
### PMW3901 cable
The PX4 has 1 SPI port with the following pinout.Pixhawk SPI connector is JST-GH 7 pins.

<p align="center">
<kbd>
  <img src="../../img/SPI.png" alt="drawing" width="200">
</kbd>
</p>

<p align="center">
<kbd>
  <img src="../../img/pmw3901.svg" alt="drawing" width="500">
</kbd>
</p>
---
### Teraranger EVO mini cable

From the official documentation, you require to wire the Teraranger like [this](https://www.terabee.com/connection-to-pixhawk-autopilots-teraranger-evo/).

The PX4 FMU v5 has two I2C ports, you are interested in the port A. Pixhawk I2C connector is JST-GH 4 pins.

<p align="center">
<kbd>
  <img src="../../img/I2C.png" alt="drawing" width="200">
</kbd>
</p>
---
### ESP8266 cable
The PX4 FMU v5 has 2 telemetry ports. Telemetry 2 is the port to connect the ESP8266. The connector is a  JST-GH 6 pins.

<p align="center">
<kbd>
  <img src="../../img/ESP8266.png" alt="drawing" width="200">
</kbd>
</p>

<p align="center">
<kbd>
  <img src="../../img/ESP8266_wire.png" alt="drawing" width="500">
</kbd>
</p>

---
### Arm button cable
The PX4 FMU v5 has 1 GPS port, this port has the pins needed for the arm button. The connector is a JST-GH 10 pins.

<p align="center">
<kbd>
  <img src="../../img/GPS.png" alt="drawing" width="200">
</kbd>
</p>

<p align="center">
<kbd>
  <img src="../../img/arm_button.svg">
</kbd>
</p>

---
### Debug IO/FMU cable
The PX4 FMU v5 has 2 debug ports, one for I/O and another for the FMU. The connector is a male JST SM06B 6 pins. The one we use is the FMU debug port.

<p align="center">
<kbd>
  <img src="../../img/debug_px4.png" alt="drawing" width="400">
</kbd>
</p>

<p align="center">
<kbd>
  <img src="../../img/ftdi.svg">
</kbd>
</p>


---
### PX4 power + sensor connector
The PX4 FMU v5 has 2 power ports, the one we are interested in is POWER 1 port. The connector is a JST-GH 6 pins. This cable s different from the previous as it connecets different parts of the system. One end requires a DF13 male connector to interact with the Power Module current and voltage sensor readings.

<p align="center">
<kbd>
  <img src="../../img/power_px4.png" alt="drawing" width="200">
</kbd>
</p>

<p align="center">
<kbd>
  <img src="../../img/power_connector.svg">
</kbd>
</p>
