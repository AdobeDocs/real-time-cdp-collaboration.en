---
title: Upload CSV file for Audience Sourcing
description: Learn how to upload your CSV file as a self-service data source to ingest audience data into Real-Time CDP Collaboration.
exl-id: bbe45689-1c19-4ee1-bc7a-33a4a48d9b63
---
# Upload CSV file for audience sourcing

This guide provides steps to upload a CSV file in the Adobe Real-Time CDP Collaboration UI to source your audience data for use in collaboration projects.

## Overview {#overview}

CSV file upload is one method to source first-party audience data for collaboration projects. This is an alternative to [connecting your AWS S3 bucket](./configure-aws-s3-audience-sourcing.md) or [sourcing audiences from Experience Platform](./onboard-audiences.md).

Follow this workflow to upload a CSV file containing your audience data to source and manage first-party audiences within Collaboration. You can map identity fields for activation and overlap analysis. Once your file is uploaded and processed, the sourced audience becomes available in the **[!UICONTROL My audiences]** workspace, where you can review, activate, and manage for your collaboration projects.

>[!IMPORTANT]
>
>* Audiences sourced through CSV upload are available for **7 days**. After this period, the audience expires and must be re-uploaded for use in your collaboration projects.
>
>* You can upload one CSV file per session at this time. To add additional audiences, complete the upload workflow again for each file you wish to source.

## Prerequisites {#prerequisites}

Before you can upload CSV files for audience sourcing, ensure you have:

* Completed account onboarding in Real-Time CDP Collaboration. See [Onboard your account](./onboard-account.md) for step-by-step instructions.
* The necessary permissions to add audiences in your organization.
* A CSV file containing your audience data with identity fields such as email or phone.

## Upload a CSV file {#upload-csv-file}

From the **[!UICONTROL My audiences]** tab within the **[!UICONTROL Setup]** workspace, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Audience]**.

If this is your first audience, you may also select the **[!UICONTROL Add]** option.

![The My audiences tab in the Setup workspace with the add icon and Add audience option displayed.](../../assets/setup/add-manage-audiences/add-audiences.png)

The Add audience workflow appears. Select **[!UICONTROL Add a new data connection]** and then select **[!UICONTROL Next]**.

![The Add audiences workspace with the Add a new data connection option highlighted.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Select CSV File as the data connection {#select-csv-file}

Select **[!UICONTROL CSV File]** as a data connection, followed by **[!UICONTROL Next]**.  

![The data connection selection screen with CSV File available as a selectable option.](../../assets/setup/csv-audience-sourcing/select-csv-data-connection.png)

### Select file {#select-file}

Choose **[!UICONTROL Select from computer]** to upload a CSV file from your local system. Alternatively, you can drag and drop the CSV file you want to upload into the [!UICONTROL Drag and drop a CSV file] panel.

>[!IMPORTANT]
>
>Only CSV files are supported. The maximum file size is **2 GB**.

![Select a CSV file containing audience data from your local system.](../../assets/setup/csv-audience-sourcing/select-file.png)

Once uploaded, the UI shows a summary including the number of columns, an estimated row count, the structure of the file, and a preview of the first 10 rows of data.

Review the summary, then select **[!UICONTROL Next]**.

![Preview the sample audience data from your CSV file.](../../assets/setup/csv-audience-sourcing/preview-sample-data.png)

#### Replace file {#replace-file}

If you need to upload a different CSV file, choose **[!UICONTROL Replace file]** and select your new file. The interface then refreshes to display an updated summary of the new data.

After reviewing the revised summary, select **[!UICONTROL Next]**.

![Select the Replace file option to upload a different CSV file.](../../assets/setup/csv-audience-sourcing/replace-file.png)

### Confirm consent acknowledgment {#confirm-consent}

Before proceeding, you must acknowledge that consent opt-outs have been removed from your audience data. Collaboration requires clean audience data without users who have opted out of data sharing.

Check the confirmation box followed by **[!UICONTROL OK]** to confirm. The dialog then closes, and you proceed to the map fields screen.

![The consent opt-out acknowledgment dialog requiring confirmation before proceeding.](../../assets/setup/csv-audience-sourcing/consent-optout-acknowledgment.png)

### Map source identity fields {#map-fields}

Field mapping determines how Collaboration uses your audience data for activation and overlap analysis. On the **[!UICONTROL Map fields]** screen, use the dropdown menus to map each source identity field from your CSV file to the appropriate target field in Collaboration. 

If you need additional details about a target field including the data type or description, select **[!UICONTROL Target fields details]** for more information.

![The dropdown to map a source identity field from your CSV audience data to the target field in Collaboration.](../../assets/setup/csv-audience-sourcing/map-fields.png)

Next, review the mapped fields, and then select **[!UICONTROL Next]**.

![The field mapping screen showing the mapped source and target identity fields.](../../assets/setup/csv-audience-sourcing/confirm-mapped-fields.png)

### Review and complete the upload {#review-and-complete}

The **[!UICONTROL Review]** screen appears with a summary of the audience settings from your CSV file. Review the information in the following sections:

* **[!UICONTROL File Information]**: Displays the file name, the number of columns, and the estimated row count.
* **[!UICONTROL Mapping]**: Lists how the source fields from your uploaded audience file (for example, `email`) map to target fields used in Collaboration (for example, Hashed email).

Select the pencil icon if you need to edit a section. Select **[!UICONTROL Complete]** to confirm all sections.

![Review the summary of upload settings including CSV file information and field mapping details.](../../assets/setup/csv-audience-sourcing/review-upload-summary.png)

A progress bar appears below the summary sections to indicate upload progress. Once the upload completes, a confirmation dialog confirms that your CSV audience was created and audience sourcing is in progress.

![After uploading file, a confirmation dialog appears stating that CSV audience was created and audience sourcing in progress.](../../assets/setup/csv-audience-sourcing/upload-success-sourcing-in-progress.png)

## Review sourced audiences {#review-sourced-audiences}

After uploading your CSV file, Collaboration begins sourcing audiences from the file. This process may take several minutes. When the sourcing finishes, your audiences are available in the **[!UICONTROL My Audiences]** tab with the same features and information as audiences sourced from Experience Platform.

![The Audiences tab showing a list of sourced audiences in grid view.](../../assets/setup/csv-audience-sourcing/csv-audiences-list.png)

When in grid view or table view, select a row item or **[!UICONTROL View audience]** to see an overview of a specific audience. It displays the audience's status, source, and data connection name, along with detailed panels for:

**[!UICONTROL Identities]**: Displays the total identity count and breakdown once data becomes available.
**[!UICONTROL Categories]**: Displays any tags used for organizing or filtering the audience.
**[!UICONTROL Connection access]**: Displays whether the audience is private, public, or shared with specific collaborators.
**[!UICONTROL Metadata visibility]**: Displays what audience information (such as identity count, overlap percentage, and index) is visible to collaborators.

Use this view to confirm audience configuration and visibility settings before using the audience in collaboration projects. For more information, see [how to view an individual audience](./onboard-audiences.md#view-individual-audiences).

## Next steps {#next-steps}

You have now successfully uploaded your CSV file in Collaboration. After sourcing completes, you can:

* Create collaboration projects with your sourced audiences. See [Discover audiences](../../guide/collaborate/discover.md).
* Activate audiences to connected destinations. See [Activate audiences](../../guide/collaborate/activate.md).
* Review audience overlap and insights. See [Measure campaign performance](../../guide/collaborate/measure.md).
* Manage your audience settings and visibility. See [Source and manage audiences](./onboard-audiences.md).

For information about other audience sourcing methods, see [Configure AWS S3 for audience sourcing](./configure-aws-s3-audience-sourcing.md) or [Source audiences from Experience Platform](./onboard-audiences.md).
