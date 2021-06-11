+++
title = "Integrate planning toolkit"
weight = 500
chapter = false
+++

1. Add the following code snippet under **STEP 5** of _main.launch_.

```
<include file="$(find interbotix_xsarm_moveit)/launch/move_group.launch">
    <arg name="robot_model" value="$(arg robot_model)"/>
    <arg name="dof" value="$(arg dof)"/>
</include>
```

2. Run the ROS application. No GUI changes are expected at this point.

```
roslaunch robomaker_workshop main.launch
```

3. Confirm that the planning interface has been succesfully set up.

```
rostopic list | grep move_group
```

About twenty new ROS topics should have been set up by MoveIt to allow for motion planning.

![MoveIt Topics](/moveit-topics.png?classes=border)

4. Interestingly, MoveIt adds a large number of key-value pairs to the ROS Parameter Server. These are used by MoveIt algorithms for planning and executing trajectories with a robot.

```
rosparam list | grep move_group
```

Well over a hundred ROS parameters should now be printed in the terminal. You do not need to understand these parameters for the purposes of this workshop.

![MoveIt Params](/moveit-params.png?classes=border)
