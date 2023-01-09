# ESP Chungus

Chungus is an ESP32-S3 development board created as a learning exercise in KiCad.

## Features

- [ESP32-S3](https://www.espressif.com/en/products/socs/esp32-s3) - Dual-core 240Mhz processor with WiFi and Bluetooth
- Breadboard-friendly pinout/dimensions (26.5 mm wide, 22.86mm between pin headers)
- 19 GPIOs broken out to pins
- Onboard WS2812B RGB LED connected to GPIO48
- Onboard Reset and Boot (GPIO0) switches
- Optional Li-ion battery charger

## Notes

Either ESP32-S3-WROOM-1 (PCB antenna) or ESP32-S3-WROOM-1U (IPEX antenna connector) are suitable for these boards.

The voltage regulator was chosen specifically for its low quiescent current. If you cannot source it, look for SOT23-5 LDO regulators with 3.3V output voltage and at least 500mA output current.

## Libraries

- [Espressif KiCad library](https://github.com/espressif/kicad-libraries)
- [WS2812B KiCad library](https://github.com/madworm/WS2812B.pretty)

## BOM

### Default

| Designator | Part                  | Notes               |
| ---------- | --------------------- | ------------------- |
| C1         | 0603 SMD 0.1uF        |                     |
| C2/C3      | 0603 SMD 10uF         |                     |
| C4         | 0603 SMD 1uF          |                     |
| D1         | 0603 SMD LED          |                     |
| J1         | Molex 47346-1001      | Micro-USB connector |
| J2/J3      | 2.54mm Pin Header     |                     |
| R1         | 0603 SMD 330 Ohm      |                     |
| R2         | 0603 SMD 10k Ohm      |                     |
| S1/S2      | PTS526_SM15_SMTR2_LFS | Tactile switch      |
| U1         | ESP32-S3-WROOM-1U     |                     |
| U2         | RT9080-33GJ5          | Voltage regulator   |
| U3         | WS2812B               | RGB LED             |

### LiPo

| Designator | Part                  | Notes               |
| ---------- | --------------------- | ------------------- |
| C1/C2/C6   | 0603 SMD 1uF          |                     |
| C3         | 0603 SMD 0.1uF        |                     |
| C4/C5      | 0603 SMD 10uF         |                     |
| J1         | Molex 47346-1001      | Micro-USB connector |
| J2         | JST-PH-2              | LiPo connector      |
| J3/J4      | 2.54mm Pin Header     |                     |
| R1         | 0603 SMD 10k Ohm      |                     |
| S1/S2      | PTS526_SM15_SMTR2_LFS | Tactile switch      |
| U1         | ESP32-S3-WROOM-1U     |                     |
| U2         | MAX1551EZK+T          | LiPo Charge IC      |
| U3         | RT9080-33GJ5          | Voltage regulator   |
| U4         | WS2812B               | RGB LED             |

## Schematic

### Default

![schematic](./images/default/schematic.png)

### LiPo

![schematic](./images/lipo/schematic.png)

## Renders

### Default

![raytraced pcb](./images/default/render-raytraced.png)
![pcb front](./images/default/render.png)
![pcb rear](./images/default/render-back.png)

### LiPo

![raytraced pcb](./images/lipo/render-raytraced.png)
![pcb front](./images/lipo/render.png)
![pcb rear](./images/lipo/render-back.png)
