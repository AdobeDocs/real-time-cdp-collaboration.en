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

As the owner of a collaboration connection, you can edit the connection settings with your collaborator after the connection is established. You can:

* Add use cases
* Add match keys. Match key removal will be supported in the future.
* Update audience activation permissions
* Update credit split settings

>[!IMPORTANT]
>
>Once a use case or match key is added to a connection, it cannot be removed.

>[!TIP]
>
>The **owner** is the collaborator who initiates the connection by sending the invite to the **recipient**. For more information, see the [establishing connections with collaborators documentation](./establishing-connections.md).

To edit connection settings, navigate to the connection settings workspace. Select the three dots icon (![Three dots icon.](/help/assets/icons/more.png)) to view available actions, then select **[!UICONTROL Edit]**.

![The connection settings workspace with the Edit option highlighted.](/help/assets/connect/manage-connections/edit-connection.png){zoomable="yes"}

A dialog appears, prompting you to edit and submit the settings changes for collaborator review. Select **[!UICONTROL Edit]**.

![The Edit connection settings dialog with the Edit option highlighted.](/help/assets/connect/manage-connections/edit-connection-settings-dialog.png){zoomable="yes"}

### Edit audience activation {#edit-audience-activation}

Audience activation settings determine which collaborator in the connection can activate audiences to destinations. To change these settings, select **[!UICONTROL Edit]** within the **[!UICONTROL Audience activation]** section.

![The edit connection settings screen showing the Audience activation section and the Edit option.](/help/assets/connect/manage-connections/edit-audience-activation.png){zoomable="yes"}

In the **[!UICONTROL Audience activation]** dialog, use the dropdown menu to update the audience activation permissions. You can choose a single collaborator or allow both collaborators to activate audiences. 

![The Audience activation dialog highlighting dropdown menu expanded for updating the audience activation permissions.](/help/assets/connect/manage-connections/audience-activation-dropdown-menu.png){zoomable="yes"}

Once finished, select **[!UICONTROL Save]**.

![The Audience activation dialog showing the new audience activation permissions and the Save option.](/help/assets/connect/manage-connections/audience-activation-dialog.png){zoomable="yes"}

### Add use cases {#add-use-cases}

In Collaboration, use cases such as Discover, Activate, and Measure determine which project sections and features you can use with your collaborator. You can add additional use cases to an existing connection for future projects. For more information, see [collaboration use cases](../overview/use-cases.md).

To add new use cases, select **[!UICONTROL Edit]** in the **[!UICONTROL Use cases]** section.

![The edit connection settings screen highlighting the Use cases section and the Edit option.](/help/assets/connect/manage-connections/edit-use-cases.png){zoomable="yes"}

In the **[!UICONTROL Use cases]** dialog, toggle on new use cases you want to add, followed by **[!UICONTROL Save]**.

![The Use cases dialog displaying the Save option highlighted.](/help/assets/connect/manage-connections/use-cases-dialog.png){zoomable="yes"}

>[!NOTE]
>
>When you [add new use cases](#add-use-cases) such as "Audience activation" or "Measurement", the edit connection settings screen updates to include the **[!UICONTROL Audience activation]** and **[!UICONTROL Credit split]** sections. You must configure the appropriate settings for these new use cases. For more details, see the [audience activation](../connect/establishing-connections.md#audience-activation) and [credit split](../connect/establishing-connections.md#credit-split) guides.
>
>![The edit connection settings screen displaying Audience activation and Credit split sections after new use cases are added.](/help/assets/connect/manage-connections/setup-audience-activation-credit-split.png){zoomable="yes"}

### Add match keys {#add-match-keys}

Only match keys that are configured in your account and also selected by your collaborator are available for the connection. Once you [add new match keys to your account](../setup/onboard-account.md#edit-match-keys) and your collaborator also selects the same keys, you can enable them within your existing connections.

In the edit connection settings screen, select **[!UICONTROL Edit]** within the **[!UICONTROL Match keys]** section.

![The edit connection settings screen highlighting the Match keys section and Edit option.](/help/assets/connect/manage-connections/edit-connection-match-keys.png){zoomable="yes"}

A **[!UICONTROL Match keys]** dialog appears, showing the existing match keys configured for the connection. Select the match keys you want to add, followed by **[!UICONTROL Save]**.

![The Match keys dialog displaying the new match keys selected and the Save option.](/help/assets/connect/manage-connections/connection-match-keys-dialog.png){zoomable="yes"}

### Edit credit split {#edit-credit-split}

The credit split settings specify which collaborator is responsible for the costs associated with each use case in the connection. To update these settings, select **[!UICONTROL Edit]** in the **[!UICONTROL Credit split]** section.

![The edit connection settings screen highlighting the Credit split section and the Edit option.](/help/assets/connect/manage-connections/edit-credit-split.png){zoomable="yes"}

In the **[!UICONTROL Credit split]** dialog, select the preferred settings for [!UICONTROL Activation-Matching] and [!UICONTROL Measurement]. Then, select **[!UICONTROL Save]** to confirm.

![The Credit split dialog showing the credit split settings and the Save option.](/help/assets/connect/manage-connections/credit-split-dialog.png){zoomable="yes"}

### Review and submit changes {#review-and-submit-changes}

When you complete editing the connection settings, review and select **[!UICONTROL Submit changes]**. The connection settings updates will be sent to your collaborator for review.

![The edit connection settings screen displaying the updates and the Submit changes option.](/help/assets/connect/manage-connections/review-and-submit-changes.png){zoomable="yes"}

#### Save connection settings changes as draft

You can save the connection settings changes as a draft and return to finish updating the connection settings at any time. 

To save the changes as a draft, select **[!UICONTROL Cancel]** next to **[!UICONTROL Submit changes]**. Then, in the **[!UICONTROL Unsubmitted changes]** dialog, select **[!UICONTROL Continue later]** to confirm.

![The edit connection settings screen.](/help/assets/connect/manage-connections/unsubmitted-changes-dialog.png){zoomable="yes"}

Your changes are now saved as a draft. In the connection settings workspace, you can see a notification indicating that there are unsubmitted changes. To make further updates, select **[!UICONTROL Continue editing]**.

![A notification in the connection settings workspace showing there are unsubmitted changes pending review and submission.](/help/assets/connect/manage-connections/continue-editing-connection.png){zoomable="yes"}
