+++
title = "Visualize robot data"
weight = 40
chapter = true
pre = "7. "
+++

# Visualize robot data

1. Add the following code snippet under **STEP 4** of _main.launch_.

```
<node name="rviz" pkg="rviz" type="rviz" respawn="false" output="screen"
    args="-f world -d $(find robomaker_workshop)/rviz/px100.rviz">
</node>
```

2. Press **Ctrl+C** to shut down the running ROS application. Then relaunch it.

```
roslaunch robomaker_workshop main.launch
```

3. The RViz GUI should appear on the virtual desktop. Take a few moments to explore its various components, and get an understanding of how RViz shows the camera livestream from our simulated Gazebo world.

![RViz GUI](/rviz.png?classes=border)
