---
title: Configure [!DNL Amazon S3] for Audience Sourcing
description: Learn how to configure and connect your [!DNL Amazon S3] storage as a self-service data source to ingest audience data into Real-Time CDP Collaboration.
hide: yes
hidefromtoc: yes
---
# Configure [!DNL Amazon S3] for Audience Sourcing

Learn how to configure and connect your [!DNL Amazon S3] storage in the Adobe Real-Time CDP Collaboration UI to source audience data for activation and overlap analysis.

>[!IMPORTANT]
>
>Before following this guide, you must have completed the steps to authorize Adobe's IAM role within your AWS account.  
>See the **Configure AWS permissions for audience sourcing** guide for step-by-step setup instructions.

<!-- Question: is that the bet doc name? -->

## Overview {#overview}

Use this workflow to source and manage first-party audiences directly from [!DNL Amazon S3] without requiring engineering assistance. After configuration, Collaboration automatically sources audiences from your S3 bucket and makes them available for activation and overlap analysis.

Audiences sourced through S3 follow the same governance and data handling rules as those sourced from Adobe Experience Platform.

## Prerequisites {#prerequisites}

Before configuring your S3 data connection, ensure the following:

* You have access to an active **[!DNL Amazon S3] bucket** containing audience files that conform to the **[Audience Sourcing Specification (v1.1)](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.1.pdf)**.
* You have created an **IAM role** in Amazon that grants Adobe permission to access your bucket using the **assumed role** method (not access/secret keys).  
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

## Configure your [!DNL Amazon S3] connection {#configure-aws-s3-connection}

From the **[!UICONTROL My audiences]** tab within the **[!UICONTROL Setup]** workspace, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Audience]**.  

If this is your first audience, you may also select the **[!UICONTROL Add]** option.

![Add an adudience.](../../assets/setup/add-manage-audiences/add-audiences.png)

The Add audience workflow appears. Select **[!UICONTROL Add a new data connection]** and then select **[!UICONTROL Next]**.

![The Add audiences workspace with the Add a new data connection option highlighted.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Select [!DNL Amazon S3] as the data connection {#select-aws-s3}

Select **[!UICONTROL Amazon S3]** as a data connection, followed by **[!UICONTROL Next]**.  

![The data connection selection screen with [!DNL Amazon S3] available as a selectable option.](../../assets/setup/aws-audience-sourcing/select-s3-data-connection.png)

### Review audience file requirements {#review-audience-requirements}

A dialog appears that explains how your audience files must be structured. Use the link to the **[!UICONTROL [audience sourcing specification]](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.1.pdf)** to learn how to format and structure audience data from [!DNL Amazon S3] for Collaboration to read it correctly.

>[!IMPORTANT]
>
>You must have authorized Adobe as an [!DNL Amazon S3] user so that Adobe can retrieve data from your [!DNL Amazon S3] storage for processing.

Your audience files must comply with the Audience Sourcing Specification. The match keys are automatically mapped based on the required format.  

Key considerations include:

* Files must be in CSV format, using commas for fields and pipes (`|`) for multiple values.
* If uploading multiple files, ensure all files contain identical columns.
* Each audience record must include identifiers such as `AUDIENCE_ID`, `HASHED_EMAIL_SHA_256`, `HASHED_PHONE_SHA_256`, `HASHED_IPV4_SHA_256`, `CRM_ID`, `LOYALTY_ID`, or `ADFIXUS_ID`.
* Data refreshes occur every 1–6 days; if not refreshed within seven days, it is deleted.

![The Prepare Your Data for Sourcing dialog with a link to the Audience Sourcing Specifications.](../../assets/setup/aws-audience-sourcing/prepare-data-sourcing-dialog.png)

### Authenticate your S3 connection {#authenticate-s3-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_sources_s3_folderpath"
>title="Folder path format"
>abstract="Enter the folder path (prefix) within your [!DNL Amazon S3] bucket where your audience files are stored.<br><ul><li>Do not start paths with a forward slash (/).</li><li>Include a trailing slash at the end of the path.</li><ul><br>Example: `base/path/`"

Next, provide your [!DNL Amazon S3] credentials to connect your S3 bucket to Collaboration.

Follow the steps outlined in [Amazon S3 configuration workflow](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#connect) to grant Adobe access to your [!DNL Amazon S3] storage. Once complete, input your values into the following UI fields:

**Input fields**

* IAM Role (required)
* S3 Bucket Name (required)
* Folder Path (required)

![The [!DNL Amazon S3] connection form with fields for IAM role, S3 Bucket Name, and Folder Path.](../../assets/setup/aws-audience-sourcing/s3-authentication-credentials-form.png)

### Confirm consent acknowledgment {#confirm-consent}

You must then acknowledge that consent opt-outs have been removed before proceeding. Check the confirmation box followed by **[!UICONTROL OK]** to confirm.

![The consent opt-out acknowledgment dialog requiring confirmation before proceeding.](../../assets/setup/aws-audience-sourcing/consent-optout-acknowledgment.png)

### Validate authentication results {#validate-authentication}

After connecting, the system validates your credentials and displays one of the following messages:

| Status                      | Message                                         | Description |
|---| ---|---|
| **Success**                 | **[!UICONTROL Authentication successful]**      | Your connection to [!DNL Amazon S3] has been established successfully.  |
| **Failed**                  | **[!UICONTROL Authentication failed]**          | Please review your credentials and try again. |
| **Access denied**           | **[!UICONTROL Access denied]**                  | Your credentials don't have the required permissions to access this [!DNL Amazon S3] bucket. Please verify access settings or contact your administrator. |
| **Invalid file format**     | **[!UICONTROL Invalid file format]**            | The audience data doesn't match the expected structure. Please ensure your files comply with the Audience Sourcing Specifications.                 |
| **No audience files found** | **[!UICONTROL No audience files found]**        | Please confirm that your audience files exist in the specified folder path and that the path is accessible.                                        |
| **Internal error**          | **[!UICONTROL An internal error has occurred]** | Please try again. If the problem persists, contact customer support. (ACPS - XXXX-XXX) Reference id: XXXXXXX-XXXXX-XXXX-XXXX-XXXXXXXX.             |


### Provide connection details {#provide-connection-details}

Enter a descriptive name and optional description for your S3 data connection. Input your values into the following UI fields:

* **[!UICONTROL Data connection name]** (required)
* **[!UICONTROL Data connection description]** (optional)

![The data connection details form with fields for connection name and description.](../../assets/setup/aws-audience-sourcing/s3-connection-name-description.png)

### Review auto-mapped identity fields {#auto-mapped-fields}

The **[!UICONTROL Mapping]** screen is read-only. You cannot add, delete, or apply transformations. Collaboration automatically maps source identity fields from your audience files to target fields based on the Audience Sourcing Specification.

Visually confirm the mapped fields and select **[!UICONTROL Next]** to continue.

![The field mapping screen showing auto-mapped source and target identity fields.](../../assets/setup/aws-audience-sourcing/s3-field-mapping-auto-mapped.png)

### Schedule refresh frequency and date range {#schedule-refresh}

The **[!UICONTROL Schedule]** view appears. Use the dropdown menu to select a refresh frequency between one and six days, then set the active date range. Use the calendar icon to specify start and end dates.

>[!IMPORTANT]
>
>Do not configure the refresh cadence to be more frequent than the refresh cadence of the underlying S3 data source.

![The schedule settings screen with refresh frequency options and date range configuration.](../../assets/setup/aws-audience-sourcing/s3-schedule-refresh-frequency.png)

### Review and complete the connection {#review-and-complete}

Finally, review your configuration settings in the summary screen. This view contains a summary of the following sections:

* **[!UICONTROL Data connection]**: Displays the IAM role, S3 bucket name, and folder path you configured.
* **[!UICONTROL Details]**: Shows the name and optional description of your data connection to help identify it later.
* **[!UICONTROL Mapping]**: Lists how the source fields from your uploaded audience files (for example, `HASHED_EMAIL`) map to target fields used in Collaboration (for example, Hashed email).
* **[!UICONTROL Schedule]**: Summarizes how often the connection refreshes audience data and the active date range for sourcing.

Select the pencil icon if you need to edit a section. Select **[!UICONTROL Complete]** to confirm all sections.

![The review summary screen displaying data connection, details, mapping, and schedule sections.](../../assets/setup/aws-audience-sourcing/s3-connection-review-summary.png)

A dialog confirmation appears stating that the data connection was created successfully and that audience sourcing in progress.

## Review sourced audiences {#review-sourced-audiences}

After completing the configuration, Collaboration begins sourcing audiences from your S3 bucket. Audiences sourced through an [!DNL Amazon S3] bucket appear in the **[!UICONTROL My Audiences]** tab and have the same functionality and information as audiences sourced from Experience Platform.

If audience sourcing is in progress, a banner appears at the top of the screen. Individual audiences appear only after sourcing completes.

![The Audiences tab showing that sourcing is in progress for [!DNL Amazon S3] audiences.](../../assets/setup/aws-audience-sourcing/s3-audiences-sourcing-in-progress.png)

Once the S3 audiences are sourced, your list of available audiences are provided in a tabulated or card view.

![The Audiences tab showing a tabulated list of sourced audiences.](../../assets/setup/aws-audience-sourcing/s3-audiences-list-view.png)

Where in grid view or table view, you can select a row item or [!UICONTROL View audience] to see an overview of a specific audience. It displays the audience's status, source, and data connection name, along with detailed panels for:

**[!UICONTROL Identities]**: Shows the total identity count and breakdown once data becomes available.
**[!UICONTROL Categories]**: Lists any tags used for organizing or filtering the audience.
**[!UICONTROL Connection access]**: Indicates whether the audience is private, public, or shared with specific collaborators.
**[!UICONTROL Metadata visibility]**: Defines what audience information (such as identity count, overlap percentage, and index) is visible to collaborators.

Use this view to confirm audience configuration and visibility settings before using the audience in collaboration projects.

See the [View audiences dashboard documentation](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-audiences#view-audiences-dashboard) to learn more.

## View your S3 data connection {#view-s3-connection}

Your newly added [!DNL Amazon S3] connection is immediately available in the **[!UICONTROL My data connections]** tab. The audience source is displayed as [!UICONTROL Amazon S3].

Your S3 data connection includes the same functionality and details as other audience data connections, except that you cannot add audiences directly from this view. To add another audience, navigate to the **[!UICONTROL My audiences]** tab.

![The My data connections tab showing the [!DNL Amazon S3] data connection with sourcing status information.](../../assets/setup/aws-audience-sourcing/s3-data-connections-tab.png)

## Next steps {#next-steps}

You have now successfully configured and connected your [!DNL Amazon S3] storage as a self-service data source in Collaboration. By completing this workflow, you enabled secure sourcing of first-party audience data for activation and overlap analysis.

After sourcing completes, your audiences appear in the **[!UICONTROL My audiences]** workspace, ready for collaboration and activation. For detailed management options, see the [source and manage audiences documentation](./onboard-audiences.md).

