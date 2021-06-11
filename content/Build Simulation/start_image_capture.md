+++
title = "Start image capture service"
weight = 700
chapter = false
+++

1. Add the following code snippet under **STEP 7** of _main.launch_.

```
<node name="image_saver" pkg="image_view" type="image_saver" output="screen">
    <remap from="image" to="camera/image_raw" />
    <param name="save_all_image" value="false" />
    <param name="filename_format" value="$(find robomaker_workshop)/scripts/image_%04d.png" />
</node>
```

2. Run the ROS application.

```
roslaunch robomaker_workshop main.launch
```

3. Confirm that the image capture service has started.

```
rosservice list | grep image_saver
```

Of particular interest to us is the _/image_saver/save_ service. We will be invoking this service to captures images from the live camera stream.

![Snap service](/snap-service.png?classes=border)
