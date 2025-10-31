---
title: Configure AWS S3 for Audience Sourcing
description: Learn how to configure and connect your Amazon S3 storage as a self-service data source to ingest audience data into Real-Time CDP Collaboration.
hide: yes
hidefromtoc: yes
---
# Configure AWS S3 for Audience Sourcing

Learn how to connect your Amazon S3 storage as a self-service data source to ingest audience data into **Real-Time CDP Collaboration**. This guide walks you through the configuration workflow within the Collaboration UI.

>[!IMPORTANT]
>
>Before following this guide, you must have completed the steps to authorize Adobe's IAM role within your AWS account.  
>Refer to the **Configure AWS permissions for audience sourcing** guide for detailed AWS setup instructions.

<!-- Question: is that the bet doc name? -->

## Overview {#overview}

Use this workflow to source and manage your first-party audiences directly from [!DNL Amazon S3] without requiring Adobe engineering assistance. Once configured, audiences stored in your S3 bucket are automatically sourced by Collaboration and made available for activation and overlap analysis.

Audiences sourced through S3 follow the same governance and data handling rules as those sourced from Adobe Experience Platform.

## Prerequisites {#prerequisites}

Before configuring your S3 data connection, ensure the following:

* You have access to an active **[!DNL Amazon S3] bucket** containing audience files that conform to the **[Audience Onboarding Specifications (v1.1)](../../assets/quick-start/RTCDP_Collaboration_Audience_Onboarding_Spec_v1.1.pdf)**.
* You have created an **IAM role** in AWS that grants Adobe permission to access your bucket using the **assumed role** method (not access/secret keys).  
  The IAM role must include the following permissions:
  
  * `ListBucket`
  * `GetBucketLocation`
  * `GetObject`

* You have the following values ready:
  
  * **IAM role Amazon Resource Name (ARN)**
  * **S3 bucket name**
  * **Folder path** (the directory prefix containing your audience files)

>[!NOTE]
>
>Audience files must be located in the **root folder path** of your authorized S3 bucket. Subfolder structures are not supported.

## Configure your AWS S3 connection {#configure-aws-s3-connection}

From the **[!UICONTROL My audiences]** tab within the **[!UICONTROL Setup]** workspace, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Audience]**.  

If this is your first audience, you may also select the **[!UICONTROL Add]** option.

<!-- another screenshot needed here -->

The Add audience workflow appears. Select **[!UICONTROL Add a new data connection]** and then select **[!UICONTROL Next]**.

![The Add audiences workspace with the Add a new data connection option highlighted.](/help/assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### 1. Select AWS S3 as the data connection {#select-aws-s3}

You can see **AWS S3** as a selectable data connection.  
Previously created AWS S3 connections appear grayed out, and you see the following copy within the card:  
Copy: *To add additional audiences, please update the audiences files within the connected Amazon S3 storage.*

![The data connection selection screen with AWS S3 available as a selectable option.](../../assets/setup/aws-audience-sourcing/1.1a.png)

![The Add audiences workspace with the Set up new data connection option selected.](../../assets/setup/aws-audience-sourcing/1.1b.png)

### 2. Review audience file requirements {#review-audience-requirements}

You see a pop-up with a link to the **Audience Onboarding specification** that explains how your audience files must be structured.

Copy:  
Title: *Prepare Your Data for Sourcing*  
Body:  
*Before starting audience sourcing from Amazon S3, please ensure that:*

* *You have authorized Adobe as a user so that Adobe can retrieve data from your Amazon S3 storage for processing.*  
* *Your data complies with the {Audience Sourcing Specifications}, as the match keys are auto-mapped based on the prescribed format.*

![The Prepare Your Data for Sourcing dialog with a link to the Audience Sourcing Specifications.](../../assets/setup/aws-audience-sourcing/1.2a.png)

### 3. Authenticate your S3 connection {#authenticate-s3-connection}

Provide your credentials to connect your AWS S3 bucket to Real-Time CDP Collaboration.

**Input fields**

* IAM Role (required)
* S3 Bucket Name (required)
* Folder Path (required)

Copy:  
*To connect your Amazon S3 storage, please authorize Adobe's service user to retrieve your audience data for processing. Follow the steps outlined in {Experience League} to grant Adobe access to your Amazon S3 storage.*

![The Amazon S3 connection form with fields for IAM role, S3 Bucket Name, and Folder Path.](../../assets/setup/aws-audience-sourcing/1.3a.png)

### 4. Confirm consent acknowledgment {#confirm-consent}

You must acknowledge that consent opt-outs have been removed before proceeding. Check the confirmation box followed by **[!UICONTROL OK]** to confirm.

![The consent opt-out acknowledgment dialog requiring confirmation before proceeding.](../../assets/setup/aws-audience-sourcing/1.4a.png)

### 5. Validate authentication results {#validate-authentication}

After connecting, the system validates your credentials and displays one of the following messages:

| Status                      | Message                                         | Description |
|---| ---|---|
| **Success**                 | **[!UICONTROL Authentication successful]**      | Your connection to Amazon S3 has been established successfully.  |
| **Failed**                  | **[!UICONTROL Authentication failed]**          | Please review your credentials and try again. |
| **Access denied**           | **[!UICONTROL Access denied]**                  | Your credentials don't have the required permissions to access this Amazon S3 bucket. Please verify access settings or contact your administrator. |
| **Invalid file format**     | **[!UICONTROL Invalid file format]**            | The audience data doesn't match the expected structure. Please ensure your files comply with the Audience Sourcing Specifications.                 |
| **No audience files found** | **[!UICONTROL No audience files found]**        | Please confirm that your audience files exist in the specified folder path and that the path is accessible.                                        |
| **Internal error**          | **[!UICONTROL An internal error has occurred]** | Please try again. If the problem persists, contact customer support. (ACPS - XXXX-XXX) Reference id: XXXXXXX-XXXXX-XXXX-XXXX-XXXXXXXX.             |

![The authentication success message confirming the connection to Amazon S3 has been established.](../../assets/setup/aws-audience-sourcing/1.5a.png)
![The authentication error messages showing various failure scenarios including access denied and invalid file format.](../../assets/setup/aws-audience-sourcing/1.5b.png)

### 6. Provide connection details {#provide-connection-details}

Enter a descriptive name and optional description for your S3 data connection.

**Fields**

* Data connection name (required)
* Data connection description (optional)

![The data connection details form with fields for connection name and description.](../../assets/setup/aws-audience-sourcing/1.6a.png)

### 7. Review auto-mapped identity fields {#auto-mapped-fields}

<!-- (1.8) -->

The source and target fields are auto-populated based on the underlying audience tables. The **Field mapping** screen is read-only. You cannot add or delete fields or apply transformations. Source and target fields are automatically mapped based on the underlying audience tables.

Copy across top of page:  
*Source identity fields from your data connection are auto-mapped to target identity fields in Real-Time CDP Collaboration based on the {Audience Onboarding Specifications}.*

![The field mapping screen showing auto-mapped source and target identity fields.](../../assets/setup/aws-audience-sourcing/1.8a.png)

### 8. Schedule refresh frequency and date range {#schedule-refresh}

<!-- (1.9) -->

Set how frequently your data connection refreshes and specify the date range during which the connection remains active.  
Available frequencies range from **daily up to every six days**.

>[!IMPORTANT]
>
>Do not configure the refresh cadence to be more frequent than the refresh cadence of the underlying S3 data source.

![The schedule settings screen with refresh frequency options and date range configuration.](../../assets/setup/aws-audience-sourcing/1.9a.png)

### 9. Review and complete the connection {#review-and-complete}

<!-- (1.11) -->

Review your configuration in the summary screen. Confirm all sections before selecting **[!UICONTROL Complete]**.

**Summary sections**

* **[!UICONTROL Data connection]**
* **[!UICONTROL Details]**
* **[!UICONTROL Mapping]**
* **[!UICONTROL Schedule]**

![The review summary screen displaying data connection, details, mapping, and schedule sections.](../../assets/setup/aws-audience-sourcing/1.11a.png)


1.13    
Audiences sourced through an AWS S3 bucket appear in the "My Audiences" tab and have the same functionality and information as audiences sourced from AEP.  
The audience source is "AWS S3".  
If sourcing is in progress, you are informed of that.  
Copy:  
Title: Audience sourcing in progress  
Body: Audiences are being sourced from [Cloud Source Name] via the [Data Connection Name] data connection and will appear once the process is complete.  
You see the message above for any or all S3 data connections that are currently sourcing audiences.  
If sourcing fails, you are informed of that.  
Copy:  
Title: Audience sourcing failed  
Body: Audience sourcing from [Cloud Source Name] via the [Data Connection Name] data connection failed. Please try again. If the problem persists, contact customer support. Reference id: XXXXXXX-XXXXX-XXXX-XXXX-XXXXXXXX

![The Audiences tab showing that AWS S3 audience sourcing is in progress.](../../assets/setup/aws-audience-sourcing/1.13a.png)

![The Audiences tab showing a tabulated list of sourced audiences.](../../assets/setup/aws-audience-sourcing/1.13b.png)

1.14    
The AWS S3 data connection appears in the "My data connections" tab and includes the same functionality and information as audiences sourced from AEP.  
The audience source is "AWS S3".  
The "+ Add audience" option is not available for S3 data connections (this appears when selecting the ellipses on the "My data connections" tab).  
The "+" icon is not available on the details page of the data connection.  
You are informed if the data connection is currently sourcing audiences.  
Copy:  
Title: Audience sourcing in progress  
Body: Audiences are being sourced from [Cloud Source Name] and will appear once the process is complete.

![The My data connections tab showing the AWS S3 data connection with sourcing status information.](../../assets/setup/aws-audience-sourcing/1.14a.png)


<!-- Below is live contextual help: -->
## Data connection details {#data-connection-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_sources_s3_folderpath"
>title="Folder path format"
>abstract="Enter the folder path (prefix) within your Amazon S3 bucket where your audience files are stored.<br><ul><li>Do not start paths with a forward slash (/).</li><li>Include a trailing slash at the end of the path.</li><ul><br>Example: `base/path/`"
