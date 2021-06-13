+++
title = "Confirm model access"
weight = 54
chapter = true
pre = "2. "
+++

# Confirm model access

1. Add the following code snippet under **STEP 1** of _main.py_.

```
rospy.loginfo("Checking state of Rekognition model...")
status = util.model_status(ARN_BASE + PROJECT_ID, model_name, MODEL_ACCESS_PROFILE)

rospy.loginfo('Current model state: %s' % status)
if status != 'RUNNING':
    rospy.logerr('Rekognition model needs to be in RUNNING state')
    return
```

2. Make sure the ROS application is running. Otherwise launch it now.

```
roslaunch robomaker_workshop main.launch
```

3. Open a new terminal tab and run the _main.py_ script in simnulation mode.

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
