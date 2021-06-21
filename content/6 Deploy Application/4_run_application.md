+++
title = "Run application on robot"
weight = 640
chapter = true
pre = "4. "
+++

# Run application on robot

1. Confirm that the robot's camera is switched **off** by opening the cameras panel. If the camera is still streaming, hit the toggle switch on the right to turn it off.

![Turn Off Camera](/turn-off-camera.png?classes=border)

> By default, a video device can only be used by one application at a time. We temporarily turn off the camera in Botworks so that it can be used by the image capturing service in our ROS application.

---

2. Capture a top-view image of the robot's environment using the _Overhead Cam_.

```
fswebcam -r 640x480 --png 9 --no-banner ~/environment/aws_ws/src/robomaker_workshop/images/image_cap.png
```

3. A snap of the camera stream will appear in the _/images_ directory with the name **image_cap.png**.

```
ls ~/environment/aws_ws/src/robomaker_workshop/images/
```

4. Turn the camera back on using the same toggle switch as earlier.

![Turn On Camera](/turn-on-camera.png?classes=border)

5. Launch the ROS application, this time with a `sim:=false` flag since we are working on the physical device.

```
roslaunch robomaker_workshop main.launch sim:=false &
```

> We start this script in the background by specifying the `&` flag so that we can use the same terminal window to execute the following steps as well.

---

6. Run the _main.py_ script. Press Enter as prompted by the terminal.

```
python ~/environment/aws_ws/src/robomaker_workshop/scripts/main.py --internal
```

> The `--internal` flag tells the script that the Rekognition model exists in your own AWS account and not in an external one as it did for the simulation exercise.

---

You should see the robot arm start moving in the livestream and attempt to fetch the coins around it. Modify and re-run the script till you have picked up all the coins!

---

7. Kill the background _roslaunch_ process once you are finished working on the robot.

```
ps u | grep roslaunch | awk 'NR==1{print $2}' | xargs kill
```
