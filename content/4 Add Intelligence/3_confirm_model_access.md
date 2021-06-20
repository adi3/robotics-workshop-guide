+++
title = "Confirm model access"
weight = 430
chapter = true
pre = "3. "
+++

# Confirm model access

1. Open the _main.py_ file located at the following path:

```c
aws_ws -> src -> robomaker_workshop -> scripts -> main.py
```

2. Add the following code snippet under **STEP 1** of _main.py_. Then hit save.

```
rospy.loginfo("Checking state of Rekognition model...")
status = util.model_status(project_name, model_name, access_profile)

rospy.loginfo('Current model state: %s' % status)
if status != 'RUNNING':
    rospy.logerr('Rekognition model needs to be in RUNNING state')
```

---

> Python is senstitive to identation so make sure that the tabs and spaces in your code _exactly_ match the code shown here.

---

3. Make sure the ROS application is running. Otherwise launch it now.

```
roslaunch robomaker_workshop main.launch
```

4. Open a new terminal tab and run the _main.py_ script in simulation mode.

```
python ~/environment/aws_ws/src/robomaker_workshop/scripts/main.py --sim
```

The terminal output should report the current model to be in the _RUNNING_ state.

```
[INFO] [1623011969.371301, 0.000000]: Checking state of Rekognition model...
[INFO] [1623011969.626026, 1734.312000]: Current model state: RUNNING
```

---

> Ask your presenter in case you are shown an _AccessDenied_ error or if you find that the model is not running.
