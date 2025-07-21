---
title: Audit Logs
description: Learn how to use the Audit Logs functionality in Real-Time CDP Collaboration to track user activities and changes.
audience: admin
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3af1ac47-dc3d-4f19-a6b9-9e4e835977c0
---
# Audit Logs

{{limited-availability-release-note}}

In order to increase the transparency and visibility of activities performed in the system, you can audit user activity for various services and capabilities in the form of audit logs in Adobe Experience Platform. These logs form an audit trail that can help with troubleshooting issues in Adobe Real-Time CDP Collaboration, and help your business effectively comply with corporate data stewardship policies and regulatory requirements.

In a basic sense, an audit log tells *who* performed *what* action, and *when*. Each action recorded in a log contains metadata that indicates the action type, date and time, the email ID of the user who performed the action, and additional attributes relevant to the action type.

Use the audit logs functionality in Collaboration to track user activities and changes within the platform. This feature is integrated with the Experience Platform audit service, and the UI for this functionality resides in Experience Platform.

![High-level overview screen of the audit logs functionality.](/help/assets/setup/audit-logs/audit-logs-overview.png)

For more comprehensive information about audit logs, visit the [Experience Platform audit logs documentation](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target="_blank"}.

## Access audit logs

You can access audit logs in two ways, as described in the sections below. Both options display a list of audit logs capturing various activities performed within Collaboration.

### Access audit logs from the Collaboration user interface

1. Navigate to the **[!UICONTROL My Activity]** tab in **[!UICONTROL Setup]** workspace in Collaboration.
2. Select the Experience Platform link in the text at the top of the page.

![Access audit logs from the My activity tab in Collaboration.](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)

### Access audit logs directly in the Experience Platform user interface

1. Navigate to [Experience Platform](https://platform.adobe.com/) and select the **[!UICONTROL Audits]** section from the left-hand menu. Reach out to your organization's system administrators to obtain the necessary permissions if you cannot view audit logs.

![Access audit logs from Experience Platform.](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## View and use audit logs

To view the audit logs:

1. Navigate to the **[!UICONTROL Audits]** section in Experience Platform.
2. Use the [filters](#filter-audit-logs) to narrow down the logs based on your criteria.
3. Select a log entry to view detailed information, including the timestamp, request ID, resource details, and action status.

![Detailed Audit Log](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### Captured activities

Audit logs capture detailed information about user activities, including:

* **Timestamp**: The exact date and time of the action performed in a month/day/year hour:minute AM/PM format.
* **Asset name**: The name of the resource on which the action was performed.
* **Category**: The type of resource the action was performed on.
* **Action**: The specific action performed, such as create or delete.
* **User**: The email address of the user who performed the action.

These logs create a comprehensive trail of all activities within your Collaboration instance, which is useful for data governance and regulatory compliance. Read more about [managing audit logs in the UI](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui).

### Filter audit logs {#filter-audit-logs}

The audit logs UI provides several filters to help you search for specific logs:

* **Category**: The type of resource the action was performed on, such as Collaboration Instance or Collaboration Connection Invite.
* **Action**: The type of action performed. Available actions depend on the category selected. For example, actions for Collaboration Instance include create, update, and delete. 
* **Request ID**: A unique identifier for the request.
* **User**: The email address of the user who performed the action.
* **Status**: The status of the action, such as allow or deny.
* **Date Range**: The range of dates for which you want to view logs.

Read more about [filtering audit logs](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs).

## Benefits

Audit logs provide several benefits for organizations using Collaboration:

* **Data Governance**: Use audit logs to ensure that all activities within the platform are tracked and auditable.
* **Regulatory Compliance**: The feature provides a trail of user activities to meet regulatory requirements.
* **Troubleshooting**: Audit logs assist in identifying and resolving issues by providing detailed logs of user actions.

## Categories and actions reference

The table below provides a reference of all categories and actions for Real-Time CDP Collaboration.

![Available categories highlighted in Real-Time CDP Collaboration audit logs.](/help/assets/setup/audit-logs/available-categories.png)

| Category                      | Actions                                  | Description |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Collaboration Instance]**        | create, update, delete                   | Manage accounts, including creating, updating, and deleting accounts. To learn morel, read the [configuring your accounts](/help/guide/setup/onboard-account.md) guide. |
| **[!UICONTROL Collaboration Connection Invite]** | create, update, delete, approve, reject | Manage connection invites, including creating, updating, deleting, approving, and rejecting invites. For more information, read the [establishing connections](/help/guide/connect/establishing-connections.md) guide. |
| **[!UICONTROL Collaboration Connection]**      | create, update, delete, approve, reject, request approval | Manage connections, including creating, updating, deleting, approving, rejecting, and requesting approval for connections. |
| **[!UICONTROL Collaboration Data Connection]** | create, update, delete                   | Manage the data connections from where you source and manage audiences, including creating, updating, and deleting data connections. For more information, read the [managing data connections](/help/guide/setup/manage-data-connection.md) guide. |
| **[!UICONTROL Collaboration Data Entity]**     | create, update, delete                   | Manage data entities for Collaboration, including creating, updating, and deleting data entities. Data entities in this context refers to audiences. For more information, read the [sourcing and managing audiences](/help/guide/setup/onboard-audiences.md) guide. |
| **[!UICONTROL Collaboration Project]**         | create, update, delete                   | Manage projects within Collaboration, including creating, updating, and deleting projects. For more information, read the [managing projects](/help/guide/collaborate/manage-projects.md) guide. |
| **[!UICONTROL Collaboration Module]**          | create, update, delete                   | Manage different modules within projects, including creating, updating, and deleting various modules in the UI. For example, the ability to [activate audiences](/help/guide/collaborate/activate.md). |

{style="table-layout:auto"}

By leveraging the audit logs functionality, you can maintain a clear and detailed record of all activities within Collaboration, ensuring transparency and accountability.
