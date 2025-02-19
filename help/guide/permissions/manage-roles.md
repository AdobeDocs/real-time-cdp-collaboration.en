---
title: Manage roles through Permissions
description: Understand all available role resources that provide access to different components within the Real-Time CDP Collaboration UI.
audience: admin
badgebeta: label="Beta" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
---
# Manage roles {#manage-roles}

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently a beta product, available to select customers. The product and documentation are subject to change. Contact your Adobe representative to learn more.

To manage user access to different components of the Real-Time CDP Collaboration UI, an [administrator](./mange-user-access.md#system-admin-gain-access) can define and assign roles. Roles define the access that an administrator or user has to [resources](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#permissions){target=_blank} in your organization. This guide will provide information on the standard roles provided in Real-Time CDP Collaboration, as well as the individual permissions you that can be assign to custom roles.

To begin managing roles, an administrator will need access to the Experience Platform product. For information on gaining administrative access, or on gaining access to Experience Platform, read the [manage user access](./mange-user-access.md#manage-user-access-through-permissions) guide.

## Standard roles {#standard-roles}

There are two roles standard role provided to you that fill two common access control use cases. These are "read only" roles meaning they cannot be customized.

| Role name | Role description | Permissions |
| --- | --- | --- | 
| Collaboration Managers | This is all-access permission, containing all 15 permissions. This allows the user to view, create, and edit all data. | All from the table below. |
| Collaboration Viewers | This is a read only access permission. A user can view and discover data, activities, connections, and more. | All read permissions from the table below. |

{style="table-layout:auto"}

## Create specific access roles {#specific-access-roles}

You'll likely want to create additional roles to provide varying levels of access to different users. When creating roles, you can manage different access levels by selecting specific permissions within the **[!UICONTROL Collaborations]** resource. To learn how to create and manage roles, refer to the [roles](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/roles#create-new-role){target=_blank} guide.

Below is a list of available permissions within the Collaborations resource:

| High Level Permission | Description |
| --- | --- |
| Manage Collaboration Instances | View, create, update, and delete an organization's collaboration instances. Discover other organizations' collaboration instances. |
| Read Collaboration Instances | Read an organization's collaboration instances and discover other organizations' collaboration instances. |
| Manage Connection Invites | View, create, and delete connection invites initiated by your organization. Accept and decline connection invite initiated by other organizations. |
| Read Connection Invites | View connection invites. |
| Manage Collaboration Connections | An advertiser can view, create, and update settings as well as submit and delete connections. A publisher can view, accept, or decline connections. |
| Read Collaboration Connections | View connections. |
| Manage Audience Data | Onboard and discover audiences. Update public, private, and custom audiences and manage Audience Inventory metadata settings |
| Read Audience Data | Read and discover audiences. Update public, private, and custom audiences and manage Audience Inventory metadata settings. |
| Manage Measurement Data | Onboard, update, and delete measurement data. |
| Read Measurement Data | Read measurement data. |
| Manage Projects | View, create, update, and delete projects. |
| Read Projects | View projects. |
| Read User Activities | Read user activities. |
| Export User Activities | Export user activities. |
| Read Collaboration Credit Monitoring | Credit wallet monitoring at the organization and instance level. |

{style="table-layout:auto"}

## Next steps

After creating roles that define access to Real-Time CDP Collaborations, you'll need to [assign the roles](./mange-user-access.md#assign-a-role) to administrators and users. Refer to the [manage permissions for a role](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions) guide for a complete overview of managing roles. 
