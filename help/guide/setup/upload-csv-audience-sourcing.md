---
title: Upload CSV files for Audience Sourcing
description: Learn how to upload your CSV file as a self-service data source to ingest audience data into Real-Time CDP Collaboration.
---
# Upload CSV files for audience sourcing

Learn how to upload CSV files in the Adobe Real-Time CDP Collaboration UI to source audience data for activation and analysis.

## Overview {#overview}

Follow this workflow to upload CSV files containing your audience data to source and manage first-party audiences within Collaboration.

>[!NOTE]
>
>You can upload one CSV file per session at this time. To add additional audiences, complete the upload workflow again for each file you wish to source.

## Upload a CSV file {#upload-csv-file}

From the **[!UICONTROL My audiences]** tab within the **[!UICONTROL Setup]** workspace, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Audience]**.

If this is your first audience, you may also select the **[!UICONTROL Add]** option.

![The My audiences tab in the Setup workspace with the add icon and Add audience option displayed.](../../assets/setup/add-manage-audiences/add-audiences.png)

The Add audience workflow appears. Select **[!UICONTROL Add a new data connection]** and then select **[!UICONTROL Next]**.

![The Add audiences workspace with the Add a new data connection option highlighted.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Select CSV File as the data connection {#select-csv-file}

Select **[!UICONTROL CSV File]** as a data connection, followed by **[!UICONTROL Next]**.  

![The data connection selection screen with CSV File available as a selectable option.](../../assets/setup/)

<!-- SCREENSHOT for select csv file as data connection here -->

### Select file {#select-file}

Select **[!UICONTROL Select from computer]** to upload a CSV file from your local system. Alternatively, you can drag and drop the CSV file you want to upload into the [!UICONTROL Drag and drop a CSV file] panel.

>[!TIP]
>
>Only CSV files are supported. The maximum file size for each file is 2 GB.

Once your file is uploaded, the UI shows a summary including the number of columns, an estimated row count, the structure of the file, and a preview of the first 10 rows of data.

Select **[!UICONTROL Next]** to continue.

#### Replace file {#replace-file}

If you wish to upload another CSV file, select **[!UICONTROL Replace file]**. When finished, select **[!UICONTROL Next]**.

### Confirm consent acknowledgment {#confirm-consent}

You must then acknowledge that consent opt-outs have been removed before proceeding. Check the confirmation box followed by **[!UICONTROL OK]** to confirm.

![The consent opt-out acknowledgment dialog requiring confirmation before proceeding.](../../assets/setup/aws-audience-sourcing/consent-optout-acknowledgment.png)

### Update source identity fields {#update-mapped-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_csv_target_field_details"
>title="Target field details"
>abstract="Target fields include ID or name of the audience segment. Each field is limited to 255 characters."

On the **[!UICONTROL Map fields]** screen, you can map fields directly, add or remove fields based on your needs. 

Use the dropdowns to map source identity fields from your audience files to target fields.

<!-- SCREENSHOT for mapping fields -->

<!-- DRAFT To add a new mapping field, select **[!UICONTROL Add field]**.
To remove a mapped field, select the delete icon (![Add icon.](/help/assets/icons/delete.png)) next to the corresponding field row. -->

Next, confirm the mapped fields, and then select **[!UICONTROL Next]** to continue.

### Review and complete the connection {#review-and-complete}

The **[!UICONTROL Review]** screen appears with a summary of the data connection from your CSV audience file. Review the information in the following sections:

* **[!UICONTROL File Information]**: Displays the file name, the number of columns, and the estimated row count.
* **[!UICONTROL Mapping]**: Lists how the source fields from your uploaded audience files (for example, `HASHED_EMAIL`) map to target fields used in Collaboration (for example, Hashed email).

Select the pencil icon if you need to edit a section. Select **[!UICONTROL Complete]** to confirm all sections.

<!-- SCREENSHOT of Review screen -->

A progress bar below the summary sections appears showing that the CSV file is uploading. Once the upload completes, a confirmation dialog notifies you that the data connection was created successfully and that audience sourcing in progress.

## Review sourced audiences {#review-sourced-audiences}

## View your CSV data connection {#view-csv-connection}

## Next steps {#next-steps}
