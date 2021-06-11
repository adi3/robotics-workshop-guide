+++
title = "Attach access policy"
weight = 20
chapter = false
hidden = true
+++

1. Log in to your AWS account with the credentials provided to you in the previous step. Go to IAM Users, then click on your user name to open the resource summary page. Select **Add inline policy** on the right.

![Add inline policy](/iam-add-inline.png?classes=border)

2. On the _Create policy_ page, choose the **JSON** tab and replace its contents with the following snippet.

```
{
    "Version": "2012-10-17",
    "Statement": {
        "Effect": "Allow",
        "Action": "sts:AssumeRole",
        "Resource": "arn:aws:iam::517502204741:role/ResourcesForRoboticsWorkshop"
    }
}
```

![Inline access policy](/iam-inline-policy.png?classes=border)

3. Click on **Review policy**. For name, type in `RoboticsWorkshopAccess`. Then hit the **Create policy** button.

![Add policy review](/iam-policy-review.png?classes=border)

---

The newly added inline policy should now be listed under the _Permissions policies_ section in the user summary page.

![Attached policies](/iam-policy-list.png?classes=border)
