+++
title = "Delete AWS resources"
date = 2021-05-03T13:44:16-05:00
weight = 500
chapter = false
+++

1. Delete the S3 bucket you created to hold the Rekognition dataset.

```
aws s3 rb s3://<YOUR_BUCKET_NAME> --force
```

2. Go to **Development environments** in the AWS RoboMaker dashboard. Select the environment you created for this workshop and click **Delete**.

![Launch IDE](/c9-delete.png?classes=border)

3. Go to Rekongition -> Custom Labels -> Projects -> Click on model -> Use model -> Stop
