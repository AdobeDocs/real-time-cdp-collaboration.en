---
title: Desintations overview
description: Learn about destinations in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 5cbbf5c4-4caa-40da-97be-690d95c1201c
---
# Destinations overview

{{limited-availability-release-note}}

Destinations are integrations used to send targeted audiences to external platforms. These integrations enable you to activate audiences across various marketing channels and platforms for use in campaigns and customer engagement.

Collaborators can configure destinations to send audiences to external platforms, such as Adobe Experience Platform, for use in campaigns. Collaborators can then [activate audiences within a project](../collaborate/activate.md), which are sent to their connection's configured destination. Activation can be done by either collaborator depending on the audience activation settings [configured in the connection](/help/guide/connect/establishing-connections.md#configure-connection-settings).

>[!IMPORTANT]
>
>Currently, when collaborators activate audiences within a project, they are automatically sent to their connection's configured destination. You **must** configure a destination before your collaborator can activate audiences within a project. 

## Configure destinations {#configure-destinations}

To configure a destination, navigate to **[!UICONTROL Setup]** and then select the **[!UICONTROL My destinations]** tab. Here, you can view all available destinations.

>[!NOTE]
>
> Currently, only Adobe Experience Platform is available as a self-serve destination within Collaboration. If you are interested in configuring a destination such as Amazon S3 or Snowflake, please contact your Adobe representative.

![The My destinations tab in the Setup workspace showing the available destinations.](/help/assets/destinations/overview/my-destinations-overview.png)

To begin configuring a destination, select the **[!UICONTROL Set up]** option within the destination of your choice. For information on configuring specific destinations, refer to the guides in the [available destinations](#available-destinations) table.

![The My destinations workspace with the Set up option highlighted for the Adobe Experience Platform desintation.](/help/assets/destinations/overview/my-destinations-set-up.png)

### Available destinations {#available-destinations}

The following destinations are available for configuration in Collaboration. To view the configuration guide for that destination, select the destination name in the table below. If you are interested in configuring a destination that is not currently available, please contact your Adobe representative.

| Destination | Availability |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | Available |
| Amazon S3 | Coming soon. |
| Snowflake | Coming soon. |
| Google Cloud Storage | Coming soon. |
| Azure Blob Storage | Coming soon. |

## Next steps

Once you've configured your destination, you can begin [activating targeted audiences](../collaborate/activate.md) within your projects.
