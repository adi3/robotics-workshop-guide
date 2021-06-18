+++
title = "Obtain physical coordinates"
weight = 450
chapter = true
pre = "5. "
+++

# Obtain physical coordinates

1. Open the _main.py_ file located at the following path.

```c
aws_ws -> src -> robomaker_workshop -> scripts -> main.py
```

2. Add the following code snippet under **STEP 3** of _main.py_. Then hit save.

```python
rospy.logwarn("Press Enter to transform coin positions into physical coordinates")
raw_input()

rospy.loginfo('Transforming pixels to physical coordinates...' % len(labels))
coins = {}

for l in labels:
    name = l['Name']
    x, y = util.get_coin_position(l['Geometry']['BoundingBox'])
    rospy.loginfo(name)
    rospy.loginfo('\tX: ' + str(x))
    rospy.loginfo('\tY: ' + str(y))
    coins[name] = [x, y]
```

3. Run the _main.py_ script in simulation mode. Press Enter as prompted by the script.

```
python ~/environment/aws_ws/src/robomaker_workshop/scripts/main.py --sim
```

4. You will now see the physical XY-coordinates of the coin's location relative to the center of the table. These coordinates are measured in meters.

![Physical coordinates](/coordinates.png?classes=border)

---

> The robot can now be informed of locations on the table that it needs to move to for collecting the coins.
