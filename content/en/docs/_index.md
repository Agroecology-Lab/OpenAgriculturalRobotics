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

### [ublox_dgnss](https://github.com/aussierobots/ublox_dgnss)
UBLOX UBX messaging, for ZED-X20P, ZED-F9P and ZED-F9R devices. 

### [farmbot-ros-trailblazer](https://github.com/Agroecology-Lab/farmbot_planner)
Coverage planner

### [farmbot-ros-pathfinder](https://github.com/farmbot-ros/pathfinder/tree/develop/src)
Navigation planner

### [farmbot-ros-drivecore](https://github.com/Agroecology-Lab/farmbot_controller)
Defines a control system that predicts and optimizes the vehicle's trajectory over a finite time horizon

### [Linrobot2 hardware](https://github.com/rosmo-robot/linorobot2_hardware/tree/master)
Provides base hardware abstraction, sensor & motor driver integration, and already bundles Nav2 (localisation, mapping, planning).


#  Message Types

| Publisher Node              | Topic                     | Message Type                     | Description                            |
| --------------------------- | ------------------------- | -------------------------------- | -------------------------------------- |
| **ublox\_dgnss**            | `/ublox_dgnss/fix`        | `sensor_msgs/msg/NavSatFix`      | GNSS position data.                    |
|                             | `/ublox_dgnss/imu`        | `sensor_msgs/msg/Imu`            | IMU orientation and acceleration.      |
| **farmbot-ros-polestar**    | `/polestar/pose`          | `geometry_msgs/msg/PoseStamped`  | Refined robot pose estimate.           |
|                             | `/polestar/odometry`      | `nav_msgs/msg/Odometry`          | Fused odometry (GNSS + IMU).           |
| **farmbot-ros-trailblazer** | `/trailblazer/coverage`   | `geometry_msgs/msg/PoseArray`    | Coverage path waypoints for the field. |
| **farmbot-ros-pathfinder**  | `/pathfinder/trajectory`  | `geometry_msgs/msg/PoseArray`    | Planned trajectory to follow.          |
| **farmbot-ros-drivecore**   | `/drivecore/commands`     | `std_msgs/msg/Float64MultiArray` | Low-level motor commands.              |
| **linorobot2\_hardware**    | `/linrobot2/odometry`     | `nav_msgs/msg/Odometry`          | Odometry from wheels/encoders.         |
|                             | `/linrobot2/imu`          | `sensor_msgs/msg/Imu`            | IMU data from onboard sensors.         |
|                             | `/linrobot2/joint_states` | `sensor_msgs/msg/JointState`     | Joint positions / wheel angles.        |


| Subscriber Node             | Topic                    | Message Type                     | Purpose                                                       |
| --------------------------- | ------------------------ | -------------------------------- | ------------------------------------------------------------- |
| **farmbot-ros-polestar**    | `/ublox_dgnss/fix`       | `sensor_msgs/msg/NavSatFix`      | Uses GNSS data for pose estimation.                           |
|                             | `/ublox_dgnss/imu`       | `sensor_msgs/msg/Imu`            | Optional: fuses IMU data with GNSS.                           |
| **farmbot-ros-trailblazer** | `/polestar/pose`         | `geometry_msgs/msg/PoseStamped`  | Uses current pose to generate coverage paths.                 |
|                             | `/polestar/odometry`     | `nav_msgs/msg/Odometry`          | Optional: alternative to pose if using odometry.              |
|                             | `/ublox_dgnss/fix`       | `sensor_msgs/msg/NavSatFix`      | Optional: if Polestar is skipped, reads raw GNSS directly.    |
| **farmbot-ros-pathfinder**  | `/trailblazer/coverage`  | `geometry_msgs/msg/PoseArray`    | Receives coverage waypoints from planner.                     |
|                             | `/polestar/pose`         | `geometry_msgs/msg/PoseStamped`  | Uses pose for trajectory execution.                           |
|                             | `/polestar/odometry`     | `nav_msgs/msg/Odometry`          | Optional: improves trajectory following accuracy.             |
| **farmbot-ros-drivecore**   | `/pathfinder/trajectory` | `geometry_msgs/msg/PoseArray`    | Receives planned trajectories to convert into motor commands. |
| **linorobot2\_hardware**    | `/drivecore/commands`    | `std_msgs/msg/Float64MultiArray` | Executes low-level motor commands.                            |


# CANbus message formats

# Installing the containers 

# Micro-rover hardware

# Rover hardware



