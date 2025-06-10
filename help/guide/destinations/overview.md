---
title: Desintations overview
description: Learn about destinations in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
---
# Destinations overview

{{limited-availability-release-note}}

Destinations are integrations used to send targeted audiences to external platforms. These integrations enable you to activate audiences across various marketing channels and platforms for use in campaigns and customer engagement.

Currently, destinations are only available to publishers in Real-Time CDP Collaboration. Publishers can configure destinations to send audiences to external platforms, such as Adobe Experience Platform, for use in campaigns. Advertisers can then [activate audiences within a project](../collaborate/activate.md), which are sent to the publisher's configured destination.

>[!IMPORTANT]
>
>Currently, when advertisers activate audiences within your project, they are automatically sent to a publisher's configured destination. As a publisher, you **must** configure a destination *before* your collaborator activates an audience. If no destination is configured, the audience will be sent to you and visible in the **[!UICONTROL Activate]** tab within a project, but will not be activated. 

## Configure destinations {#configure-destinations}

To configure a destination, navigate to **[!UICONTROL Setup]** and then select the **[!UICONTROL My desintations]** tab. Here, you can view all available destinations.

>[!NOTE]
>
> Currently, only Adobe Experience Platform is available as a self-serve destination within Real-Time CDP Collaboration. If you are interested in configuring a destination such as Amazon S3 or Snowflake, please contact your Adobe representative.

![The My destinations tab in the Setup workspace showing the available destinations.](/help/assets/destinations/overview/my-destinations-overview.png)

To begin configuring a destination, select the **[!UICONTROL Set up]** option within the destination of your choice. For information on configuring specific destinations, refer to the guides in the [available destinations](#available-destinations) table.

![The My destinations workspace with the Set up option highlighted for the Adobe Experience Platform desintation.](/help/assets/destinations/overview/my-destinations-set-up.png)

### Available destinations {#available-destinations}

The following destinations are available for configuration in Real-TIme CDP Collaboration. To view the configuration guide for that destination, select the destination name in the table below. If you are interested in configuring a destination that is not currently available, please contact your Adobe representative.

| Destination | Availability |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | Available |
| Amazon S3 | Coming soon. |
| Snowflake | Coming soon. |
| Google Cloud Storage | Coming soon. |
| Azure Blob Storage | Coming soon. |

## Next steps

Once you've configured your destination, you can begin [activating targeted audiences](../collaborate/activate.md) within your projects. 
