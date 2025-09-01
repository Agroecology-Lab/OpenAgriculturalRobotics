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
An open-source agricultural robotics platform integrating FarmBot-ROS, Linorobot2 hardware, and edge AI capabilities for field applications

# Core Packages

### Open Agricultural Robotics _interfaces

### farmbot-ros-trailblazer 

### farmbot-ros-coverage planner

### farmbot-ros-polestar 
robot localization 

### Linrobot2 hardware 
Provides base hardware abstraction, sensor integration, and already bundles Nav2 (localisation, mapping, planning).


# APIs & Message Types

| Topic            | Message Type                                | Publisher                         | Subscriber(s)                          | Purpose                                |
| ---------------- | ------------------------------------------- | --------------------------------- | -------------------------------------- | -------------------------------------- |
| `/cmd_vel`       | `geometry_msgs/Twist`                       | farmbot-ros task planner          | Linorobot2 motor controller            | Robot motion commands                  |
| `/joint_states`  | `sensor_msgs/JointState`                    | Linorobot2 HW drivers             | farmbot-ros, state estimator           | Robot arm/joint positions              |
| `/tool_control`  | `std_msgs/String` or custom                 | farmbot-ros task planner          | Tool actuator drivers                  | Activate tools (e.g. seeder, weeder)   |
| `/planting_task` | `std_msgs/String` or custom                 | farmbot-ros scheduler             | farmbot-ros execution engine           | High-level task sequencing             |
| `/sensor_data`   | `sensor_msgs/Imu`, `std_msgs/Float32`, etc. | Linorobot2 sensors                | farmbot-ros analytics, AGRARIAN uplink | Soil moisture, temp, other IoT sensors |
| `/gps/fix`       | `sensor_msgs/NavSatFix`                     | ZED-F9P GNSS                      | farmbot-ros navigation, AGRARIAN cloud | GNSS position (RTK-corrected)          |
| `/navsat/odom`   | `nav_msgs/Odometry`                         | ZED-F9P GNSS + farmbot-ros fusion | Navigation stack                       | Robot localization                     |
| `/logs`          | `std_msgs/String`                           | ROS2 logger                       | NB-IoT uplink → AGRARIAN Testbed 3     | System diagnostics                     |
| `/status`        | `std_msgs/String`                           | farmbot-ros                       | AGRARIAN Testbed 3 dashboard           | High-level system status               |


# CANbus message formats

# Installing the containers 

# Micro-rover hardware

# Rover hardware



