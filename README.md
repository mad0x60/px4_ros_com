# px4_ros_com

[![GitHub license](https://img.shields.io/github/license/PX4/px4_ros_com.svg)](https://github.com/PX4/px4_ros_com/blob/master/LICENSE) [![GitHub (pre-)release](https://img.shields.io/github/release-pre/PX4/px4_ros_com.svg)](https://github.com/PX4/px4_ros_com/releases/tag/beta) [![DOI](https://zenodo.org/badge/142936318.svg)](https://zenodo.org/badge/latestdoi/142936318) [![Build Status](https://travis-ci.com/PX4/px4_ros_com.svg?token=wyo8gnJf2urtswRL6tUy&branch=master)](https://travis-ci.com/PX4/px4_ros_com)

This package materializes the PX4-FastRTPS bridge, with an interface between the PX4 autopilot stack, ROS2 and ROS1 (from now on, referenced as ROS) over [`ros1_bridge`](https://github.com/ros2/ros1_bridge). It has a straight dependency on the [`px4_msgs`](https://github.com/PX4/px4_msgs) package, as it depedends on the ROS interfaces and ROS msgs to generate the micro-RTPS bridge and also build the example nodes.

The package is divided into two different branches:

1. The [`master`](https://github.com/PX4/px4_ros_com/tree/master) branch composes the required Cmake modules and build structure to generate the ROS2 message headers and source files, which are then used and propagated on the RTPS DDS layer;
2. The [`ros1`](https://github.com/PX4/px4_ros_com/tree/ros1) branch is a product of the `master` branch and its purpose is also generate the ROS message headers and source files, but to use on the ROS side. The interface between the ROS2 and ROS is possible through the [`ros1_bridge`](https://github.com/ros2/ros1_bridge).

## Install, build and usage

Check the [RTPS/ROS2 Interface](https://dev.px4.io/en/middleware/micrortps.html) section on the PX4 Devguide for details on how to install the required dependencies, build the package (composed by the two branches) and use them.

## Bug tracking and feature requests

Use the [Issues](https://github.com/PX4/px4_ros_com/issues) section to create a new issue. Report your issue or feature request [here](https://github.com/PX4/px4_ros_com/issues/new).

## Questions and troubleshooting

Reach the PX4 development team on the `#messaging` PX4 Slack channel:
[![Slack](https://px4-slack.herokuapp.com/badge.svg)](http://slack.px4.io)
