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

3. Navigate to your project in the Rekognition Customs Labels dashboard. Choose your model, click on **Use Model** and then press **Stop**.

![Stop Model](/stop-model.png?classes=border)

4. Connect to your team's robot via [Botworks](https://dev.d1aqmxpt45hipw.amplifyapp.com/) and wipe off your AWS credentials and ROS application from the machine.

```
rm -rf ~/.aws ~/environment
```
