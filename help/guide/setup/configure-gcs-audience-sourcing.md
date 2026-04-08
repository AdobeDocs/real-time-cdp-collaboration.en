---
title: Configure [!DNL Google Cloud Storage] for Audience Sourcing
description: Learn how to configure and connect your [!DNL Google Cloud Storage] as a self-service data source to ingest audience data into Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8f4e2b91-6c3d-4a1f-9e82-7b5d4c3a2f10
---
# Configure [!DNL Google Cloud Storage] for audience sourcing

Learn how to configure and connect your [!DNL Google Cloud Storage] (GCS) in the Adobe Real-Time CDP Collaboration UI to source audience data for activation and overlap analysis.

## Overview {#overview}

[!DNL Google Cloud Storage] is one of the supported options for sourcing first-party audience data into Collaboration. Other available methods include sourcing audiences from [Experience Platform](./onboard-audiences.md), connecting an [[!DNL Amazon S3] bucket](./configure-aws-s3-audience-sourcing.md), using [[!DNL Snowflake]](./configure-snowflake-audience-sourcing.md), or uploading a [CSV file](./upload-csv-audience-sourcing.md).

Use this workflow to source and manage first-party audiences directly from GCS. After configuration, Collaboration sources audiences from your bucket and makes them available for insights and activation.

Audiences sourced through GCS follow the same governance and data handling rules as those sourced from Adobe Experience Platform.

## Prerequisites {#prerequisites}

Before configuring your GCS data connection, ensure the following:

* You have access to an active **[!DNL Google Cloud Storage] bucket** containing audience files that conform to the **[Audience Sourcing Specification (v1.2)](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)**.
* You can grant Adobe access to read objects in that bucket in line with your organization’s Google Cloud security policies.

>[!NOTE]
>
>Detailed **Google Cloud access, service accounts, and required IAM roles** for this integration will be documented in a dedicated guide. Until that guide is published, work with your Google Cloud administrator to ensure Collaboration can authenticate and read audience files from your bucket using the mechanism shown in the Collaboration UI.

## Configure your [!DNL Google Cloud Storage] connection {#configure-gcs-connection}

From the **[!UICONTROL My audiences]** tab within the **[!UICONTROL Setup]** workspace, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Audience]**.

If this is your first audience, you may also select the **[!UICONTROL Add]** option.

![The My audiences tab in the Setup workspace with the add icon and Add audience option displayed.](../../assets/setup/add-manage-audiences/add-audiences.png)

The Add audience workflow appears. Select **[!UICONTROL Add a new data connection]** and then select **[!UICONTROL Next]**.

![The Add audiences workspace with the Add a new data connection option highlighted.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Select [!DNL Google Cloud Storage] as the data connection {#select-gcs}

Select **[!UICONTROL Google Cloud Storage]** (or the Google Cloud–labeled option) as your data connection, followed by **[!UICONTROL Next]**.

### Review audience file requirements {#review-audience-requirements}

A dialog appears that explains how your audience files must be structured. Use the **[[!UICONTROL Audience Sourcing Specification]](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)** to learn how to format and structure audience data from GCS for Collaboration to read it correctly.

Your audience files must comply with the Audience Sourcing Specification. Match keys are automatically mapped based on the required format.

Key considerations include:

* Files must be in CSV format, using commas as delimiters and pipes (`|`) for multiple values.
* If uploading multiple files, ensure all files contain identical columns.
* Each audience record must include an `AUDIENCE_ID` and at least one match key, such as `HASHED_EMAIL_SHA_256`, `HASHED_PHONE_SHA_256`, `HASHED_IPV4_SHA_256`, `CRM_ID`, `LOYALTY_ID`, or `ADFIXUS_ID`.
* Data refreshes occur on a schedule you set during sourcing setup in Collaboration (typically between one and six days, consistent with other cloud file sources).

### Authenticate your GCS connection {#authenticate-gcs-connection}

Provide the **[!DNL Google Cloud Storage]** credentials and bucket details shown in the UI to connect your bucket to Collaboration. Exact fields depend on the product configuration; complete all required inputs and select **[!UICONTROL Next]** or **[!UICONTROL Continue]** as prompted.

### Confirm consent acknowledgment {#confirm-consent}

Acknowledge any consent or data-use prompts required for your region and use case, then proceed.

### Validate authentication results {#validate-authentication}

After connecting, the system validates your credentials and may display success or error states. If authentication fails, verify bucket name, path, permissions, and credentials with your Google Cloud administrator, then try again.

### Provide connection details {#provide-connection-details}

Enter a descriptive name and optional description for your GCS data connection.

### Review auto-mapped identity fields {#auto-mapped-fields}

The **[!UICONTROL Mapping]** screen is read-only unless the product allows edits. Collaboration maps source identity fields from your audience files to target fields based on the Audience Sourcing Specification. Confirm the mappings and select **[!UICONTROL Next]**.

### Schedule refresh frequency and date range {#schedule-refresh}

Use the **[!UICONTROL Schedule]** view to set refresh frequency and the active date range for sourcing, consistent with [managing data connection scheduling](./manage-data-connection.md#scheduling).

>[!IMPORTANT]
>
>To manage your Collaboration credits effectively, align refresh frequency with how often your underlying GCS data is updated.

### Review and complete the connection {#review-and-complete}

Review the summary of your data connection, details, mapping, and schedule. Select **[!UICONTROL Complete]** (or equivalent) to create the connection.

## Review sourced audiences {#review-sourced-audiences}

After configuration, Collaboration begins sourcing audiences from GCS. Audiences appear in the **[!UICONTROL My audiences]** tab with the same general functionality as audiences sourced from other connections.

If audience sourcing is in progress, a banner may appear at the top of the workspace until processing completes.

>[!TIP]
>
>Audience sourcing time varies based on data volume and the refresh frequency you configured.

When in grid or table view, select an audience or **[!UICONTROL View audience]** to review status, source, data connection name, identities, categories, connection access, and metadata visibility. See [View individual audiences](./onboard-audiences.md#view-individual-audiences) for more detail.

## View your GCS data connection {#view-gcs-connection}

Your GCS connection appears in the **[!UICONTROL My data connections]** tab. To manage match keys, scheduling, and audiences attached to this connection, see [Manage data connections](./manage-data-connection.md). The management workflow is the same as for other audience data connections.

## Next steps {#next-steps}

You have configured [!DNL Google Cloud Storage] as a data source in Collaboration. After sourcing completes, your audiences are available in the **[!UICONTROL My audiences]** workspace. For broader workflows, see [source and manage audiences](./onboard-audiences.md).

For other audience sourcing methods, see:

* [Configure [!DNL Amazon S3] for audience sourcing](./configure-aws-s3-audience-sourcing.md)
* [Source audiences from Experience Platform](./onboard-audiences.md)
* [Upload CSV file for audience sourcing](./upload-csv-audience-sourcing.md)
