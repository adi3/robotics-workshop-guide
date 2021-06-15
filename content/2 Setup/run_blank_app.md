+++
title = "Run blank application"
weight = 50
chapter = false
hidden = true
+++

1. Install catkin build tools.

```
sudo apt update

sudo apt install python-catkin-tools -y
```

2. Build the ROS project.

```
cd ~/environment/aws_ws

catkin build

source devel/setup.bash
```

3. Click on **Virtual Desktop** at the top, then select **Launch Virtual Desktop** to open up the Ubuntu desktop GUI.

![Virtual Desktop](/virtual-desktop.png?classes=border)

4. Launch the ROS application, and confirm that it runs without errors. No GUI is expected to appear yet.

```
roslaunch robomaker_workshop main.launch
```

---

The starter code for our ROS application is now all set up and ready for our changes. Explore application topography by looking at output from the following commands:

```
rostopic list

rosnode list

rosparam list
```
