# DIY 1.8" TFT Display Module

A compact **DIY 1.8-inch TFT Display Module** designed for easy integration with ESP32, ESP32-S3 and other 3.3V microcontrollers.

The module uses a **16-pin, 0.5 mm pitch FPC interface** for the display and provides a simple **8-pin external interface**.

## ✨ Features

- 1.8-inch TFT display
- 8-pin external interface
- 16-pin, 0.5 mm pitch FPC
- 3.3V power supply
- SPI display interface
- Hardware reset
- Dedicated LCD backlight pins
- Compact DIY design
- Suitable for ESP32 / ESP32-S3 and similar MCUs

## 🔌 External Interface

| Pin | Signal | Description |
|---:|---|---|
| 1 | GND | Ground |
| 2 | 3.3V | 3.3V Power |
| 3 | DC | Data / Command |
| 4 | SCK | SPI Clock |
| 5 | MOSI/SDA | SPI Data |
| 6 | CS | Chip Select |
| 7 | RST | Display Reset |
| 8 | NC | Not Connected |

## 🖥️ Display FPC Pinout

The display uses a **16-pin, 0.5 mm pitch FPC**.

| FPC Pin | Signal |
|---:|---|
| 1 | GND |
| 2 | GND |
| 3 | GND |
| 4 | GND |
| 5 | VCC3P3 |
| 6 | VCC3P3 |
| 7 | DC |
| 8 | SCL |
| 9 | SDA |
| 10 | CS |
| 11 | GND |
| 12 | RESET |
| 13 | LED_A |
| 14 | LED_K1 |
| 15 | LED_K2 |
| 16 | GND |

## 🔗 Signal Mapping

```text
External Pin       Display FPC

GND       ────────> GND
3.3V      ────────> VCC3P3
DC        ────────> DC
SCK       ────────> SCL
MOSI/SDA  ────────> SDA
CS        ────────> CS
RST       ────────> RESET
NC        ────────> NC
```

## 💡 Backlight

The LCD FPC exposes three backlight-related connections:

```text
Pin 13 → LED_A
Pin 14 → LED_K1
Pin 15 → LED_K2
```

## ⚙️ ESP32 Connection

Example connection:

```text
Display Module       ESP32

GND       ─────────> GND
3.3V      ─────────> 3V3
DC        ─────────> GPIO
SCK       ─────────> SPI SCK
MOSI/SDA  ─────────> SPI MOSI
CS        ─────────> GPIO
RST       ─────────> GPIO
NC        ─────────> Not Connected
```

GPIO numbers can be selected according to the target ESP32 board and firmware.

## 📋 Specifications

| Parameter | Specification |
|---|---|
| Display Size | 1.8" |
| Display Interface | SPI |
| Logic / Power | 3.3V |
| External Interface | 8-Pin |
| Display FPC | 16-Pin |
| FPC Pitch | 0.5 mm |
| Reset | Hardware Reset |
| Backlight | LED_A / LED_K1 / LED_K2 |

## ⚠️ Important Notes

- The schematic specifies `VCC3P3` and a 3.3V external supply. Do not assume 5V compatibility.
- The display uses a 16-pin, 0.5 mm pitch FPC.
- Pin 8 of the external interface is marked `NC` and should be left unconnected.
- ST7735 Driver For 1.8 inch Display


## 📄 Schematic

**Revision:** 1.0  
**Date:** 2026-07-13  
**Designed By:** Samir Alam  
**Project:** Quadever


## 👨‍💻 Author

**Samir Alam**

### Quadever

DIY hardware and embedded electronics projects.

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.
