---
title: Access Control Overview
description: Learn how to gain access to Adobe Real-Time Customer Data Platform (CDP) Collaboration.
audience: admin
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: af48f5ea-8258-42a6-a39e-f4a4ca5b4a69
---
# Access control overview

{{limited-availability-release-note}}

>[!IMPORTANT]
>
> If you're an end user wanting access to Real-Time CDP Collaboration, reach out to your system or product administrator to check for existing access. If you don't know who your system administrator is, please reach out to your Adobe representative.

Access control for Real-Time Customer Data Platform (CDP) Collaboration is provided through the Admin Console and Permissions in [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}. In this guide, you'll learn how to give access to yourself or other members of your team, depending on your use case. 

## Access control hierarchy {#hierarchy}

To configure access control to Real-Time CDP Collaboration, you **must** have system or product administrator privileges. A system administrator has no restrictions and is provisioned during the onboarding process. Meanwhile, a product administrator can provide administrative functions for all products they've been assigned to. A product administrator must be given product and administrative access by a system administrator. 

These guides will describe configuring access for system administrators, product adminstrators, and end users. Refer to the table below to understand the key difference between the roles.

| Role | Description |
| --- | --- | 
| System administrator | The super user for the organization. They are able to perform all administrative tasks in the Admin Console and have permissions to delegate administrative functions to other users.  |
| Product administrator | Administers the products assigned to them and all associated administrative functions, such as adding users to organizations, adding or removing users from product profiles, and adding or removing other product administrators from a product. |
| End user | The users in your organization who use the products. | 

{style="table-layout:auto"}

For more information on administrative roles, visit the [Adobe Help Center](https://helpx.adobe.com/enterprise/using/admin-roles.html). 

>[!TIP]
>
>The use of **administrators** in these guides will refer to **both system and product administrators**.

## Additional products {#products}

Before you can give access to Real-Time CDP Collaboration, you'll need access to multiple products, depending on your [use case](#use-cases). The access control guides may work through mutiple user interfaces as you progress, each serving a specific purpose within the access configuration process. Refer to the table below to get a deeper understanding of what each product will be used for.

| Product | Uses |
| --- | --- |
| [Admin Console](https://adminconsole.adobe.com/) | Administrators use this to assign users product and/or admin access. |
| [Permissions](https://experience.adobe.com/) | Administrators use this to assign administrators or end users roles. |
| [Experience Platform](https://platform.adobe.com/) | Administrators and end users need to be given access to Experience Platform product to assign them to roles. |

## Where to begin {#use-cases}

Now that you have a deeper understanding of the user and administrative roles, as well as the different Experience Cloud products, you can begin giving access to Real-Time CDP Collaboration. There are two main factors that influence the steps you'll need to take:

- if you're assigning administrator or end user access
- if the users already has access to the Experience Platform product
  
Refer to the chart below to determine who is needed to configure the privileges and where to start based off your access control use case. **Be sure to follow the tutorial through to the end of the guide from your starting place.**

>[!TIP]
>
> A super user refers to the highest level of access to be gained by the system administrator. A super user can perform all administrative tasks and user functionality. A system administrator does not have product functionality out-of-the-box and need to give themselves the appropriate access, as shown in the chart below. 

| Use case | Required role | Where to begin | 
| --- | --- | --- | 
| Super user with no existing Experience Platform product access. | A system administrator. | [Configure product administrator access](./manage-user-access.md#admin-access) |
| Super user for an existing Experience Platform system administrator **with** Experience Platform UI access. | A system administrator. | [Configure Real-Time CDP Collaboration access](./manage-user-access.md#RTCDP-collab-access) |
| Super user for an existing Experience Platform system administrator **without** Experience Platform UI access. | A system administrator. | [Configure product administrator access](./manage-user-access.md#admin-access) |
| Product administrator privileges and Real-Time CDP Collaboration access for a new product administrator. | A system administrator. | [Configure product administrator access](./manage-user-access.md#admin-access) |
| Real-Time CDP Collaboration access for an existing Experience Platform product administrator **with** Experience Platform UI access. | A system or product administrator. | [Configure Real-Time CDP Collaboration access](./manage-user-access.md#RTCDP-collab-access) |
| Real-Time CDP Collaboration access for an existing Experience Platform product administrator **without** Experience Platform UI access. | A system or product administrator. | [Configure user access](./manage-user-access.md#user-access) |
| Real-Time CDP Collaboration access for a new end user. | A system or product administrator. | [Configure user access](./manage-user-access.md#user-access) |
| Real-Time CDP Collaboration access for an existing user with Experience Platform access. | A system or product administrator. | [Configure Real-Time CDP Collaboration access](./manage-user-access.md#RTCDP-collab-access) |

{style="table-layout:auto"}

## Additional Permissions

Once you've gained access to Real-Time CDP Collaboration, you may need some additional Experience Platform permissions for specific functionality. 

### Audience importation {#audience-importation}

Before you can begin sharing audiences with collaborators, you need to import audiences into Real-Time CDP Collaboration. Currently, the only data connection supported for importing audiences is Experience Platform. To begin, the user(s) managing audience onboarding will need to be assigned a role containing the following **Profile Management** resource permissions:

| Permission | Description |
| ---- | ---- |
| View Segments | Allows the user to see the list of available audiences in a sandbox. |
| View Profiles | Allows the user to see the fields available for mapping to collaboration fields. |

Below, you can see an example role with the above permissions added. For more information on creating or assigning roles, refer to the [manage roles](./manage-roles.md) guide. 

![The resources workspace in Permissions with the View Segments and View Profiles permissions added to the Profile Management resource.](../../assets/permissions/sample-audience-role.png)

>[!NOTE]
>
>Users are able to work with audiences within Real-Time CDP Collaboration after they've been imported without any of the above permissions.

## Next steps

Once you've determined where to begin, follow your use case's link to get started configuring access. If you're wanting to learn about configuring access to Real-Time CDP Collaboration as an administrator beyond those use cases, refer to the [manage user access](manage-user-access.md) guide. To learn about roles and their part in configuring access to various components of Real-Time CDP Collaboration, refer to the [manage roles](manage-roles.md) guide.
