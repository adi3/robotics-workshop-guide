+++
title = "Delete AWS resources"
weight = 500
chapter = false
+++

1. Delete the Rekognition dataset you uploaded to S3.

```
aws s3 rm s3://<REKOGNITION_S3_BUCKET>/assets/px100-dataset --recursive
```

2. Go to **Development environments** in the AWS RoboMaker dashboard. Select the environment you created for this workshop and click **Delete**.

![Launch IDE](/c9-delete.png?classes=border)

3. Go to Rekongition -> Custom Labels -> Projects -> Click on model -> Use model -> Stop
