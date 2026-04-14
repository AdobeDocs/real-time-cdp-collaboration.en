---
title: Manage measurement data connections
description: Learn how to manage measurement data connections, including details and match keys in Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: dfe72315-6fcc-4ad7-b100-fc992ba9abbc
---
# Manage measurement data connections

{{limited-availability-release-note}}

## Overview

Use measurement data connections in Real-Time CDP Collaboration to source your conversion data from various platforms. Learn how to manage details and match keys for your existing data connections.

## View measurement data connections {#view-measurement-data-connections}

You can view details for any existing measurement data connection, including how your conversion data is sourced, which match keys are in use, and all conversion events linked to the connection.

From the **[!UICONTROL Setup]** workspace, navigate to the **[!UICONTROL My data connections]** tab. All your current measurement data connections are displayed under the **[!UICONTROL Measurement]** section in tabular or grid view. Select **[!UICONTROL View data connection]** on the relevant connection card, or select the data connection name when in table view to open its workspace and view all details. 

![The My data connections tab highlighting a measurement data connection card and the View data connection option.](/help/assets/setup/manage-measurement-data-connection/view-measurement-data-connection.png){zoomable="yes"}

### Measurement data connection details {#measurement-data-connection-details}

In this section, you can see the following details of the data connection:

| Field             | Description |
|-------------------|-------------|
| Status            | The current state of the measurement data connection, for example, **[!UICONTROL Active]**. |
| Source            | The platform or system providing the measurement data for this connection. |
| Sandbox           | The name of the sandbox where the measurement data connection is configured. |
| Dataset           | The name of the dataset used for sourcing measurement data in the connection. |
| Last updated      | The timestamp of the most recent update to the measurement data connection. |
| Last updated by   | The user that last modified the measurement data connection. |
| Created           | The timestamp when the measurement data connection was created. |
| Created by        | The user that originally created the measurement data connection. |

{style="table-layout:auto"}

### Match keys {#match-keys}

Match keys are the target fields you mapped your source fields to when you [source your measurement data](./onboard-measurement-data.md). To learn more about how match keys work, see the [match keys](./onboard-account.md#set-up-match-keys) guide.

![A measurement data connection workspace with the Match keys section highlighted.](/help/assets/setup/manage-measurement-data-connection/view-match-keys.png){zoomable="yes"}

### Conversion events {#conversion-events}

A list of conversion events attached to the data connection are displayed at the bottom of the workspace. The list displays a brief overview of each event, including its status, conversion type, and source. You can select the event name to view and edit its configurations, or remove the conversion event with the delete option (![Delete icon](/help/assets/common/delete.svg)). For a complete guide on managing a conversion event, refer to the [add and manage measurement data](./onboard-measurement-data.md) guide.

![A measurement data connection workspace with the conversion events section highlighted.](/help/assets/setup/manage-measurement-data-connection/view-conversion-events.png){zoomable="yes"}

## Edit measurement data connection {#edit-measurement-data-connection}

You can update the details and match keys of an existing measurement data connection at any time to ensure your reporting and analysis remain accurate. To begin, navigate to the **[!UICONTROL My data connections]** tab and select the measurement data connection you want to edit. This opens the data connection workspace, where you can follow the steps below to make necessary changes.

### Edit name and description {#edit-name-and-description}

To update the data connection's name and description, select the edit icon (![Edit icon](/help/assets/icons/edit.png)) next to the current connection name.

![The measurement data connection workspace highlighting the Edit icon next to the data connection name.](/help/assets/setup/manage-measurement-data-connection/edit-name-description.png){zoomable="yes"}

In the **[!UICONTROL Edit data connection]** dialog, update the fields with the desired values, then select **[!UICONTROL Save]** to apply your changes. 

![The Edit data connection dialog with the Save option highlighted.](/help/assets/setup/manage-measurement-data-connection/edit-name-description-dialog.png){zoomable="yes"}

A confirmation dialog appears to confirm that the details were successfully updated.

### Edit match keys {#edit-match-keys}

>[!IMPORTANT]
>
>Before editing the match keys for a data connection, note the following:
>
>* Only match keys that are configured for your account can be used for data connections.
>* At this time, you can add additional match keys to a data connection, but once a match key is enabled, it cannot be removed.

In the data connection workspace, select **[!UICONTROL Edit]** within the **[!UICONTROL Match keys]** panel.

![The Match keys section with the Edit option highlighted.](/help/assets/setup/manage-measurement-data-connection/edit-match-keys.png){zoomable="yes"}

A confirmation dialog appears, explaining that any changes to the data connection will apply to all associated conversions. Select **[!UICONTROL OK]** to confirm. You can choose to skip this confirmation in the future.

![Confirmation dialog showing that any changes to the data connection will apply to all associated conversions.](/help/assets/setup/manage-measurement-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

In the **[!UICONTROL Match keys]** dialog, you can review enrichment settings and see the current mappings between your source fields and the target fields (match keys). 

![The Match keys dialog showing the enrichment settings and existing mappings between source fields and the corresponding target fields.](/help/assets/setup/manage-measurement-data-connection/edit-match-keys-dialog.png){zoomable="yes"}

#### Enrichment {#enrichment}

If enrichment was not enabled when you [sourced your measurement data](./onboard-measurement-data.md), you have the option to enrich your event dataset with attributes from Real‑Time Customer Profile. Note that once enrichment is turned on for measurement data, it cannot be disabled. You can still update the enrichment join keys as needed.

When you enable enrichment in the **[!UICONTROL Match keys]** dialog, the UI expands to display more configuration options under the **[!UICONTROL Enrich your event data with IDs from profiles]** section.

Select the **[!UICONTROL Source field join key]** option.

![The Match keys dialog with the Source field join key option highlighted.](../../assets/setup/manage-measurement-data-connection/enrich-event-data.png){zoomable="yes"}

In the **[!UICONTROL Source field join key]** dialog, choose the source field, followed by **[!UICONTROL Select]**.

![The Source field join key dialog highlighting the selected source field and the Next option.](../../assets/setup/manage-measurement-data-connection/source-field-join-key-dialog.png){zoomable="yes"}

Next, select the **[!UICONTROL Profile join key]** option. In the **[!UICONTROL Profile join key]** dialog, select the profile field from the list. You can use the Search option to find the desired field. Then, choose **[!UICONTROL Select]** to confirm.

![The Profile join key dialog highlighting the selected profile field and the Select option.](../../assets/setup/manage-measurement-data-connection/profile-join-key-dialog.png){zoomable="yes"}

#### Edit mapping {#edit-mapping}

To edit an existing match key, update its associated source field and target field within the **[!UICONTROL Match keys]** dialog. If you want to include a new match key, select **[!UICONTROL Add field]**. This creates an empty row where you can define additional mapping between source and target fields.

![After selecting Add field, the Match keys dialog displays an empty new mapping row ready for input.](/help/assets/setup/manage-measurement-data-connection/add-new-field.png){zoomable="yes"}

Next, select the empty source field. The **[!UICONTROL Select source field]** dialog appears with a list of available source fields grouped under options such as **[!UICONTROL Identity namespaces]** and **[!UICONTROL Profile attributes]**. You can filter the list and find the desired source field with the search option.

Choose the source field that you want, followed by **[!UICONTROL Select]**. 

![The Select source field dialog highlighting the Search option, the Phone source field, and the Select option.](/help/assets/setup/manage-measurement-data-connection/select-source-field.png){zoomable="yes"}

In the **[!UICONTROL Match keys]** dialog, use the dropdown menu to map the new source field to a target field. All available target fields are the match keys configured for your Collaborator account. If you don't see the target field you need, [edit your account's match keys](./onboard-account.md#edit-match-keys) to add it.

Use the **[!UICONTROL Apply transformation]** option if you want to source a non-hashed field to a hashed target field, for example, when mapping a plain text phone source field to the **[!UICONTROL Hashed phone]** target field.

![The dropdown menu displaying all available target fields to map with the new source field.](/help/assets/setup/manage-measurement-data-connection/target-field-dropdown.png){zoomable="yes"}

After you finish mapping fields, review your updates and select **[!UICONTROL Confirm]** to apply the changes.

![The Match keys dialog showing the updated field mapping with the Confirm option highlighted.](/help/assets/setup/manage-measurement-data-connection/confirm-edit-match-keys.png){zoomable="yes"}

A confirmation dialog confirms that the match keys were updated successfully.

## Delete data connection

Deleting a data connection will remove all underlying conversions, associated settings, and usage across Collaboration. This action cannot be undone.

To delete an existing data connection, select the delete icon (![Delete icon](/help/assets/common/delete.svg)) within an individual data connection's workspace.

![A data connections workspace with the delete option highlighted.](/help/assets/setup/manage-measurement-data-connection/delete-measurement-data-connection.png){zoomable="yes"}

A confirmation dialog appears. Select **[!UICONTROL Delete]** to finish deleting the data connection.

![The Delete data connection dialog with the Delete option highlighted.](/help/assets/setup/manage-measurement-data-connection/delete-measurement-data-connection-confirm.png){zoomable="yes"}

A confirmation dialog confirms that the data connection was deleted successfully.

## Next steps {#next-steps}

After managing your measurement data connections, you can:

* Add more conversion events linked to your data connection as needed. For detailed steps, read the [add and manage measurement data](./onboard-measurement-data.md) documentation.
* Generate measurement reports to gain insights into your campaign's performance and impact. For more information on available report types and how to create them, see the [measure performance](/help/guide/collaborate/measure.md) guide.
