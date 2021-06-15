+++
title = "Set up images dataset"
weight = 520
chapter = true
pre = "2. "
+++

# Set up images dataset

1. Execute the **fetch_dataset.sh** script, which grabs the images dataset to the S3 bucket you created in the previous step.

```
source ~/environment/aws_ws/src/robomaker_workshop/fetch_dataset.sh
```

2. Copy the **S3 Path** printed out by the script at the end.

![Dataset Path](/dataset-path.png?classes=border)

3. Head back to the Rekognition Custom Labels console and select **Datasets** on the left. Then click on **Create dataset**.

![Create Dataset](/create-dataset.png?classes=border)

4. Enter a name for your dataset, preferably with your username in it so as to keep it unique within your team. Then select the _Import images from Amazon S3 bucket_ option.

![Dataset Config](/dataset-config.png?classes=border)

5. A new option will appear asking for your _S3 folder location_. Enter the **S3 Path** you copied above.

![Dataset Submit](/dataset-submit.png?classes=border)

6. The images dataset will be created and presented to you in a grid layout, all set to be labelled.

![Dataset Loaded](/dataset-loaded.png?classes=border)
