---
title: Configure [!DNL Databricks Delta Share] for Audience Sourcing
description: Learn how to configure and connect [!DNL Databricks Delta Share] for audience sourcing in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
---

# Configure [!DNL Databricks Delta Share] for audience sourcing

Follow the steps in this guide to connect your [!DNL Databricks Delta Share] to Adobe Real-Time CDP Collaboration and begin sourcing first-party audience data through the UI.

Connect a [!DNL Databricks Delta Share] to Collaboration to ingest first-party audience data directly from your Unity Catalog share without exporting files to object storage. Once connected, Collaboration sources audiences from the tables you specify and makes them available for activation and overlap analysis within your collaboration projects. Sourcing your audiences is a required step before you can activate them or use them in overlap analysis with collaborators.

This guide covers the end-to-end configuration workflow: preparing prerequisites, connecting your [!DNL Delta Share], specifying membership and optional metadata tables, mapping identity fields, and confirming that sourcing completed successfully.

Audiences sourced from [!DNL Databricks] follow the same governance and data handling rules as audiences sourced from Adobe Experience Platform and other supported cloud sources.

Other available sourcing methods include [Experience Platform](./onboard-audiences.md), [Amazon S3](./configure-aws-s3-audience-sourcing.md), [Google Cloud Storage](./configure-gcs-audience-sourcing.md), [Snowflake](./configure-snowflake-audience-sourcing.md), [Azure storage](./configure-azure-storage-audience-sourcing.md), and [CSV file upload](./upload-csv-audience-sourcing.md). To learn more about all available sources in Collaboration, see [Sources overview](./source-overview.md).

## Prerequisites {#prerequisites}

Complete all items in this section before starting the configuration workflow. Incomplete prerequisites are the most common reason setup fails or audiences do not appear after sourcing. Before following this guide, you must have completed [account onboarding and setup](./onboard-account.md).

Some steps in this section require action by a [!DNL Databricks] administrator. If you are not the [!DNL Databricks] administrator for your organization, identify the appropriate person before starting.

### [!DNL Databricks Delta Share] access {#databricks-delta-share-access}

Before proceeding, confirm the following with your [!DNL Databricks] administrator:

* Your organization has published a [!DNL Delta Share] to Adobe's [!DNL Databricks] account using native Databricks-to-Databricks sharing (Unity Catalog). Collaboration does not support bearer-token or OIDC credential entry in the UI for this workflow.
* You know the provider name as registered in Adobe's Unity Catalog metastore, the share name, and the schema that contains your audience tables.
* [!DNL Databricks Delta Share] audience sourcing is available for your Collaboration account and region. If Databricks sourcing is not yet available in your region, contact your Adobe account representative to confirm a timeline.

For step-by-step instructions on publishing a share to Adobe, see the [Publish your Delta Share to Adobe](#publish-delta-share) section in this guide.

### Prepare your audience data {#prepare-audience-data}

Your audience tables must be structured so Collaboration can discover audiences and map identities correctly. Key requirements include:

* **Membership table (required):** A table within your shared schema that contains one row per profile-audience pair. This table must include a column mappable to `AUDIENCE_ID` and at least one supported match key column.
* **Metadata table (optional):** If you maintain a separate catalog of audiences (one row per audience with audience ID, name, counts, or similar metadata), you can provide this table so Collaboration reads audience definitions from it instead of inferring distinct audience IDs from the membership table alone.
* **Supported match keys:** `HASHED_EMAIL_SHA_256`, `HASHED_PHONE_SHA_256`, `HASHED_IPV4_SHA_256`, `CRM_ID`, `LOYALTY_ID`, `ADFIXUS_ID`, and other match keys enabled for your Collaboration account.
* **Hashing requirements:** All match key values must be trimmed, lowercased, and SHA256-hashed before they are stored in [!DNL Databricks]. Collaboration does not hash or normalize data before ingestion.
* **Column consistency:** The membership table must expose stable column names that Collaboration can map to your enabled match keys.

All match keys present in your membership table must also be enabled for your Collaboration account. To add or enable match keys, see [Set up match keys](./onboard-account.md#set-up-match-keys).

### Values required before you begin {#required-values}

Have the following values ready before starting the configuration wizard.

| Value | Description |
| ----- | ----------- |
| Provider name             | The provider identifier Adobe uses in Unity Catalog to consume your [!DNL Delta Share]. Your [!DNL Databricks] administrator or Adobe onboarding contact can supply this value. It is not the same as your [!DNL Databricks] workspace URL. |
| Share name                | The name of the [!DNL Delta Share] published to Adobe.  |
| Schema                    | The schema within the share that contains your audience tables. |
| Membership table          | The table name within the schema that holds audience membership rows (one row per profile in an audience). |
| Metadata table (optional) | The table name within the schema that lists audiences (one row per audience), if you use a metadata-driven audience catalog. |

{style="table-layout:auto"}

## Configure your [!DNL Databricks] connection {#configure-databricks-connection}

The configuration workflow is a multi-step wizard inside the **[!UICONTROL Setup]** workspace. Complete each step in sequence. You can return to any step using the pencil icon on the final review screen before you create the connection.

### Add a new data connection {#add-data-connection}

From the **[!UICONTROL My audiences]** tab within the **[!UICONTROL Setup]** workspace, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Audience]**.

If this is your first audience, you may also select the **[!UICONTROL Add]** option.

![The My audiences tab in the Setup workspace with the add icon and Add audience option displayed.](../../assets/adobe-logo-old.png)

The Add audience workflow appears. Select **[!UICONTROL Add a new data connection]** and then select **[!UICONTROL Next]**.

![The Add audiences workspace with the Add a new data connection option highlighted.](../../assets/adobe-logo-old.png)

### Select [!DNL Databricks Delta Share] as the data source {#select-databricks-delta-share}

The data source selection screen lists all available connection types. Select **[!UICONTROL Databricks Delta Share]** and then select **[!UICONTROL Next]**.

![The Add audience workflow showing the data source selection screen with Databricks Delta Share selected and Next highlighted.](../../assets/adobe-logo-old.png)

A prerequisite dialog outlining required configuration steps appears. It confirms that your [!DNL Delta Share] is published to Adobe, that you know your provider name, share name, schema, and table names, and that your membership table includes mappable match keys including `AUDIENCE_ID`. Select **[!UICONTROL Start onboarding]** to confirm before proceeding.

![The "Prepare your Databricks Delta Share for onboarding" modal listing prerequisites, including publishing a share to Adobe and preparing membership (and optional metadata) tables, with Cancel and "Start onboarding" options.](../../assets/adobe-logo-old.png)

### Connect your [!DNL Delta Share] {#connect-delta-share}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sharing_databricks"
>title="Add audience from Databricks Delta Share"
>abstract="Connect a Databricks Delta Share to source your audience data. Follow the steps outlined in Experience League to configure your share and grant Adobe access."

Provide the details required to allow Collaboration to access your [!DNL Delta Share]. After entering the required information, select **[!UICONTROL Next]**.

Collaboration validates the share and mounts it in Adobe's workspace. This step may take up to one minute. A progress indicator appears while the connection is established.

| Field | Description |
| --- | --- |
| **[!UICONTROL Provider name]** | The Unity Catalog provider name Adobe uses to consume your share. See [Values required before you begin](#required-values). |
| **[!UICONTROL Share name]** | The name of the [!DNL Delta Share] published to Adobe. |
| **[!UICONTROL Schema]** | The schema within the share that contains your audience tables. |

{style="table-layout:auto"}

![The Add audience workflow showing the Databricks connect-share form with provider name, share name, and schema fields, and the Next button available.](../../assets/adobe-logo-old.png)

If the share cannot be found or the schema is not yet visible, an error message appears. Verify the values with your [!DNL Databricks] administrator and try again.

### Specify tables and audience discovery {#specify-tables-and-audience-discovery}

Specify which tables Collaboration uses to source audiences and how audiences are discovered.

#### Choose how audiences are discovered {#audience-discovery}

Select one of the following options:

* **[!UICONTROL From membership data]** (default): Collaboration discovers distinct audience IDs from your membership table. Use this option when you do not maintain a separate audience catalog table in [!DNL Databricks].
* **[!UICONTROL From a metadata table]**: Collaboration reads audience definitions from a dedicated metadata table (one row per audience). Use this option when you maintain an audience catalog in [!DNL Databricks]. Collaboration still reads membership rows from the membership table for identity data.

#### Enter table names {#specify-table}

| Field | When required | Description |
| --- | --- | --- |
| **[!UICONTROL Membership table]** | Always | The table that contains one row per profile-audience pair. Must include columns mappable to `AUDIENCE_ID` and your match keys. |
| **[!UICONTROL Metadata table]** | When using metadata-driven discovery | The table that lists audiences (one row per audience). Required when you select **[!UICONTROL From a metadata table]**. |

{style="table-layout:auto"}

For each table, select **[!UICONTROL Preview table]** to confirm the table name and review sample columns before continuing. If preview fails, verify the table name and that the table exists in the shared schema.

![The Add audience workflow showing the tables step with audience discovery options, membership table and metadata table fields, and Preview table actions.](../../assets/adobe-logo-old.png)

Select **[!UICONTROL Next]** to continue.

### Confirm consent and data use acknowledgment {#confirm-consent}

You must confirm that consent opt-outs have been removed from the audience data before Collaboration can process it. If you are unsure whether your data meets this requirement, review the [governance policy and enforcement actions](./onboard-audiences.md#governance-policy-and-enforcement-actions) guide before proceeding. Select the confirmation checkbox and then select **[!UICONTROL OK]** to proceed.

### Provide connection details {#provide-connection-details}

Enter a name and an optional description for this data connection. The name you provide appears in the **[!UICONTROL My data connections]** tab and helps distinguish this source if you manage multiple data connections.

* **[!UICONTROL Data connection name]** (required)
* **[!UICONTROL Data connection description]** (optional)

Select **[!UICONTROL Next]** to continue.

![Add audience workflow on the "Provide details" step showing fields for Data connection name and Data connection description populated with example values, with "Next" visible in the top-right corner.](../../assets/adobe-logo-old.png)

### Map identity fields {#map-identity-fields}

The **[!UICONTROL Mapping]** screen displays source columns from your membership table mapped to target identity fields. Collaboration automatically maps source fields to target fields based on column names and your enabled match keys. You can adjust mappings before continuing.

**`AUDIENCE_ID`** must be mapped to a source column before you can proceed. At least two fields must be fully mapped (source and target).

>[!TIP]
>
>Select **[!UICONTROL Preview source data]** to review a sample of your membership table in tabular format, then select **[!UICONTROL Close]** to return to the mapping screen.

![The "Databricks data preview" dialog showing a sample table of audience data with columns such as AUDIENCE_ID and HASHED_EMAIL_SHA_256, and a Close button in the bottom-right corner.](../../assets/adobe-logo-old.png)

Confirm that the displayed mappings reflect the columns in your membership table. If **`AUDIENCE_ID`** is not mapped or required match keys are missing, correct your table structure or adjust mappings before proceeding. Select **[!UICONTROL Next]** to continue.

![Add audience workflow on the "Map fields" step showing source fields mapped to target identity fields, with the "Preview source data" option visible and the Next button in the top-right corner.](../../assets/adobe-logo-old.png)

### Review and complete the connection {#review-and-complete}

Review the configuration summary before creating the connection. The summary screen displays the following sections:

* **[!UICONTROL Share connection]**: The provider name, share name, and schema you configured.
* **[!UICONTROL Tables]**: The membership table, optional metadata table, and audience discovery model.
* **[!UICONTROL Details]**: The name and optional description of this data connection.
* **[!UICONTROL Mapping]**: The source and target identity field mappings.

![Add audience workflow on the "Review" step showing a summary of the share connection, tables, details, and mapping sections with configured values, and the Complete button visible in the top-right corner.](../../assets/adobe-logo-old.png)

Select the pencil icon (![A pencil icon.](../../assets/icons/edit.png)) next to any section to return to that step and make changes. When all sections are correct, select **[!UICONTROL Complete]**.

A confirmation dialog appears, indicating that Collaboration created the data connection and that audience sourcing is in progress.

>[!IMPORTANT]
>
>[!DNL Databricks] audience sourcing is a one-time import when you create the connection. Unlike some other sources, this workflow does not include a recurring refresh schedule. To source updated audience data from [!DNL Databricks], contact your Adobe account representative for guidance on your supported update path.

## Review sourced audiences {#review-sourced-audiences}

After you complete the configuration wizard, Collaboration begins sourcing audiences from your [!DNL Databricks] tables asynchronously. Navigate to **[!UICONTROL Setup]** > **[!UICONTROL My audiences]** to monitor progress. Sourcing does not complete immediately; the time required depends on the size of your data.

### Monitor audience sourcing progress {#monitor-sourcing-progress}

While Collaboration is retrieving your audience data, a banner at the top of the **[!UICONTROL My audiences]** workspace indicates that sourcing is in progress. Individual audiences appear in the list only after sourcing completes for each audience.

![Setup workspace on the My audiences tab showing an "Audience sourcing in progress" banner indicating that audiences are being sourced from a Databricks data connection, with the audience list displayed below.](../../assets/adobe-logo-old.png)

>[!TIP]
>
>Audience sourcing time varies based on the size of your membership table and whether you use a metadata table for audience discovery. Larger datasets may take longer to appear in the **[!UICONTROL My audiences]** workspace.

### View sourced audience details {#view-audience-details}

Once sourcing completes, your [!DNL Databricks] audiences appear in the **[!UICONTROL My audiences]** tab alongside audiences sourced from other connections. Select a row item or **[!UICONTROL View audience]** to open the detail view for a specific audience.

![The "My audiences" tab in the Setup workspace showing a table of audiences, including one sourced from Databricks Delta Share, with selectable checkboxes and row actions available.](../../assets/adobe-logo-old.png)

The detail view displays the audience's status, source, and data connection name, along with the following panels:

* **[!UICONTROL Identities]**: The total identity count and breakdown for the audience, once data becomes available.
* **[!UICONTROL Categories]**: Any tags applied for organizing or filtering the audience.
* **[!UICONTROL Connection access]**: Whether the audience is private, public, or shared with specific collaborators.
* **[!UICONTROL Metadata visibility]**: What audience information, such as identity count, overlap percentage, and index, is visible to collaborators.

![Individual audience detail view showing Status: Active, the source system, and data connection name at the top, with four panels below: Identities, Categories, Connection access, and Metadata visibility.](../../assets/adobe-logo-old.png)

Review these settings before using the audience in a collaboration project. To update categories, connection access, or metadata visibility, see [View and manage individual audiences](./onboard-audiences.md#view-individual-audiences).

### Edit audience settings {#edit-audience-settings}

You can edit audience metadata directly from the **[!UICONTROL My audiences]** list view without opening the detail view. Select the checkbox for an audience to reveal the action toolbar, then select an action: **[!UICONTROL Edit metadata visibility]**, **[!UICONTROL Edit connection access]**, **[!UICONTROL Edit name and description]**, **[!UICONTROL Edit categories]**, or **[!UICONTROL Delete]**.

![The My audiences list view showing audiences sourced from different systems, with one row selected using a checkbox, revealing a bottom toolbar with edit and delete options.](../../assets/adobe-logo-old.png)

### View your [!DNL Databricks] data connection {#view-databricks-connection}

To review the connection itself, including its match keys, navigate to **[!UICONTROL Setup]** > **[!UICONTROL My data connections]**. Your new [!DNL Databricks] connection is available there. The audience source is displayed as **[!UICONTROL Databricks Delta Share]**.

## Known limitations {#known-limitations}

Be aware of the following constraints when configuring and using Databricks Delta Share audience sourcing:

* **Native sharing only:** The UI supports native Databricks-to-Databricks [!DNL Delta Sharing] only. Bearer-token and OIDC authentication flows are not available in the configuration wizard.
* **No in-wizard table browser:** You must enter table names manually. Collaboration validates table names when you preview tables; it does not list all tables in your share automatically.
* **One-time import:** The configuration wizard does not include a recurring refresh schedule. Plan your data update strategy with your Adobe account team if you need ongoing refreshes from [!DNL Databricks].
* **Metadata table row limit:** When you use a metadata table for audience discovery, Collaboration imports up to 100,000 audience rows from that table. Contact Adobe support if your catalog exceeds this limit.
* **Match key constraints:** Once a match key is enabled for a data connection, it cannot be removed. You can add match keys to an existing connection, but you cannot disable or delete them. To change the active match keys, you must [delete the data connection](./manage-data-connection.md#delete-data-connection) and create a new one.
* **Membership table required:** Even when you use a metadata table for audience discovery, you must specify a membership table. Collaboration reads identity rows from the membership table during ingestion.

## Troubleshooting {#troubleshooting}

Use this section to resolve issues that occur during or after configuration. For errors during share connection, review your provider name, share name, and schema with your [!DNL Databricks] administrator.

**Share connection fails or times out**

* Verify that your [!DNL Delta Share] is published to Adobe's [!DNL Databricks] account and that the provider name, share name, and schema are correct.
* Confirm the schema is visible in the share. Newly published shares may take time to propagate.
* If connection continues to fail after several minutes, discard the in-progress setup and start again, or contact Adobe customer support with the values you entered (excluding sensitive credentials).

**Table preview fails**

* Confirm the table name is spelled correctly and exists in the schema you specified.
* Ensure the table is included in the [!DNL Delta Share] published to Adobe.
* For metadata-driven discovery, preview both the membership table and the metadata table before continuing.

**Field mapping validation blocks progress**

* Confirm your membership table includes a column mappable to **`AUDIENCE_ID`**.
* Ensure at least two identity fields are fully mapped (source and target).
* Use **[!UICONTROL Preview source data]** to verify column names match your enabled match keys.

**Audiences are not appearing or sourcing is taking longer than expected**

* Sourcing time scales with data volume. Extended processing time is expected for large membership tables.
* If audiences have not appeared within 24 hours, check the **[!UICONTROL My data connections]** tab for error indicators on the connection.
* Verify that your membership table structure and field mappings match the requirements in [Prepare your audience data](#prepare-audience-data).
* If the issue persists, contact Adobe customer support and provide the data connection name and table details.

**The data connection shows a failed status after initially succeeding**

* Confirm that the [!DNL Delta Share] and tables have not been removed or renamed in [!DNL Databricks] since you created the connection.
* Verify that Adobe's access to the share has not been revoked.
* If the issue persists, contact Adobe customer support.

## Publish your [!DNL Delta Share] to Adobe {#publish-delta-share}

[!DNL Databricks] Unity Catalog [!DNL Delta Sharing] lets you share tables securely with other [!DNL Databricks] accounts without copying data. To allow Collaboration to read your audience data, your [!DNL Databricks] administrator must publish a [!DNL Delta Share] to Adobe's [!DNL Databricks] consumer account.

### Before you publish {#before-you-publish}

Work with your Adobe account representative or onboarding contact to obtain:

* Confirmation that Adobe is ready to receive your share in your region.
* The provider name Adobe uses in its Unity Catalog metastore to identify your organization as a share provider.

Prepare the following in your [!DNL Databricks] workspace:

* A [!DNL Delta Share] containing the schema and tables Collaboration will read.
* A membership table with one row per profile-audience pair and columns for **`AUDIENCE_ID`** and match keys.
* An optional metadata table if you plan to use metadata-driven audience discovery.

### Publish the share {#publish}

Follow your organization's [!DNL Databricks Delta Sharing] procedures to grant Adobe's consumer account access to the share. Exact steps depend on your [!DNL Databricks] deployment and governance model. In general:

1. In Unity Catalog, create or identify the share that contains your audience schema and tables.
2. Add the schema (or individual tables) to the share.
3. Grant the share to Adobe's [!DNL Databricks] consumer account using native Databricks-to-Databricks sharing.
4. Confirm with your Adobe contact that the share is visible on the consumer side and note the provider name and share name for the Collaboration configuration wizard.
5. For [!DNL Databricks] product documentation on [!DNL Delta Sharing], see the [Databricks Delta Sharing documentation](https://docs.databricks.com/aws/en/delta-sharing).

### Collect [!DNL Databricks] details for Collaboration {#collect-databricks-details}

Gather the details below before starting the Collaboration configuration wizard.

| Field | Description | Example |
| ------| ----------- | ------- |
| Provider name  | Provider identifier in Adobe's Unity Catalog metastore (from Adobe onboarding) | `your_org_provider`       |
| Share name    | Name of the published [!DNL Delta Share]   | `audience_share_prod`     |
| Schema | Schema  | `collaboration_audiences` |
| Membership table  | Table with profile-audience membership rows  | `audience_members`        |
| Metadata table (optional) | Table listing audiences (one row per audience) | `audience_catalog` |

{style="table-layout:auto"}

## Next steps {#next-steps}

You have configured [!DNL Databricks Delta Share] as a data source in Collaboration. After sourcing completes, your audiences are available in the **[!UICONTROL My audiences]** workspace and ready for use in collaboration projects.

From here, you can:

* [Create and manage collaboration projects](../collaborate/manage-projects.md)
* [Activate audiences within a project](../collaborate/activate.md)
* [Review overlaps and measure performance](../collaborate/measure.md)
* [Manage audience settings and visibility](./onboard-audiences.md#view-individual-audiences)
* View your [!DNL Databricks] data connection in **[!UICONTROL My data connections]**

For other audience sourcing methods, see:

* [Configure [!DNL Google Cloud Storage] for audience sourcing](./configure-gcs-audience-sourcing.md)
* [Configure [!DNL Amazon S3] for audience sourcing](./configure-aws-s3-audience-sourcing.md)
* [Configure [!DNL Snowflake] for audience sourcing](./configure-snowflake-audience-sourcing.md)
* [Source audiences from Experience Platform](./onboard-audiences.md)
* [Upload a CSV file for audience sourcing](./upload-csv-audience-sourcing.md)
