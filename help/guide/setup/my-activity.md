---
title: Track your credit consumption activity
description: Learn how to track your organization's credit consumption activity in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
---
# Track your credit consumption activity

{{limited-availability-release-note}}

Use the **[!UICONTROL My Activity]** tab to monitor and track your organization's estimated credit consumption across all collaboration activities. This feature provides detailed insights into how credits are being used across different connections and activities, helping you manage your resources effectively.

>[!IMPORTANT]
>
>The credit consumption table is rounded up and aggregated by day for monitoring. The figures in the **[!UICONTROL My Activity]** dashboard represent an *estimated* credit consumption. The *actual* credit consumption used for billing is tracked in internal systems and is available to you upon request. Contact your Adobe representative to obtain that information.

To access your estimated credit consumption activity, navigate to **[!UICONTROL Setup]** in the main navigation, then select the **[!UICONTROL My activity]** tab.

![My Activity dashboard showing credit consumption details](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>The **[!UICONTROL My activity]** view does not include information about user actions in different parts of the Real-Time Collaboration CDP user interface. Use the [audit logs](/help/guide/setup/audit-logs.md) functionality to get that information. 

## Understand your activity dashboard {#understand-dashboard}

The activity dashboard displays a comprehensive list of all credit-consuming operations within your organization. Each row represents a distinct activity and provides key information about the credit usage:

>[!NOTE]
>
>**[!UICONTROL Audience Management]** activities are not associated with another collaborator, so the **[!UICONTROL Connection ID]** and **[!UICONTROL Connection name]** columns for these activity types indicate a **[!UICONTROL N/A]** value.

| Column   | Description  |
|------------|--------------|
| **[!UICONTROL Date]**   | The date when the activity occurred, displayed in MM/DD/YYYY format.  |
| **[!UICONTROL Connection ID]** | A unique identifier for each connection associated with a credit-consuming activity, represented as an alphanumeric string. |
| **[!UICONTROL Connection name]** | The name of the collaborator associated with the connection and the credit-consuming activity. |
| **[!UICONTROL Activity]** | The type of activity performed, such as **Activation - Sharing**, **Activation - Egress**, or **Audience management**. |
| **[!UICONTROL Inputs processed]** | The total number of inputs (for example, IDs or rows) processed for the activity.|
| **[!UICONTROL Total credits used]** | The total number of credits consumed by the activity. |
| **[!UICONTROL My credit share]** | Your organization's portion of the credits used for the activity.  |

{style="table-layout:auto"}

## Types of activities {#types-of-activities}

The **[!UICONTROL Activity]** column shows different types of credit-consuming operations.

* **[!UICONTROL Audience Management]**: Credits are consumed when audiences are sourced into Real-Time CDP Collaboration. Credits are consumed as a function of the number of IDs (in millions) indexed within Real-Time CDP Collaboration across all audiences, and the frequency of that indexing (daily, every three days, or weekly). To learn more, read the [importing and managing audiences](/help/guide/setup/onboard-audiences.md) guide.
* **[!UICONTROL Activation - Matching]** – Credits are consumed as a function of the number of IDs matched and prepared for activation. To learn more, read the [activating audiences](/help/guide/collaborate/activate.md) guide.
* **[!UICONTROL Activation - Egress]** – Credits are consumed as a function of the number of IDs are sent to a destination. This is always charged to the collaborator that receives the audience. To learn more, read the [activating audiences](/help/guide/collaborate/activate.md) guide.
* **[!UICONTROL Audience Measurement]** – Execute activities in Real-Time CDP Collaboration to generate campaign performance reports and insights. Credits are consumed based on the number of rows in campaign reports across all campaigns and the frequency of reporting (daily, every three days, or weekly).

## Manage your credit consumption {#manage-credit-consumption}

To effectively manage your credit consumption:

1. **Understand** the credit consumpton associated with each activity. Check the [Real-Time CDP Collaboration product description](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} for a table of collaboration credits used per activity.   
2. **Monitor regularly**: Check your activity dashboard frequently to understand usage patterns.
3. **Track by connection**: Use the connection name to identify which partnerships are consuming the most credits.

<!--

## Pagination and navigation

The activity list is paginated to improve performance and readability. Use the navigation controls at the bottom of the table to move between pages and adjust how many records you can view at once.

-->
