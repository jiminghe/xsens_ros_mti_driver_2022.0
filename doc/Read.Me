# Xsens MTi driver for ROS
## Introduction
The Xsens MTi driver enables the use of Xsens MTi devices with ROS. In this document, we will give you a brief overview of this driver and instructions about how to use it in your ROS-based application.

## Overview

The workflow of Xsens MTi driver is shown in the figure below:

[![N|Solid](xsens_mti_driver.png)](https://nodesource.com/products/nsolid)

MTi node only receives data from an MTi device and publishes it to ROS, it isn't capable of configuring a device. To configure an MTi you can either use MT Manager, Xsens Device API (XDA), Low Level Communication Protocol or by extending MTi node.

The Xsens MTi driver uses Public Xsens Device API for scanning, connecting, packet parsing and log file handling. The implemention of this driver is done in C/C++, so you can build and run it on a different platforms. You can also configure an MTi using Public XDA by extending XdaInterface class, for more information about how to do that have a look at our 'Public XDA receive data example'.

## Requirements
- MTSDK from Xsens MT Software Suite 2022.0
- ROS Kinetic or Melodic
- C/C++ Compiler: GCC 5.4.0 or MSVC 14.0
- C++11

## Building the Xsens MTi node
1. Copy xsens_ros_mti_driver folder from your MT SDK directory into your catkin workspace 'src' folder. Make sure the permissions are set to o+rw on your files and directories. For details on creating a catkin workspace environment refer to Creating a catkin ws.
2. Build xspublic from your catkin workspace:
```sh
$ pushd src/xsens_ros_mti_driver/lib/xspublic && make && popd 
```
3. Build Xsens MTi driver package:
```sh
$ catkin_make 
```
4. Source workspace:
```sh
$ source devel/setup.bash 
```

## Running the Xsens MTi node
1. Configure your MTi device to output desired data (e.g. for display example - orientation output)
2. Launch the Xsens MTi driver from your catkin workspace:
 Display example (orientation data should be enabled):
```sh
$ roslaunch xsens_mti_driver display.launch 
```
Simple example:
 ```sh
$ roslaunch xsens_mti_driver example.launch 
```


## Running the Xsens MTi node
To change the configuration of the Xsens MTi node you can edit the xsens_mti_node.yaml file. Following parameters can be configured:
- Device settings for finding a defined MTi device
- Log file recording option
- Publishers queue size
- Message publishers

## Published topics
- imu/data (sensor_msgs/Imu)
orientation, angular velocity and linear acceleration
- imu/acceleration (geometry_msgs/Vector3Stamped)
acceleration
- imu/angular_velocity (geometry_msgs/Vector3Stamped)
angular velocity
- imu/mag (geometry_msgs/Vector3Stamped)
magnetic field
- imu/dq (geometry_msgs/QuaternionStamped)
quaternion from device
- imu/dv (geometry_msgs/Vector3Stamped)
linear acceleration from device
- imu/time_ref (sensor_msgs/TimeReference)
timestamp from device
- filter/quaternion (geometry_msgs/QuaternionStamped)
quaternion from filter
- filter/free_acceleration (geometry_msgs/Vector3Stamped)
linear acceleration from filter
- filter/twist (geometry_msgs/TwistStamped)
velocity and angular velocity
- filter/positionlla (geometry_msgs/Vector3Stamped)
filtered position output in latitude (x), longitude (y) and altitude (z) as Vector3
- filter/velocity (geometry_msgs/Vector3Stamped)
filtered velocity output as Vector3
- temperature (sensor_msgs/Temperature)
temperature from device
- pressure (sensor_msgs/FluidPressure)
pressure from device
- gnss (sensor_msgs/NavSatFix)
latitude, longitude, altitude and status
tf (geometry_msgs/TransformStamped)
- transformed orientation

## Troubleshooting
**The MTi-1 (Motion Tracker Development Board) is not recognized.**
Support for the Development Board is present in recent kernels. (Since June 12, 2015). If your kernel does not support the Board, you can add this manually:
 ```sh
$ sudo /sbin/modprobe ftdi_sio
$ echo 2639 0300 | sudo tee /sys/bus/usb-serial/drivers/ftdi_sio/new_id 
```

**The device is recognized, but I cannot ever access the device.**
Make sure you are in the correct group (often dialout or uucp) in order to access the device. You can test this with:
 ```sh
$ ls -l /dev/ttyUSB0
crw-rw---- 1 root dialout 188, 0 May  6 16:21 /dev/ttyUSB0
$ groups
dialout audio video usb users plugdev 
```

If you aren't in the correct group, you can fix this in two ways:
1. Add yourself to the correct group. You can add yourself to it by using your distributions user management tool, or call:
 ```sh
$ sudo usermod -G dialout -a $USER 
```
2. Be sure to replace dialout with the actual group name if it is different. After adding yourself to the group, either relogin to your user, or add the current terminal session to the group:
 ```sh
$ newgrp dialout 
```
3. Use udev rules. Alternatively, put the following rule into /etc/udev/rules.d/99-custom.rules:
 ```sh
$ SUBSYSTEM=="tty", ATTRS{idVendor}=="2639", ACTION=="add", GROUP="$GROUP", MODE="0660" 
```
Change $GROUP into your desired group (e.g. adm, plugdev, or usb).

**The device is inaccessible for a while after plugging it in.**
When having problems with the device being busy the first 20 seconds after plugin, purge the modemmanager application.


**RViz doesn't show an MTi model.**
It is a known issue with urdfdom in ROS Melodic. A workaround is to unset/modify the LC_NUMERIC environment variable:
 ```sh
$ LC_NUMERIC="en_US.UTF-8" 
```

## Questions?
We are always ready to help with any questions you might have! Check our Knowledge base for immediate answers to the most common questions, search or post on our community forum, or request technical support.
