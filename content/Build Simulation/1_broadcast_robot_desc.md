+++
title = "Broadcast robot description"
weight = 31
chapter = true
pre = "1. "
+++

# Broadcast robot description

1. Add the following code snippet under **STEP 1** of _main.launch_.

```
<param name="robot_description"
    command="xacro $(find robomaker_workshop)/urdf/$(arg robot_model).urdf.xacro">
</param>

<node name="robot_state_publisher"
    pkg="robot_state_publisher"
    type="robot_state_publisher">
</node>
```

2. Run the ROS application.

```
roslaunch robomaker_workshop main.launch
```

3. Confirm robot information is being published.

```
rosparam get -p /robot_description
```

4. You will see some XML output printed in the terminal that describes the form-factor and physics of the robot.

![Robot Description](/robot-desc.png?classes=border)
