---
layout: post
title: "ESP32-based Battery Monitoring and Stepper Control (Ongoing)"
description: "Ongoing development of a PCB integrating battery monitoring and stepper motor control. The design uses an ESP32C3 microcontroller, a BMS IC for voltage and current sensing, and a PCB-built RF antenna for testing small-form-factor Wi-Fi/BLE communication. The project is currently in the schematic capture phase, focusing on initial circuit design and component selection."
skills:
  - Electrical Design
  - PCB Design
  - Microcontroller Integration
  - Power Management
  - Wireless Communication
  - Schematic Capture

main-image: "/partial_schematic.png"
---

### More Details

This project focuses on developing a PCB capable of monitoring battery parameters and controlling stepper motors. The design is based on the ESP32C3 MCU, chosen for its low power consumption, integrated Wi-Fi/BLE, and compact form factor. A BMS IC is used to measure both voltage and current, providing real-time battery telemetry. The PCB also includes a built-in RF antenna for small-form-factor Wi-Fi and BLE testing. This board is being developed for a Mars Rover GNSS and Communications team project where our overarching goal is to create autonomous mechanically steerable antennas.  

{% include image-gallery.html images="partial_schematic.png" height="650"%}
<span style="font-size: 14px">Partially completed schematic of the ESP32C3-based PCB showing BMS IC, USB-C, and built-in RF antenna</span>

The schematic is still in development, with component selection, signal routing, and integration of the stepper motor drivers ongoing. Future work will include PCB layout, testing of the RF antenna, and validation of battery monitoring functionality.
