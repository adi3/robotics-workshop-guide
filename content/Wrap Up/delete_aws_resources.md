+++
title = "Delete AWS resources"
weight = 810
chapter = true
pre = "1. "
+++

# Delete AWS resources

1. Delete the Rekognition dataset you uploaded to S3.

```
aws s3 rb s3://$(aws s3 ls | awk '{print $3}' | grep "custom-labels-console") --force
```

2. Go to **Development environments** in the AWS RoboMaker dashboard. Select the environment you created for this workshop and click **Delete**.

![Launch IDE](/c9-delete.png?classes=border)

3. Go to Rekongition -> Custom Labels -> Projects -> Click on model -> Use model -> Stop
