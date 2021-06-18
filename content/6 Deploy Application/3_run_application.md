+++
title = "Run application on robot"
weight = 630
chapter = true
pre = "3. "
+++

# Run application on robot

1. Fetch and build the finished application to the remote robot.

```
git clone https://github.com/adi3/robomaker_workshop.git --branch completed --single-branch ~/aws_ws/src/robomaker_workshop

cd ~/aws_ws

catkin build

source devel/setup.bash
```

2. Launch the ROS application, this time with a `sim:=false` flag since we are working on the physical device.

```
roslaunch robomaker_workshop main.launch sim:=false
```

...switch off camera stream...
..take manual image from ROS..

image should be saved to /scripts path as image_cap.png
`fswebcam -r 640x480 --png 9 image_cap.png`

specify image...
..switch on camera stream..
..execute main.py
