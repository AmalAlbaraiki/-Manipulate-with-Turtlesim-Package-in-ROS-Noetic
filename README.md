# -Manipulate-with-Turtlesim-Package-in-ROS-Noetic



Introduction

In this task, the goal is to manipulate the turtlesim package in ROS Noetic. The turtlesim package is a simple simulator that allows users to control a virtual turtle in a graphical window. It is often used for learning the basic concepts of ROS, including topics such as publishers, subscribers, and services. In this report, I will demonstrate how to set up and control the turtlesim node using ROS Noetic.
Installation

To start using the turtlesim package, we first need to ensure that it is installed. The following command installs the package in ROS Noetic:

sudo apt-get install ros-noetic-turtlesim

This installs the necessary files and dependencies for using the turtlesim package in ROS Noetic.

Running the Turtlesim Node

Once the package is installed, we can run the turtlesim_node by using the following command:

rosrun turtlesim turtlesim_node

This command will start the turtlesim_node, which opens a graphical window with a turtle.



Manipulating the Turtle

After launching the turtlesim_node, you can control the turtle using the turtle_teleop_key node. This allows you to manipulate the turtle using the keyboard.
To launch the teleoperation node, use the following command:

rosrun turtlesim turtle_teleop_key

This opens a terminal where you can use the arrow keys to move the turtle:

•	The up arrow (↑) moves the turtle forward.

•	The down arrow (↓) moves the turtle backward.

•	The left arrow (←) turns the turtle to the left.

•	The right arrow (→) turns the turtle to the right.

Understanding the ROS Nodes and Topics

The turtlesim package operates using ROS nodes and topics. The main node is the turtlesim_node, which controls the graphical simulation. The turtle_teleop_key node subscribes to the keyboard input and publishes velocity commands to move the turtle.
To check the available topics, use the following command:

rostopic list

You should see topics like:

•	/turtle1/pose – Publishes the turtle's position.

•	/turtle1/cmd_vel – Receives velocity commands for movement.

To check the current pose of the turtle, you can use:

rostopic echo /turtle1/pose

This will display information such as the position (x, y), orientation (theta), and velocity of the turtle.

Conclusion

The turtlesim package in ROS Noetic provides a simple and effective way to get started with ROS. It helps users understand the basic concepts of ROS communication, such as publishing and subscribing to topics, as well as controlling a virtual entity in a graphical interface. By manipulating the turtle, users can practice using ROS commands and learn how to interact with ROS nodes and topics.

References

•	ROS Noetic Documentation: https://www.ros.org/

•	Turtlesim Package Documentation: ROS Wiki Turtlesim


![لقطة شاشة 2025-02-08 172840](https://github.com/user-attachments/assets/6a38ceee-c296-46f6-a9d4-19a108ec4d9e)
