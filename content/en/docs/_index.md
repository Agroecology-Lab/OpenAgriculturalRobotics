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

Documenting two open hardware platforms, a small development rover and a full scale ag rover.

# Core ROS2 Packages

### ublox_dgnss
UBLOX UBX messaging, for ZED-X20P, ZED-F9P and ZED-F9R devices. 

### [farmbot-ros-polestar](https://github.com/farmbot-ros/polestar)
robot localization 

### [farmbot-ros-trailblazer](https://github.com/Agroecology-Lab/farmbot_planner)
Coverage planner

### [farmbot-ros-pathfinder](https://github.com/farmbot-ros/pathfinder/tree/develop/src)
Navigation planner

### [farmbot-ros-drivecore](https://github.com/Agroecology-Lab/farmbot_controller)
Defines a control system that predicts and optimizes the vehicle's trajectory over a finite time horizon

### [Linrobot2 hardware](https://github.com/rosmo-robot/linorobot2_hardware/tree/master)
Provides base hardware abstraction, sensor & motor driver integration, and already bundles Nav2 (localisation, mapping, planning).

### [flexbe](https://github.com/flexbe) 
FlexBE is a high-level behavior engine coordinating the capabilities of a robot in order to solve complex tasks. Behaviors are modeled as hierarchical state machines (HFSM)

### [flexible_behavior_trees](https://github.com/FlexBE/flexible_behavior_trees)
The FlexBE state implementations send goals to the BT server to load and execute a BT with and without a user defined goal. FlexBE orchestrates the execution of different BTs while the BehaviorTree.CPP framework executes the BTs and passes data between nodes and BTs.


#  Message Types

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



