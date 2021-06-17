+++
title = "Run application on robot"
weight = 650
chapter = true
pre = "5. "
+++

```
git clone https://github.com/adi3/robomaker_workshop.git --branch completed --single-branch ~/aws_ws/src/robomaker_workshop
```

cd ~/aws_ws
catkin build
source devel/setup.bash

roslaunch robomaker_workshop main.launch sim:=false

...switch off camera stream...
..take manual image from ROS..

image should be saved to /scripts path as image_cap.png
`fswebcam -r 640x480 --png image_cap.png`

specify image...
..switch on camera stream..
..execute main.py
