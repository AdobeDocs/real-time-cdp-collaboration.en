---
title: Latest Real-Time CDP Collaboration Release Notes
description: Follow the latest releases for Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
---
# Latest Real-Time CDP Collaboration Release Notes

{{limited-availability-release-note}}

**Last update**: April, 2025.

These release notes cover the functionality released in Real-Time Customer Data Platform Collaboration. Real-Time CDP Collaboration releases operate on a continuous delivery model, which allows for an approximate monthly release cadence. These release notes get updated often, so be sure to check them regularly.

## May 2025 {#may-2025}

* Real-Time CDP Collaboration is now available to customers in **Australia** and **New Zealand**. It is automatically available to Real-Time CDP Prime and Ultimate customers in these regions.
* Real-Time CDP Collaboration now offers [self-serve desinations](../setup/manage-destinations) through the My desintations tab in the Setup section. Destinations allow you to activate audiences in third-party platforms, such as advertising networks or data management platforms, to reach your customers across various channels. Currently, only Adobe Experience Platform destinations are supported. If you are interested in configuring a different destination, please contact your Adobe representative. To learn more about destinations, read the [destinations overview](../destinations/overview) guide.
  * Destinations also adds support to view Real-Time CDP Collaboration audiences in the [Adobe Experience Platform audience portal](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences). 
* You can now edit the audience refresh frequency for existing data connections in Real-Time CDP Collaboration. Currently, you can choose from refreshing your audiences daily, or every 2 - 6 days. To learn more about how to edit the audience refresh frequency, read the [manage data connections](../setup/manage-data-connection.md#scheduling) guide.
* Credit splits between collaborators are now set for each use case selected within the connection. This allows you to set different credit consumption rules for each use case. To learn more about about the credit split funtionality, read the [connection settings](../connect/establishing-connections.md#connection-settings) guide. To learn more about how credits are consumed, read the [credit activity types](../setup/my-activity.md#types-of-activities) guide. <br> ![Connection settings screen showing the credit split functionality.](/help/assets/release-notes/2025/credit-split.png){zoomable="yes"}
* Publishers can now set advertiser names and IDs before accepting the connection settings from an advertiser. This allows publishers to set names and IDs that align with their internal systems, which can be different from the advertiser's names and IDs. To learn more about adding advertiser names and IDs, read the [connection settings](../connect/establishing-connections.md#connection-settings) guide. <br> ![Connection settings screen showing the publisher setting advertiser names and IDs.](/help/assets/release-notes/2025/add-advertiser-names-modal.png){zoomable="yes"}

## April 2025 {#april-2025}

* A new **Inputs Processed** column has been added to the credit consumption activity table. This column displays the total number of inputs (for example, IDs or rows) processed for each activity. [Read more](/help/guide/setup/my-activity.md#inputs-processed). <br> ![Inputs processed column highighted in My activity view.](/help/assets/release-notes/2025/inputs-processed-column.png){zoomable="yes"}
* A new contact email option has been added to account creation. This helps partner collaborators reach out to you as needed during the connection process. [Read more](../setup/onboard-organization.md).

## March 2025 {#march-2025}

* When [importing audiences](/help/guide/setup/onboard-audiences.md) into Real-Time CDP Collaboration, you can now set an audience refresh frequency from **every 1 to 6 days** to better manage the [Audience Management credit activity](/help/guide/setup/my-activity.md#types-of-activities). [Read more](/help/guide/setup/onboard-audiences.md#schedule). <br> ![Schedule screen showing different frequency intervals for updating audience membership.](/help/assets/setup/add-manage-audiences/Step-Schedule-Set-Frequency.png){zoomable="yes"}
* When establishing a connection with a collaborator, you can now select from predefined **use cases**. The selected use case determines which project sections and product functionality become available. [Read more](/help/guide/collaborate/manage-projects.md#project-use-cases).
    * *Campaign measurement* enables the **Measure** project section.
    * *Audience discovery* enables the **Discover** project section.
    * *Audience sharing and activation* enables the **Share** and **Activate** *(publisher-only)* project sections. <br> ![Use cases highlighted in the connection view.](/help/assets/release-notes/2025/use-cases.png"){zoomable="yes"}
* You can now delete connections with collaborators you no longer wish to work with. [Read more](/help/guide/connect/establishing-connections.md#delete-connections). 


## February 2025 - General availability for US customers {#february-2025-ga}

Real-Time CDP Collaboration, purpose-built to enable advertisers and publishers to discover, activate, and measure high-value audiences without third-party cookies, is now generally available in the United States.

### Get started

1. **Access Setup**: System administrators configure access permissions for users. [Read more](/help/guide/permissions/manage-user-access.md#RTCDP-collaboration-access).
2. **Connect Data Sources**: Import audiences to use in Real-Time CDP Collaboration. [Read more](/help/guide/setup/onboard-audiences.md).
3. **Establish Partner Connections**: Begin collaborating with trusted brands or publishers. [Read more](/help/guide/connect/establishing-connections.md).
4. **Discover & Activate**: Create projects to identify valuable audience segments and activate in campaigns. [Read more](/help/guide/collaborate/manage-projects.md).

### Availability

* Real-Time CDP Collaboration is currently available to US customers only.
* It is automatically available to Real-Time CDP Prime and Ultimate customers

For more information, read:

* [Real-Time CDP Collaboration overview](/help/guide/home.md)
* [End-to-End workflow](/help/guide/end-to-end-workflow.md)
* [Permissions overview](/help/guide/permissions/overview.md)
