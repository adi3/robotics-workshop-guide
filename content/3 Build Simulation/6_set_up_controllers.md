+++
title = "Set up controllers"
weight = 360
chapter = true
pre = "6. "
+++

# Set up controllers

1. Add the following code snippet under **STEP 3** of _main.launch_.

```
<rosparam command="load" file="$(find robomaker_workshop)/config/controllers.yaml" />

<node pkg="controller_manager" name="controller" type="controller_manager" respawn="false" output="screen"
    args="spawn arm_controller gripper_controller joint_state_controller" />
```

2. Press **Ctrl+C** to shut down the running ROS application. Then relaunch it.

```
roslaunch robomaker_workshop main.launch
```

3. Confirm that the interface for executing robot control has been successfully set up. Around two dozen ROS topics spawned by the _controller_manager_ package should appear in the output.

```
rostopic list | grep controller
```

![Controller Topics](/controller-topics.png?classes=border)

4. Our Gazebo simulation will now show torques being applied to the virtual robot arm.

![Torqued Arm](/torqued-arm.png?classes=border)
