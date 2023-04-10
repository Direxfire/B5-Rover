B5 Rover Controls System

This repository contains the code for the controls system of the B5 Rover, developed by EGEN 310 Team B5. The controls system is built using ROS2.
Overview

The controls system consists of several ROS2 nodes that communicate with each other to control the rover's movement and actions. The main nodes are:

    b5_driver: This node interfaces with the hardware of the rover (such as motors, sensors, etc.) and provides a ROS2 interface for controlling them.
    b5_navigation: This node implements the navigation system for the rover, allowing it to move to specified locations and avoid obstacles.
    b5_manipulation: This node controls the manipulator arm of the rover, allowing it to perform tasks such as picking up objects.
    b5_gui: This node provides a graphical user interface (GUI) for controlling the rover.

Hardware

The B5 Rover is equipped with the following hardware components:

    Drive Motors: The B5 Rover uses two 228:1 Pololu Plastic Offset motors for propulsion.
    Motor Driver: The motor driver for the B5 Rover is an OSEPP TB6112 Motor Driver, controlled by an Arduino UNO R3.
    ROS2 Controller: The main ROS2 controller on board the B5 Rover is a Raspberry Pi 4 B+.

Installation

To install the B5 Rover controls system, follow these steps:

Clone this repository to your local machine.
    Install ROS2 (if you haven't already) by following the instructions on the ROS2 installation page.
Build the code using the colcon build system by running the following command in the root of the repository:

colcon build

    Source the setup file by running the following command:

bash

source install/setup.bash

Usage

To run the B5 Rover controls system, follow these steps:

Connect the hardware of the rover to your machine.

    Launch the b5_driver node by running the following command:

ros2 launch b5_driver b5_driver_launch.py

    Launch the b5_navigation node by running the following command:

ros2 launch b5_navigation b5_navigation_launch.py

    Launch the b5_manipulation node by running the following command:

ros2 launch b5_manipulation b5_manipulation_launch.py

    Launch the b5_gui node by running the following command:

ros2 launch b5_gui b5_gui_launch.py

License

This code is licensed under the MIT License. See the LICENSE file for more details.
Contributors

    Drew Currie (Electrical Engineer)
    Sam Clyncke (Mechanical Engineer)
    Ryan Dowdy (Chemical Engineer)
    Calvin Servheen (Industrial Engineer)

Acknowledgments

    ROS2 - Robot Operating System
    OpenCV - Open Source Computer Vision Library
