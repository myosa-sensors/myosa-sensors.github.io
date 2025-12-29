---
publishDate: 2025-12-26T00:00:00Z
title: Forest Sentinel - Aware but not always Awake
excerpt: A low-power multisensor intrusion detection system for forest and wildlife protection.
image: ./cover.jpg
category: Projects
tags:
  - myosa
  - sensors
  - iot
  - security
---

> A low-power, camera-free intrusion detection system using the MYOSA Development kit.

## Acknowledgements
This project was developed using the MYOSA Development kit. The authors acknowledge the MYOSA team for providing hardware and documentation support.

## Overview
Forest Sentinel is a low-power, neuromorphic-inspired intrusion detection system built using the MYOSA Development kit. It is designed for forest and wildlife protection in environments where continuous camera-based surveillance is impractical.

### Proposed Solution
Forest Sentinel uses multiple low-power sensors as parallel sensory channels. These channels generate events only when changes exceed thresholds, allowing the system to remain mostly idle while continuously “aware.”

## Demo / Examples

### Images
![Hardware Setup](./setup.jpg)
*MYOSA-based Forest Sentinel hardware setup*

![Block Diagram](./blockdiagram.jpg)
*System Architecture and Block Diagram*

![Monitoring Dashboard](./dashboard_3.jpg)
*Intrusion Detected Alert on Dashboard*

### Video
[Watch Project Demonstration](./demo.mp4)

## Tech Stack
* **Hardware:** ESP32 motherboard, APDS9960 proximity/light sensor, SW420 vibration sensor, OLED display, and Buzzer.
* **Firmware:** C++ (Arduino framework) developed in the PlatformIO environment.

## Usage Instructions
1. Power the MYOSA board via USB cable.
2. Plug in sensors using MYOSA cascade slots.
3. Upload firmware using PlatformIO: `platformio run --target upload`.

## License
MIT License