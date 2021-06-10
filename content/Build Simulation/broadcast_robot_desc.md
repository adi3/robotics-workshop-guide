+++
title = "Broadcast robot description"
date = 2021-05-03T13:44:16-05:00
weight = 100
chapter = false
+++

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

You should see some XML output printed in the terminal that describes the form-factor and physics of the robot.

![Robot Description](/robot-desc.png?classes=border)