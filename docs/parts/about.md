# Parts
The drone assembly requires a combination of purchased parts,
custom designed 3D printed parts, and custom made cabling.
This page details all necessary parts and how they can be obtained.
If you are assembling this drone for the KTH CAS-UAV lab, you should
check all inventory prior to making any purchase orders as some parts
are likely already be on hand.


## Parts Summary by System

### Body / Landing Gear
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
| Flight Systems     | FCU Vibration Isolator    | Pixhawk 4 Vibration Damping Mount         | Purchased  |
| Flight Systems     | FCU Arming Switch         | PX4 Arming Switch                         | Purchased  |
| Flight Systems     | Range Finder              | TeraRanger Evo Mini                       | Purchased  |
| Flight Systems     | Optical Flow Sensor       | PWM3901 Optical Flow Sensor               | Purchased  |
| Flight Systems     | ESP8266 Wifi Module       | Adafruit Feather HUZZAH with ESP8266      | Purchased  |
| Flight Systems     | Radio Receiver            | FrSky D4R-II 4ch Receiver                 | Purchased  |
| Flight Systems     | Radio Controller          | FrSky Taranis X9D Plus <sup>1</sup>       | Purchased  |
| Flight Systems     | Sensor Plate              | Low Level Sensor Plate                    | 3D Printed |

#### Notes
1. Can be shared among multiple UAVs.

### Peripherals
| System             | Part Name                 | Part Description                          | Category   |
| ------             | ---------                 | ---------                                 | ---------- |
| Companion Computer | Intel NUC <sup>1</sup>    | Intel® NUC 8 Pro Board - NUC8v7PNB        | Purchased  |
| Companion Computer | NUC Mount <sup>2</sup>    | NUC Mount Assembly                        | 3D Printed |
| Perception         | RealSense Lidar Camera    | RealSense L515                            | Purchased  |
| Perception         | L515 Camera Mount         | L515 Camera Mount                         | 3D Printed |
| Perception         | RealSense Stereo Camera   | RealSense D435i                           | Purchased  |

#### Notes
1. It is recommended to purchase the up-to-date, highest quality NUC model.
2. The 3D printed NUC mount CAD file may need modifications if the footprint changes with newer models.

### Power Supply
| System             | Part Name                 | Part Description                          | Category   |
| ------             | ---------                 | ---------                                 | ---------- |
| Power Supply       | Battery Voltage Alarm     | In Line Battery Voltage Alarm             | Purchased  |
| Power Supply       | Hot Swap Board            | Y-PWR (5-30V, max. 2x 10A)                | Purchased  |
| Power Supply       | LiPo Battery              | 4S - 8500mAh - 50C LiPo                   | Purchased  |
| Power Supply       | Boost Converter           | DC-DC 10-32V To 12-35V 150W Booster       | Purchased  |
| Power Supply       | Boost Converter Mount     | Boost Converter Mount                     | 3D Printed |
| Power Supply       | PX4 power supply          | PX4 power supply (Buck Converter)         | Purchased  |
| Power Supply       | Capacitor                 |                                           | Purchased  |
| Power Supply       | Power Connector Holder    | Power Connector Holder                    | 3D Printed |
| Power Supply       | FCU Power Switch          | FCU Power / Reboot Switch                 | Purchased  |
| Power Supply       | XT60 Connectors           | XT60 Connectors                           | Purchased  |
| Power Supply       | XT90 Connectors           | XT90 Connectors                           | Purchased  |

### Propulsion
| System             | Part Name                 | Part Description                          | Category   |
| ------             | ---------                 | ---------                                 | ---------- |
| Propulsion         | Motors                    | SunnySky X2216 V3 - 1250kV - short shaft  | Purchased  |
| Propulsion         | 30A, 2S-4S ESC's          | 30A, 2S-4S Multirotor ESC's               | Purchased  |
| Propulsion         | Propellers                | 8045 Propellers - 2x CW & 2x CCW          | Purchased  |
| Propulsion         | Propeller Adapters        | 5mm (M5) prop adapters - 2x CW & 2x CCW   | Purchased  |
| Propulsion         | Propeller Guards          | Propeller Guards - 8045 props             | Either     |

#### Notes
1. There are two options for propeller guards. The purchased guards have proven to withstand more damage during collisions.


### Cabling

--

<ins>**TODO:** We need a summary of all cabling (esp. custom cables) required for building the drone.</ins>

--

### Hardware / etc.

   * Zipties
     * Small
     * Large
   * Screws w/ nuts (M3, M4, M5)
   * Double sided sticky foam pads
   * ...


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
| Part Name              | Part Description                      | Unit Price | Quantity          | Purchase Link |
| ---------              | ---------                             | ---------- | --------          | ------------- |
| Drone Frame            | 380mm Multirotor Quadcopter Frame     | 128 SEK    | 1                 | [Q380 Drone Frame](https://www.aliexpress.com/item/32416043953.html) |
| Landing Gear Magnets   |                                       |            | 24+ <sup>1</sup>  |               |

#### Notes
1. 3 per leg are installed (12 total). It is worth ordering a full extra set as they are fragile.


### Flight Systems
| Part Name              | Part Description                       | Unit Price | Quantity  | Purchase Link |
| ---------              | ---------                              | ---------- | --------  | ------------- |
| Pixhawk 4 (FCU)        | Pixhawk 4 (plastic) & PM07​ (SKU20045)  | 1,391 SEK  | 1         | [Pixhawk 4](https://shop.holybro.com/pixhawk-4_p1089.html) |
| FCU Vibration Isolator | Pixhawk 4 Vibration Damping Mount      | 74 SEK     | 1         | [PX4 Mount](https://www.amazon.com/ShareGoo-Absorber-Anti-vibration-Damping-Controller/dp/B072KB31YT/ref=psdc_16413721_t1_B01KKB4SNI) |
| FCU Arming Switch      | PX4 Arming Switch                      | 25 SEK     | 1         | [Arming Switch](https://www.aliexpress.com/item/33060035462.html?src=google&albch=shopping&acnt=494-037-6276&isdl=y&slnk=&plac=&mtctp=&albbt=Google_7_shopping&aff_platform=google&aff_short_key=UneMJZVf&&albagn=888888&albcp=9765961330&albag=100795971798&trgt=893380456706&crea=en33060035462&netw=u&device=c&albpg=893380456706&albpd=en33060035462&gclid=Cj0KCQiA3NX_BRDQARIsALA3fILsHg18GC2DRCPcCJEo6q3CWfeeYMpiraQjtbHvxQHZJ76jEH4vG7gaAnRHEALw_wcB&gclsrc=aw.ds) |
| Range Finder           | TeraRanger Evo Mini (I2C / UART)       | 272 SEK    | 1         | [TeraRanger Evo Mini](https://www.terabee.com/shop/lidar-tof-range-finders/teraranger-evo-mini/) |
| Optical Flow Sensor    | PWM3901 Optical Flow Sensor            | 174 SEK    | 1         | [PWM3901 SPI](https://www.mouser.se/ProductDetail/Pimoroni/PIM453?qs=%2Fha2pyFadujcrkzpONsj8cpNlTta6xJ%252BLCS4A0%2FMxllTtYUHJXr3xg==) |
| ESP8266 Wifi Module    | Adafruit Feather HUZZAH with ESP8266   | 249 SEK    | 1         | [HUZZAH with ESP8266](https://www.m.nu/esp8266/adafruit-feather-huzzah-with-esp8266-wifi?gclid=CjwKCAiAudD_BRBXEiwAudakXxkArK_9KV-ZcGk-k5BBhP_KHf8zPEcFNFU5CW21lHIi_QdFZW6AgRoCgJQQAvD_BwE)  |
| Radio Receiver         | FrSky D4R-II 4ch Receiver <sup>1</sup> | 205 SEK    | 1         | [FrSky D4R-II](https://hobbyking.com/en_us/frsky-d4r-ii-4ch-2-4ghz-accst-receiver-w-telemetry.html) |
| Radio Controller       | FrSky Taranis X9D Plus                 | 1,787 SEK  | 1         | [FrSky Taranis X9D Plus](https://www.amazon.com/FrSky-Taranis-Access-Telemetry-Silver/dp/B07VRP1V76?ref_=ast_sto_dp) |

#### Notes
1. May need to be updated to a newer FrSky model if stock can't be found.

### Peripherals
| Part Name               | Part Description                     | Unit Price | Quantity   | Purchase Link |
| ---------               | ---------                            | ---------- | --------   | ------------- |
| Intel NUC               | Intel® NUC 8 Pro Board - NUC8v7PNB   | 6,950 SEK  | 1          | [Intel NUC 8](https://www.intel.com/content/www/us/en/products/boards-kits/nuc/boards/nuc8v7pnb.html) |
| RealSense Lidar Camera  | RealSense L515                       | 2,866 SEK  | 1          | [RealSense L515](https://store.intelrealsense.com/buy-intel-realsense-lidar-camera-l515.html?_ga=2.143016189.994846934.1609904308-148542041.1609904308)   |
| RealSense Stereo Camera | RealSense D435i                      | 1,638 SEK  | 2          | [RealSense D345i](https://store.intelrealsense.com/buy-intel-realsense-depth-camera-d435i.html?_ga=2.143016189.994846934.1609904308-148542041.1609904308) |

### Power Supply
| Part Name              | Part Description                       | Unit Price | Quantity   | Purchase Link |
| ---------              | ---------                              | ---------- | --------   | ------------- |
| Battery Voltage Alarm  | In Line Battery Voltage Alarm          |  84 SEK    | 1          | [Voltage Alarm](https://www.banggood.com/In-Line-Battery-Voltage-Alarm-with-LED-XT60-Plug-For-2-6s-Lipo-Battery-p-1177822.html?gmcCountry=SE&currency=SEK&createTmp=1&utm_source=googleshopping&utm_medium=cpc_union&utm_content=xibei&utm_campaign=xibei-ssc-se-all-0716&gclid=Cj0KCQjwtsv7BRCmARIsANu-CQd8WyIR64i91Yg7cU2ZQOLiWxwwMilk2XDveCLeTr-AbmSQR3E-rn4aAr1JEALw_wcB&cur_warehouse=CN) |
| Hot Swap Board         | Y-PWR (5-30V, max. 2x 10A)             | 201 SEK    | 1          | [Y-PWR Hot Swap Board](https://www.cartft.com/en/catalog/il/1330) |
| LiPo Battery           | 4S - 8500mAh - 50C LiPo                | 1,340 SEK  | 1          | [4s 8500mAh - 50C - Gens Ace XT90 LiPo](https://www.elefun.se/p/prod.aspx?v=49695) |
| Boost Converter        | DC-DC 10-32V To 12-35V 150W Booster    | 59 SEK     | 1          | [Boost Converter](https://www.banggood.com/2Pcs-DC-DC-10-32V-To-12-35V-150W-Booster-Module-For-Laptop-Adapter-p-948153.html?gmcCountry=SE&currency=SEK&createTmp=1&utm_source=googleshopping&utm_medium=cpc_bgs&utm_content=xibei&utm_campaign=xibei-ssc-se-en-ecs-0724&gclid=CjwKCAjw8MD7BRArEiwAGZsrBZ_ucC_BZepWcxMNf89zM9WKc2TAgvkuiYDC1v7J4TeG6H4Ztzin4BoCmJgQAvD_BwE&cur_warehouse=CN) |
| PX4 power supply       | PX4 power supply (Buck Converter)      | 106 SEK    | 1          | [PX4 Power Module](https://www.amazon.com/Pixhawk4-PXFmini-Pixracer-Quadcopter-Connector/dp/B07PHRS4C4) |
| Capacitor              |                                        |            |            |               |
| FCU Power Switch       | FCU Power / Reboot Switch              |            |            |               |
| XT60 Connectors        | XT60 Connectors (10 pack) <sup>1</sup> | 57 SEK     | 1          | [XT60 pack](https://www.amazon.com/MCIGICM-Female-Bullet-Connectors-Battery/dp/B07DVDKL42/ref=asc_df_B07DVDKL42/?tag=hyprod-20&linkCode=df0&hvadid=242124331408&hvpos=&hvnetw=g&hvrand=17600348725652844901&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9031214&hvtargid=pla-487616023903&psc=1) |
| XT90 Connectors        | XT90 Connectors (5 pack) <sup>1</sup>  | 106 SEK    | 1          | [XT90 pack](https://www.amazon.com/Amass-Connector-Anti-Spark-Battery-Charger/dp/B074PTHZ3M/ref=asc_df_B074PTHZ3M/?tag=hyprod-20&linkCode=df0&hvadid=241976201237&hvpos=&hvnetw=g&hvrand=15813005595323829712&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9031214&hvtargid=pla-454617925652&psc=1) |

#### Notes
1. Only 1 each of XT60 & XT90 connectors needed, but they are usually purchased in a pack.


### Propulsion
| Part Name              | Part Description                         | Unit Price | Quantity           | Purchase Link |
| ---------              | ---------                                | ---------- | --------           | ------------- |
| Motors                 | SunnySky X2216 V3 - 1250kV - short shaft | 187 SEK    | 6+ <sup>1</sup>    | [SunnySky V3 X2216 Motors](https://sunnyskyusa.com/products/sunnysky-x2216?variant=27868073394270) |
| 30A, 2S-4S ESC's       | 30A, 2S-4S Multirotor ESC's              | 86 SEK     | 12+ <sup>2,3</sup> | [30A, 4S ESC's](https://hobbyking.com/en_us/blheli-s-30a.html?utm_source=google&utm_medium=cpc&utm_campaign=google_us_shopping&countrycode=US&gclid=Cj0KCQiA3NX_BRDQARIsALA3fIKZ4hVcBt_OM8rsq9deMwhyn5tWA2MbVwPeuNdMDwFlwVMlrfD3hTUaAvgHEALw_wcB&gclsrc=aw.ds) |
| Propellers             | 8045 Propellers - 2x CW & 2x CCW         | 32 SEK     | 10+ <sup>4</sup>   | [8045 CW & CCW Propellers](https://hobbyking.com/en_us/8x4-5-sf-propellers-std-and-reverse-rotation-black-4pcs.html?___store=en_us) |
| Propeller Adapters     | 5mm (M5) prop adapters - 2x CW & 2x CCW  | 71 SEK     | 1                  | [M5 Prop Adapters](https://www.aliexpress.com/item/32811870942.html?spm=a2g0o.productlist.0.0.3e2a65f2dhOpjR&algo_pvid=514ee6fd-d665-467b-a778-3d5a8518a859&algo_expid=514ee6fd-d665-467b-a778-3d5a8518a859-0&btsid=0bb0623416018166608475111e42e9&ws_ab_test=searchweb0_0,searchweb201602_,searchweb201603_) |
| Propeller Guards       | Propeller Guards - 8045 props            |            | 8+ <sup>5</sup>    |               |

#### Notes
 1. Purchase at least 5 motors in case one is damaged or fails (somewhat likely).
 2. These are only a representative example of 30A ESC's. Any similar product will do.
 3. Purchase at least 12 ESC's in case some fail / burn up (very likely).
    1. Technically the recommended motors can draw > 30 A, but shouldn't under the design conditions.
    2. Additionally, 40 A ESC's are excessively heavy and more expensive.
 4. Purchase around 10 packs of blades (4 per pack) as any collisions may result in damaged propellers that require replacement.
 5. Purchase at least 2 sets of propeller guards as any extreme collisions may result in damaged guards that require replacement.


## 3D Printed Parts Summary

The following 3D printed parts are required for constructing the drone as designed.
Note that all links include the required .stl files for 3D printing, while some
links will include .ipt (AutoDesk Inventor) files that can be improved / customized.

If there are any access issues please contact Kyle Coble at [kwc57@cornell.edu](kwc57@cornell.edu).

[Link to all CAD file folders](https://drive.google.com/drive/folders/1cGAwa-KiyMPA3GqdAuRivi8l1ZGf-k5G?usp=sharing)


| System             | Part Type                 | Part Name                     | Quantity | CAD Link |
| ------             | ---------                 | ---------                     | -------- | ----     |
| Body               | Large Battery Adapter     | Large Battery Adapter         | 4        | [Large Battery Adapter ](https://drive.google.com/drive/folders/1uap2Yj39mSSUyjF8RAOGZAhPu2N2kLyg?usp=sharing) |
| Landing Gear       | Landing Gear Assembly     | Landing Gear Assembly         | 4        | [Landing Gear Assembly ](https://drive.google.com/drive/folders/18POZlQbrHtJMRAQEIRWGYhrx_C7PdH1Q?usp=sharing) |
| Flight Systems     | Sensor Plate              | Low Level Sensor Plate        | 1        | [Low Level Sensor Plate](https://drive.google.com/drive/folders/1gYHbsAsMWU1eWWXqgtkynMo1hv9yFUdo?usp=sharing) |
| Companion Computer | NUC Mount                 | NUC Mount Assembly            | 1        | [NUC Mount Assembly    ](https://drive.google.com/drive/folders/1BV5lZG86zBsEEb_vWatxMujV6_MNMZNt?usp=sharing) |
| Perception         | L515 Camera Mount         | L515 Camera Mount             | 1        | [L515 Camera Mount     ](https://drive.google.com/drive/folders/1u5H9TtVz9fjSNWXMWIMLbXnKLl3-7Bkz?usp=sharing) |
| Power Supply       | Boost Converter Mount     | Boost Converter Mount         | 1        | [Boost Converter Mount ](https://drive.google.com/drive/folders/13RaEbpgpk8FFmrktdRqJVaby-_lfqt-y?usp=sharing) |
| Power Supply       | Power Connector Holder    | Power Connector Holder        | 1        | [Power Connector Holder](https://drive.google.com/drive/folders/1f3mKzfqlhNqATIsFCsNNFlk3i8NtxnCB?usp=sharing) |
| Propulsion         | Propeller Guards          | Propeller Guards - 8045 props | 4        | [Propeller Guards      ](https://drive.google.com/drive/folders/1s5grezjiT4flGRODpr2cLomOxQAkHWBo?usp=sharing) |
