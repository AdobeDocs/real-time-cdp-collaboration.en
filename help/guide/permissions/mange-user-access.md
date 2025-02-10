---
title: Manage user access through Permissions
description: Understand how to manage users access to different parts of the Real-Time CDP Collaboration UI.
audience: admin
badgebeta: label="Beta" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
---
# Manage user access through Permissions {#manage-user-access}

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently a beta product, available to select customers. The product and documentation are subject to change. Contact your Adobe representative to learn more.

Manage permissions and user access to individual components within Real-Time CDP Collaboration through Experience Cloud's [Permissions UI](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/browse). Permissions allows administrators to define [roles](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/roles) to manage users access to specific features and resources. 

To access the Permissions UI, you must be an administrator that has a subscription to Adobe Experience Platform. Refer to the sections below to gain access as a system administrator, or to grant access to your team.

## System administrators: grant the necessary permissions for yourself and your role {#system-admin-gain-access}

As a [system administrator](https://helpx.adobe.com/enterprise/using/admin-roles.html), you have out-of-the box access to specific Experience Cloud products, such as Adobe Admin Console. However, to use products such as Permissions and Experience Platform, you are also required to give yourself administrator and user access to the Experience Platform product. This access allows you to use the product as well as grant and manage user access to your team. Follow the step-by-step guide below to give yourself administrative access to these products as a system admin.

### Gain access to Experience Platform and Permissions {#experience-platform-and-permissions}

Log in to [Adobe Experience Cloud](https://experience.adobe.com/) with your credentials. The home view displays with the **[!UICONTROL Quick access]** section providing access to your available products. To begin gaining access to Experience Platform and Permissions, select **[!UICONTROL Admin Console]**.

![Experience Cloud's home view with Admin Console highlighted.](../../assets/permissions/experience-cloud.png)

#### Gain admin access

The [Adobe Admin Console](https://adminconsole.adobe.com/) overview dashboard displays. Select **[!UICONTROL Adobe Experience Platform]** from the **[!UICONTROL Products]** list under **[!UICONTROL Products and services]**.

![Admin Console's overview dashboard with the Adobe Experience Platform product highlighted.](../../assets/permissions/admin-console.png)

The Adobe Experience Plaform dashboard displays. Select the **[!UICONTROL Admins]** tab and then select **[!UICONTROL Add admin]**.

![Adobe Experience Platform product dashboard with the Admins tab selected and Add admin highlighted.](../../assets/permissions/add-admin.png)

The **[!UICONTROL Add product administrators]** dialog appears. Enter your email or username into the **[!UICONTROL Email or username]** text field and then select your account from the dropdown. Select **[!UICONTROL Save]** to finish adding yourself as an administrator.

![The Add product administrators dialog with a users information filled in and the Save option selected.](../../assets/permissions/add-product-administrators.png)

#### Gain product access

Next, select the **[!UICONTROL Users]** tab and then select **[!UICONTROL Add users]**.

![Adobe Experience Platform product dashboard with the Users tab selected and Add users highlighted.](../../assets/permissions/add-users.png)

The **[!UICONTROL Add users to this product]** dialog appears. Enter your name or email into the **[!UICONTROL Name, user group or email address]** text field and then select your account from the dropdown. Next, select **[!UICONTROL Products]** add option.

![The Add users to this product dialog with a users information filled in and the Products add option selected.](../../assets/permissions/add-users-to-product.png)

The **[!UICONTROL Select product profiles]** dialog appears. Select **[!UICONTROL AEP-Default-All-Users]** and **[!UICONTROL Default Production All Access]** and then select **[!UICONTROL Apply]**.

![The Select product profiles dialog with the AEP-Default-All-Users and Default Production All Access options selected and Apply highlighted.](../../assets/permissions/select-product-profiles.png)

Confirm your information is correct and then select **[!UICONTROL Save]**.

![The Add users to products dialog with the users information and product profiles displayed and Save highlighted.](../../assets/permissions/save-selections.png)

#### Gain Experience Platform access

Return to Adobe Experience Cloud. You should now see **[!UICONTROL Experience Platform]** and **[!UICONTROL Permissions]** inside of **[!UICONTROL Quick access]**. 

![Experience Cloud's home view with Experience Platform and Permissions highlighted.](../../assets/permissions/experience-cloud-products.png)

>[!NOTE]
>
> The products can take several minutes to gain access to and you'll receive an email alerting you you've recieved access. If you're not seeing Experience Platform or Permissions in Adobe Experience Cloud after receiving the email, log out and then back in to your account. 

At this stage, you can now access **[!UICONTROL Permissions]**. If you try to access **[!UICONTROL Experience Platform]**, you'll get a warning that no sandboxes are enabled, as shown below. To solve this, you need to assign the [default roles](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#default-roles) to your user.

Select **[!UICONTROL Permissions]**

![Experience Cloud's home view with a warning displayed and Permissions highlighted.](../../assets/permissions/experience-cloud-warning.png)

The **[!UICONTROL Permissions]** dashboard will display. Select **Users** from the panel and then select your name.

![Permissions dashboard with the Users workspace displayed and a user highlighted.](../../assets/permissions/permissions-user.png)

Select the **[!UICONTROL Roles]** tab and then select **[!UICONTROL Add roles]**.

![The user workspace with the Roles tab displayed and Add roles highlighted.](../../assets/permissions/user-roles.png)

The **[!UICONTROL Add Roles]** dialog appears. Select **[!UICONTROL Default Production All Access]** and **[!UICONTROL Sandbox Administrators]** and then select **[!UICONTROL Save]**.

![The Add Roles dialog with Default Production All Access and Sandbox Administrators selected, and Save highlighted.](../../assets/permissions/add-roles.png)

You now have access to Experience Platform and Permissions. Next, you'll give yourself access to Real-Time CDP Collaboration.

### Gain access to Real-Time CDP Collaboration

To access the Real-Time CDP Collaboration UI, you'll need to define an all-access role within Permissions. To learn how to create an all-access role for Real-Time CDP Collaboration, refer to the [manage roles](./manage-roles.md#all-access-role) guide. 

#### Assign a role

Once your role is created, add that role to your user following the same steps [as before](#gain-experience-platform-access), or by adding a user directly to the role as follows.

In **[!UICONTROL Permissions]** select **[!UICONTROL Roles]** from the panel and then select your role from the list.

![The Permissions dashboard with the Roles workspace displayed and a role highlighted.](../../assets/permissions/select-role.png)

The role's detail page displays. Select the **[!UICONTROL Users]** tab and then select **[!UICONTROL Add Users]**.

![The role's detail workspace with the Users tab displayed and Add Users highlighted.](../../assets/permissions/role-users.png)

The **[!UICONTROL Add Users]** dialog appears. Select the user(s) from the list and then select **[!UICONTROL Save]**.

![The Add Users dialog with a user select and the Save option highlighted.](../../assets/permissions/add-users-to-role.png)

Next, return to Experience Cloud. You should now see **[!UICONTROL RTCDP Collaboration]** listed as a product under **[!UICONTROL Quick Access]**.

![Experience Cloud with RTCDP Collaboration product highlighted under Quick access](../../assets/permissions/rtcdp-experience-cloud.png)

## System administrators: grant the necessary permissions for your team

Next, you'll give Real-Time CDP Collaboration access to your team. Every user will need product access for Experience Platform even if they're only working with Real-Time CDP Collaboration. Follow the steps in the [gain product access](#gain-product-access) section for each user of your team to give them access.

Once you've provided product access to each user, navigate to **[!UICONTROL Permissions]**. You'll need to assign users roles containing the correct resource permissions for the access they need. Follow the guide on creating [specific access roles](./manage-roles.md#specific-access-roles) for information on how to create the roles as well as detailed information about each resource permission.

When you've created your roles, follow the [assign a role to a user](#assign-a-role) guide for each user to finish granting access to your team.

## Next Steps

Now that you and your team have access to Real-Time CDP Collaboration you can begin using the product. To learn more about the product as a whole, read the [overview guide](../home.md). 

