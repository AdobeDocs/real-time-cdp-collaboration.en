---
title: Desintations overview
description: Learn about destinations in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 5cbbf5c4-4caa-40da-97be-690d95c1201c
TQID: https://experienceleague.adobe.com/1VvnSt3Z65dfQBfXnjJJi3H0Oj9BxFStexq3icVKxkY
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# Destinations overview

{{limited-availability-release-note}}

>[!NOTE]
>
>This page covers destinations that audiences are activated **to**, such as cloud storage platforms. Looking to activate audiences **to a collaborator** within a shared project instead? See the [activate audiences](/help/guide/collaborate/activate.md) guide.

Destinations are integrations used to send targeted audiences to external platforms. These integrations enable you to activate audiences across various marketing channels and platforms for use in campaigns and customer engagement.

Collaborators can configure destinations to send audiences to external platforms, such as Adobe Experience Platform or a cloud storage platform, for use in campaigns. Collaborators can then [activate audiences within a project](../collaborate/activate.md), which are sent to their connection's configured destination. Activation can be done by either collaborator depending on the audience activation settings [configured in the connection](/help/guide/connect/establishing-connections.md#configure-connection-settings).

>[!IMPORTANT]
>
>Currently, when collaborators activate audiences within a project, they are automatically sent to their connection's configured destination. You **must** configure a destination before your collaborator can activate audiences within a project. 

## Available destinations {#available-destinations}

The following destinations are available for configuration in Collaboration. To view the configuration guide for that destination, select the destination name in the table below.

| Destination | Availability |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | Available |
| [[!DNL Amazon S3]](./manage-destinations.md) | Available |
| [[!DNL Snowflake]](./manage-destinations.md) | Available |
| [[!DNL Google Cloud Storage]](./manage-destinations.md) | Available |
| [[!DNL Azure Blob Storage]](./manage-destinations.md) | Available |
| [[!DNL SFTP]](./manage-destinations.md) | Available |
| [[!DNL Data Landing Zone]](./manage-destinations.md) | Available |

<!-- TODO (CORE-167477): SFTP and Data Landing Zone were missing from this table even in the old "Coming soon" version. Added them here since they're in scope per the ticket/transcript (Cloud Storage category) — confirm this wasn't an intentional exclusion before publishing. -->

>[!NOTE]
>
>**[!DNL Google Cloud Storage]** in this table refers to **destinations** (where Collaboration sends audiences during activation). To **source audiences from** a GCS bucket in the **[!UICONTROL Setup]** workspace, see [Configure GCS for audience sourcing](../setup/configure-gcs-audience-sourcing.md).

## Next steps

To configure a destination, refer to the [configure and manage a destination](./manage-destinations.md) guide. Once you've configured your destination, you can begin [activating targeted audiences](../collaborate/activate.md) within your projects.
