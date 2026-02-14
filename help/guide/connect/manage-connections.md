---
title: Manage connections
description: Learn how to manage your connections in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 50120839-4a20-4ec1-8887-9342bd17c52d
---
# Manage connections {#manage-connections}

{{limited-availability-release-note}}

The **[!UICONTROL My connections]** workspace provides a centralized location for managing your connections. You can view existing connections in the **[!UICONTROL Existing connections]** section and see any connections that require action in the **[!UICONTROL Action required]** section.

## View connection {#view-connection}

To view your existing connections, navigate to the **[!UICONTROL Connect]** workspace. As a publisher, your existing connection will be displayed. As an advertiser, you should then navigate to **[!UICONTROL My connections]**.

![The View connection option highlighted for a connection in the My connections workspace.](/help/assets/connect/manage-connections/view-connection.png){zoomable="yes"}

The connection overview workspace appears, displaying details about the connection and its active projects. Select **[!UICONTROL Connection settings]** to view the connection settings.

![The Connection settings option highlighted in the connection overview workspace.](/help/assets/connect/manage-connections/connection-overview.png){zoomable="yes"}

The connection settings workspace appears, displaying the connection details between you and your collaborator. Here, you can view all the settings selected during the connection process, the current status of the connection, the connection owner, and the contact information for your collaborator. For information on specific connection settings, see the [connection settings](/help/guide/connect/establishing-connections.md#connection-settings) guide.

![The connection settings workspace displaying connection details.](/help/assets/connect/manage-connections/connection-settings.png){zoomable="yes"}

## Delete connection {#delete-connection}

You can delete any connections with collaborators that you do not want to continue working with. To delete a connection, navigate to the connection you wish to delete and then select the delete icon ![delete icon](/help/assets/common/delete.svg) in the connection workspace.

![The delete icon highlighted in the connection workspace.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

A confirmation dialog appears, asking you to confirm the deletion of the connection. Select **[!UICONTROL Delete]** to confirm the deletion.

![The confirmation dialog to delete a connection.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Once the connection is deleted, all existing projects in the collaboration will be permanently deleted and unrecoverable. The connection request will remain in a pending state within the **[!UICONTROL Action required]** section within **[!UICONTROL My connections]**, but the connection and its configurations will no longer be active. You will need to re-establish the connection if you want to connect with the collaborator again.

## Edit connection {#edit-connection}

If you are the owner of a collaboration connection, you can edit the connection settings with your collaborator even after the connection has been established. Note that you cannot change the existing configuration of the connection.

>[!TIP]
>
>The **owner** is the collaborator who initiates the connection by sending the invite to the **recipient**. For more information, see the [establishing connections with collaborators](./establishing-connections.md).

To edit a connection, navigate to its connection settings workspace. Select the three dots icon (![Three dots icon.](/help/assets/icons/more.png)) to view available actions. Then, select **[!UICONTROL Edit]**.

![The connection settings workspace with the Edit option highlighted.](/help/assets/connect/establish-connection/edit-connection.png){zoomable="yes"}

A dialog appears, prompting you to edit and submit the settings changes for collaborator review. Select **[!UICONTROL Edit]**.

![The Edit connection settings dialog with the Edit option highlighted.](/help/assets/connect/establish-connection/edit-connection-settings-dialog.png){zoomable="yes"}

### Add use cases {#add-use-cases}

You can include additional use cases in your projects with a collaborator. For details about available use cases, see [collaboration use cases](../overview/use-cases.md) documentation.

To add new use cases, select **[!UICONTROL Edit]** in the **[!UICONTROL Use cases]** section. 

In the **[!UICONTROL Use cases]** dialog, toggle on the new use cases you want to add, followed by **[!UICONTROL Save]**.

![The Use cases dialog displaying the new use cases selected and the Save option highlighted.](/help/assets/connect/establish-connection/edit-use-cases.png){zoomable="yes"}

### Edit audience activation and credit split {#edit-audience-activation-credit-split}

When you add `Audience activation` as a new use case, the edit connection settings screen updates to display both the **[!UICONTROL Audience activation]** and **[!UICONTROL Credit split]** sections. If you add only `Measurement` use case, the screen shows only the **[!UICONTROL Credit split]** section. 

To configure audience activation or credit split, select **[!UICONTROL Set up]** within each relevant section. For detailed instructions, see the [audience activation](../connect/establishing-connections.md#audience-activation) and [credit split](../connect/establishing-connections.md#credit-split) guides.

![The edit connection settings screen displaying Audience activation and Credit split sections after new use cases are added.](/help/assets/connect/establish-connection/audience-activation-credit-split.png){zoomable="yes"}

### Add match keys {#add-match-keys}

After [adding new match keys in your Collaborator account](../setup/onboard-account.md#edit-match-keys), you can enable these match keys for your existing connections.

In the edit connection settings screen, select **[!UICONTROL Edit]** within the **[!UICONTROL Match keys]** section.

![.](/help/assets/connect/establish-connection/edit-match-keys.png){zoomable="yes"}
