---
title: Manage user access through permissions
description: Understand all available permissions and how to grant users access to different parts of the Real-Time CDP Collaboration UI.
audience: admin
badgebeta: label="Beta" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
exl-id: ae492846-bc0a-4422-86ca-577bcc1fa60c
---
# Manage user access through permissions

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently a beta product, available to select customers. The product and documentation are subject to change. Contact your Adobe representative to learn more.

>[!IMPORTANT]
>
>All permissions operations must be performed by a system administrator.

The Permissions UI allows admins to grant users access to specific parts of the Real-Time CDP Collaboration product UI. This ensures that users only have access to the features and data they need for their roles. Understand all available permissions and how to grant users access to different parts of the Real-Time CDP Collaboration UI.

## Accessing the Permissions UI

To access the Permissions UI, navigate to **[!UICONTROL Admin]** > **[!UICONTROL Permissions]**. This page is only available to users with admin privileges.

!Permissions UI Overview

## Creating and Managing Roles

Roles are groups of permissions that can be assigned to users. To create a new role:

1. Select **[!UICONTROL Create Role]**.
2. Provide a name and description for the role.
3. Add the necessary permissions to the role by selecting from the available options.

!Create Role

### Example: Creating a "Manage Projects" Role

To create a role that allows users to manage projects:

1. Select **[!UICONTROL Create Role]**.
2. Name the role "Manage Projects".
3. Add the following permissions:
   - **Read Projects**: Allows users to view projects.
   - **Manage Projects**: Allows users to create and edit projects.

!Manage Projects Role

## Assigning Roles to Users

Once roles are created, they can be assigned to users:

1. Navigate to the **[!UICONTROL Users]** tab.
2. Select **[!UICONTROL Add Users]**.
3. Search for the user by name or email.
4. Assign the desired role to the user.

!Assign Role to User

## Viewing and Editing Permissions

Admins can view and edit the permissions assigned to each role:

1. Navigate to the **[!UICONTROL Roles]** tab.
2. Select the role you want to edit.
3. Add or remove permissions as needed.

!Edit Role Permissions

## Best Practices

- **Combine Permissions**: When assigning the "Manage" permission, always include the corresponding "Read" permission to ensure users have the necessary access.
- **Use Roles Effectively**: Create roles that align with job functions to streamline permission management.

>[!TIP]
>
>Regularly review and update roles to ensure they meet the evolving needs of your organization.

## Permissions Reference

For extensive information about roles, consult this link.

| High Level Permission | Description |
| --- | --- |
| Manage Collaboration Instances | View, Create, Update and Delete org's own collaboration instances. Discover other org's collaboration instances. |
| Read Collaboration Instances | Read org's own collaboration instances. Discover other org's collaboration instances. |
| Manage Connection Invites | View, Create, Delete handshakes initiated by the org. Accept/Decline handshakes initiated by other orgs. |
| Read Connection Invites | View handshakes. |
| Manage Collaboration Connections | For advertiser, View, Create, Update settings, Submit, Delete connections. For publisher, View connections and Accept/Decline connections. |
| Read Collaboration Connections | View connections. |
| Manage Audience Data | Onboarding of Audiences and updating of Public, Private, Custom Audiences and Audience Inventory metadata settings and removing audiences. Discover audiences. |
| Read Audience Data | Reading of Audiences and updating of Public, Private, Custom Audiences and Audience Inventory metadata settings. Discover audiences. |
| Manage Measurement Data | Onboarding, updating and deleting of measurement data. |
| Read Measurement Data | Reading of measurement data. |
| Manage Projects | View, Create, Update and Delete projects. |
| Read Projects | View projects. |
| Read User Activities | Read user activities. |
| Export User Activities | Export user activities. |
| Read Collaboration Credit Monitoring | Credit wallet monitoring at the org + instance level. |