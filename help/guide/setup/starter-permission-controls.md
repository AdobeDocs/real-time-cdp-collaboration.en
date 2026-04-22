---
title: Configure permission controls for Collaboration [!DNL Starter] onboarding
description: Learn how to configure permissions for Adobe Real-Time CDP Collaboration [!DNL Starter] using the Permissions in Adobe Experience Cloud.
audience: users invited to Real-Time CDP Collaboration [!DNL Starter]
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 4e50b6cc-58f7-4a0c-8b6d-f5aa4f092e9f
---
# Configure permission controls for Collaboration [!DNL Starter] onboarding

After setting up administrator and user access to the Adobe Experience Platform products, you need to assign yourself roles with the proper permissions for Real-Time CDP Collaboration. Read this guide to learn how to add the right roles to your account through the Experience Cloud Permissions interface, so you can access and manage user access to Collaboration features.

For details about standard roles and available permissions included in the Collaboration resource, see [how to manage roles guide](../permissions/manage-roles.md).

## Prerequistes {#prerequisites}

Ensure that you have both **administrator privileges** and **user access** to the Adobe Experience Platform product. If you haven't already set up these access levels, see the [administrator access guide](./starter-admin-access.md) for step-by-step instructions.

## Set up permissions {#setup-permissions}

Follow the steps below to set up the permissions you need for Collaboration. First, log in to [Adobe Experience Cloud](https://experience.adobe.com/) with your credentials. 

### Access Permissions {#access-permissions}

Once logged in, navigate to the **[!UICONTROL Quick access]** section and select **[!UICONTROL Permissions]**. This opens the Permissions dashboard where you can assign yourself the necessary roles.

![Experience Cloud homepage with Permissions within the Quick access section highlighted.](../../assets/setup/starter/access-permissions.png){zoomable="yes"}

### Select a user {#select-user}

In the **[!UICONTROL Permissions]** dashboard, select **[!UICONTROL Users]** from the left panel. Then select your account from the Users table.

>[!NOTE]
>
> If you are the first user from your organization to access Experience Platform, you may be the only user listed in the **Users** table. To invite additional team members, follow the steps in the [user access configuration guide](../permissions/manage-user-access.md#administrators-configure-user-access-to-experience-platform).

![Permissions dashboard displays the Users table with a user account highlighted.](../../assets/setup/starter/select-user.png){zoomable="yes"}

### Assign roles {#assign-roles}

In the corresponding **[!UICONTROL User]** workspace, navigate to the **[!UICONTROL Roles]** tab. Then select **[!UICONTROL Add Roles]**.

![The corresponding User workspace displays the Roles tab with the Add Roles option highlighted.](../../assets/setup/starter/add-roles.png){zoomable="yes"}

The **[!UICONTROL Add Roles]** dialog appears with a table of available roles. Each row in the table represents a role with the following information:

| **Column**    | **Description**                                         |
|---------------|--------------------------------------------------------|
| **Name**      | The name of the role.                                  |
| **Description** | A short summary outlining the role's function. Note that "read-only" roles cannot be customized. |
| **Sandboxes** | Specifies which sandboxes (for example, `Prod`) the role provides access to. |
| **Modified**  | The date the role was last updated.                    |

{style="table-layout:auto"}

For an in-depth overview of a specific role and its permissions, see the [Manage permissions for a role](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions) guide.

Review the information and select the roles you want to assign to your account. When finished, select **[!UICONTROL Save]**.

![Add Roles dialog displays the roles selected and the Save option highlighted.](../../assets/setup/starter/add-roles-dialog.png){zoomable="yes"}

A confirmation dialog confirms that new roles were successfully added. 

To make sure your permissions are set up correctly, return to the [Experience Cloud](https://experience.adobe.com/) homepage. Select **[!UICONTROL Real-Time CDP Collaboration]** within **[!UICONTROL Quick access]**. You should be able to access Collaboration workspace and begin using the features available for your [!DNL Starter] account.

## Next steps {#next-steps}

With your permissions set up, you are ready to access Collaboration. Next, you can:

* [Create custom roles with specific permissions to manage different access levels](../permissions/manage-roles.md#create-specific-access-roles).
* [Assign multiple users to one role in Permissions](../permissions/manage-user-access.md#assign-a-role).
* [Set up Collaboration account and establish connections with your inviting collaborator](../overview/starter-overview.md#set-up-connections).
* [Learn more about credit usage and consumption in Collaboration [!DNL Starter]](./starter-credit-usage.md).

To get a complete overview of Real-Time CDP Collaboration and its key features, read the [overview guide](../home.md).
