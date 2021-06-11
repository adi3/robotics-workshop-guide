+++
title = "Set up robot controllers"
date = 2021-05-03T13:44:16-05:00
weight = 300
chapter = false
+++

1. Add the following code snippet under **STEP 3** of _main.launch_.

```
<rosparam command="load"
    file="$(find robomaker_workshop)/config/controllers.yaml">
</rosparam>

<node pkg="controller_manager"
    name="controller"
    type="controller_manager"
    respawn="false"
    output="screen"
    args="spawn arm_controller gripper_controller joint_state_controller">
</node>
```

2. Run the ROS application. No GUI changes are expected at this point.

```
roslaunch robomaker_workshop main.launch
```

3. Confirm that the interface for executing robot control has been successfully set up.

```
rostopic list | grep controller
```

More than two dozen ROS topics spawned by the _controller_manager_ package should appear in the output.

![Controller Topics](/controller-topics.png?classes=border)

4. Our Gazebo simulation will now show torques being applied to the virtual robot arm.

![Torqued Arm](/torqued-arm.png?classes=border)