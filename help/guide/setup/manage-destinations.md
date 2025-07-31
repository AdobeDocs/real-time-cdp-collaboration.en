---
title: Configure and manage destinations
description: Learn how to configure and manage destinations in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b4b26761-46ac-420f-b9f7-6e829d67aec9
---
# Configure and manage destinations

{{limited-availability-release-note}}

Destinations are integrations used to send targeted audiences to external platforms. These integrations enable you to activate audiences across various marketing channels and platforms for use in campaigns and customer engagement.

Collaborators can configure destinations to send audiences to external platforms, such as Adobe Experience Platform, for use in campaigns. Collaborators can then [activate audiences within a project](../collaborate/activate.md), which are sent to their connection's configured destination. Activation can be done by either collaborator depending on the audience activation settings [configured in the connection](/help/guide/connect/establishing-connections.md#configure-connection-settings).

![The My destinations tab in the Setup workspace showing an active Adobe Experience Platform destinations.](/help/assets/setup/manage-destinations/my-destinations-overview.png)

To learn more about destinations, refer to the [destinations overview](../destinations/overview.md) guide.

## Configure destinations {#configure-destinations}

Desintations are configured in the **[!UICONTROL Setup]** section of Collaboration. To configure a destination, navigate to **[!UICONTROL Setup]** and then select the **[!UICONTROL My destinations]** tab. Here, you can view all available destinations.

>[!IMPORTANT]
>
>To configure and manage desintations, your user must have a role with the **Manage Audience Data** permission assigned to them. For more information about managing roles, refer to the [manage roles](../permissions/manage-roles.md) guide.

![The My destinations tab in the Setup workspace showing the available destinations.](/help/assets/setup/manage-destinations/my-destinations.png)

The set up process for destinations is dependent on the destination you are configuring. Refer to the [available destinations](../destinations/overview.md#available-destinations) catalog to view the available destinations and their configuration guides.

>[!NOTE]
>
>Currently, only Adobe Experience Platform is available as a self-serve destination within Real-Time CDP Collaboration. If you are interested in configuring a different destination, please contact your Adobe representative.

## Delete destinations {#delete-destinations}

Deleting a destination removes it from your account, removes any previously sent audiences from the destination, and prevents any future audiences from being sent to that destination.

To delete a destination, navigate to the **[!UICONTROL My destinations]** tab in the **[!UICONTROL Setup]** section. Select the **[!UICONTROL Delete]** option for the destination that you want to remove.

![The My destinations workspace with the Delete option highlighted for the Adobe Experience Platform destination.](/help/assets/setup/manage-destinations/delete-destination.png)

A confirmation dialog appears, where you can confirm that you want to delete the destination. Select **[!UICONTROL Delete]** to remove the destination.

![The Delete destination dialog with the Delete option highlighted.](/help/assets/setup/manage-destinations/delete-destination-confirmation.png)

## Next steps

Once you've configured your destination, you can begin collaborating within your connections to [activate targeted audiences](../collaborate/activate.md) within your projects.
