---
title: Track your credit consumption activity
description: Learn how to track your organization's credit consumption activity in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
---
# Track your credit consumption activity

{{limited-availability-release-note}}

>[!BEGINSHADEBOX]

**90-Day No-Overage Period**: Customers in eligible regions benefit from a 90-day no-overage period starting from the date of availability in their region. During this time, customers do not incur overage fees for exceeding their credit entitlement.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>The credit consumption table is rounded up and aggregated by day for monitoring. The figures in the **[!UICONTROL My Activity]** dashboard represent an *estimated* credit consumption. The *actual* credit consumption used for billing is tracked in internal systems and is available to you upon request. Contact your Adobe representative to obtain that information.

To access your estimated credit consumption activity, navigate to **[!UICONTROL Setup]** in the main navigation, then select the **[!UICONTROL My activity]** tab.

![My Activity dashboard showing credit consumption details](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>The **[!UICONTROL My activity]** view does not include information about user actions in different parts of Collaboration user interface. Use the [audit logs](/help/guide/setup/audit-logs.md) functionality to get that information. 

## Understand your activity dashboard {#understand-dashboard}

The activity dashboard displays a comprehensive list of all credit-consuming operations within your account. Each row represents a distinct activity and provides key information about the credit usage:

>[!NOTE]
>
>**[!UICONTROL Audience Management]** activities are not associated with another collaborator, so the **[!UICONTROL Connection ID]** and **[!UICONTROL Connection name]** columns for these activity types indicate a **[!UICONTROL -]** value.

| Column   | Description  |
|------------|--------------|
| **[!UICONTROL Date]**   | The date when the activity occurred, displayed in MM/DD/YYYY format.  |
| **[!UICONTROL Connection ID]** | A unique identifier for each connection associated with a credit-consuming activity, represented as an alphanumeric string. |
| **[!UICONTROL Connection name]** | The name of the collaborator associated with the connection and the credit-consuming activity. |
| **[!UICONTROL Activity]** | The type of activity performed, such as **Activation - Matching**, **Activation - Egress**, or **Audience Management**. |
| **[!UICONTROL Inputs processed]** | The total number of inputs (for example, IDs or rows) processed for the activity.|
| **[!UICONTROL Total credits used]** | The total number of credits consumed by the activity. |
| **[!UICONTROL My credit share]** | Your account's portion of the credits used for the activity.  |

{style="table-layout:auto"}

## Types of activities {#types-of-activities}

The **[!UICONTROL Activity]** column shows different types of credit-consuming operations.

* **[!UICONTROL Audience Management]**: Credits are consumed when audiences are sourced into Collaboration. Credits are consumed as a function of the number of IDs (in millions) indexed within Collaboration across all audiences, and the frequency of that indexing (daily, every three days, or weekly). To learn more, read the [sourcing and managing audiences](/help/guide/setup/onboard-audiences.md) guide.
* **[!UICONTROL Activation - Matching]** – Credits are consumed as a function of the number of IDs matched and prepared for activation. To learn more, read the [activating audiences](/help/guide/collaborate/activate.md) guide.
* **[!UICONTROL Activation - Egress]** – Credits are consumed as a function of the number of IDs are sent to a destination. This is always charged to the collaborator that receives the audience. To learn more, read the [activating audiences](/help/guide/collaborate/activate.md) guide.
* **[!UICONTROL Measurement]** – Execute activities in Collaboration to generate campaign performance reports and insights. Credits are consumed based on the number of rows in campaign reports across all campaigns and the frequency of reporting (daily, every three days, or weekly).

## Manage your credit consumption {#manage-credit-consumption}

To effectively manage your credit consumption:

1. **Understand** the credit consumption associated with each activity. Check the [Collaboration product description](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} for a table of credits used per activity.
2. **Monitor regularly**: Check your activity dashboard frequently to understand usage patterns.
3. **Track by connection**: Use the connection name to identify which connections are consuming the most credits.
