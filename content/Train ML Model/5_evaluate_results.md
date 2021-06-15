+++
title = "Evaluate training results"
weight = 550
chapter = true
pre = "5. "
+++

# Evaluate training results

1. Go to the Rekognition Custom Labels console and select **Projects** on the left. Then click on the model that has been trained for you.

[SCREENSHOT]

2. Check out the various metrics describing the performance of the model against your labeled dataset in the _Evaluation results_ section. The closer their value is to 1, the better is the model's performance.

[SCREENSHOT]

> Rekognition also provides performane metrics for individual labels and the confidence with which the model can identify them in an image.

3. Compare your model's performance with that of your teammates. Choose the one with the highest F1 score and copy its ARN from the _Use Model_ tab. In addition, click on _Start_ to begin inference with this model.

[SCREESHOT]

4. Set the **REAL_MODEL** constant in _main.py_ as the model ARN you just copied.

```
REAL_MODEL = "arn:aws:rekognition:eu-central-1:517502204741:project/PX100/version/PX100.2021-06-07T01.15.17/1623021317812"
```
