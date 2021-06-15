+++
title = "Broadcast robot description"
weight = 340
chapter = true
pre = "4. "
+++

# Broadcast robot description

1. Add the following code snippet under **STEP 2** of _main.launch_.

```
<param name="robot_description"
    command="xacro $(find robomaker_workshop)/urdf/$(arg robot_model).urdf.xacro" />

<node name="robot_state_publisher" pkg="robot_state_publisher" type="robot_state_publisher" />

<node pkg="gazebo_ros" name="urdf_spawner" type="spawn_model" respawn="false" output="screen"
    args="-urdf -model $(arg robot_model) -param robot_description -x $(arg x_offset) -z $(arg table_height)" />
```

2. Press **Ctrl+C** to shut down the running ROS application. Then relaunch it.

```
roslaunch robomaker_workshop main.launch
```

3. Go to the virtual desktop and confirm that the robot arm appears in the simulated world.

![Simulated Arm](/sim-arm.png?classes=border)

---

> You can check out the raw robot information being broadcasted by printing the associated ROS parameter. This parameter holds the XML output describing the form-factor and physics of the robot.

```
rosparam get -p /robot_description
```

![Robot Description](/robot-desc.png?classes=border)
