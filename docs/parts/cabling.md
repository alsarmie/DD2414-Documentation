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

<kbd>
  <img src="../../img/SPI.png" alt="drawing" width="200">
</kbd>

<kbd>
  <img src="../../img/pmw3901.svg">
</kbd>

---
### Teraranger EVO mini cable

From the official documentation, you require to wire the Teraranger like [this](https://www.terabee.com/connection-to-pixhawk-autopilots-teraranger-evo/).

The PX4 FMU v5 has two I2C ports, you are interested in the port A. Pixhawk I2C connector is JST-GH 4 pins.

<kbd>
  <img src="../../img/I2C.png" alt="drawing" width="200">
</kbd>
---
### ESP8266 cable
The PX4 FMU v5 has 2 telemetry ports. Telemetry 2 is the port to connect the ESP8266. The connector is a  JST-GH 6 pins.

<kbd>
  <img src="../../img/ESP8266.png" alt="drawing" width="200">
</kbd>

<kbd>
  <img src="../../img/ESP8266_wire.png">
</kbd>


---
### Arm button cable
The PX4 FMU v5 has 1 GPS port, this port has the pins needed for the arm button. The connector is a JST-GH 10 pins.

<kbd>
  <img src="../../img/GPS.png" alt="drawing" width="200">
</kbd>

<kbd>
  <img src="../../img/arm_button.svg">
</kbd>
