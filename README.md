# Task-4-ROS
1Install the necessary packages
sudo apt-get install ros-noetic-turtlesim
2Create a single script to launch everything:

Create a file named start_turtle.sh
touch start_turtle.sh
chmod +x start_turtle.sh

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

3 Run the script

