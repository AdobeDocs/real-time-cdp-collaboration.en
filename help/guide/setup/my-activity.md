---
title: Track your credit consumption activity
description: Learn how to track your organization's credit consumption activity in Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgebeta: label="Limited availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
---

# Track your credit consumption activity

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently a limited availability release, available to US customers only. The product and documentation are subject to change. Contact your Adobe representative to learn more.

Use the **[!UICONTROL My Activity]** tab to monitor and track your organization's estimated credit consumption across all collaboration activities. This feature provides detailed insights into how credits are being used across different connections and activities, helping you manage your resources effectively.

>[!IMPORTANT]
>
>The credit consumption table is rounded and aggregated by day for monitoring. The figures in the **[!UICONTROL My Activity]** dashboard represent an *estimated* credit consumption. The *actual* credit consumption used for billing is tracked in internal systems and is available fo you upon request. Contact your Adobe representative to obtain that information.

To access your estimated credit consumption activity, navigate to **[!UICONTROL Setup]** in the main navigation, then select the **[!UICONTROL My activity]** tab.

![My Activity dashboard showing credit consumption details](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>The **[!UICONTROL My activity]** view does not include information about user actions in different parts of the Real-Time Collaboration UI. Use the audit logs functionality to get that information. 

## Understand your activity dashboard

The activity dashboard displays a comprehensive list of all credit-consuming operations within your organization. Each row represents a distinct activity and provides key information about the credit usage:

>[!NOTE]
>
>**[!UICONTROL Audience Management]** activities are not associated with another collaborator, so the **[!UICONTROL Connection ID]** and **[!UICONTROL Connection name]** columns for these activity types indicate a **[!UICONTROL N/A]** value.

| Column | Description |
|--------|-------------|
| **[!UICONTROL Date]** | The date when the activity occurred, displayed in MM/DD/YYYY format. |
| **[!UICONTROL Connection ID]** | A unique identifier for each connection associated with a credit-consuming activity, represented as an alphanumeric string. |
| **[!UICONTROL Connection name]** | The name of the collaborator associated with the connection and the credit-consuming activity. |
| **[!UICONTROL Activity]** | The type of activity performed, such as **Activation - Sharing**, **Activation - Egress**, or **Audience management**. |
| **[!UICONTROL Total credits used]** | The total number of credits consumed by the activity. |
| **[!UICONTROL My credit share]** | Your organization's portion of the credits used for the activity. |

{style="table-layout:auto"}

## Types of activities {#types-of-activities}

The Activity column shows different types of credit-consuming operations.

* **[!UICONTROL Audience Management]**: Credits are consumed when audiences are imported into Real-Time CDP Collaboration. Credits are consumed as a function of the number of IDs (in millions) indexed within Real-Time CDP Collaboration across all audiences, and the frequency of that indexing (daily, every three days, or weekly) throughout the billing period. Read more about [importing and managing audiences](/help/guide/setup/onboard-audiences.md).
* **[!UICONTROL Activation - Sharing]** – Credits are consumed as a function of the number of IDs activated from Real-Time CDP Collaboration throughout the billing period. Read more about [sharing](/help/guide/collaborate/share.md) and [activating audiences](/help/guide/collaborate/activate.md) in Real-Time CDP Collaboration.
* **[!UICONTROL Activation - Egress]** – Credits are consumed as a function of the number of IDs activated from Real-Time CDP Collaboration throughout the billing period. Read more about [sharing](/help/guide/collaborate/share.md) and [activating audiences](/help/guide/collaborate/activate.md) in Real-Time CDP Collaboration.


<!--

**[!UICONTROL Audience Overlaps]** – Credits are consumed as a function of the number of matched IDs across 2 or more shared audiences throughout the billing period. Read more about [audience overlaps in the discover tab](/help/guide/collaborate/discover.md).

Collaboration Measurement – Credits are consumed as a function of the number of rows existing in campaign reports across all campaigns, and the frequency of that reporting (daily, every three days, or weekly).

-->


## Manage your credit consumption {#manage-credit-consumption}

To effectively manage your credit consumption:

1. **Monitor regularly**: Check your activity dashboard frequently to understand usage patterns.
2. **Track by connection**: Use the connection name to identify which partnerships are consuming the most credits.
3. **Analyze activity types**: Understand which activities are using the most credits to optimize your operations.
4. **Review credit share**: Compare your credit share against total credits used to understand cost distribution in partnerships.

<!--

## Pagination and navigation

The activity list is paginated to improve performance and readability. Use the navigation controls at the bottom of the table to move between pages and adjust how many records you can view at once.

-->