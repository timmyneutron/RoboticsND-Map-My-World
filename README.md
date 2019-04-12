# Udacity Robotics Nanodegree
# Project #4: Map My World

![Screenshot](img/screenshot.jpg)

## Introduction
This is a project for Udacity's Robotics NanoDegree. It's a robot that uses a Hokuyo laser scanner and RGBD camera to perform simultaneous localization and mapping (SLAM).

## Concepts and Classes
Concepts explored in this project:

  - Simultaneous Localization and Mapping
  - ROS RTAB-Map package

## Getting Started
To view this project, you must have Gazebo and ROS installed on Linux.

[Click here for Gazebo download and installation instructions](http://gazebosim.org).

[Click here for ROS installation instructions](http://wiki.ros.org/ROS/Installation).

To begin, several ROS packages need to be installed as dependencies:

```
$ sudo apt-get update && sudo apt-get upgrade -y
$ sudo apt-get install ros-kinetic-teleop-twist-keyboard
```

With the dependencies installed, download/clone the repository, navigate up to the root level directory, and execute:

```
$ catkin_make
$ source devel/setup.bash
$ roslaunch my_robot world.launch
```


To operate the robot via the keyboard, open a second terminal, navigate to the root level directory, and execute:

```
$ source devel/setup.bash
$ rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```

You can then command the robot to move using the keys indicated by the teleop node.

Finally, to run SLAM, open a third terminal, navigate to the root level directory, and execute:

```
$ source devel/setup.bash
$ roslaunch my_robot mapping.launch
```

As you move the robot around, RTAB-Map will build a map of the room. When you terminate the mapping window, the map will be saved as a  database file in the launch folder. To view the map, execute:

```
$ rtabmap-databaseViewer src/my_robot/launch/rtabmap.db
```

Click "yes" when asked about database parameters, and then select "Constraint View" and "Graph View" from the View menu.
