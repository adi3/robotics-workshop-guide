+++
title = "Visualize robot data"
weight = 370
chapter = true
pre = "7. "
+++

# Visualize robot data

1. Open the _main.launch_ file located at the following path.

```c
aws_ws -> src -> robomaker_workshop -> launch -> main.launch
```

2. Add the following code snippet under **STEP 4** of _main.launch_. Then hit save.

```
<node name="rviz" pkg="rviz" type="rviz" respawn="false" output="screen"
    args="-f world -d $(find robomaker_workshop)/rviz/px100.rviz">
</node>
```

3. Press **Ctrl+C** to shut down the running ROS application. Then relaunch it.

```
roslaunch robomaker_workshop main.launch
```

4. The RViz GUI should appear on the virtual desktop.

![RViz GUI](/rviz.png?classes=border)

---

> Pay special attention to the camera livestream of our simulated Gazebo world that shows up in Rviz.
