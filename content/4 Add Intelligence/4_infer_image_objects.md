+++
title = "Infer objects in image"
weight = 440
chapter = true
pre = "4. "
+++

# Infer objects in image

1. Open the _main.py_ file located at the following path:

```c
aws_ws -> src -> robomaker_workshop -> scripts -> main.py
```

2. Add the following code snippet under **STEP 2** of _main.py_. Then hit save.

```python
labels = util.find_coins(IMAGE_NAME, model_arn, CONFIDENCE_THRESHOLD, access_profile)
rospy.loginfo('Found %d labels in image' % len(labels))

util.print_labels(labels)
util.display_labels(image, labels)
```

---

> Python is senstitive to identation so make sure that the tabs and spaces in your code _exactly_ match the code shown here.

---

3. Run the _main.py_ script in simulation mode. Press Enter as prompted by the script.

```
python ~/environment/aws_ws/src/robomaker_workshop/scripts/main.py --sim
```

4. The terminal will print out details of the objects detected by Amazon Rekognition.

![Detections in terminal](/detections-term.png?classes=border)

5. Head over to the virtual desktop and you will see the snapped image superimposed with labels detected by the machine learning model.

![Detections in terminal](/detections-vis.png?classes=border)

---

Our model is thus able to reliably

- identify the right number of objects in the image
- categorize the objects as the correct type, and
- locate each object at its precise location
