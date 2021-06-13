+++
title = "Initiate simulation world"
weight = 33
chapter = true
pre = "2. "
+++

# Initiate simulation world

1. Add the following code snippet under **STEP 1** of _main.launch_.

```
<include file="$(find gazebo_ros)/launch/empty_world.launch">
    <arg name="world_name" value="$(arg world_name)"/>
</include>
```

2. Run the ROS application.

```
roslaunch robomaker_workshop main.launch
```

3. Go to the virtual desktop to view our Gazebo world.

![Gazebo World](/gazebo-world.png?classes=border)

You should see a black table with a few colorful coins on it. Take a few moments to familiarize yourself with the Gazebo GUI and the various options it offers.
