+++
title = "Connect to remote robot"
weight = 620
chapter = true
pre = "2. "
+++

# Connect to remote robot

Only one user may connect to a robot at a time.

---

1. Click on an available slot against your team's assigned robot to reserve yourself time on the hardware. You can drag your mouse to book multiple successive slots at once.

![Reserve Slot](/reserve-slot.png?classes=border)

> Make sure the current time falls between the start and end times of your booking. You can only connect to the robot when your booking window starts.

2. Hover on your reservation to view details of the booking. Click on **Start Session** in the pop-up window.

![Start Session](/start-session.png?classes=border)

3. You will be connected to the robot and an in-browser terminal will open up that gives you admin access to the robot.

![Robot Session](/robot-session.png?classes=border)

From this terminal window, you can execute any command and carry out any ROS development as you would if the robot was sitting next to you.

---

> If your terminal window seems stuck after printing a single `$` sign as shown below, click on **View Cameras** and ensure that the camera livestream is turned off. Then restart your session. Inform the presenters in case the problem still persists.
> ![Stuck Session](/stuck-session.png?classes=border)

---

4. Click on **View Cameras** on the left. An on-site camera associated with the robot will be displayed under _Available Cameras_. Click on the toggle switch next to the camera.

![View Cameras](/view-cameras.png?classes=border)

5. A low-latency livestream from the camera will be started. You can toggle the camera on and off through its switch at your will.

![Camera Stream](/camera-stream.png?classes=border)

6. In case the camera view presents a blank window for more than 10 seconds, click on the camera's toggle switch _twice_ to restart the camera. This usually fixes the livestream. Always give the livestream a few seconds to go live before attempting to refresh it.

---

> If the camera window remains blank even after troubleshooting, inform the presenters and they will hard-reset the camera connection for you.

---

7. Confirm that you are able to control the robot by executing a sample script on the hardware.

```
roslaunch interbotix_xsarm_control xsarm_control.launch robot_model:=px100 use_rviz:=false &

python ~/Desktop/random_dance.py
```

![Random Dance](/random-dance.gif?classes=border)

The robot should become animated and attempt to reach randomly generated waypoints in an infinite loop. Press **Ctrl+C** in the terminal window to stop the script.
