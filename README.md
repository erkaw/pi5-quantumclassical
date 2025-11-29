# pi5-quantumclassical

Module C 
- python3-gpiozero [https://gpiozero.readthedocs.io/en/stable/index.html]
- libgpiod-dev [https://libgpiod.readthedocs.io/en/stable/]

Description        : Raspberry Pi 5B rev 1.1
Revision           : d04171
SoC                : BCM2712
RAM                : 8GB
Storage            : MicroSD
USB ports          : 4 (of which 2 USB3)
Ethernet ports     : 1 (1000Mbps max. speed)
Wi-fi              : True
Bluetooth          : True
Camera ports (CSI) : 2
Display ports (DSI): 2

,--------------------------------.
| oooooooooooooooooooo J8   : +====
| 1ooooooooooooooooooo      : |USB2
|  Wi  Pi Model 5B  V1.1  fan +====
|  Fi     +---+      +---+       |
|         |RAM|      |RP1|    +====
||p       +---+      +---+    |USB3
||c      -------              +====
||i        SoC      |c|c J14     |
(        -------  J7|s|s 12 +======
|  J2 bat   uart   1|i|i oo |   Net
| pwr\..|hd|...|hd|o|1|0    +======
`-| |-1o|m0|---|m1|--------------'

J8:
   3V3  (1) (2)  5V
 GPIO2  (3) (4)  5V
 GPIO3  (5) (6)  GND
 GPIO4  (7) (8)  GPIO14
   GND  (9) (10) GPIO15
GPIO17 (11) (12) GPIO18
GPIO27 (13) (14) GND
GPIO22 (15) (16) GPIO23
   3V3 (17) (18) GPIO24
GPIO10 (19) (20) GND
 GPIO9 (21) (22) GPIO25
GPIO11 (23) (24) GPIO8
   GND (25) (26) GPIO7
 GPIO0 (27) (28) GPIO1
 GPIO5 (29) (30) GND
 GPIO6 (31) (32) GPIO12
GPIO13 (33) (34) GND
GPIO19 (35) (36) GPIO16
GPIO26 (37) (38) GPIO20
   GND (39) (40) GPIO21

J2:
RUN (1)
GND (2)

J7:
COMPOSITE (1)
      GND (2)

J14:
TR01 TAP (1) (2) TR00 TAP
TR03 TAP (3) (4) TR02 TAP

This program checks the board's user-accessible GPIO pins. The board's model is: Raspberry Pi 5B rev 1.1. The following pins are selected for testing:

GPIO22, GPIO6, GPIO16, GPIO10, GPIO12, GPIO25, GPIO9, GPIO13, GPIO5, GPIO7, GPIO20, GPIO2, GPIO15, GPIO19, GPIO21, GPIO17, GPIO23, GPIO0, GPIO18, GPIO1, GPIO4, GPIO27, GPIO14, GPIO26, GPIO3, GPIO8, GPIO11, GPIO24

Please ensure that nothing is connected to any of the pins listed above for the test duration.

Proceed with test? [y/N] y
Testing GPIO22...ok
Testing GPIO6...ok
Testing GPIO16...ok
Testing GPIO10...ok
Testing GPIO12...ok
Testing GPIO25...ok
Testing GPIO9...ok
Testing GPIO13...ok
Testing GPIO5...ok
Testing GPIO7...ok
Testing GPIO20...ok
Testing GPIO2...ok
Testing GPIO15...ok
Testing GPIO19...ok
Testing GPIO21...ok
Testing GPIO17...ok
Testing GPIO23...ok
Testing GPIO0...ok
Testing GPIO18...ok
Testing GPIO1...ok
Testing GPIO4...ok
Testing GPIO27...ok
Testing GPIO14...ok
Testing GPIO26...ok
Testing GPIO3...ok
Testing GPIO8...ok
Testing GPIO11...ok
Testing GPIO24...ok


gpiodetect - 5 lines:
```shell
gpiochip0 [pinctrl-rp1] (54 lines)
gpiochip10 [gpio-brcmstb@107d508500] (32 lines)
gpiochip11 [gpio-brcmstb@107d517c00] (15 lines)
gpiochip12 [gpio-brcmstb@107d517c20] (6 lines)
gpiochip13 [gpio-brcmstb@107d508520] (4 lines)
```
gpiochip0 - 54 lines:
```shell
        line   0:       "ID_SDA"                input
        line   1:       "ID_SCL"                input
        line   2:       "GPIO2"                 input
        line   3:       "GPIO3"                 input
        line   4:       "GPIO4"                 input
        line   5:       "GPIO5"                 input
        line   6:       "GPIO6"                 input
        line   7:       "GPIO7"                 input
        line   8:       "GPIO8"                 input
        line   9:       "GPIO9"                 input
        line  10:       "GPIO10"                input
        line  11:       "GPIO11"                input
        line  12:       "GPIO12"                input
        line  13:       "GPIO13"                input
        line  14:       "GPIO14"                input
        line  15:       "GPIO15"                input
        line  16:       "GPIO16"                input
        line  17:       "GPIO17"                input
        line  18:       "GPIO18"                input
        line  19:       "GPIO19"                input
        line  20:       "GPIO20"                input
        line  21:       "GPIO21"                input
        line  22:       "GPIO22"                input
        line  23:       "GPIO23"                input
        line  24:       "GPIO24"                input
        line  25:       "GPIO25"                input
        line  26:       "GPIO26"                input
        line  27:       "GPIO27"                input
        line  28:       "PCIE_RP1_WAKE"         input
        line  29:       "FAN_TACH"              input
        line  30:       "HOST_SDA"              input
        line  31:       "HOST_SCL"              input
        line  32:       "ETH_RST_N"             output active-low consumer="phy-reset"
        line  33:       "-"                     input
        line  34:       "CD0_IO0_MICCLK"        output consumer="cam0_reg"
        line  35:       "CD0_IO0_MICDAT0"       input
        line  36:       "RP1_PCIE_CLKREQ_N"     input
        line  37:       "-"                     input
        line  38:       "CD0_SDA"               input
        line  39:       "CD0_SCL"               input
        line  40:       "CD1_SDA"               input
        line  41:       "CD1_SCL"               input
        line  42:       "USB_VBUS_EN"           output
        line  43:       "USB_OC_N"              input
        line  44:       "RP1_STAT_LED"          output active-low consumer="PWR"
        line  45:       "FAN_PWM"               output
        line  46:       "CD1_IO0_MICCLK"        output consumer="cam1_reg"
        line  47:       "2712_WAKE"             input
        line  48:       "CD1_IO1_MICDAT1"       input
        line  49:       "EN_MAX_USB_CUR"        output
        line  50:       "-"                     input
        line  51:       "-"                     input
        line  52:       "-"                     input
        line  53:       "-"                     input
```
