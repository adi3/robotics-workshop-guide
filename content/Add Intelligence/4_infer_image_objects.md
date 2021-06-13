+++
title = "Infer objects in image"
weight = 300
chapter = true
pre = "4. "
+++

# Infer objects in image

1. Add the following code snippet under **STEP 3** of _main.py_.

```python
rospy.logwarn('Press Enter to discover labels with Rekognition')
raw_input()

labels = util.find_coins(image, model_arn, CONFIDENCE_THRESHOLD, MODEL_ACCESS_PROFILE)
rospy.loginfo('Found %d labels in image' % len(labels))

util.print_labels(labels)
util.display_labels(image, labels)
```

2. Run the _main.py_ script in simulation mode. Press Enter as prompted by the script.

```
python ~/environment/aws_ws/src/robomaker_workshop/scripts/main.py --sim
```

3. The terminal will print out details of the objects detected by Amazon Rekognition.

![Detections in terminal](/detections-term.png?classes=border)

4. Head over to the virtual desktop and you will see the snapped image superimposed with labels detected by the machine learning model.

![Detections in terminal](/detections-vis.png?classes=border)

---

Our model is thus able to reliably

- identify the right number of objects in the image
- categorize the objects as the correct type, and
- locate each object at its precise location
