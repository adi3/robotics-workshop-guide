+++
title = "Snap image from camera"
weight = 200
chapter = true
pre = "3. "
+++

# Snap image from camera

1. Add the following code snippet under **STEP 7** of _main.launch_.

```
<node name="image_saver" pkg="image_view" type="image_saver" output="screen">
    <remap from="image" to="camera/image_raw" />
    <param name="save_all_image" value="false" />
    <param name="filename_format" value="$(find robomaker_workshop)/scripts/image_%04d.png" />
</node>
```

2. Press **Ctrl+C** to shut down the running ROS application. Then relaunch it.

```
roslaunch robomaker_workshop main.launch
```

3. Now add the following code snippet under **STEP 2** of _main.py_.

```
rospy.logwarn('Press Enter to snap image from ROS topic')
raw_input()

image = util.snap_image()
if image == None:
    rospy.logerr('Trouble snapping image from ROS topic')
    return

rospy.loginfo('Snapped image from local camera stream: %s' % image)
```

4. Run the _main.py_ script in simulation mode. Press Enter as prompted by the script.

```
python ~/environment/aws_ws/src/robomaker_workshop/scripts/main.py --sim
```

5. The terminal output will confirm that an image has been snapped.

```
[INFO] [1623013252.228023, 667.865000]: Snapped image from local camera stream: image_0000.png
```

---

A snap of the camera stream should have appeared in your _/scripts_ directory. Double-click on the file to view the image.

![Camera stream snap](/stream-snap.png?classes=border)
