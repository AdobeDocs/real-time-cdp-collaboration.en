---
title: Audit Logs
description: Learn how to use the Audit Logs functionality in Real-Time CDP Collaboration to track user activities and changes.
audience: admin
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
---
# Audit Logs

{{limited-availability-release-note}}

In order to increase the transparency and visibility of activities performed in the system, you can audit user activity for various services and capabilities in the form of audit logs in Adobe Real-Time Customer Data Platform (CDP). These logs form an audit trail that can help with troubleshooting issues in Real-Time CDP Collaboration, and help your business effectively comply with corporate data stewardship policies and regulatory requirements.

In a basic sense, an audit log tells *who* performed *what* action, and *when*. Each action recorded in a log contains metadata that indicates the action type, date and time, the email ID of the user who performed the action, and additional attributes relevant to the action type.

Use the audit logs functionality in Real-Time CDP Collaboration to track user activities and changes within the platform. This feature is integrated with the Adobe Experience Platform audit service, and the UI for this functionality resides in Experience Platform.

![High-level overview screen of the audit logs functionality](/help/assets/setup/audit-logs/audit-logs-overview.png)

For more comprehensive information about audit logs, visit the [Adobe Experience Platform Audit Logs documentation](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target=_blank}.

## Access audit logs

You can access audit logs in two ways, as described in the sections below. Both options display a list of audit logs capturing various activities performed within the Real-Time CDP Collaboration UI

### Access audit logs from the Real-Time CDP Collaboration user interface

1. Navigate to the **[!UICONTROL My Activity]** tab in the Real-Time CDP Collaboration UI.
2. Select the Experience Platform link in the UI text at the top of the page.

![Access audit logs from the Real-Time CDP Collaboration UI](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)

### Access audit logs directly in the Experience Platform user interface

1. Navigate to the Adobe Experience Platform UI and select the **[!UICONTROL Audits]** section from the left-hand menu. Reach out to your organization's system administrators to obtain the necessary permissions if you cannot view audit logs.

![Access audit logs from the Experience Platform UI](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## View and use audit logs

To view the audit logs:

1. Navigate to the **[!UICONTROL Audits]** section in the Adobe Experience Platform UI.
2. Use the filters to narrow down the logs based on your criteria.
3. Select a log entry to view detailed information, including the timestamp, request ID, resource details, and action status.

![Detailed Audit Log](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### Captured activities

Audit logs capture detailed information about user activities, including:

* **User ID**: The identifier of the user who performed the action.
* **Action**: The type of action performed (e.g., create, update, delete).
* **Resource**: The resource that was modified or created.
* **Timestamp**: The time when the action was performed.

These logs create a comprehensive trail of all activities within your Real-Time CDP Collaboration instance, which is useful for data governance and regulatory compliance. Read more about [managing audit logs in the UI](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui).

### Filter audit logs

The audit logs UI provides several filters to help you search for specific logs:

* **Category**: Refers to the resource type (for example: collaboration instance, connection, project).
* **Action**: The type of action performed (for example: create, delete, update).
* **Request ID**: A unique identifier for the request.
* **User Email**: The email address of the user who performed the action.
* **Status**: The status of the action (for example: allowed, denied).
* **Date Range**: The range of dates for which you want to view logs.

Read more about [filtering audit logs](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs).

### Example usage

Audit logs are generated and displayed in the Experience Platform audits UI when you perform actions within the Real-Time CDP Collaboration UI, such as managing audiences, extending connection invites, creating projects, and so on. For example, operations to create or update parts of a project are captured as shown below:

![Example of audit logs generated when creating and updating parts of a project.](/help/assets/setup/audit-logs/create-project-audits.png)

## Benefits

Understand some of the benefits of using audit logs:

* **Data Governance**: Use audit logs to ensure that all activities within the platform are tracked and auditable.
* **Regulatory Compliance**: The feature provides a trail of user activities to meet regulatory requirements.
* **Troubleshooting**: Audit logs assist in identifying and resolving issues by providing detailed logs of user actions.

## Categories and actions reference

The table below provides a reference of all categories and actions for Real-Time CDP Collaboration.

![Available categories highlighted in Real-Time CDP Collaboration audit logs.](/help/assets/setup/audit-logs/available-categories.png)

| Category                      | Actions                                  | Description |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Collaboration Instance]**        | create, update, delete                   | Manage organization accounts, including creating, updating, and deleting organizations. Read more about [setting up organizations](/help/guide/setup/onboard-organization.md). |
| **[!UICONTROL Collaboration Connection Invite]** | create, update, delete, approve, reject | Manage connection invites, including creating, updating, deleting, approving, and rejecting invites. Read more about [connection invites](/help/guide/connect/establishing-connections.md). |
| **[!UICONTROL Collaboration Connection]**      | create, update, delete, approve, reject, request approval | Manage collaboration connections, including creating, updating, deleting, approving, rejecting, and requesting approval for connections. |
| **[!UICONTROL Collaboration Data Connection]** | create, update, delete                   | Manage data connections for collaboration to import and manage audiences, including creating, updating, and deleting data connections. Read more about [managing data connections](/help/guide/setup/manage-data-connection.md). |
| **[!UICONTROL Collaboration Data Entity]**     | create, update, delete                   | Manage data entities for collaboration, including creating, updating, and deleting data entities. Data entities in this context refers to audiences. Read more about [importing and managing audiences](/help/guide/setup/onboard-audiences.md). |
| **[!UICONTROL Collaboration Project]**         | create, update, delete                   | Manage projects within collaboration, including creating, updating, and deleting projects. Read more about [managing projects](/help/guide/collaborate/manage-projects.md). |
| **[!UICONTROL Collaboration Module]**          | create, update, delete                   | Manage different modules within collaboration projects, including creating, updating, and deleting various modules in the UI. For example, the ability to [share audiences](/help/guide/collaborate/share.md). |

{style="table-layout:auto"}

By leveraging the audit logs functionality, you can maintain a clear and detailed record of all activities within your Real-Time CDP Collaboration instance, ensuring transparency and accountability.