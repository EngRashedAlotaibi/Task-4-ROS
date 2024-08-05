# Task-4-ROS
Install the necessary packages (if not already installed):

sh

sudo apt-get install ros-noetic-turtlesim
Create a single script to launch everything:

Create a file named start_turtle.sh:

sh

touch start_turtle.sh
chmod +x start_turtle.sh
Edit start_turtle.sh to include the following content:

sh

#!/bin/bash
# Source ROS setup

source /opt/ros/noetic/setup.bash

source ~/catkin_ws/devel/setup.bash


# Start roscore

gnome-terminal -- bash -c "roscore" &


# Wait for roscore to start

sleep 2

# Start turtlesim node

gnome-terminal -- bash -c "rosrun turtlesim turtlesim_node" &


# Start turtle teleop key

gnome-terminal -- bash -c "rosrun turtlesim turtle_teleop_key"

FInally run the script



