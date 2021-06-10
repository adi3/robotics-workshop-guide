+++
title = "Upload dataset to S3"
date = 2021-05-03T13:44:16-05:00
weight = 100
chapter = false
+++

1. Fetch images of the real-world setup which is already prepared for you.

```
aws s3 cp s3://adsnghw-robotics/px100-dataset.zip .
```

2. Unzip the downloaded archive.

```
unzip px100-dataset.zip
```

3. Create a bucket on S3. You need to choose a name for your bucket that is globally unique. Refer to [S3 naming rules](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html) for more information.

```
aws s3 mb s3://<YOUR_BUCKET_NAME>
```

4. Upload the dataset to your S3 bucket.

```
aws s3 cp px100-dataset/ s3://<YOUR_BUCKET_NAME> --recursive
```

5. Go to the S3 dashboard and confirm that your dataset has been uploaded. It should contain 50 images.

### SCREENSHOT HERE

---

Optionally, clean your workspace by deleting the downloaded assets.

```
rm -rf px100-dataset*
```
