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
Forest Sentinel is a low-power, neuromorphic-inspired intrusion detection system designed for forest and wildlife protection where continuous camera-based surveillance is impractical. Instead of continuous capture, the system is event-driven, sensing environmental perturbations like artificial light, proximity changes, and ground vibrations.

### Problem Addressed
* High energy consumption of continuous camera-based monitoring.
* Reduced reliability of vision systems during night-time and low-light conditions.
* Difficulty of deploying complex sensing infrastructure in remote forest regions.

### Proposed Solution
Forest Sentinel uses multiple low-power sensors as parallel sensory channels. These channels generate events only when changes exceed thresholds, allowing the system to remain mostly idle while continuously “aware.”

## Demo / Examples

### Images
![Hardware Setup](./cover.jpg)
*MYOSA-based Forest Sentinel hardware setup*

![Block Diagram](./blockdiagram.png)
*System Architecture and Block Diagram*

![Monitoring Dashboard](./dashboard_3.png)
*Intrusion Detected Alert on Dashboard*

### Video
[Watch Project Demonstration](./demo.mp4)

## Features (Detailed)
1. **Context-Aware Night-Time Operation:** Transitions to active monitoring based on ambient light levels.
2. **Event-Driven Monitoring:** Passively monitors vibrations and proximity as early indicators of movement.
3. **Light-Triggered Confirmation:** Confirms intrusion only when sudden light (like a flashlight) is detected.
4. **Multi-Modal Notification:** Activates an audible buzzer, OLED display alert, and web dashboard logging.

## Tech Stack
* **Hardware:** ESP32 motherboard, APDS9960 proximity/light sensor, SW420 vibration sensor, OLED display, and Buzzer.
* **Firmware:** C++ (Arduino framework) developed in the PlatformIO environment.
* **Libraries:** Embedded sensor libraries compatible with the MYOSA platform.
* **Interface:** Web-based dashboard (HTML).

## Usage Instructions
1. Power the MYOSA board via USB cable or power bank.
2. Plug in sensors using MYOSA cascade slots.
3. Upload firmware using PlatformIO: `platformio run --target upload`.
4. Monitor status on the OLED display and web dashboard.

## License
MIT License