+++
title = "Command robot to fetch"
weight = 460
chapter = true
pre = "6. "
+++

# Command robot to fetch

1. Open the _main.py_ file located at the following path:

```c
aws_ws -> src -> robomaker_workshop -> scripts -> main.py
```

2. Add the following code snippet under **STEP 4** of _main.py_. Then hit save.

```
for name, position in coins.items():
    robot.home()
    robot.open_gripper()

    x = position[0]
    y = position[1]

    rospy.loginfo("Picking up %s..." % name)
    success = robot.pick(x, y)
    if success:
        robot.deposit()

rospy.loginfo("No more coins. Going to sleep...")
robot.sleep()
```

---

> Python is senstitive to identation so make sure that the tabs and spaces in your code _exactly_ match the code shown here.

---

3. Run the _main.py_ script in simulation mode.

```
python ~/environment/aws_ws/src/robomaker_workshop/scripts/main.py --sim
```

The simulated robot arm will calculate an appropriate trajectory for moving to a coin's location, pick up the coin, and deposit it at a pre-defined location. The robot will do this for each of the coins found in the previous steps.

![Robot fetching coins](/robot-fetching.gif?classes=border)

---

> In case the robot is unable to grasp the coin in its first attempt, simply rerun the script. Since our machine learning model is built to handle dynamic scenarios, the coin will be accurately located even if it has been randomly nudged around by the robot arm during previous attempts.
