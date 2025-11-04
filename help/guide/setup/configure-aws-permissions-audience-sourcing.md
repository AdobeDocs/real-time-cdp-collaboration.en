---
title: Configure AWS Permissions for Audience Sourcing
description: Learn how to configure AWS Identity and Access Management (IAM) permissions to grant Adobe secure, read-only access to your [!DNL Amazon S3] bucket for audience sourcing in Real-Time CDP Collaboration.
---
# Configure AWS permissions for audience sourcing

Use this guide to configure the required AWS Identity and Access Management (IAM) policy and role for Real-Time CDP Collaboration. This configuration grants Adobe secure, read-only access to your Amazon S3 bucket, allowing audiences to be sourced into Collaboration.

>[!IMPORTANT]
>
>This document applies to implementations of Real-Time CDP Collaboration using Amazon S3 as a data connection. If your instance runs in a different region or uses a different cloud provider, contact your Adobe representative before proceeding.

## Prerequisites {#prerequisites}

Before continuing, confirm that you meet the following requirements and have access to the required information.

### Required AWS permissions

To complete this setup, you must have permission to:

* Create and attach IAM policies for Amazon S3 buckets.
* Access the Amazon S3 console to view bucket names and folder paths.
* Create or modify IAM roles in your AWS account.
* Add the Real-Time CDP Collaboration AWS IAM role as a trusted entity in your IAM role.

If you do not have these permissions, contact your AWS administrator before proceeding.

### Information you'll need

* The S3 bucket name where your audience files are stored.
* The folder path (prefix) under which your audience files are located.
* The Resource Amazon Resource Name (ARN) for the folder path, for example:

```
arn:aws:s3:::my-company-data/audience-files/
```

* The appropriate Adobe IAM Role ARN for your region:

| Region | Adobe IAM Role ARN |
|---------|-------------------|
| North America (VA6) | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-va6-role` |
| Australia (AUS3) | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-aus3-role` |
| EMEA | Contact Adobe Representative |

>[!NOTE]
>
>An Amazon Resource Name (ARN) is a unique string that identifies AWS resources, such as EC2 instances, S3 buckets, and IAM roles. The Resource ARN identifies your specific S3 bucket and folder path using this format:
>
>```
>arn:aws:s3:::<bucket-name>/<optional-folder-path>
>```

## Step 1: Create an IAM policy {#create-policy}

Create an IAM policy that grants **read-only access** to your S3 bucket. This policy allows Adobe to read the files necessary for audience sourcing but does not grant write or delete permissions.

1. Open the [AWS Management Console](https://aws.amazon.com/console/), and navigate to **IAM** > **Policies** > **Create policy**.
2. Select the **JSON** tab and paste the following example policy.
3. Replace `<Your AWS ARN for bucket folder path>` and `<Your AWS ARN for bucket>` with your specific S3 ARNs.

```json
{
  "Version": "2012-10-17",
  "Statement": [
      {
          "Sid": "Statement1",
          "Effect": "Allow",
          "Action": [
              "s3:GetObject",
              "s3:ListBucket",
              "s3:GetBucketLocation"
          ],
          "Resource": "<Your AWS ARN for bucket folder path>"
      },
      {
          "Sid": "Statement2",
          "Effect": "Allow",
          "Action": [
              "s3:ListBucket"
          ],
          "Resource": "<Your AWS ARN for bucket>"
      }
  ]
}
```

4. Review the policy and select **Create policy**.
5. Record the policy name for later use.

>[!TIP]
>
> To locate your bucket name and folder path, open the **Amazon S3 console**. On the **Buckets** page, select your bucket name to open it. The **Objects** view lists your files and folders, and the path at the top of the page shows your current folder path.

## Step 2: Create an IAM role {#create-role}

Next, create an IAM role and set the Real-Time CDP Collaboration AWS IAM role as the **trusted entity**. This enables Adobe's services to assume the role and securely read your S3 audience data.

1. In the **IAM** console, navigate to **Roles** > **Create role**.
2. Under **Trusted entity type**, select **Custom trust policy**.
3. In the **Custom trust policy** editor, paste the following example and replace `<Adobe IAM Role ARN>` with the value for your region.

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "Statement1",
            "Effect": "Allow",
            "Principal": {
                "AWS": "<Adobe IAM Role ARN>"
            },
            "Action": "sts:AssumeRole"
        }
    ]
}
```

4. Select **Next** to continue.
5. In the **Add permissions** step, search for and attach the IAM policy you created in [Step 1](#create-policy).
6. Select **Next** again.
7. Provide a role name (for example, `s3-iam-role`) and optional description, then select **Create role**.

## Step 3: Provide the IAM Role ARN {#provide-arn}

After creating the role, record its Amazon Resource Name (ARN).
You'll need to enter this value during the **Authenticate your S3 connection** step in the [Configure AWS S3 for audience sourcing](./configure-aws-s3-audience-sourcing.md) workflow.

## Summary {#summary}

By completing this setup, you have:

* Granted read-only access for Adobe's Collaboration service to your S3 bucket.
* Established a trust relationship between your AWS account and Adobe's IAM role.
* Prepared the IAM Role ARN required to authenticate your data connection in Real-Time CDP Collaboration.

For more information about sourcing audiences, refer to [Source and manage audiences](./onboard-audiences.md).

## Next steps {#next-steps}

Once permissions are configured:

* Proceed to [Configure AWS S3 for audience sourcing](./configure-aws-s3-audience-sourcing.md) to connect your S3 bucket to Collaboration.
* Verify successful authentication by reviewing your sourced audiences under **[!UICONTROL My audiences]** in the **[!UICONTROL Setup]** workspace.
