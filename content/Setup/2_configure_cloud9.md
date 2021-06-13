+++
title = "Configure Cloud9 IDE"
weight = 220
chapter = true
pre = "2. "
+++

# Configure Cloud9 IDE

1. Go to the AWS RoboMaker dashboard and select **Development environments** from the left column.

![RoboMaker Dashboard](/rm-dashboard.png?classes=border)

2. Click on **Create development environment**, provide a name for the resource, and choose _Melodic_ for the ROS distribution. Select _c4.8xlarge_ for instance type, leaving all other options as default. Then click **Create**.

![Launch IDE](/c9-launch.png?classes=border)

3. The IDE will open up in a new tab and spin up any required resources. This usually takes a few minutes. Once the IDE is active, click on the gear icon in the top-right corner of the window.

![Cloud9 Homepage](/c9-home.png?classes=border)

4. In the **Preferences** tab, scroll down to select **AWS Settings**, then choose **Credentials**. Toggle the switch against _AWS managed temporary credentials_. We want this setting disabled for the exercise.

![Cloud9 Preferences](/c9-preferences.png?classes=border)

5. Add your IAM user credentials to the machine via the terminal.

```
aws configure
```

6. Follow the prompts and enter your _Access Key ID_ and _Secret Access Key_. When prompted for a default region name, type in `us-east-1`. For default output format, type in `json`.

![AWS Credentials](/aws-creds.png?classes=border)
