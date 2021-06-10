+++
title = "Initiate model training"
date = 2021-05-03T13:44:16-05:00
weight = 300
chapter = false
+++

1. Add the following code snippet under **STEP 3** of _main.py_.

```python
rospy.logwarn('Press Enter to discover labels with Rekognition')
raw_input()

labels = util.find_coins(image, model_arn, CONFIDENCE_THRESHOLD, MODEL_ACCESS_PROFILE)
rospy.loginfo('Found %d labels in image' % len(labels))

util.print_labels(labels)
```

2. Run the _main.py_ script in simulation mode. Press Enter as prompted by the script.

```
python main.py --sim
```

The terminal will print out details of the objects detected by Amazon Rekognition.

![Detections in terminal](/detections-term.png?classes=border)

3. Install the _ImageMagick_ package so that our python script can visualize labels.

```
sudo apt install imagemagick
```

4. Add the following line at the end of **STEP 3** of _main.py_.

```
util.display_labels(image, labels)
```

5. Run the _main.py_ script. Press Enter as prompted by the script.

```
python main.py --sim
```

Head over to the virtual desktop and you will see the snapped image superimposed with the labels detected by our machine learning model.

![Detections in terminal](/detections-vis.png?classes=border)

---

Our model is thus able to reliably

- identify the right number of objects in the image
- categorize the objects as the correct type, and
- locate each object at its precise location
