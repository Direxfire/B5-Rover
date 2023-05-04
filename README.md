<h1>B5 Rover Controls System</h1>

This repository contains the code for the controls system of the B5 Rover, developed by EGEN 310 Team B5. The controls system is built using ROS2.
Overview

The controls system consists of several ROS2 nodes that communicate with each other to control the rover's movement and actions. The main nodes are:

    b5_driver: This node interfaces with the hardware of the rover (such as motors, sensors, etc.) and provides a ROS2 interface for controlling them.
    b5_navigation: This node implements the navigation system for the rover, allowing it to move to specified locations and avoid obstacles.
    b5_manipulation: This node controls the manipulator arm of the rover, allowing it to move the camera.
    b5_gui: This node provides a graphical user interface (GUI) for controlling the rover.

**Hardware**

The B5 Rover is equipped with the following hardware components:

    Drive Motors: The B5 Rover uses four 228:1 Pololu Plastic Offset motors for propulsion. 
        https://www.pololu.com/product/1118
    Motor Driver: The motor driver for the B5 Rover is an OSEPP TB6112 Motor Driver, controlled by an Arduino UNO R3. 
        https://www.osepp.com/electronic-modules/shields/120-motor-shield-6612
    ROS2 Controller: The main ROS2 controller on board the B5 Rover is a Raspberry Pi 4 B+.

**Installation**

To install the B5 Rover controls system, follow these steps:

Clone this repository to your local machine.
    Install ROS2 (if you haven't already) by following the instructions on the ROS2 installation page.
Build the code using the colcon build system by running the following command in the root of the repository:

    colcon build

Source the setup file by running the following command:


    source install/setup.bash
    


**Usage**

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


**RViz**

RViz files are used to render the collision and visual models of the rover in RViz2 this allows for testing of the controls, collision, and sensors without need for testing on the actual robot. This is a useful tool for mocking up the rover to do basic modeling and testing. This has allowed me to continue to work on the controls system without need for a finalized rover design.   
**To-Do**

- [x] Sync Raspberry Pi and Dev Computer with GitHub
- [x] Create a ROS2 arduino Serial Bridge 
- [x] Create a PWM motor driver signal on Arduino
- [x] Test battery power management
- [x] Test motor current draw
- [x] Design Battery holder
- [x] Design Electronics mount  
- [x] Model rover in Rviz
- [x] Render model in Gazebo (Gazebo Ignition)
- [x] Impliment controls system with keyboard in Gazebo
- [x] Impliment X-Box controls system in Gazebo
- [ ] Finalize ROS2 Arduino Motor Control --See Articulated Robotics
- [ ] Add delight to the experience when all tasks are complete :tada:


**License**

This code is licensed under the MIT License. See the LICENSE file for more details.

**Contributors**

    Drew Currie (Electrical Engineer)
    Sam Clyncke (Mechanical Engineer)
    Ryan Dowdy (Chemical Engineer)
    Calvin Servheen (Industrial Engineer)

**Acknowledgments**

    ROS2 - Robot Operating System
    OpenCV - Open Source Computer Vision Library
    Josh Newans - ROS2 community contributor and creator of the template this project was built on 
        [Josh Newans]([url](https://articulatedrobotics.xyz/))
