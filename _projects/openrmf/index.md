---
layout: post
title: "Open-RMF Multi-Robot Coordination & Edge Coverage Based Goal Assignment"
description: "Developed a multi-robot coordination framework using Open-RMF middleware, integrating simulation, hardware adapters, and goal selection algorithms to optimize fleet navigation and task efficiency."
skills:
  - ROS2
  - Open-RMF
  - Navigation 2
  - Bash
  - Ubuntu 24.04
  - Embedded Systems
  - Simulations
  - Python
  - C++
  - XML
  - Computer-Vision Control Loops
main-image: "/sim_map.jpg"
date: 2025-11-30
---

### More details
> Check out the code in this [repository](https://github.com/edic-nus/OPEN-RMF/tree/main).

This project explored multi-robot coordination using Open-RMF middleware, combining simulation, experimental testing, and hardware integration to improve fleet navigation and task assignment. The workflow began with building accurate Gazebo simulations of the EDIC building, enabling safe and repeatable testing of coordination strategies and autonomous navigation behaviors.

{% include image-gallery.html images="merged.png" height="400" %}
<span style="font-size: 14px">Gazebo simulation of the 2nd floor in the EDIC E2A building at NUS</span>

To enable coordinated multi-robot operation for edge-coverage tasks, a modular system architecture was designed that integrates core software nodes, sensors, and hardware interfaces. Maps—either randomly generated or designed using the Traffic Editor—are converted into NetworkX graph representations for processing by the goal selection algorithm, which assigns tasks across the robot fleet. Open-RMF handles route planning, conflict resolution, and lane management, while Navigation 2 executes robot-level control to reach designated waypoints.  

Robots dynamically respond to obstacles using local costmaps: detected obstacles are published to a lane closure topic, ensuring that both Open-RMF and the goal selection algorithm avoid blocked edges. Battery management is automated through a dispatcher node, which submits a charge request when a robot’s battery is low. The Nav2 docking server then autonomously aligns the robot to the charger using AprilTag detection, achieving precise docking with minimal supervision.

{% include image-gallery.html images="architecture.png" height="400" %}
<span style="font-size: 14px">System architecture for multi-robot edge-coverage</span>

Goal Assignment and Edge-Coverage

A novel goal selection algorithm was implemented to optimize active edge coverage on graph maps, reducing exploration time by efficiently assigning tasks and avoiding redundant traversal. Simulation results on randomly generated graphs confirmed that this approach outperforms baseline frontier-based strategies, providing measurable efficiency gains in multi-robot coordination.

{% include image-gallery.html images="random_graph.png, Result.png" height="400" %}
<span style="font-size: 14px">Edge coverage results and an example random graph generated for goal selection</span>

### Hardware Integration

Beyond simulations, an ESP32-based door adapter was built to enable Wi-Fi-controlled actuation at 10–20 Hz with sub-300 ms latency. This hardware interface demonstrates the seamless interaction of real-world devices with the Open-RMF system, bridging the gap between software planning and physical execution.

{% include image-gallery.html images="esp32.png" height="400" %}
<span style="font-size: 14px">ESP32 door adapter integrated with Open-RMF workflows</span>

