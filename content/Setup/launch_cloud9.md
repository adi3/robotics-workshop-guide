+++
title = "Launch Cloud9 IDE"
date = 2021-05-03T13:44:16-05:00
weight = 30
chapter = false
+++

1. Go to the AWS RoboMaker dashboard and select **Development environments** from the left column.

![RoboMaker Dashboard](/rm-dashboard.png?classes=border)

2. Click on **Create development environment**, provide a name for the resource, and choose _Melodic_ for the ROS distribution. Select _c5.9xlarge_ for instance type, leaving all other options as default. Then click **Create**.

![Launch IDE](/c9-launch.png?classes=border)

3. The IDE will open up in a new tab and spin up any required resources. This usually takes a few minutes. Once the IDE is active, click on the gear icon in the top-right corner of the window.

![Cloud9 Homepage](/c9-home.png?classes=border)

4. In the **Preferences** tab, scroll down to select **AWS Settings**, then choose **Credentials**. Toggle the switch against _AWS managed temporary credentials_. We want this setting disabled for the exercise.

![Cloud9 Preferences](/c9-preferences.png?classes=border)

5. Add your IAM user credentials to the machine via the terminal.

```
aws configure
```

Follow the prompts and enter your _Access Key ID_ and _Secret Access Key_. When prompted for a default region name, type in **us-east-1**. For default output format, type in **json**.

6. Set up a supplementary CLI profile that allows external Rekognition access.

```
aws configure set profile.rekognition_access.role_arn \
    arn:aws:iam::517502204741:role/RekognitionForRoboticsWorkshop

aws configure set profile.rekognition_access.source_profile default

aws configure set profile.rekognition_access.region eu-central-1
```

---

Before we begin developing, confirm the ROS version installed by issuing the following command in the terminal:

```
rosversion -d
```

The terminal should print out _melodic_.
