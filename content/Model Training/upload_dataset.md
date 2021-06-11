+++
title = "Upload dataset to S3"
weight = 100
chapter = false
+++

1. Fetch images of the real-world setup which is already prepared for you. Make sure to substitue your team name in the appropriate spot.

```
aws s3 cp s3://adsnghw-robotics/px100-dataset/<YOUR_TEAM_NAME>.zip /tmp/px100-dataset.zip --profile robomaker_workshop
```

2. Decompress the archive and upload the data to the S3 bucket set up by Rekognition.

```
unzip -q /tmp/px100-dataset.zip -d /tmp/px100-dataset/

aws s3 cp /tmp/px100-dataset/ s3://<REKOGNITION_S3_BUCKET>/assets/ --recursive
```

3. Confirm that your dataset has been correctly received by S3.

```
aws s3 ls s3://<REKOGNITION_S3_BUCKET>/assets | wc -l
```

The terminal should print out `50`, implying that all fifty images of the dataset are now in the appropriate S3 location.
