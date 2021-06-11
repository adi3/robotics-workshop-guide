+++
title = "Obtain physical coordinates"
weight = 400
chapter = false
+++

1. Add the following code snippet under **STEP 4** of _main.py_.

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

2. Run the _main.py_ script in simulation mode. Press Enter as prompted by the script.

```
python main.py --sim
```

You will now see the physical XY-coordinates of the coin's location relative to the center of the table. These coordinates are measured in meters.

![Physical coordinates](/coordinates.png?classes=border)

---

The robot can now be informed of locations on the table that it needs to move to for collecting the coins.
