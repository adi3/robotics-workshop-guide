+++
title = "Initiate simulation world"
weight = 320
chapter = true
pre = "2. "
+++

# Initiate simulation world

1. Open the _main.launch_ file located at the following path.

```c
aws_ws -> src -> robomaker_workshop -> launch -> main.launch
```

2. Add the following code snippet under **STEP 1** of _main.launch_. Then hit save.

```
<include file="$(find gazebo_ros)/launch/empty_world.launch">
    <arg name="world_name" value="$(arg world_name)"/>
</include>
```

3. Press **Ctrl+C** to shut down the running ROS application. Then run it again.

```
roslaunch robomaker_workshop main.launch
```

4. Go to the virtual desktop to view our Gazebo world.

![Gazebo World](/gazebo-world.png?classes=border)

You should see a black table with a few colorful coins on it. Take a few moments to familiarize yourself with the Gazebo GUI and the various options it offers.
