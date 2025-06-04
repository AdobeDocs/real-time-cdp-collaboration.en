---
title: Manage data connections
description: Learn how to manage data connections, including match keys, scheduling, use cases, and audience filtering in Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
---
# Manage data connections

{{limited-availability-release-note}}

## Overview

Use data connections in Real-Time CDP Collaboration to import audiences from various sources. Learn how to manage match keys and schedule data imports for your existing data connections. Additionally, you'll be able to filter audiences by different attributes for more granular insights.

## View data connections

To view existing data connections, navigate to **[!UICONTROL Setup]** and then select the **[!UICONTROL My data connections]** tab. All your current data connection are displayed, showing a brief overview for each connection. For a complete view of a data connection's information, including its match keys, scheduling details, and audiences, select **[!UICONTROL View data connection]** on the corresponding connection.

![Setup workspace with My data connections tab view displayed and highlighted.](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### Match keys {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Match keys"
>abstract="Match keys determine how data from different sources will be matched. Choose the match keys that are most relevant to your use cases and privacy guidelines."

Match keys are identifiers used to reconcile members across audiences from different data sources. You cannot edit the match keys you initially selected for your data connection. 

Available match keys include:

- **Hashed email**

![A data connections workspace with the Match keys section highlighted.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Scheduling {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Scheduling"
>abstract="View the scheduling details for your data connection, and edit refresh frequency if required."

View and manage the scheduling settings for your data connections. Scheduling determines how often audience data is refreshed from the source system.

After a data connection is created, you can update its refresh frequency directly from the **[!UICONTROL Scheduling]** section of the data connection workspace.

>[!NOTE]
>
>The first export from Real-Time CDP occurs within 24 hours after the audience is sourced. After the initial export, Real-Time CDP refreshes audience data according to the defined frequency.

For more information about scheduling options during audience import, see the [scheduling section](/help/guide/setup/onboard-audiences.md#schedule) in the audience import workflow guide.

![A data connections workspace with the Scheduling section highlighted.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes" alt="The Scheduling section in the data connection workspace, showing frequency and date range settings."}

#### Edit scheduling {#edit-scheduling}

You can edit the frequency of an existing data connection to better control how often audiences are refreshed. To edit the schedule, select **[!UICONTROL Edit]**. 

In the **[!UICONTROL Scheduling]** dialog, select the dropdown menu to update the **[!UICONTROL Frequency]**. Set the refresh frequency to run daily or every two to six days. When you're done, select **[!UICONTROL Save]** to apply your changes.

>[!IMPORTANT]
>
>You can update the refresh frequency. Other data connection settings, such as match keys, cannot be changed.

![The Scheduling dialog, showing options to set frequency and date range.](../../assets/setup/manage-data-connection/scheduling-dialog.png){zoomable="yes" alt="The Scheduling dialog with editable fields for frequency."}

## Delete data connection

Deleting a data connection will remove all underlying audiences, associated settings, and usage across the platform. This action cannot be undone.

To delete an existing data connection, select the delete icon (![Delete icon](/help/assets/common/delete.svg)) within an individual data connection's workspace.

![A data connections workspace with the delete option highlighted.](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

A confirmation dialogue will appear. Select **[!UICONTROL Delete]** to finish deleting the data connection.

![The Delete data connection dialog with the Delete option highlighted.](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## Manage audiences {#manage-audiences}

A list of audiences attached to the data connection are displayed at the bottom of the workspace. THe list displays a brief overview of each audience, including its status, source, and connection access. To edit an audience's categories, connection access, or metadata visbility, select the audience's name. For a complete guide on managing an audience, refer to the [view individual audiences](./onboard-audiences.md#view-individual-audiences) guide.

![A data connections workspace with the audiences highlighted.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Next steps

After managing your data connections, you can [discover overlaps](/help/guide/collaborate/discover.md) between your audiences and the audiences that your collaborator has made discoverable.
