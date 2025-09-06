---
title : "Docs"
description: "Docs Doks."
lead: ""
date: 2020-10-06T08:48:23+00:00
lastmod: 2020-10-06T08:48:23+00:00
draft: false
images: []
---

## Getting Started
An open-source agricultural robotics platform integrating key software projects into a coherent containerised stack.

Documenting two open hardware platforms running the stack, a small development rover and a full scale ag rover.

# Core ROS2 Packages

### [Linrobot2 hardware](https://github.com/rosmo-robot/linorobot2_hardware/tree/master)
Provides base hardware abstraction, sensor & motor driver integration, and already bundles Nav2 (localisation, mapping, planning).

### [ublox_dgnss](https://github.com/aussierobots/ublox_dgnss)
UBLOX UBX messaging, for ZED-X20P, ZED-F9P and ZED-F9R devices.

### [Flexible Navigation](https://github.com/FlexBE/flexible_navigation)

### [Flexbe behaviour tree](https://github.com/FlexBE/flexible_behavior_trees)


#  ROS2 Message Types

| Publisher Node              | Topic                     | Message Type                     | Description                            |
| --------------------------- | ------------------------- | -------------------------------- | -------------------------------------- |
| **ublox\_dgnss**            | `/ublox_dgnss/fix`        | `sensor_msgs/msg/NavSatFix`      | GNSS position data.                    |
|                             | `/ublox_dgnss/imu`        | `sensor_msgs/msg/Imu`            | IMU orientation and acceleration.      |
| **linorobot2\_hardware**    | `/linrobot2/odometry`     | `nav_msgs/msg/Odometry`          | Odometry from wheels/encoders.         |
|                             | `/linrobot2/imu`          | `sensor_msgs/msg/Imu`            | IMU data from onboard sensors.         |
|                             | `/linrobot2/joint_states` | `sensor_msgs/msg/JointState`     | Joint positions / wheel angles.        |


# CANbus message formats

[OpenCyphal](https://opencyphal.org/)

# Micro-rover development hardware

### Electronics

| Components                | Description                               | Quantity |
| ------------------------- | ----------------------------------------- | -------- |
| Olimex [iMX8MP-SOM-4GB-IND](https://www.olimex.com/Products/SOM/NXP-iMX8/iMX8MP-SOM-4GB-IND/open-source-hardware) with [carrier](https://www.olimex.com/Products/SOM/NXP-iMX8/iMX8MP-SOM-EVB-IND/open-source-hardware): |   A powerful System-on-Module (SoM) featuring a quad-core Arm Cortex-A53 processor, Cortex-M7 real-time core, 4GB LPDDR4 RAM, and a 2.3 TOPS Neural Processing Unit (NPU). It supports mainline Linux and operates in an industrial-grade temperature range of -20°C to +85°C.   | 2       |
|[Adafruit Metro RP2350](https://www.adafruit.com/product/6003): |A microcontroller board featuring the RP2350 chip, offering dual-core processing capabilities, ample GPIO pins, and support for various peripherals.| 1 |
|Waveshare [Canbus shield](https://wiki.seeedstudio.com/CAN-BUS_Shield_V2.0/)|1|
|Sparkfun [GNSS/RTK](https://www.sparkfun.com/sparkfun-gnss-rtk-l1-l5-breakout-neo-f9p-qwiic.html)|2|


# Full size Rover hardware

Skid steer 4x4 rover

# Electronics 
As above from Micro-rover

### Mechanical


| Components                | Description                               | Quantity |
| ------------------------- | ----------------------------------------- | -------- |
|  SimpleFOC canbus drivers |  [RP2350](https://github.com/sequoia-hope/rp2350-motor-controller)    | 2       |
|  500w electric wheel   |    [wheelbarrow wheel with ag tyre](https://www.aliexpress.com/item/1005009662727177.html)   |   4   |
| Suspension              |   [Fatbike fork](https://www.aliexpress.com/item/1005005666919971.html?)    | 4       |
|    Chassis structure      |          | many       |
|  Chassis connections      | 33.7 [keeclamp aluminum](https://www.scaffolding-direct.co.uk/aluminium-90-degree-crossover-33-7mm-kee-lite-l45-6/)   | Many      |






