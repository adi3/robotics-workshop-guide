+++
title = "Integrate MoveIt"
weight = 43
chapter = true
pre = "9. "
+++

# Integrate MoveIt

1. Add the following code snippet under **STEP 5** of _main.launch_.

```
<include file="$(find interbotix_xsarm_moveit)/launch/move_group.launch">
    <arg name="robot_model" value="$(arg robot_model)"/>
    <arg name="dof" value="$(arg dof)"/>
</include>
```

2. Press **Ctrl+C** to shut down the running ROS application. Then relaunch it. The robot arm will appear in its default upright position.

```
roslaunch robomaker_workshop main.launch
```

3. Open a new terminal tab and execute the **init.py** script.

```
python ~/environment/aws_ws/src/robomaker_workshop/scripts/init.py
```

4. Head over to the virtual desktop. The simulated arm will become animated and move to its _sleep_ position.

![Init Arm](/init-arm.gif?classes=border)

---

The same effect can be achieved by running the python script automatically on application launch.

5. Add the following code snippet under **STEP 6** of _main.launch_.

```
<node pkg="robomaker_workshop" name="init" type="init.py" output="screen" />
```

6. Run the ROS application.

```
roslaunch robomaker_workshop main.launch
```

7. Check out the Gazebo window and you will see the arm once again curl up as previously to its _sleep_ position.

---

> We can thus run arbitrary python scripts to interact with a robot both during application launch and after the application is already up and running.
