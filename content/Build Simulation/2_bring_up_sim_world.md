+++
title = "Bring up simulation world"
weight = 32
chapter = true
+++

1. Add the following code snippet under **STEP 2** of _main.launch_.

```
<include file="$(find gazebo_ros)/launch/empty_world.launch">
    <arg name="world_name" value="$(arg world_name)"/>
</include>
```

2. Run the ROS application.

```
roslaunch robomaker_workshop main.launch
```

3. Go to the virtual desktop to view our Gazebo world. You should see a black table with a few colorful coins on it. Take a few moments to familiarize yourself with the Gazebo GUI and the various options it offers.

![Gazebo World](/gazebo-world.png?classes=border)

4. Add the following code snippet under, once again, **STEP 2** of _main.launch_.

```
<node pkg="gazebo_ros"
    name="urdf_spawner"
    type="spawn_model"
    respawn="false"
    output="screen"
    args="-urdf -model $(arg robot_model) -param robot_description -x $(arg x_offset) -z $(arg table_height)">
</node>
```

5. Run the ROS application again.

```
roslaunch robomaker_workshop main.launch
```

6. Go to the virtual desktop and confirm that the robot arm appears in the simulated world.

![Simulated Arm](/sim-arm.png?classes=border)
