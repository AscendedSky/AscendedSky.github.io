---
layout: post
title: "STM32 Microcontroller Game & IIR Filter Implementation"
description: "Developed a real-time STM32-based game system with interrupt-driven input handling and peripheral coordination, alongside an optimized 10th-order IIR filter implemented in assembly, achieving over 75% reduction in execution cycles compared to a C implementation."
skills:
  - Embedded Systems
  - STM32
  - ARM Assembly
  - Digital Signal Processing
  - Optimization
main-image: "/oled.jpg"
date: 2025-11-30
---
### More details
> Check out the code in this [repository](https://github.com/AscendedSky/EE2028/tree/main).

My role in this project involved the design and implementation of a real-time embedded system on an STM32 microcontroller, combining interactive game logic with a highly optimized digital signal processing component.

The project began with the development of a microcontroller-based game framework, coordinating multiple on-chip peripherals using the STM32 HAL. System configuration included setup of the system clock, GPIO, ADC, timers, DMA, UART, and I²C interfaces. Hardware timers (TIM16/TIM17) were used to drive deterministic tasks such as LED blinking and buzzer toggling, while sensor data was periodically sampled and monitored.

{% include image-gallery.html images="STM32.jpg" height="350" %}
<span style="font-size: 14px">STM32 Microcontroller Setup</span>

User input handling was implemented using GPIO interrupts, with custom logic to detect single presses as well as rapid and slow double-press events. These inputs were used to switch between games or replay the current game state. To avoid blocking execution, DMA-based UART communication was configured to transmit environmental status updates asynchronously.

The system also interfaced with an OLED display over I²C, providing real-time visual feedback for game state and system information.

{% include image-gallery.html images="oled.jpg" height="350" %}
<span style="font-size: 14px">OLED Display Output</span>

In parallel with the game logic, a 10th-order IIR digital filter was implemented directly in ARM assembly. The filter design focused on performance optimization through the use of circular buffers, modular indexing, and register reuse to minimize memory access. Efficient arithmetic operations were implemented using MLA/MLS instructions, enabling scalable circular indexing and reducing instruction count.

Compared to an equivalent C implementation, the optimized assembly version achieved a greater than 75% reduction in execution cycles, significantly improving real-time performance and demonstrating effective low-level optimization techniques.
