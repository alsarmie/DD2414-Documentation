# Parts
The drone assembly requires a combination of purchased parts,
custom designed 3D printed parts, and custom made cabling.
This page details all necessary parts and how they can be obtained.
If you are assembling this drone for the KTH CAS-UAV lab, you should
check all inventory prior to making any purchase orders as some parts
are likely already be on hand.


## Parts Summary by System

### Body
| System             | Part Name                 | Part Description                          | Category   |
| ------             | ---------                 | ---------                                 | ---------- |
| Body               | Drone Frame               | 380mm Multirotor Quadcopter Frame         | Purchased  |
| Body               | Large Battery Adapter     | Large Battery Adapter                     | 3D Printed |
| Landing Gear       | Landing Gear Assembly     | Landing Gear Assembly                     | 3D Printed |
| Landing Gear       | Landing Gear Magnets      |                                           | Purchased  |

### Flight Systems
| System             | Part Name                 | Part Description                          | Category   |
| ------             | ---------                 | ---------                                 | ---------- |
| Flight Systems     | Flight Control Unit (FCU) | PixHawk 4                                 | Purchased  |
| Flight Systems     | FCU Vibration Isolator    |                                           | Purchased  |
| Flight Systems     | FCU Arming Switch         |                                           | Purchased  |
| Flight Systems     | Range Finder              | TeraRanger Evo Mini                       | Purchased  |
| Flight Systems     | Optical Flow Sensor       | PWM3901                                   | Purchased  |
| Flight Systems     | ESP8266 Wifi Module       | Adafruit Feather HUZZAH with ESP8266      | Purchased  |
| Flight Systems     | Radio Receiver            | FrSky D4R-II 4ch Receiver                 | Purchased  |
| Flight Systems     | Radio Controller          | FrSky Taranis X9D Plus &sup1;             | Purchased  |
| Flight Systems     | Sensor Plate              | Low Level Sensor Plate                    | 3D Printed |

#### Notes
1. Can be shared among multiple UAVs.

### Peripherals
| System             | Part Name                 | Part Description                          | Category   |
| ------             | ---------                 | ---------                                 | ---------- |
| Companion Computer | Intel NUC                 |                                           | Purchased  |
| Perception         | RealSense Lidar Camera    | RealSense L515                            | Purchased  |
| Perception         | L515 Camera Mount         | L515 Camera Mount                         | 3D Printed |
| Perception         | RealSense Stereo Camera   | RealSense D435i                           | Purchased  |

### Power Supply
| System             | Part Name                 | Part Description                          | Category   |
| ------             | ---------                 | ---------                                 | ---------- |
| Power Supply       | Battery Voltage Alarm     |                                           | Purchased  |
| Power Supply       | Hot Swap Board            | Y-PWR (5-30V, max. 2x 10A)                | Purchased  |
| Power Supply       | LiPo Battery              | 4S - 8500mAh - 50C LiPo                   | Purchased  |
| Power Supply       | Boost Converter           |                                           | Purchased  |
| Power Supply       | Buck Converter            | Buck Converter (PX4 power supply)         | Purchased  |
| Power Supply       | Capacitor                 |                                           | Purchased  |
| Power Supply       | Power Connector Holder    | Power Connector Holder                    | Purchased  |
| Power Supply       | FCU Power Switch          | FCU Power / Reboot Switch                 | Purchased  |

### Propulsion
| System             | Part Name                 | Part Description                          | Category   |
| ------             | ---------                 | ---------                                 | ---------- |
| Propulsion         | Motors                    | SunnySky X2216 V3 - 1250kV - short shaft  | Purchased  |
| Propulsion         | 30A ESC's                 |                                           | Purchased  |
| Propulsion         | Propellers                | 8045 Propellers - 2x CW & 2x CCW          | Purchased  |
| Propulsion         | Propeller Adapters        | 5mm (M5) prop adapters - 2x CW & 2x CCW   | Purchased  |
| Propulsion         | Propeller Guards          |                                           |            |



## Purchased Parts Summary

The table below includes prices, quantities, and links for items to be purchased for constructing
a replica of the drone designed in this project.


**Disclaimers:**

   * Some links may expire, prices will vary (esp. with fluctuating currency exchange rates),
and exact parts may become unavailable.
   * These are not the only sources for purchasing these components.
   * It is recommended to order duplicates (or more) of all parts as damage/failure of certain components is likely during flights and collisions.
     * Certain parts are noted as a strong recommendation to order spares, but spares for all parts are worthwhile.
   * Prices are presented in SEK, from January 2021.
   * Prices do not include taxes, shipping, import fees, etc.


### Body
| Part Name              | Part Description                      | Unit Price | Quantity   | Purchase Link |
| ---------              | ---------                             | ---------- | --------   | ------------- |
| Drone Frame            | 380mm Multirotor Quadcopter Frame     | 128 SEK    | 1          | [Q380 Drone Frame](https://www.aliexpress.com/item/32416043953.html) |
| Landing Gear Magnets   |                                       |            | 24+ &sup1; |               |

#### Notes
1. 3 per leg are installed (12 total). It is worth ordering a full extra set as they are fragile.


### Flight Systems
| Part Name              | Part Description                      | Unit Price | Quantity  | Purchase Link |
| ---------              | ---------                             | ---------- | --------  | ------------- |
| Pixhawk 4 (FCU)        | Pixhawk 4 (plastic) & PM07​ (SKU20045) | 1,391 SEK  | 1         | [Pixhawk 4](https://shop.holybro.com/pixhawk-4_p1089.html) |
| FCU Vibration Isolator |                                       |            |           |               |
| FCU Arming Switch      |                                       |            |           |               |
| Range Finder           | TeraRanger Evo Mini (I2C / UART)      | 272 SEK    | 1         | [TeraRanger Evo Mini](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-evo-mini/) |
| Optical Flow Sensor    | PWM3901                               | 174 SEK    | 1         | [PWM3901 SPI](https://www.mouser.se/ProductDetail/Pimoroni/PIM453?qs=%2Fha2pyFadujcrkzpONsj8cpNlTta6xJ%252BLCS4A0%2FMxllTtYUHJXr3xg==) |
| ESP8266 Wifi Module    | Adafruit Feather HUZZAH with ESP8266  | 249 SEK    | 1         | [HUZZAH with ESP8266](https://www.m.nu/esp8266/adafruit-feather-huzzah-with-esp8266-wifi?gclid=CjwKCAiAudD_BRBXEiwAudakXxkArK_9KV-ZcGk-k5BBhP_KHf8zPEcFNFU5CW21lHIi_QdFZW6AgRoCgJQQAvD_BwE)  |
| Radio Receiver         | FrSky D4R-II 4ch Receiver &sup1;      | 205 SEK    | 1         | [FrSky D4R-II](https://hobbyking.com/en_us/frsky-d4r-ii-4ch-2-4ghz-accst-receiver-w-telemetry.html) |
| Radio Controller       | FrSky Taranis X9D Plus                | 1,787 SEK  | 1         | [FrSky Taranis X9D Plus](https://www.amazon.com/FrSky-Taranis-Access-Telemetry-Silver/dp/B07VRP1V76?ref_=ast_sto_dp) |

#### Notes
1. May need to be updated to a newer FrSky model if stock can't be found.

### Peripherals
| Part Name               | Part Description                     | Unit Price | Quantity   | Purchase Link |
| ---------               | ---------                            | ---------- | --------   | ------------- |
| Intel NUC               |                                      |            |            |               |
| RealSense Lidar Camera  | RealSense L515                       | 2,866 SEK  | 1          | [RealSense L515](https://store.intelrealsense.com/buy-intel-realsense-lidar-camera-l515.html?_ga=2.143016189.994846934.1609904308-148542041.1609904308)   |
| RealSense Stereo Camera | RealSense D435i                      | 1,638 SEK  | 2          | [RealSense D345i](https://store.intelrealsense.com/buy-intel-realsense-depth-camera-d435i.html?_ga=2.143016189.994846934.1609904308-148542041.1609904308) |

### Power Supply
| Part Name              | Part Description                      | Unit Price | Quantity   | Purchase Link |
| ---------              | ---------                             | ---------- | --------   | ------------- |

[4s 8500mAh - 50C - Gens Ace XT90 LiPo](https://www.elefun.se/p/prod.aspx?v=49695)

### Propulsion
| Part Name              | Part Description                         | Unit Price | Quantity   | Purchase Link |
| ---------              | ---------                                | ---------- | --------   | ------------- |
| Motors                 | SunnySky X2216 V3 - 1250kV - short shaft | 187 SEK    | 6+ &sup1;  | [SunnySky V3 X2216 Motors](https://sunnyskyusa.com/products/sunnysky-x2216?variant=27868073394270) |
| 30A ESC's              |                                          |            | 12+ &sup2; |               |
| Propellers             | 8045 Propellers - 2x CW & 2x CCW         | 32 SEK     | 10+ &sup3; | [8045 CW & CCW Propellers](https://hobbyking.com/en_us/8x4-5-sf-propellers-std-and-reverse-rotation-black-4pcs.html?___store=en_us) |
| Propeller Adapters     | 5mm (M5) prop adapters - 2x CW & 2x CCW  | 71 SEK     | 1          | [M5 Prop Adapters](https://www.aliexpress.com/item/32811870942.html?spm=a2g0o.productlist.0.0.3e2a65f2dhOpjR&algo_pvid=514ee6fd-d665-467b-a778-3d5a8518a859&algo_expid=514ee6fd-d665-467b-a778-3d5a8518a859-0&btsid=0bb0623416018166608475111e42e9&ws_ab_test=searchweb0_0,searchweb201602_,searchweb201603_) |
| Propeller Guards       |                                          |            |            |               |

#### Notes
 1. Purchase at least 5 motors in case one is damaged or fails (somewhat likely).
 2. Purchase at least 12 ESC's in case some fail / burn up (very likely).
    1. Technically the recommended motors can draw > 30 A, but shouldn't under the design conditions.
    2. Additionally, 40 A ESC's are excessively heavy and more expensive.
 3. Purchase around 10 packs of blades (4 per pack) as any collisions may result in damaged propellers that require replacement.


## 3D Printed Parts Summary
| Part Type    | Part Name             | Quantity | CAD Link |
| ---------    | ---------             | -------- | ----     |
| Landing Gear | Landing Gear Assembly | 4        |          |

### 3D Printed Parts Notes
1. 

