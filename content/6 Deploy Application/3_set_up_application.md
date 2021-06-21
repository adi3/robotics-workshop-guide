+++
title = "Set up ROS application"
weight = 630
chapter = true
pre = "3. "
+++

# Set up ROS application

1. Fetch and build the finished application to the remote robot.

```
git clone https://github.com/adi3/robomaker_workshop.git --branch completed --single-branch ~/environment/aws_ws/src/robomaker_workshop

cd ~/environment/aws_ws

catkin build

source devel/setup.bash
```

2. Open the _main.py_ script in a command-line editor.

```
nano ~/environment/aws_ws/src/robomaker_workshop/scripts/main.py
```

3. Set the **REAL_MODEL_ARN** constant in _main.py_ as the model ARN you copied at the end of the last section.

![Real Model](/real-model.png?classes=border)

> Press **Ctrl+O** followed by **Enter** to save a file in the _nano_ editor. Press **Ctrl+X** to exit the application.

---

5. Configure your AWS credentials on the robot. These will be used by the ROS application to access your Rekognition model.

```
aws configure
```

![Configure Robot](/configure-robot.png?classes=border)

---

> A nifty way of testing your AWS credentials setup is by confirming that S3 buckets can be successfully listed by the terminal.

```
aws s3 ls
```
