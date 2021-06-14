+++
title = "Set up images dataset"
weight = 520
chapter = true
pre = "2. "
+++

# Set up images dataset

1. Execute the **fetch_data.sh** script, which grabs the images dataset to the S3 bucket you created in the previous step.

```
source ~/environment/aws_ws/src/robomaker_workshop/fetch_data.sh
```

<!-- 1. Fetch images of the real-world setup which is already prepared for you. Make sure to substitue your team name in the appropriate spot.

```
aws s3 cp s3://adsnghw-robotics/px100-dataset/real_coins.zip /tmp/px100-dataset.zip --profile robomaker_workshop

unzip -q /tmp/px100-dataset.zip -d /tmp/px100-dataset

BUCKET=px100-dataset-$(cut -d'-' -f1 <<< $(uuidgen))

aws s3 cp /tmp/px100-dataset s3://$BUCKET/assets/px100-dataset --recursive
```

2. Decompress the archive and upload the data to the S3 bucket set up by Rekognition.

```
unzip -q /tmp/px100-dataset.zip -d /tmp/px100-dataset/

aws s3 cp /tmp/px100-dataset s3://<REKOGNITION_S3_BUCKET>/assets/px100-dataset --recursive
```

3. Confirm that your dataset has been correctly received by S3.

```
aws s3 ls s3://<REKOGNITION_S3_BUCKET>/assets/px100-dataset/ | wc -l
```

The terminal should print out `50`, implying that all fifty images of the dataset are now in the appropriate S3 location. -->
