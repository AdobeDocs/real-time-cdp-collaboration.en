---
title: Configure AWS Permissions for Audience Sourcing
description: Learn how to configure AWS Identity and Access Management (IAM) permissions to grant Adobe secure, read-only access to your [!DNL Amazon S3] bucket for audience sourcing in Real-Time CDP Collaboration.
---
# Configure AWS permissions for audience sourcing

Use this guide to configure AWS Identity and Access Management (IAM) policies and roles that grant Adobe secure, read-only access to your Amazon S3 bucket. This access enables Real-Time CDP Collaboration to source audiences from your S3 bucket.

## Prerequisites {#prerequisites}

Before continuing, confirm that you meet the following requirements and have access to the required information.

### Required AWS permissions

To complete this setup, your account must have AWS administrator access. Administrator access ensures that you can create and manage IAM policies and roles required to authorize Adobe's access to your S3 bucket. If you do not have administrator privileges, contact your AWS administrator before proceeding.

### Required information

As you go through the steps below, keep note of the following information. These details are used in the [[!DNL Amazon S3] audience sourcing UI guide](./configure-aws-s3-audience-sourcing.md).

* The S3 bucket name where your audience files are stored.
* The folder path (prefix) under which your audience files are located.
* The Amazon Resource Name (ARN) for your newly created IAM Role, for example: `arn:aws:s3:::my-company-data/audience-files/`

>[!TIP]
>
>An Amazon Resource Name (ARN) uniquely identifies AWS resources, such as S3 buckets and IAM roles. Use the following format to specify your bucket and optional folder path:
>
>```
>arn:aws:s3:::<bucket-name>/<optional-folder-path>
>```

## Create an IAM policy {#create-policy}

To begin the setup, first create an IAM policy that grants **read-only access** to your S3 bucket. This policy allows Adobe to read the files necessary for audience sourcing but does not grant write or delete permissions.

Open the [AWS Management Console](https://aws.amazon.com/console/), and navigate to **[!DNL IAM]** > **[!DNL Policies]** > **[!DNL Create policy]**.

In the AWS Create policy workspace, select the **JSON** tab and paste the following example policy.

>[!NOTE]
>
>Replace `<Your AWS ARN for bucket folder path>` and `<Your AWS ARN for bucket>` with your specific S3 ARNs. When specifying the bucket folder path, include `/*` at the end of the ARN (for example, `arn:aws:s3:::my-company-data/audience-files/*`). This ensures Adobe has access to all files and subfolders within the specified folder path.

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

Review the policy settings and select **[!DNL Create policy]**. Record the policy name for use in a later step.

>[!TIP]
>
>To locate your bucket name and folder path, open the **Amazon S3 Management Console**. On the **Buckets** page, select your bucket name to open it. The **Objects** view lists your files and folders, and the path at the top of the page shows your current folder path.

## Create an IAM role {#create-role}

Next, create an IAM role and set the Real-Time CDP Collaboration AWS IAM role as the **trusted entity**. This enables Adobe's services to assume the role and securely read your S3 audience data.

In the **[!DNL IAM]** tab of the Amazon S3 Management Console, navigate to **[!DNL Roles]** > **[!DNL Create role]**.

Under [!DNL Step 1] of the [!DNL Create role] workflow, in the **[!DNL Trusted entity type]** section, select **[!DNL Custom trust policy]**. Then, in the **[!DNL Custom trust policy]** editor, paste the following example and replace `<Adobe IAM Role ARN>` with the value for your region.

* The appropriate Adobe IAM Role ARN for your region:

| Region | Adobe IAM Role ARN |
|---------|-------------------|
| North America | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-va6-role` |
| Australia | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-aus3-role` |
| EMEA | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-deu1-role` |

An example trust policy:

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

Review the policy and select **Next** to continue.

In [!DNL Step 2] **[!DNL Add permissions]** section of the [!DNL Create role] workflow, search for and attach the IAM policy you created [earlier](#create-policy). Select the policy followed by **[!DNL Next]** to continue to [!DNL Step 3].

In the [!DNL Step 3] **[!DNL Name review, and create - Role details]** section, provide a role name (for example, `s3-iam-role`) and optional description.

This page displays the trusted entity policy, the permissions policy summary, and any tags you may have added for internal organization and tracking.

Finally, select **Create role** to confirm the setup.

>[!IMPORTANT]
>
>You must record the Amazon Resource Name (ARN) after creating the role. You will need to provide the IAM Role ARN during the **Authenticate your S3 connection** step in the [Configure AWS S3 for audience sourcing](./configure-aws-s3-audience-sourcing.md) workflow.

## Next steps {#next-steps}

This setup grants Adobe read-only access to your S3 bucket and establishes a trusted connection with Adobe's IAM role.

Next, proceed to [Configure AWS S3 for audience sourcing](./configure-aws-s3-audience-sourcing.md) to connect your S3 bucket to Collaboration.

For more information about sourcing audiences, refer to [Source and manage audiences](./onboard-audiences.md).
