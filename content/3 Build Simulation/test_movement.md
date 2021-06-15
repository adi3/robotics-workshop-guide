+++
title = "Test robot movement"
weight = 600
chapter = false
hidden = true
+++

2. Add the following code snippet under **STEP 6** of _main.launch_.

```
<node pkg="robomaker_workshop" name="init" type="init.py" output="screen" />
```

3. Run the ROS application.

```
roslaunch robomaker_workshop main.launch
```

4. Check out the Gazebo window. The simulated arm should become animated and move to its _sleep_ position.

![Init Arm](/init-arm.gif?classes=border)

The same effect can be achieved by running the python script independently of the launch file.

5. Comment out the code added under **Step 6** of _main.launch_.

```
<!-- <node pkg="robomaker_workshop" name="init" type="init.py" output="screen" /> -->
```

6. Run the application again. The robot arm will appear in its default upright position.

```
roslaunch robomaker_workshop main.launch
```

7. Now execute the **init.py** script from the _/scripts_ folder.

```
cd ~/environment/aws_ws/src/robomaker_workshop/scripts

python init.py
```

Head over to the virtual desktop and you will see the arm once again curl up as previously to its _sleep_ position.

---

Before proceeding, remember to add back the init node statement in the launch file. We will start all our robot operations from this _sleep_ position from now on.

<!-- The application will now run **init.py** as part of its launch process. -->

<!-- 3. Confirm that the planning interface has been succesfully set up.

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

![MoveIt Params](/moveit-params.png?classes=border) -->
