---
title: Manage data connections
description: Learn how to manage data connections, including match keys, scheduling, use cases, and audience filtering in Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
---
# Manage data connections

{{limited-availability-release-note}}

## Overview

Use data connections in Real-Time CDP Collaboration to import audiences from various sources. Learn how to manage match keys, schedule data imports, and configure use cases for your existing data connections. Additionally, you'll be able to filter audiences by different attributes for more granular insights.

Before managing your data connections here, you should initially set them up during the [audience onboarding workflow](./onboard-audiences.md). This will ensure the correct data sources are connected for use in Real-Time CDP Collaboration.

## View data connections

>[!IMPORTANT]
>
>Deleting a data connection is currently not supported in the Real-Time CDP Collaboration user interface. To delete a data connection, please reach out to your Adobe representative or [create a customer support ticket](https://experienceleague.adobe.com/home?lang=en&support-tab=open-ticket#support){target=_blank}.

To view existing data connections, navigate to **[!UICONTROL Setup]** > **[!UICONTROL My audiences]**, and select **[!UICONTROL Manage data connections]**.

![View of the audiences screen, with Manage data connections highlighted.](/help/assets/setup/manage-data-connection/manage-data-connection-highlighted.png)

This brings up a view of all your currently set up data connections, with information about the number of audiences in each of them, the source of the data connection, and more. Select **[!UICONTROL View data connection]** to view information about the match keys, scheduling, use cases, and the audiences that are part of this data connection. 

![View of the data connection screen, with View data connections highlighted.](/help/assets/setup/manage-data-connection/view-data-connection-highlighted.png)

### Match keys {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Match keys"
>abstract="Match keys determine how data from different sources will be matched. Choose the match keys that are most relevant to your use cases and privacy guidelines."

Match keys are identifiers used to reconcile members across audiences from different data sources. Available match keys include:

- **Hashed email**

You cannot edit the match keys used in this data connection.

![View of the data connection, with Match keys highlighted.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png)

### Scheduling {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Scheduling"
>abstract="This view displays the scheduling options that you selected initially for your data connection."

You cannot edit the scheduling options that you selected initially for your data connection. For more information about scheduling options, view the [scheduling section](/help/guide/setup/onboard-audiences.md#schedule) in the audience import workflow document.

![View of the data connection, with Scheduling highlighted.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png)

<!--

### Use cases {#use-cases}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_usecases"
>title="Use cases"
>abstract="Use cases selection is not part of the beta release of Real-Time CDP Collaboration"

>[!IMPORTANT]
>
>In the beta release, the use cases are preselected and do not have an effect on campaigns.

Use cases define how the imported audience data can be leveraged in Real-Time CDP Collaboration. Available use cases include:

- **Discover**
- **Share**
- **Activate**
- **Measure**

You can configure different use cases for each match key (for example hashed email, hashed phone number). To modify use case settings, select the **[!UICONTROL Edit]** button in the Use Cases section.

![View of the data connection, with Use cases highlighted.](/help/assets/setup/manage-data-connection/view-data-connection-use-cases.png)

-->

## Manage audiences {#manage-audiences}

When viewing the list of audiences from your data connection, you can select to view the audiences, edit their categories, or remove them from the data connection.

![View of the data connection, with the audiences highlighted.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png)

## Next steps

After managing your data connections, you can [discover overlaps](/help/guide/collaborate/discover.md) between your audiences and the audiences that your collaborator has made discoverable.
