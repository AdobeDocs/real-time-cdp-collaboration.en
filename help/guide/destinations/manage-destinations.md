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

This task explains how to configure a cloud storage destination from the **[!UICONTROL Activation]** workspace. After you configure a destination, it becomes available when you activate audiences. To see the full list of destinations you can configure, refer to the [available destinations](./overview.md#available-destinations) table.

>[!NOTE]
>
>This guide uses an **[!DNL Amazon S3]** destination as an example. The configuration guided setup is shared across supported cloud storage destination types, although connector-specific fields can vary. For connector-specific requirements, refer to the corresponding Adobe Experience Platform destination documentation. A list of specific configuration fileds required for each are listed in the [Cloud storage destination requirements](./cloud-storage-destination-requirements.md) with links to their respective documentation. Adobe Experience Platform itself has its own dedicated setup process in Real-Time CDP Collaboration, see [Configure Adobe Experience Platform as a destination](./experience-platform.md) instead.

## Prerequisites {#prerequisites}

Before you configure a destination, ensure that:

* Your user has a role with the **Manage Audience Data** permission assigned. For more information about managing roles, refer to the [manage roles](../permissions/manage-roles.md) guide.
* You have access to the **[!UICONTROL Activation]** workspace.
* You have the connection information required for your cloud storage provider.
* If you create a new account, you have the credentials or permissions required by your cloud storage provider.

## Configure a destination {#configure-destination}

When you configure a destination, you connect your cloud storage account to Real-Time CDP Collaboration so that you can activate audiences to it. To begin, navigate to **[!UICONTROL Activation]** > **[!UICONTROL Catalog]**.

The **[!UICONTROL Catalog]** tab displays the available destination providers. Each destination appears as a card. Depending on the destination, a card can display configured accounts and actions for viewing additional information.

![The Catalog tab displaying destination provider cards.](/help/assets/destinations/manage-destinations/destination-provider-catalog.png)

Locate the destination provider that you want to configure and select **[!UICONTROL Set up]**. The destination configuration guided setup opens and guides you through four steps: **[!UICONTROL Authenticate]**, **[!UICONTROL Create destination]**, **[!UICONTROL Map fields]**, and **[!UICONTROL Review]**.

### Authenticate {#authenticate}

The **[!UICONTROL Authenticate]** step establishes the connection between Adobe Experience Platform and your destination account.

If an existing account is available, select the account that you want to use from the droppdown selector. To create a new account, select **[!UICONTROL New account]**.

Select an existing account or create an account. Authentication options and required account information vary by destination. For connector-specific prerequisites and configuration requirements, see [Cloud storage destination requirements](./cloud-storage-destination-requirements.md).

Choose your authentication type for the destination.

Input the required account information as required by your cloud storage provider. 

Select **[!UICONTROL Connect to Amazon S3]**, or respective destination provider.

Once the account is validated, a check mark appears next to the providers name. Select **[!UICONTROL Next]** to continue.

![The Authenticate step showing account selection and new account creation.](/help/assets/destinations/manage-destinations/authenticate-destination-account.png)

### Create destination {#create-destination}

The **[!UICONTROL Create destination]** step defines where audience export files are delivered.

Complete all required destination settings, including:

* **Destination name**
* **Bucket name**
* **Folder path**
* **S3 encryption algorithm**
* **Compression format**
* **File type**

Use the available dropdown lists to select values for the required configuration options. After you complete all required fields, select **[!UICONTROL Next]**. The guided setup advances to the field mapping step.

![The Create destination step displaying destination configuration fields.](/help/assets/destinations/manage-destinations/configure-new-destination.png)

<!-- TODO (CORE-167477): the fields listed above (bucket name, S3 encryption algorithm, compression format, file type) are confirmed for Amazon S3 only. Verify against the other five in-scope connectors (Azure Blob, Data Landing Zone, Google Cloud Storage, SFTP, Snowflake) before publishing — see the open gap in DOCUMENTATION_ACTION_ITEMS.md. -->

Accepted file types are: JSON, CSV, and Parquet. For CSV file type, ensure the file formatting settings are correct for the file format. use the dropdown selectors to configure these options. For more details, refer to the configuration guide on how to [Configure file formatting options for file-based destinations](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/batch-destinations-file-formatting-options#file-configuration).

JSON and Parquet file formats have the option to include heriarchical data such as arrays, maps, and objects as part of your activation. See the [Export arrays, maps, and objects from Real-Time CDP guide](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-arrays-maps-objects) for more information. Select the [!UICONTROL Include Hierarchical Output] checkbox to enable this function.

### Map fields {#map-fields}

The **[!UICONTROL Map fields]** step defines how match keys are mapped to a target identity for the destination.
<!-- Can we elaborate on what that means for the user. -->

Select [!UICONTROL Add field] to add additional match keys, or the trash icon to remove unwanted rows. Review and configure the required field mappings. When the mappings are complete, select **[!UICONTROL Next]**. The guided setup advances to the review step.

![The Map fields step displaying activation match key mapping configuration.](/help/assets/destinations/manage-destinations/map-destination-fields.png)

### Review {#review-destination}

The **[!UICONTROL Review]** step summarizes your destination configuration before it is created. Review the destination settings. If changes are required, select the pencil icon ![The pencil icon.](../../assets/icons/edit.png) to return to the appropriate guided setup step and update the configuration.

When the configuration is correct, select **[!UICONTROL Complete]**. The destination is created and becomes available for audience activation.

![The Review step displaying the destination configuration summary before completion.](/help/assets/destinations/manage-destinations/review-destination-configuration.png)

## View configured destinations {#view-configured-destinations}

After you configure a destination, it appears in your destination inventory, where you can review its status and the audiences activated to it.

Navigate to **[!UICONTROL Activation]** > **[!UICONTROL Destinations]**. The **[!UICONTROL Destinations]** tab displays a table of your configured destinations.

![The Destinations tab displaying configured destinations.](/help/assets/destinations/manage-destinations/configured-destinations-list.png)

## Delete a destination {#delete-destination}

Delete a destination when it is no longer required for audience activation. Deleting a destination removes it from your account and prevents any future audiences from being sent to that destination.

>[!IMPORTANT]
>
>Deleting a destinations does not remove any previously sent audiences from the destination. You must independently remove that data from the datastore.

Navigate to **[!UICONTROL Activation]** > **[!UICONTROL Destinations]**, locate the destination that you want to remove, and select the elipses in the [!UICONTROL Action] column. Select Delete from the dropdown menu to permenently remove that destination.

![The Destinations tab of the Activation workspace with the ellipses and Delete highlighted in the Action column.](../../assets/destinations/manage-destinations/delete-configured-destination)

A confirmation dialog appears. Review the destination that will be removed, then select **[!UICONTROL Delete]** to confirm the action. The destination is removed from your destination inventory and is no longer available when activating audiences.

## Next steps {#next-steps}

After you configure a destination, you can begin [activating targeted audiences](../collaborate/activate.md) within your projects.
