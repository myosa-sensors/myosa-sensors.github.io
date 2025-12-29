---
publishDate: 2025-12-26
title: Forest Sentinel - Aware but not always Awake
excerpt: A low-power multisensor intrusion detection system for forest and wildlife protection.
image: cover.jpg
tags:
  - myosa
  - sensors
  - iot
  - security
---
> A low-power, camera-free intrusion detection system using MYOSA Development kit.

## Acknowledgements

This project was developed using the MYOSA Development kit.
The authors acknowledge the MYOSA team for providing hardware and documentation support.

## Overview

Forest Sentinel is a low-power, neuromorphic-inspired intrusion detection system built using the MYOSA Development kit.
It is designed for forest and wildlife protection in environments where continuous camera-based surveillance is impractical
due to power, visibility, and deployment constraints.

Instead of relying on continuous data capture, the system operates in an event-driven manner by sensing localized
environmental perturbations such as sudden artificial light, proximity changes and ground vibrations. These sparse, meaningful events are processed using simple thresholding and decision logic,
closely mirroring how biological sensory systems respond only to significant stimuli.

### Problem Addressed
- High energy consumption of continuous camera-based monitoring
- Reduced reliability of vision systems during night-time and low-light conditions
- Difficulty of deploying and maintaining complex sensing infrastructure in remote forest regions

### Proposed Solution
Forest Sentinel adopts a neuromorphic sensing philosophy, where multiple low-power sensors act as parallel sensory channels.
Each channel generates events only when environmental changes exceed predefined thresholds, allowing the system to remain
mostly idle while continuously “aware” of its surroundings. This event-driven, non-visual approach enables efficient,
robust intrusion detection with minimal computational and power overhead.

## Demo / Examples

### Images

<p align="center">
  <img src="src/content/post/myosa-forest-sentinel/cover.jpg" width="800"><br/>
  <i>MYOSA-based Forest Sentinel hardware setup</i>
</p>

<p align="center">
  <img src="src/content/post/myosa-forest-sentinel/blockdiagram.png" width="800"><br/>
  <i>MYOSA-based Forest Sentinel hardware setup</i>
</p>

<p align="center">
  <img src="src/content/post/myosa-forest-sentinel/setup.png" width="800"><br/>
  <i>MYOSA-based Forest Sentinel hardware setup</i>
</p>

<p align="center">
  <img src="src/content/post/myosa-forest-sentinel/dashboard_1.png" width="800"><br/>
  <i>System Idle during daytime</i>
</p>

<p align="center">
  <img src="src/content/post/myosa-forest-sentinel/dashboard_2.png" width="800"><br/>
  <i>System Monitoring</i>
</p>

<p align="center">
  <img src="src/content/post/myosa-forest-sentinel/dashboard_3.png" width="800"><br/>
  <i>Intrusion Detected</i>
</p>

### Videos

<video controls width="100%">
  <source src="src/content/post/myosa-forest-sentinel/demo.mp4" type="video/mp4">
</video>

## Features (Detailed)

### 1. Context-Aware Night-Time Operation
Forest Sentinel remains inactive during daytime conditions and automatically transitions to an active monitoring state
during night-time based on ambient light levels. This significantly reduces unnecessary power consumption while 
maintaining continuous situational awareness after dark.

### 2. Event-Driven Vibration and Proximity Monitoring
During night-time operation, the system passively monitors ground vibrations and proximity changes. These sensors act as
early indicators of nearby movement, allowing the system to remain idle until meaningful environmental activity is
detected.

### 3. Artificial Light–Triggered Intrusion Confirmation
The presence of vibration and proximity activity places the system in a heightened monitoring state. An intrusion event
is confirmed only when a sudden increase in light intensity, such as from a flashlight or torch is detected. This final
event acts as a decisive trigger, minimizing false alarms caused by animals or natural disturbances.

### 4. Alert Generation and Multi-Modal Notification
Upon intrusion confirmation, the system immediately activates an audible buzzer to alert nearby forest officials. The
intrusion status is simultaneously displayed on the MYOSA OLED screen and logged on the monitoring dashboard, enabling
officials to quickly verify and respond to the event.

## Usage Instructions

1. Power the MYOSA board using a USB cable or power bank
2. Plug in the required sensors using the MYOSA cascade slots
3. Upload the firmware to the MYOSA board
4. Monitor system status and intrusion alerts on the OLED display and dashboard

To upload the firmware using PlatformIO:
```plaintext
platformio run --target upload
```

## Tech Stack

### Hardware
- ESP32 motherboard1
- APDS9960 proximity and light sensor
- SW420 vibration sensor
- OLED display
- Buzzer

### Firmware
- C++ (Arduino framework)
- PlatformIO development environment
- Embedded sensor libraries compatible with the MYOSA platform

### Interface
- Web-based dashboard (HTML)

## Requirements / Installation

- MYOSA motherboard with supported sensors
- USB cable or power bank for power supply
- PlatformIO development environment (optional, for firmware modification)

The system operates out-of-the-box using the preloaded firmware. Firmware customization,
if required, can be done using PlatformIO or the Arduino IDE

## 🗂 File Structure
```
/myosa-forest-sentinel
├─ myosa-forest-sentinel.md
├─ cover.png
├─ blockdiagram.png
├─ setup.png
├─ dashboard_1.png
├─ dashboard_2.png
├─ dashboard_3.png
└─ demo.mp4
```
## License

MIT License

## Contribution Notes

Contributions and improvements are welcome.







