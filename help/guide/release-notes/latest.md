---
title: Latest Real-Time CDP Collaboration Release Notes
description: Follow the latest releases for Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
---
# Latest Real-Time CDP Collaboration Release Notes

{{limited-availability-release-note}}

**Last update**: January 2026.

These release notes cover the functionality released in Adobe Real-Time CDP Collaboration. Collaboration releases operate on a continuous delivery model, which allows for an approximate monthly release cadence. These release notes get updated often, so be sure to check them regularly.

## January 2026 {#january-2026}

Real-Time CDP Collaboration now supports CSV file upload as a new method for sourcing audiences into Collaboration.

**New features**

| Feature | Description |
| ------- | ----------- |
| CSV upload for Audience Sourcing | Upload CSV files to source audiences into Collaboration directly from the UI. Ideal for onboarding first-party data for short-term collaboration projects. For more information, see the [upload CSV file for audience sourcing guide](../setup/upload-csv-audience-sourcing.md). |

{style="table-layout:auto"}

## December 2025 {#december-2025}

Real-Time CDP Collaboration is now available to customers in **Europe, the Middle East, and Africa (EMEA))**. It is automatically available to Real-Time CDP Prime and Ultimate customers in these regions.

## August 2025 {#august-2025}

Real-Time CDP Collaboration is now available to customers in **Canada**. It is automatically available to Real-Time CDP Prime and Ultimate customers in these regions.

* Collaboration now supports the following [match keys](../setup/onboard-account.md#supported-match-keys):
  * Hashed email
  * Hashed phone number
  * CRM ID
  * Loyalty ID
  * Hashed IPv4
  * AdFixus ID
* Multiple match keys are now available across Collaboration, giving you the ability to expand your audience size and improve match rates. Multiple match keys can be used when sourcing audiences, establishing connections, and activating audiences. To learn more about using multiple match keys, read the [set up match keys](../setup/onboard-account.md) and [sourcing audiences](../setup/onboard-audiences.md#map-fields) guides.

>[!IMPORTANT]
>
>When activating audiences where multiple match keys are used, if one (or more) match key has no overlaps, no audience counts, or falls below threshold, the entire activation will fail. Ensure your audiences have sufficient overlap and meet the minimum threshold of 1000 IDs across all match keys before activating.

* The Adobe Experience Platform destination now supports activating audiences with multiple match keys. Additionally, you can now used a linked key when configuring your destination's mapping to specify which match key is sent during activation. To learn more, read the [Experience Platform destination](../destinations/experience-platform.md#linked-keys) guide.
* Collaborators can now edit multiple audiences at once. You can now edit audience metadata, connection access, names, descriptions, and categories for multiple audiences using the bulk edit tool. To learn more about editing audiences, read the [manage audiences](../setup/onboard-audiences.md#edit-audiences) guide.
  
## July 2025 {#july-2025}

Real-time CDP Collaboration now supports brand-to-brand collaboration. Collaborators can now form connections, regardless of whether they are an advertiser or publisher. This allows for more flexible collaboration opportunities and enables brands to leverage each other's data and insights. To learn more about the differences between brand-to-brand collaboration and advertiser-to-publisher collaboration, read the [collaboration patterns](../overview/collaboration-patterns.md) guide.

* Collaborators can now connect to each other using [private connection invites](../connect/establishing-connections.md#private-connection-invites). Share your account's unique connect code with a collaborator who can then use it to connect with you directly. This is a core feature of brand-to-brand collaboration, allowing collaborators to establish connections beyond advertisers exploring the **[!UICONTROL Discover collaborators]** directory.
* [Self-serve destinations](../setup/manage-destinations.md) are now available to both advertisers and publishers.
* Audience activation is now available for both collaborators in a connection, regardless of their [account role](../overview/roles.md). Audience activation settings are configured while [establishing connections](../connect/establishing-connections.md#configure-connection-settings), allowing you to specify which collaborator can activate audiences. To learn more about audience activation, read the [activate audiences](../collaborate/activate.md) guide.
* The **[!UICONTROL Activate]** use case has been reconfigured to support brand-to-brand collaboration. The **[!UICONTROL Activate]** tab within a project now displays the audiences that have been sent to your collaborator, and the audiences activated to your destination by your collaborator. To learn more, read the [activate audiences](../collaborate/activate.md) guide. <br> ![The Activate dashboard with the Audiences sent to and Audiences activated sections.](/help/assets/release-notes/2025/activate-dashboard.png){zoomable="yes"}
* Audience index scores are now available in the **[!UICONTROL Discover]** tab of a project. The audience index score is a measure of how well an audience matches your collaborator's audience. This score is calculated based on on underlying audience counts & overlaps. To learn more about audience index scores, read the [audience index score](../collaborate/discover.md#audience-index-score) guide.

## May 2025 {#may-2025}

* Real-Time CDP Collaboration is now available to customers in **Australia** and **New Zealand**. It is automatically available to Real-Time CDP Prime and Ultimate customers in these regions.
* Real-Time CDP Collaboration now offers [self-serve destinations](../setup/manage-destinations.md) through the **[!UICONTROL My destinations]** tab in the **[!UICONTROL Setup]** section. Destinations allow you to activate audiences in third-party platforms, such as advertising networks or data management platforms, to reach your customers across various channels. Currently, only Adobe Experience Platform destinations are supported. If you are interested in configuring a different destination, please contact your Adobe representative. To learn more about destinations, read the [destinations overview](../destinations/overview.md) guide.
  * Destinations also adds support to view Collaboration audiences in the [Adobe Experience Platform audience portal](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences).
* You can now edit the audience refresh frequency for existing data connections in Collaboration. Currently, you can choose to refresh your audiences daily or every two to six days. To learn more about how to edit the audience refresh frequency, read the [manage data connections](../setup/manage-data-connection.md#scheduling) guide.
* Credit splits between collaborators are now set for each use case selected within the connection. You can set different credit consumption rules for each use case to better control how your credits are used. To learn more about about the credit split funtionality, read the [connection settings](../connect/establishing-connections.md#connection-settings) guide. To learn more about how credits are consumed, read the [credit activity types](../setup/my-activity.md#types-of-activities) guide. <br> ![Connection settings screen showing the credit split functionality.](/help/assets/release-notes/2025/credit-split.png){zoomable="yes"}
* Publishers can now set advertiser names and IDs before accepting the connection settings from an advertiser. Publishers can set names and IDs that align with their internal systems, which can be different from the advertiser's names and IDs. To learn more about adding advertiser names and IDs, read the [connection settings](../connect/establishing-connections.md#connection-settings.md) guide. <br> ![Connection settings screen showing the publisher setting advertiser names and IDs.](/help/assets/release-notes/2025/add-advertiser-names-modal.png){zoomable="yes"}

## April 2025 {#april-2025}

* A new **[!UICONTROL Inputs Processed]** column has been added to the credit consumption activity table. This column displays the total number of inputs (for example, IDs or rows) processed for each activity. [Read more](/help/guide/setup/my-activity.md#inputs-processed). <br> ![Inputs processed column highighted in My activity view.](/help/assets/release-notes/2025/inputs-processed-column.png){zoomable="yes"}
* A new contact email option has been added to account creation. This helps partner collaborators reach out to you as needed during the connection process. [Read more](../setup/onboard-account.md).

## March 2025 {#march-2025}

* When [sourcing audiences](/help/guide/setup/onboard-audiences.md) into Collaboration, you can now set an audience refresh frequency from **every one to six days** to better manage the [Audience Management credit activity](/help/guide/setup/my-activity.md#types-of-activities). For more information, read the [manage audiences](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences) guide. <br> ![Schedule screen showing different frequency intervals for updating audience membership.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png "Schedule screen showing different frequency intervals for updating audience membership."){width="250" align="center" zoomable="yes"}
* When establishing a connection with a collaborator, you can now select from predefined **use cases**. The selected use case determines which project sections and product functionality become available. For more information, read the [manage projects](/help/guide/collaborate/manage-projects.md#project-use-cases) guide.
    * *Measurement* enables the **Measure** project section.
    * *Audience discovery* enables the **Discover** project section.
    * *Audience activation* enables the  **Activate** project sections <br>
* You can now delete connections with collaborators you no longer wish to work with. To learn how to delete connections, read the [deleting connections](/help/guide/connect/establishing-connections.md#delete-connections) guide.

## February 2025 {#february-2025}

Adobe Real-Time CDP Collaboration, purpose-built to enable advertisers and publishers to discover, activate, and measure high-value audiences without third-party cookies, is now generally available in the United States.

### Get started

1. **Access Setup**: System administrators configure access permissions for users. To learn more about configuring access permissions, read the [manage user access](/help/guide/permissions/manage-user-access.md#RTCDP-collaboration-access) guide.
2. **Connect Data Sources**: Source audiences to use in Collaboration. To begin sourcing audiences, read the [source and manage audiences](/help/guide/setup/onboard-audiences.md) guide.
3. **Establish Connections**: Begin collaborating with trusted advertisers or publishers. To learn more about forming connections, read the [establishing connections](/help/guide/connect/establishing-connections.md) guide.
4. **Discover & Activate**: Create projects to identify valuable audiences to activate in campaigns. To learn more about creating projects, read the [manage projects](/help/guide/collaborate/manage-projects.md) guide.

### Availability

* Adobe Real-Time CDP Collaboration is currently available to US customers only.
* It is automatically available to Adobe Real-Time CDP Prime and Ultimate customers

For more information, read the:

* [Collaboration overview](/help/guide/home.md)
* [End-to-End workflow](/help/guide/overview/end-to-end-workflow.md)
* [Permissions overview](/help/guide/permissions/overview.md)
