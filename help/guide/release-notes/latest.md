---
title: Latest Real-Time CDP Collaboration Release Notes
description: Follow the latest releases for Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
TQID: https://experienceleague.adobe.com/re4oFblCLiZpspWIS7D4EEYNh36EDhULEOd2-ccXH28
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
    internal-label: Use cases
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
---
# Latest Real-Time CDP Collaboration Release Notes

{{limited-availability-release-note}}

**Last update**: July 2026.

These release notes cover the functionality released in Adobe Real-Time CDP Collaboration. Collaboration releases operate on a continuous delivery model, which allows for an approximate monthly release cadence. These release notes get updated often, so be sure to check them regularly.

## July 2026 {#july-2026}

Real-Time CDP Collaboration now supports additional self-service audience sourcing options, including [!DNL Databricks Delta Share] and Adobe Audience Manager.

**New or updated features**

| Feature | Description |
| ------- | ----------- |
| Self-service audience sourcing from [!DNL Databricks Delta Share] and Adobe Audience Manager | You can now source first-party audiences directly from your [!DNL Databricks Delta Share] or bring eligible Adobe Audience Manager segments into Collaboration. For setup instructions, see the following guides: <ul><li>[Configure [!DNL Databricks Delta Share] for audience sourcing](../setup/configure-databricks-audience-sourcing.md)</li><li>[Configure Adobe Audience Manager for audience sourcing](../setup/configure-aam-audience-sourcing.md)</li></ul> |

{style="table-layout:auto"}

## April 2026 {#april-2026}

New features are now available in Real-Time CDP Collaboration. These include Collaboration [!DNL Starter] for inviting partners, expanded audience sourcing from [!DNL Snowflake] and [!DNL Google Cloud Storage], support for [!DNL Demdex ID (ECID)] as a match key, and two new collaborator roles: Agency and Data partner.

**New or updated features**

| Feature | Description |
| ------- | ----------- |
| Real-Time CDP Collaboration [!DNL Starter] | You can now invite partners who do not have a Collaboration license to collaborate with you through Collaboration [!DNL Starter]. Invited partners can source audiences, discover overlaps, and activate audiences within the shared connection. See the [Collaboration [!DNL Starter] overview](../overview/starter-overview.md) to get started. |
| Self-service audience sourcing from [!DNL Snowflake] and [!DNL Google Cloud Storage] | You can now source first-party audiences directly from your [!DNL Snowflake Secure Data Share] or [!DNL Google Cloud Storage] bucket into Collaboration. For setup instructions, see the following guides: <ul><li>[Configure [!DNL Snowflake] for audience sourcing](../setup/configure-snowflake-audience-sourcing.md) </li><li> [Configure [!DNL Google Cloud Storage] for audience sourcing](../setup/configure-gcs-audience-sourcing.md) </li></ul> |
| [!DNL Demdex ID] match key | [!DNL Demdex ID] (ECID) is now supported as a match key for matching anonymous cookie-based identities across platforms. It improves audience overlap accuracy without relying on authenticated user data. See [supported match keys](../setup/onboard-account.md#supported-match-keys) for details. |
| New collaborator roles | Collaboration now supports two additional collaborator roles, including **Agency** and **Data partner**. These roles expand how different organizations can participate and work together within the platform. Learn more about: <ul><li>[Collaborator account roles](../overview/roles.md)</li><li>[Collaboration patterns](../overview/collaboration-patterns.md)</li><li>[End-to-end workflow](../overview/end-to-end-workflow.md)</li></ul> |

{style="table-layout:auto"}

## March 2026 {#march-2026}

You can now generate campaign measurement reports and manage measurement data in Real-Time CDP Collaboration.

**New or updated features**

| Feature | Description |
| ------- | ----------- |
| Measurement general availability | Measurement reporting is now generally available in Collaboration. You can now enter campaign IDs associated with marketing campaigns as a publisher, source conversion data as an advertiser, and generate two types of reports: **Campaign Summary** for overall campaign results, and **Attribution** for campaign effectiveness insights. To get started, see the following guides: <ul><li>[Input campaign IDs](../collaborate/manage-projects.md#manage-campaign-id)</li><li>[Source conversion data](../setup/onboard-measurement-data.md)</li><li>[Create and view measurement reports](../collaborate/measure.md)</li></ul> |
| Measurement lifecycle management | Collaboration also supports measurement management:<ul><li> Advertisers can now edit or delete both measurement data connections and associated conversion events to ensure accurate and up-to-date campaign analysis. For more details, see [Manage measurement data connection](../setup/manage-measurement-data-connection.md) and [Manage conversion events](../setup/onboard-measurement-data.md#edit-measurement-data).</li><li>You can also edit or delete scheduled measurement reports directly from the **[!UICONTROL Measure]** tab in any collaboration project. This is available to all users. See the [manage measurement reports guide](../collaborate/measure.md) for more details.</li></ul> |

{style="table-layout:auto"}

## February 2026 {#february-2026}

Real-Time CDP Collaboration now supports editing existing connection and data connection settings directly in the interface.

**New or updated feature**

| Feature | Description |
| ------- | ----------- |
| Edit connection settings | Connection owners can now update use cases, match keys, activation permissions, and credit splits after a connection is established. See [Edit connection](../connect/manage-connections.md#edit-connection) for step-by-step instructions. |
| Edit data connections | Update match keys and scheduling configurations for your existing data connections directly within Collaboration. See [Edit data connection](../setup/manage-data-connection.md#edit-data-connection) for step-by-step instructions. |

## January 2026 {#january-2026}

Real-Time CDP Collaboration now supports CSV file upload as a new method for sourcing audiences, as well as new mobile match keys (IDFA and GAID) for enhanced audience matching and measurement.

**New or updated features**

| Feature | Description |
| ------- | ----------- |
| CSV upload for Audience Sourcing | Upload CSV files to source audiences into Collaboration directly from the UI. Ideal for onboarding first-party data for short-term collaboration projects. For more information, see the [upload CSV file for audience sourcing guide](../setup/upload-csv-audience-sourcing.md). |
| Mobile Match Key Support | Collaboration now supports mobile match keys, including IDFA and GAID, for audience matching and measurement. These match keys are selected during account setup and can then be used when configuring connection settings for new connections and in downstream collaboration workflows. See the [Match keys setup guide](../setup/onboard-account.md#set-up-match-keys) for more details. |

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
