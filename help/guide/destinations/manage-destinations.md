---
title: Configure and manage a destination
description: Learn how to configure and manage a destination in Real-Time CDP Collaboration.
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

<!-- exl-id/TQID to be assigned by the publishing pipeline when this page is finalized. -->

# Configure and manage a destination

{{limited-availability-release-note}}

>[!NOTE]
>
>This guide covers the common steps for configuring or deleting most destinations. Adobe Experience Platform has its own dedicated setup process — see [Configure Adobe Experience Platform as a destination](./experience-platform.md) instead.

Destinations are configured in the **[!UICONTROL Activation]** workspace. To see the full list of destinations you can configure, refer to the [available destinations](./overview.md#available-destinations) table.

>[!IMPORTANT]
>
>To configure and manage destinations, your user must have a role with the **Manage Audience Data** permission assigned to them. For more information about managing roles, refer to the [manage roles](../permissions/manage-roles.md) guide.

## Configure a destination {#configure-destination}

To configure a destination, navigate to the **[!UICONTROL Activation]** workspace and select the **[!UICONTROL Catalog]** tab. Find the destination you want to configure, and select **[!UICONTROL Set up]**.

The **[!UICONTROL Configure new destination]** workflow opens, with four steps:

1. **[!UICONTROL Authenticate]** — Connect to the destination using a new or existing account.
1. **[!UICONTROL Create destination]** — Name your destination and configure destination-specific settings, such as authentication and storage details.
1. **[!UICONTROL Map fields]** — Configure mappings by selecting the Real-Time CDP Collaboration match keys for activation. Target field names are auto-generated to match the source and can be edited if needed.
1. **[!UICONTROL Review]** — Review your configuration, then select **[!UICONTROL Complete]** to finish.

<!-- TODO (CORE-167477): these four steps and the Map fields wording are confirmed against Amazon S3 staging screenshots only. Verify the Create destination step's fields against the other five in-scope connectors (Azure Blob, Data Landing Zone, Google Cloud Storage, SFTP, Snowflake) before removing this note, and add screenshots once available — see the open gap in DOCUMENTATION_ACTION_ITEMS.md. -->

Once configured, your destination appears in the **[!UICONTROL Destinations]** tab, where you can view its status and the audiences activated to it.

## Delete a destination {#delete-destination}

Deleting a destination removes it from your account, removes any previously sent audiences from the destination, and prevents any future audiences from being sent to that destination.

To delete a destination, navigate to the **[!UICONTROL Activation]** workspace, select the **[!UICONTROL Destinations]** tab, and select **[!UICONTROL Delete]** for the destination that you want to remove. A confirmation dialog appears — select **[!UICONTROL Delete]** again to confirm.

## Next steps

Once you've configured your destination, you can begin [activating targeted audiences](../collaborate/activate.md) within your projects.
