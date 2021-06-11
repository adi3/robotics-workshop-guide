+++
title = "Set up ROS project"
weight = 40
chapter = false
+++

1. Create a workspace for the ROS project in our Cloud9 IDE.

```
mkdir -p ~/environment/aws_ws/src/

cd aws_ws/src
```

2. Download starter code for our ROS application from GitHub.

```
git clone https://github.com/adi3/robomaker_workshop
```

3. Install package dependencies. This step will take several minutes to complete.

```
cd ~/environment/aws_ws

rosdep install --from-paths src --ignore-src --rosdistro melodic -r -y
```

4. Set up Interbotix robot arm modules. Type `no` when prompted to set up the perception pipeline in the terminal.

```
cd ~/environment

curl 'https://raw.githubusercontent.com/Interbotix/interbotix_ros_manipulators/main/interbotix_ros_xsarms/install/amd64/xsarm_amd64_install.sh' > xsarm_amd64_install.sh

chmod +x xsarm_amd64_install.sh

./xsarm_amd64_install.sh
```

5. Add our workspace setup to the _.bashrc_ file. Then execute its contents.

```
echo “~/environment/aws_ws/src/robomaker_workshop/devel/setup.bash” >> ~/.bashrc

source ~/.bashrc
```

---

Our ROS app is now configured and ready to be launched. Take a few moments to explore the code we have downloaded. Expand the directories in the explorer on the left, and double-click on files to view their contents.
