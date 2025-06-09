---
title: Configure and manage destinations
description: Learn how to configure and manage destinations in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
---
# Configure and manage destinations

{{limited-availability-release-note}}

Destinations are integrations used to send targeted audiences to external platforms. These integrations enable you to activate audiences across various marketing channels and platforms for use in campaigns and customer engagement.

Currently, destinations are only available to publishers in Real-Time CDP Collaboration. Publishers can configure destinations to send audiences to external platforms, such as Adobe Experience Platform, for use in campaigns. Advertisers can then [activate audiences within a project](../collaborate/activate.md), which are sent to the publisher's configured destination.

![The My destinations tab in the Setup workspace showing an active Adobe Experience Platform destinations](/help/assets/setup/manage-destinations/my-destinations-overview.png)

To learn more about destinations, refer to the [destinations overview](../destinations/overview.md) guide.

## Configure destinations {#configure-destinations}

Desintations are configured in the **[!UICONTROL Setup]** section of Real-Time CDP Collaboration. To configure a destination, navigate to **[!UICONTROL Setup]** and then select the **[!UICONTROL My destinations]** tab. Here, you can view all available destinations.

>[!IMPORTANT]
>
>To configure and manage desintations, your user must have a role with the **Manage Audience Data** permission assigned to them. For more information about managing roles, refer to the [manage roles](../permissions/manage-roles.md) guide.

![The My destinations tab in the Setup workspace showing the available destinations.](/help/assets/setup/manage-destinations/my-destinations.png)

The set up process for destinations is dependent on the destination you are configuring. Refer to the [available destinations](../destinations/overview.md#available-destinations) catalog to view the available destinations and their configuration guides.

>[!NOTE]
>
>Currently, only Adobe Experience Platform is available as a self-serve destination within Real-Time CDP Collaboration. If you are interested in configuring a different destination, please contact your Adobe representative.

## Delete destinations {#delete-destinations}

Deleting a destination removes it from your organization, removes any previously sent audiences from the desination, and prevents any future audiences from being sent to that destination.

To delete a destination, navigate to the **[!UICONTROL My destinations]** tab in the **[!UICONTROL Setup]** section. Select the **[!UICONTROL Delete]** option for the destination that you want to remove.

![The My destinations workspace with the Delete option highlighted for the Adobe Experience Platform destination.](/help/assets/setup/manage-destinations/delete-destination.png)

A confirmation dialog appears, where you can confirm that you want to delete the destination. Select **[!UICONTROL Delete]** to remove the destination.

![The Delete destination dialog with the Delete option highlighted.](/help/assets/setup/manage-destinations/delete-destination-confirm.png)

## Next steps

Once you've configured your destination, you can begin collaborating with your advertisers to [activate targeted audiences](../collaborate/activate.md) within your projects.
