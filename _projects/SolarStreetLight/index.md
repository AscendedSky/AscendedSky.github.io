---
layout: post
title: "Solar-Powered Street Light"
description: "Designed an off-grid solar-powered street lighting system, including schematic design, illuminance modelling for luminaire and regulator selection, and power budgeting. Built and tested a stripboard prototype, involving soldering, debugging, and validation of system operation."
skills:
  - Electronics
  - Solar Power Systems
  - Circuit Design
  - Illuminance Modelling
  - Power Budgeting
  - Control Systems
  - Soldering
  - Debugging
main-image: "/Stripboard.jpg"
date: 2024-11-30
---
### More information
My role in this project involved the end-to-end design of an off-grid solar-powered street lighting system, followed by prototype implementation and testing.

The project began with the design of the street light system architecture, including selection of the LED luminaire, solar panel, battery capacity, and voltage regulation stages. Illuminance modelling was performed to evaluate light coverage and ensure compliance with the required lux levels over the target road area. These simulations guided the selection of streetlights  and operating points while balancing efficiency and coverage.

{% include image-gallery.html images="simulation.png" height="400" %}
<span style="font-size: 14px">Illuminance Modelling – Light Coverage and Lux Distribution</span>

Based on the lighting requirements, a power budget analysis was conducted to size the solar panel and battery, ensuring the system could operate for up to two nights without sunlight. Following this, the complete street light schematic was designed, incorporating regulation, control, and load stages.

{% include image-gallery.html images="streetlight.png" height="400" %}
<span style="font-size: 14px">System Schematic – Solar-Powered Street Light</span>

A physical prototype was then designed and constructed on stripboard, including the voltage regulation circuitry which was a boost converter and a discrete LED array representative of the final luminaire. The build process involved manual soldering, layout planning for current handling, and verification of all electrical connections.
{% include image-gallery.html images="boostconverter.png" height="400" %}
<span style="font-size: 14px">Prototype Schematic</span>
{% include image-gallery.html images="Stripboard.jpg" height="400" %}
<span style="font-size: 14px">Hardware Prototype</span>
