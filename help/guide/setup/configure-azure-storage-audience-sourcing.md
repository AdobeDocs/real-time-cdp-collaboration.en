---
title: Source audiences from Azure storage in Real-Time CDP Collaboration
description: Connect Azure Blob Storage or Azure Data Lake Storage Gen2 to Real-Time CDP Collaboration and source first-party audiences on a recurring schedule.
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
---
# Configure Azure storage for audience sourcing

Follow the steps in this guide to connect **Azure Blob Storage** or **Azure Data Lake Storage Gen2** to Adobe Real-Time CDP Collaboration and begin sourcing first-party audience data through the UI.

Connect Azure storage to Collaboration to ingest first-party audience data directly without engineering support. Once connected, Collaboration sources audiences from your container or data lake path on a recurring schedule and makes them available for activation and overlap analysis within your collaboration projects. Sourcing your audiences is a required step before you can activate them or use them in overlap analysis with collaborators.

This guide covers the end-to-end configuration workflow: choosing the right Azure source type, preparing prerequisites, granting Adobe access in Azure, completing the configuration wizard, reviewing auto-mapped identity fields, scheduling data refresh, and confirming that sourcing completed successfully.

Audiences sourced from Azure follow the same governance and data handling rules as audiences sourced from Adobe Experience Platform.

Other available sourcing methods include Experience Platform, Amazon S3, Google Cloud Storage, Snowflake, and CSV file upload.

## Choose your Azure source type

Collaboration supports two Azure ingestion options. Use the table below to pick the guide path that matches where your audience files live.

| | **Azure Blob Storage** | **Azure Data Lake Storage Gen2** |
|---|------------------------|----------------------------------|
| **Use when** | Files are in a standard Blob **container** on a storage account (no hierarchical namespace required). | Files are in a **filesystem** on a storage account with **hierarchical namespace** enabled. |
| **Wizard label** | **Azure Blob Storage** | **Azure Data Lake Storage Gen2** |
| **Key fields** | Storage account, **Container**, **Path** | Storage account, **Filesystem**, **Path** |
| **Permissions section** | [Azure Blob permissions](#set-up-azure-blob-storage-permissions) | [ADLS Gen2 permissions](#set-up-adls-gen2-permissions) |

You configure **one source type per data connection**. To source from both Blob and ADLS, create separate data connections.

## Prerequisites

Complete all items in this section before starting the configuration workflow. Incomplete prerequisites are the most common reason setup fails or audiences do not appear after sourcing. Before following this guide, you must have completed [account onboarding and setup](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-account).

Some steps require action by an **Azure administrator**. If you are not the Azure administrator for your organization, identify the appropriate person before starting.

### Azure access and permissions

Before proceeding, confirm the following with your Azure administrator:

- Adobe has been granted read access to the **container** (Blob) or **filesystem** (ADLS Gen2) where audience files are stored. See [Set up Azure permissions](#set-up-azure-permissions).
- Azure audience sourcing is available in your region (NA, EMEA, ANZ). If Azure sourcing is not yet available in your region, contact your Adobe account representative.

### Prepare your audience data

Your audience files must conform to the **[Audience Sourcing Specification (v1.2)](https://cdn.experienceleague.adobe.com/assets/Adobe-Enterprise-Docs/real-time-cdp-collaboration.en/main/help/assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)** before sourcing begins.

Key requirements include:

- **File format:** CSV, using commas as field delimiters and pipes (`|`) as separators for multiple values within a single field.
- **Required fields:** Every record must include an `AUDIENCE_ID` column and at least one supported match key column.
- **Supported match keys:** `HASHED_EMAIL_SHA_256`, `HASHED_PHONE_SHA_256`, `HASHED_IPV4_SHA_256`, `CRM_ID`, `LOYALTY_ID`, `ADFIXUS_ID`.
- **Hashing requirements:** All match key values must be trimmed, lowercased, and SHA256-hashed before upload. Collaboration does not hash or normalize data before ingestion.
- **Column consistency:** All files under your configured path must use identical column structures.

All match keys present in your audience files must also be enabled for your Collaboration account. See [Set up match keys](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-account#set-up-match-keys).

### Values required before you begin

Have the following values ready before starting the configuration wizard.

| Value | Blob Storage | ADLS Gen2 |
|-------|--------------|-----------|
| **Storage account** | Azure Storage account name | ADLS Gen2-enabled storage account name |
| **Container / filesystem** | Blob **container** name | ADLS **filesystem** name (shown as a container in Azure Portal) |
| **Path** | Prefix within the container (e.g. `sourcing/audiences/path1/`). Use a trailing `/` to include all files under the prefix. | Directory prefix within the filesystem (e.g. `sourcing/inbound/`) |

## Configure your Azure connection

The configuration workflow is a multi-step wizard inside the **Setup** workspace. Complete each step in sequence. You can return to any step using the pencil icon on the final review screen before you create the connection.

### Add a new data connection

From the **My audiences** tab within the **Setup** workspace, select the add icon and then select **Audience**.

If this is your first audience, you may also select the **Add** option.

The **Add audience** workflow appears. Select **Add a new data connection** and then select **Next**.

### Select your Azure data source

The data source selection screen lists all available connection types. Select **Azure Blob Storage** or **Azure Data Lake Storage Gen2**, then select **Next**.

A prerequisite dialog outlines required steps (storage setup, Adobe access, Audience Sourcing Specification compliance). Select **Start onboarding** to confirm compliance before proceeding.

> **Product note:** Azure onboarding may show a **pending** state while external access configuration is verified. Complete the [permission steps](#set-up-azure-permissions) for your source type and wait until the connection is active before continuing field mapping.

### Enter your Azure connection details

Provide the details required for Collaboration to access your data. After entering the required information, select **Next**.

| Field | Description |
|-------|-------------|
| **Storage account** | The Azure Storage account that hosts your audience files. |
| **Container** (Blob) or **Filesystem** (ADLS Gen2) | The Blob container or ADLS filesystem where files are stored. |
| **Path** | The path prefix within the container or filesystem where audience files are stored. |

Collaboration validates **container** (or filesystem), **path**, and **authentication type** (`authType`). Access is established through Azure RBAC for Adobe's service principal or managed identity; you do not enter storage account keys in the wizard.

### Confirm consent and data use acknowledgment

You must confirm that consent opt-outs have been removed from the audience data before Collaboration can process it. If you are unsure whether your data meets this requirement, review the governance policy and enforcement actions guide before proceeding. Select the confirmation checkbox and then select **OK** to proceed.

### Provide connection details

Enter a name and an optional description for this data connection. The name appears in **My data connections** and helps distinguish this source if you manage multiple connections.

- **Data connection name** (required)
- **Data connection description** (optional)

Select **Next** to continue.

### Review auto-mapped identity fields

The **Mapping** screen is read-only. Collaboration automatically maps source identity fields from your audience files to target fields based on the column names defined in the Audience Sourcing Specification. You cannot add, remove, or apply transformations to mapped fields at this stage.

**TIP:** Select **Preview source data** to review a sample of your audience data in tabular format, then select **Close** to return to the mapping screen.

Confirm that the displayed mappings reflect the fields in your audience files. If they do not, stop and correct your files before proceeding. Select **Next** to continue.

### Schedule data refresh

In the **Schedule** view, set how often Collaboration retrieves updated audience data and define the active date range for sourcing.

Use the **Frequency** dropdown (from **Daily** to **Every 6 days**). Set **Start date** and **End date** for the active sourcing period. When the end date is reached, sourcing ceases and previously sourced audiences expire.

**IMPORTANT:** Set the refresh frequency to match or not exceed how often your underlying data is updated. The minimum supported refresh interval is once every six days.

Select **Next** to continue.

### Review and complete the connection

Review the configuration summary:

- **Data connection:** Storage account, container or filesystem, and path
- **Details:** Name and description
- **Mapping:** Auto-mapped identity fields
- **Schedule:** Refresh frequency and date range

Select the pencil icon next to any section to edit it. When all sections are correct, select **Complete**.

A confirmation dialog indicates that the data connection was created and audience sourcing is in progress.

## Review sourced audiences

After you complete the wizard, Collaboration sources audiences asynchronously. Navigate to **Setup** > **My audiences** to monitor progress.

### Monitor audience sourcing progress

While ingestion runs, a banner indicates **Audience sourcing in progress**. Individual audiences appear in the list as sourcing completes for each one.

**TIP:** Sourcing time varies with data volume and refresh frequency.

### View sourced audience details

Completed audiences appear in **My audiences** with other connections. Select **View audience** for status, source, identities, categories, connection access, and metadata visibility.

### View your Azure data connection

Under **Setup** > **My data connections**, your connection is listed with **Azure Blob Storage** or **Azure Data Lake Storage Gen2** as the source.

## Known limitations

- **Match key constraints:** Once enabled for a connection, match keys cannot be removed. Add match keys to an existing connection, but to change the active set you must delete the connection and create a new one.
- **One active connection per Azure source type:** Typically one active Blob connection and one active ADLS Gen2 connection at a time per account. To change storage location, delete the existing connection and create a new one.
- **Subfolder support:** Files must be at the configured path prefix; Collaboration does not traverse arbitrary subfolders beyond that prefix.
- **Separate source types:** Blob and ADLS Gen2 are distinct connections—do not mix configuration between them in a single wizard run.

## Troubleshooting

**Audiences are not appearing or sourcing is slow**

- Confirm files exist at the configured path and comply with the Audience Sourcing Specification.
- Check **My data connections** for errors.
- Contact Adobe support with connection name, storage account, and container/filesystem details if issues persist after 24 hours.

**Connection failed after initial success**

- Verify Azure RBAC for Adobe's principal was not removed or narrowed.
- Confirm files still exist at the path and match the specification.

**Refresh / format errors**

- Ensure new files keep the same column structure and hashing rules as the initial ingest.

## Set up Azure permissions

Grant Adobe read access using **Azure RBAC**. The same Adobe principal is typically used for both Blob and ADLS Gen2; confirm identifiers with your Adobe account team.

### Collect Adobe's Azure principal information

| Region | Adobe principal (TBD — confirm with Adobe) |
|--------|---------------------------------------------|
| North America | _Contact your Adobe account team_ |
| EMEA | _Contact your Adobe account team_ |
| Australia | _Contact your Adobe account team_ |

### Set up Azure Blob Storage permissions

**IMPORTANT:** You need permission to assign roles on the storage account or container (for example **Owner** or **User Access Administrator**, or equivalent).

1. In the [Azure portal](https://portal.azure.com/), open **Storage account** > **Containers** > your **container**.
2. **Access control (IAM)** > **Add role assignment**.
3. Assign Adobe's principal:

    | Role | Purpose |
    |------|---------|
    | **Storage Blob Data Reader** | Read and list blobs in the container. |

4. Select **Save**.

    | Field | Example |
    |-------|---------|
    | Storage account | `customerdatastore` |
    | Container | `audience-ingest` |
    | Path | `sourcing/audiences/path1/` |

### Set up ADLS Gen2 permissions

**Requirements:**

- Storage account has **hierarchical namespace** enabled (Data Lake Storage Gen2).
- Firewall / private endpoint rules allow Adobe access per your Adobe network guidance.

**Role assignment:**

1. Open **Storage account** > **Containers** > your **filesystem**.
2. **Access control (IAM)** > **Add role assignment** > **Storage Blob Data Reader** for Adobe's principal at filesystem or directory scope.
3. Select **Save**.

| Field | Example |
|-------|---------|
| Storage account | `datalake-prod` |
| Filesystem | `audiences` |
| Path | `sourcing/inbound/` |

After permissions are in place, complete the [configuration workflow](#configure-your-azure-connection).


## Next steps

After sourcing completes, audiences are available in **My audiences** for collaboration projects (activate, overlap, measurement).

For other audience sourcing methods, see:

- [Configure Google Cloud Storage for audience sourcing](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/source-audiences/configure-gcs-audience-sourcing)
- [Configure Snowflake for audience sourcing](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/source-audiences/configure-snowflake-audience-sourcing)
- [Configure AWS S3 for audience sourcing](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/source-audiences/configure-aws-s3-audience-sourcing)
- [Source audiences from Experience Platform](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/source-audiences/onboard-audiences)
- [Upload a CSV file for audience sourcing](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/source-audiences/upload-csv-audience-sourcing)
