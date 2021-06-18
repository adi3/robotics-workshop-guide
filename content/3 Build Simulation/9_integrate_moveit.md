+++
title = "Integrate MoveIt"
weight = 390
chapter = true
pre = "9. "
+++

# Integrate MoveIt

1. Open the _main.launch_ file located at the following path.

```c
aws_ws -> src -> robomaker_workshop -> launch -> main.launch
```

2. Add the following code snippet under **STEP 5** of _main.launch_. Then hit save.

```
<include file="$(find interbotix_xsarm_moveit)/launch/move_group.launch">
    <arg name="robot_model" value="$(arg robot_model)"/>
    <arg name="dof" value="$(arg dof)"/>
</include>
```

3. Press **Ctrl+C** to shut down the running ROS application. Then relaunch it. The robot arm will appear in its default upright position.

```
roslaunch robomaker_workshop main.launch
```

4. Open a new terminal tab and execute the **init.py** script.

```
python ~/environment/aws_ws/src/robomaker_workshop/scripts/init.py
```

5. Head over to the virtual desktop. The simulated arm will become animated and move to its _sleep_ position.

![Init Arm](/init-arm.gif?classes=border)

---

The same effect can be achieved by running the python script automatically on application launch.

6. Add the following code snippet under **STEP 6** of _main.launch_.

```
<node pkg="robomaker_workshop" name="init" type="init.py" output="screen" />
```

7. Run the ROS application.

```
roslaunch robomaker_workshop main.launch
```

8. Check out the Gazebo window and you will see the arm once again curl up as previously to its _sleep_ position.

---

> We can thus run arbitrary python scripts to interact with a robot both during application launch and after the application is already up and running.
