+++
title = "Draw bounding boxes"
weight = 200
chapter = false
+++

1. Add the following code snippet under **STEP 2** of _main.py_.

```
rospy.logwarn('Press Enter to snap image from ROS topic')
raw_input()

image = util.snap_image()
if image == None:
    rospy.logerr('Trouble snapping image from ROS topic')
    return

rospy.loginfo('Snapped image from local camera stream: %s' % image)
```

2. Run the _main.py_ script in simulation mode. Press Enter as prompted by the script.

```
python main.py --sim
```

The terminal output will confirm that an image has been snapped.

```
[INFO] [1623013252.228023, 667.865000]: Snapped image from local camera stream: image_0000.png
```

---

A snap of the camera stream should have appeared in your _/scripts_ directory. Double-click on the file to view the image.

![Camera stream snap](/stream-snap.png?classes=border)
