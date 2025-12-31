---
layout: post
title: "Arduino Power Management Shield"
description: "Design and PCB implementation of a custom Arduino Uno shield for distributing 12 V and 5 V power. The shield powers the Arduino and two high-power LEDs while meeting mechanical, layout, and efficiency requirements."
skills:
  - PCB Design
  - Schematic Capture
  - Power Electronics

main-image: "/PCB.png"
---
### More Details

In this project, I designed a custom Arduino Uno shield to handle power distribution for both the Arduino board and two high-power LEDs, while being atleast 90% efficient. The shield receives a 12 V DC input, regulates part of it to 5 V for the Arduino, and supplies 12 V directly to the LEDs, while providing sufficient current for all components.

The design process began by creating the schematic, including the four pin headers required to connect the shield to the Arduino Uno. The schematic captures all key components for voltage regulation and LED power delivery.

{% include image-gallery.html images="Schematic.png" height="550"%}
<span style="font-size: 14px">Schematic showing 12 V input, 5 V regulation, and LED connections</span>

Next, I designed the PCB layout on a single top layer, keeping components aligned with the Arduino header pins and maintaining a standard board thickness of approximately 62 mils. High-current traces were routed to support the LEDs, and care was taken to fit all components within the fixed footprint of the shield.

{% include image-gallery.html images="PCB.png" height="500"%}
<span style="font-size: 14px">Top-layer PCB layout of the Arduino power shield</span>

