10cm x 10cm structure for all electronic modules, can be stacked, electronics system for [Open Robotic Platform](https://openroboticplatform.com/) [orp 10x10](https://easyeda.com/editor#id=b403f122191b47ddaedabcfa5c958d17) all modules available for purchase from upstream vendors or Electronz

**SBC**
[Avaota](https://pine64.com/product/yuzuki-avaota-a1-single-board-computer-4gb-32gb/)
Orin nano for those that need it

**Microcontroller**
v1 [S3](https://www.olimex.com/Products/IoT/ESP32-S3/ESP32-S3-DevKit-Lipo/open-source-hardware)
v2 [P4](https://oshwhub.com/tiny-development-board-studio/wt9932p4-tiny-2) 10cmx10cm carrier with [canbus](https://wiki.seeedstudio.com/xiao-can-bus-expansion/) to be developed

[MCP23017 Expansion if needed](https://learn.adafruit.com/adafruit-mcp23017-i2c-gpio-expander/overview)
[Expansion and relay if needed](https://www.olimex.com/Products/Modules/IO/MOD-IO/open-source-hardware)

**Motor drivers**
Canbus control, handle encoders locally

Brushless/ Brushed
[RP2350](https://github.com/sequoia-hope/rp2350-motor-controller)

Brushed
[Vnh7040](https://oshwhub.com/hezi/vnh7040-v1)
[Carrier](https://easyeda.com/editor#id=640f514fb8e94284a5564d27022b1241) 
[Demir firmware](https://github.com/dsm/demir_firmware) Make it talk RP2350 canbus


[Meta carrier](https://easyeda.com/editor#id=!a8b7ed53f554478da1b66d16b2d54550|b0f557ea608b423eaac4b90f4e69ec9f) for VNH7049 or RP2035 modules to be routed, incorporates [MJbot switch](https://mjbots.com/products/mjpower-ss)


**Power**
36v Sodium ION

[isolated stepdown](https://pro.easyeda.com/editor#id=255049bcb74545bfafbd2995b33272fb,tab=*4d8477bf67e0429a955038099f58c3df@255049bcb74545bfafbd2995b33272fb) - complete ordered for testing

[Additional distro](https://oshwhub.com/moonfeather/modulized_distributor)


**Firmware**
[Lizard](https://lizard.dev/)  to be added: RP2350 Canbus profile, 

**RTK**
[Sparkfun F9P](https://www.sparkfun.com/sparkfun-gps-rtk2-board-zed-f9p-qwiic-gps-15136.html)

**ROS/ ROSYS**

[Basekit ROS](https://github.com/zauberzeug/basekit_ros) to be added F9P support [stereo-mono-RTK-fusion](https://github.com/Agroecology-Lab/gnss-stereo-inertial-fusion) rebase against [Lincoln LCAS ROS](https://github.com/LCAS/rosdistro)

[Rosys/Field friend](https://github.com/Agroecology-Lab/field_friend) - Needs F9P





