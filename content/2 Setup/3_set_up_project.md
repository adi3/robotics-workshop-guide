+++
title = "Set up ROS project"
weight = 230
chapter = true
pre = "3. "
+++

# Set up ROS project

1. Fetch and run the setup script for configure your ROS workspace.

```
curl https://raw.githubusercontent.com/adi3/robomaker_workshop/master/setup.sh > setup.sh

source setup.sh
```

While the environment is being readied, let us learn a little about the [Robot Operating System](/setup/4_robot_os/), often abbreviated as ROS.

---

2. Click on **Virtual Desktop** at the top, then select **Launch Virtual Desktop** to open up the Ubuntu desktop GUI.

![Virtual Desktop](/virtual-desktop.png?classes=border)

3. Launch the ROS application, and confirm that it runs without errors. No GUI is expected to appear yet.

```
roslaunch robomaker_workshop main.launch
```

---

> The starter code for our ROS application is now all set up and ready for our changes. Explore application topography by looking at output from the following commands:

```
rostopic list

rosnode list

rosparam list
```
