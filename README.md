# ESPhome on a Waveshare ESP32S3-ePaper-1.54

This repository provides the **ESPhome YAML configuration** and a custom **3D printed stand** for the Waveshare ESP32-S3-ePaper-1.54 development board.

The configuration is optimized for low-power operation and easy integration with **Home Assistant**.

## Hardware and Key Configuration

The Waveshare ESP32-S3-ePaper-1.54 requires specific GPIO manipulation to properly control power to peripherals. 

| Component | Function | GPIO Pin | ESPhome Status |
| :--- | :--- | :--- | :--- |
| **EPD 3.3V Enable** | Enables power to the e-Paper display. | **GPIO6** | Must be set to `LOW`
| **BAT Control** | Controls the main power path (Vbat to VSYS), essential for deep sleep/battery management. | **GPIO17** | Must be held `HIGH` during operation. |

## ESPhome YAML

The corresponding ESPhome configuration file, which includes the required `output` definitions for power control (GPIO6 and GPIO17) and the display setup, can be found here:

* **ESPhome Configuration:** [`waveshare_154_epd.yaml`](waveshare_154_epd.yaml)

## 3D Printed Stand

A custom stand was designed to house the board, providing stability and a clean desktop look.

* **FreeCAD Design Source:** [`esp32s3-ePaper-stand.FCStd`](esp32s3-ePaper-stand.FCStd)
* **Ready-to-Print STL:** [Download STL File](esp32s3-ePaper-stand.stl)
* **Finished Product:** !(esp32s3-ePaper-stand.jpg)

## Resources

For detailed hardware information and schematics, refer to the official Waveshare documentation.

* **Waveshare Wiki:** [ESP32-S3-ePaper-1.54](https://www.waveshare.com/wiki/ESP32-S3-ePaper-1.54)
* **Board Schematic (PDF):** [ESP32-S3-Touch-ePaper-1.54-Schematic.pdf](https://files.waveshare.com/wiki/ESP32-S3-ePaper-1.54/ESP32-S3-Touch-ePaper-1.54-Schematic.pdf)

