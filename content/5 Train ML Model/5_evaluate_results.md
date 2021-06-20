+++
title = "Evaluate training results"
weight = 550
chapter = true
pre = "5. "
+++

# Evaluate training results

1. Once your model is ready to run, its status will be changed to _TRAINING COMPLETED_ in the Rekognition Custom Labels console.

![Training Completed](/training-completed.png?classes=border)

2. Select your project and check out the various metrics describing the performance of the model against your labeled dataset in the _Evaluation results_ section. The closer their value is to 1, the better is the model's performance.

![Evaluation Metrics](/eval-metrics.png?classes=border)

> Rekognition also provides performane metrics for individual labels and the confidence with which the model can identify them in an image.

3. Compare your model's performance with that of your teammates. Choose the one with the highest F1 score and copy its ARN from the _Use Model_ tab. In addition, click on _Start_ to begin inference with this model.

![Start Model](/start-model.png?classes=border)
