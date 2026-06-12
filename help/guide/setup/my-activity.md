---
title: Track your credit consumption activity
description: Learn how to view your organization's Credit Wallet and track credit consumption activity in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
TQID: https://experienceleague.adobe.com/hDvkKFUCBYvsX8wntcYFrL6qZTxOo5CZOWAbxNwk7mw
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# Track your credit consumption activity {#track-credit-consumption-activity}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_my_activity"
>title="Read more"
>abstract=""

{{limited-availability-release-note}}

>[!BEGINSHADEBOX]

**90-Day No-Overage Period**: Customers in eligible regions benefit from a 90-day no-overage period starting from the date of availability in their region. During this time, customers do not incur overage fees for exceeding their credit entitlement.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>The figures in the **[!UICONTROL My activity]** view reflect credit usage data that refreshes daily. The *actual* credit consumption used for billing is tracked in internal systems and is available upon request. Contact your Adobe representative to obtain that information.

To access your Credit Wallet and credit consumption activity, navigate to **[!UICONTROL Setup]** in the main navigation, then select the **[!UICONTROL My activity]** tab.

![The My activity tab showing the Credit Wallet with credits provisioned, credits consumed, available credits, and the credit consumption activity table.](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>The **[!UICONTROL My activity]** view does not include user actions from other areas of the Real-Time CDP Collaboration interface. Use the [audit logs](/help/guide/setup/audit-logs.md) functionality to get that information. 

## Understand the My activity view {#understand-dashboard}

Use the **[!UICONTROL My activity]** view to monitor your credit usage and review the activities that consume credits. The view includes the Credit Wallet and an activity table.

The Credit Wallet shows your provisioned credits, consumed credits, and available credits. 

| Metric | Description |
|---------|-------------|
| **[!UICONTROL Credits provisioned]** | The number of credits provisioned for your account. |
| **[!UICONTROL Credits consumed]** | The number of credits consumed by your account as of the most recent daily refresh. |
| **[!UICONTROL Available credits]** | The number of credits available to your account, calculated from provisioned credits minus consumed credits. |

{style="table-layout:auto"} 

The activity table lists daily credit consumption records by date, activity type, inputs processed, and credits used:

>[!NOTE]
>
>**[!UICONTROL Audience Management]** activities are not associated with another collaborator, so the **[!UICONTROL Connection ID]** and **[!UICONTROL Connection name]** columns for these activity types show a **[!UICONTROL -]** value.

| Column   | Description  |
|------------|--------------|
| **[!UICONTROL Date]** | The date when the activity occurred, displayed in MM/DD/YYYY format. |
| **[!UICONTROL Connection ID]** | A unique identifier for each connection associated with a credit-consuming activity, represented as an alphanumeric string. |
| **[!UICONTROL Connection name]** | The name of the collaborator associated with the connection and the credit-consuming activity. |
| **[!UICONTROL Activity]** | The type of activity performed, such as **[!UICONTROL Activation - Audience Access (Once)]**, **[!UICONTROL Activation - Audience Access (Recurring)]**, **[!UICONTROL Activation - Audience Egress (Once)]**, **[!UICONTROL Activation - Audience Egress (Recurring)]**, or **[!UICONTROL Audience Management]**. |
| **[!UICONTROL Inputs processed]** | The total number of inputs (for example, IDs or rows) processed for the activity. |
| **[!UICONTROL Total credits used]** | The total credits consumed by the activity. |
| **[!UICONTROL My credit share]** | Your account's portion of the credits used for the activity. |

{style="table-layout:auto"}

## Types of activities {#types-of-activities}

The **[!UICONTROL Activity]** column shows different types of credit-consuming operations.

* **[!UICONTROL Audience Management]**: Credits are consumed when audiences are sourced into Collaboration. Credits are consumed as a function of the number of IDs indexed within Collaboration across all audiences, and the frequency of that indexing, such as daily, every three days, or weekly. To learn more, read the [sourcing and managing audiences](/help/guide/setup/onboard-audiences.md) guide. 
* **[!UICONTROL Activation - Audience Access (Once)]**: Credits are consumed when audience access is processed once through the activation workflow. To learn more, read the [activating audiences](/help/guide/collaborate/activate.md) guide. 
* **[!UICONTROL Activation - Audience Access (Recurring)]**: Credits are consumed when audience access is processed on a recurring schedule through the activation workflow. To learn more, read the [activating audiences](/help/guide/collaborate/activate.md) guide. 
* **[!UICONTROL Activation - Audience Egress (Once)]**: Credits are consumed when audience egress to a destination is processed once through the activation workflow. This activity is charged to the collaborator that receives the audience. To learn more, read the [activating audiences](/help/guide/collaborate/activate.md) guide. 
* **[!UICONTROL Activation - Audience Egress (Recurring)]**: Credits are consumed when audience egress to a destination is processed on a recurring schedule through the activation workflow. This activity is charged to the collaborator that receives the audience. To learn more, read the [activating audiences](/help/guide/collaborate/activate.md) guide. 
* **[!UICONTROL Measurement]**: Credits are consumed when you generate campaign performance reports and insights in Collaboration. Credits are consumed based on the number of rows in campaign reports across all campaigns and the frequency of reporting, such as daily, every three days, or weekly.

## Manage your credit consumption {#manage-credit-consumption}

To effectively manage your credit consumption:

1. **Understand** the credit consumption associated with each activity. Check the [Collaboration product description](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} for a table of credits used per activity. 
2. **Monitor usage regularly**: Review your available credits and activity table to understand usage patterns across audience management, audience access, audience egress, and measurement activities. 
3. **Track by connection**: Use the connection name to identify which connections are consuming the most credits.
