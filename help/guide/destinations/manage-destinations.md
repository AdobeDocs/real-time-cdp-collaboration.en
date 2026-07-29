---
title: Configure and manage cloud storage destinations
description: Learn how to configure, view, and delete a cloud storage destination in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# Configure and manage cloud storage destinations

Use this guide to configure, view, and delete cloud storage destinations from the **[!UICONTROL Activation]** workspace. Use the **[!UICONTROL Catalog]** tab to configure destinations, the **[!UICONTROL Destinations]** tab to manage them, and the **[!UICONTROL Activated audiences]** tab to review audiences activated to destinations.

After you configure a destination, it becomes available when you activate audiences. To see the full list of supported destinations, refer to the [available destinations](./overview.md#available-destinations) table.

>[!NOTE]
>
> This guide uses an **[!DNL Amazon S3]** destination as an example. The guided configuration workflow is shared across supported cloud storage destination types, but authentication methods, required fields, and connector capabilities can vary. Before configuring a destination, review the [cloud storage destination requirements](./cloud-storage-destination-requirements.md), which link to the corresponding Adobe Experience Platform destination documentation.
>
> Adobe Experience Platform has a separate configuration workflow in Real-Time CDP Collaboration. To configure it, see [Configure Adobe Experience Platform as a destination](./experience-platform.md).

## Prerequisites {#prerequisites}

Before you configure a destination, ensure that:

* Your user has a role with the **Manage Audience Data** permission assigned. For more information about managing roles, see [Manage roles](../permissions/manage-roles.md).
* You have access to the **[!UICONTROL Activation]** workspace.
* You have the connection information required by your cloud storage provider.
* If you need to create an account, you have the required credentials or permissions.
* You have reviewed the [requirements for your cloud storage destination](./cloud-storage-destination-requirements.md).

## Configure a destination {#configure-destination}

When you configure a destination, you connect a cloud storage account to Real-Time CDP Collaboration and define how audience data is exported to it.

Navigate to **[!UICONTROL Activation]** > **[!UICONTROL Catalog]**.

The **[!UICONTROL Catalog]** tab displays the available destination providers. Each destination appears as a card. Depending on the destination, its card can display configured accounts and actions for viewing additional information.

![The Catalog tab displaying destination provider cards.](/help/assets/destinations/manage-destinations/destination-provider-catalog.png)

Locate the destination provider that you want to configure and select **[!UICONTROL Set up]**.

The destination configuration guided setup opens and guides you through four steps: **[!UICONTROL Authenticate]**, **[!UICONTROL Create destination]**, **[!UICONTROL Map fields]**, and **[!UICONTROL Review]**.

### Authenticate {#authenticate}

The **[!UICONTROL Authenticate]** step establishes a connection between Real-Time CDP Collaboration and your destination account.

If an existing account is available, select it from the account selector. To create an account, select **[!UICONTROL New account]**.

Select an authentication method and provide the required account information. Available authentication methods and fields depend on the selected destination provider. For connector-specific requirements, see [Cloud storage destination requirements](./cloud-storage-destination-requirements.md).

Select **[!UICONTROL Connect to Amazon S3]**. For other destination providers, the button displays the corresponding provider name.

After the account is validated successfully, select **[!UICONTROL Next]**.

![The Authenticate step showing account selection and new account creation.](/help/assets/destinations/manage-destinations/authenticate-destination-account.png)

### Create destination {#create-destination}

The **[!UICONTROL Create destination]** step defines where and how audience export files are delivered.

Enter a destination name and complete the required storage and export settings. The available fields depend on the selected destination provider. For definitions and connector-specific requirements, refer to the destination documentation linked from [Cloud storage destination requirements](./cloud-storage-destination-requirements.md).

After you complete all required fields, select **[!UICONTROL Next]**. The guided setup advances to the field-mapping step.

![The Create destination step displaying destination configuration fields.](/help/assets/destinations/manage-destinations/configure-new-destination.png)

### Map fields {#map-fields}

The **[!UICONTROL Map fields]** step defines how audience match keys are mapped to the identity fields expected by the destination.

Unlike the standard Real-Time CDP destinations workflow, Real-Time CDP Collaboration configures these mappings while the destination is created. Audience match keys appear as source fields. Map each source field to the corresponding target identity so that the destination can recognize the exported identifiers and associate them with the intended users.

Select **[!UICONTROL Add field]** to add another match-key mapping, or select the delete icon to remove a mapping. Review and configure all required mappings.

When the mappings are complete, select **[!UICONTROL Next]**. The guided setup advances to the review step.

![The Map fields step displaying activation match key mapping configuration.](/help/assets/destinations/manage-destinations/map-destination-fields.png)

### Review {#review-destination}

The **[!UICONTROL Review]** step summarizes the destination configuration before it is created.

Review the destination settings. To make changes, select the pencil icon ![The pencil icon.](../../assets/icons/edit.png) for the applicable section and update the configuration.

When the configuration is correct, select **[!UICONTROL Complete]**. The destination is created and becomes available for audience activation.

![The Review step displaying the destination configuration summary before completion.](/help/assets/destinations/manage-destinations/review-destination-configuration.png)

## View configured destinations {#view-configured-destinations}

After you configure a destination, it appears in your destination inventory. From the inventory, you can review its status and the audiences activated to it.

Navigate to **[!UICONTROL Activation]** > **[!UICONTROL Destinations]**. The **[!UICONTROL Destinations]** tab displays a table of configured destinations.

![The Destinations tab displaying configured destinations.](/help/assets/destinations/manage-destinations/configured-destinations-list.png)

## Delete a destination {#delete-destination}

Delete a destination when it is no longer required for audience activation. Deleting a destination removes it from your destination inventory and prevents audiences from being activated to it in the future.

>[!IMPORTANT]
>
>Deleting a destination does not remove audience data that was previously exported to it. Remove previously exported data directly from the destination datastore.

Navigate to **[!UICONTROL Activation]** > **[!UICONTROL Destinations]**.

Locate the destination that you want to remove, select the ellipsis icon in the **[!UICONTROL Action]** column, and then select **[!UICONTROL Delete]**.

![The Destinations tab of the Activation workspace with the ellipsis icon and Delete action highlighted.](/help/assets/destinations/manage-destinations/delete-configured-destination.png)

A confirmation dialog appears. Review the destination that will be removed, and then select **[!UICONTROL Delete]** to confirm.

The destination is removed from your destination inventory and is no longer available for audience activation.

## Next steps {#next-steps}

After you configure a destination, you can begin [activating audiences](../collaborate/activate.md) within your projects.
