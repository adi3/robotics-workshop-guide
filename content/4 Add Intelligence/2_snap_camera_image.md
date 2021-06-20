+++
title = "Snap image from camera"
weight = 420
chapter = true
pre = "2. "
+++

# Snap image from camera

1. Launch the ROS application if it is not already running.

```
roslaunch robomaker_workshop main.launch
```

2. In a new terminal tab, call the ROS service in charge of capturing an image.

```
rosservice call /image_saver/save
```

3. A snap of the camera stream will appear in the _/images_ directory with the name **image_cap.png**.

```
ls ~/environment/aws_ws/src/robomaker_workshop/images/
```

---

Double-click on the file to view the image in Cloud9.

![Camera stream snap](/stream-snap.png?classes=border)
