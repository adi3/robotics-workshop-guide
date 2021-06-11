+++
title = "Test robot movement"
weight = 600
chapter = false
+++

1. Add the following code snippet under **STEP 6** of _main.launch_.

```
<node pkg="robomaker_workshop" name="init" type="init.py" output="screen" />
```

2. Run the ROS application.

```
roslaunch robomaker_workshop main.launch
```

3. Check out the Gazebo window. The simulated arm should become animated and move to its _sleep_ position.

![Init Arm](/init-arm.gif?classes=border)

The same effect can be achieved by running the python script independently of the launch file.

4. Comment out the code added under **Step 6** of _main.launch_.

```
<!-- <node pkg="robomaker_workshop" name="init" type="init.py" output="screen" /> -->
```

5. Run the application again. The robot arm will appear in its default upright position.

```
roslaunch robomaker_workshop main.launch
```

6. Now execute the **init.py** script from the _/scripts_ folder.

```
cd ~/environment/aws_ws/src/robomaker_workshop/scripts

python init.py
```

Head over to the virtual desktop and you will see the arm once again curl up as previously to its _sleep_ position.

---

Before proceeding, remember to add back the init node statement in the launch file. We will start all our robot operations from this _sleep_ position from now on.
