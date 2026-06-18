---
title: Source audiences from Azure storage in Real-Time CDP Collaboration
description: Connect Azure Blob Storage or Azure Data Lake Storage Gen2 to Real-Time CDP Collaboration and perform a one-time import of first-party audience data.
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
---
# Configure Azure storage for audience sourcing

Follow the steps in this guide to connect **Azure Blob Storage** or **Azure Data Lake Storage Gen2** to Adobe Real-Time CDP Collaboration and perform a one-time import of first-party audience data.

Connect Azure storage to Collaboration to ingest first-party audience data directly without engineering support. After you create the connection, Collaboration performs a one-time import of audiences from the configured container path and makes them available for activation and overlap analysis within your collaboration projects. Sourcing your audiences is a required step before you can activate them or use them in overlap analysis with collaborators.

This guide covers the end-to-end configuration workflow: choosing the right Azure source type, preparing prerequisites, granting Adobe read access to your storage container, completing the configuration wizard, reviewing auto-mapped identity fields, and confirming that the connection was created successfully.

Audiences sourced from Azure follow the same governance and data handling rules as audiences sourced from Adobe Experience Platform.

Other available sourcing methods include Experience Platform, Amazon S3, Google Cloud Storage, Snowflake, and CSV file upload.

## Choose your Azure source type {#choose-source-type}

Collaboration supports two Azure ingestion options. Use the table below to pick the guide path that matches where your audience files live.

| | **Azure Blob Storage** | **Azure Data Lake Storage Gen2** |
|---|---|---|
| **Use when** | Files are in a standard Blob **container** on a storage account (no hierarchical namespace required). | Files are in a **filesystem** on a storage account with **hierarchical namespace** enabled. |
| **Wizard label** | **Azure Blob Storage** | **Azure Data Lake Storage Gen2** |
| **Key fields** | Storage account, **Container**, **Path** | Storage account, **Container**, **Path** |
| **Permissions section** | [Azure Blob permissions](#set-up-azure-blob-storage-permissions) | [ADLS Gen2 permissions](#set-up-adls-gen2-permissions) |

You configure **one source type per data connection**. To source from both Blob and ADLS, create separate data connections.

## Prerequisites {#prerequisites}

Complete all items in this section before starting the configuration workflow. Incomplete prerequisites are the most common reason setup fails or audiences do not appear after sourcing. Before following this guide, you must have completed [account onboarding and setup](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-account).

Some steps require action by an **Azure administrator**. If you are not the Azure administrator for your organization, identify the appropriate person before starting.

### Azure access and permissions {#azure-access-and-permissions}

This guide follows a two-phase workflow. You must complete both phases in order.

**Phase 1 — Azure preparation:** Before starting the Collaboration configuration wizard, you or your Azure administrator must grant Adobe read access to your storage container. This is covered in [Set up Azure permissions](#set-up-azure-permissions).

**Phase 2 — Collaboration configuration:** After Azure preparation is complete, you complete the connection wizard inside Collaboration. This is covered in [Configure your Azure connection](#configure-your-azure-connection).

Azure audience sourcing must also be available in your region (NA, EMEA, ANZ). If Azure sourcing is not yet available in your region, contact your Adobe account representative.

### Prepare your audience data {#prepare-audience-data}

Your audience files must conform to the **[Audience Sourcing Specification (v1.2)](https://cdn.experienceleague.adobe.com/assets/Adobe-Enterprise-Docs/real-time-cdp-collaboration.en/main/help/assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)** before sourcing begins.

Key requirements include:

- **File format:** CSV, using commas as field delimiters and pipes (`|`) as separators for multiple values within a single field.
- **Required fields:** Every record must include an `AUDIENCE_ID` column and at least one supported match key column.
- **Supported match keys:** `HASHED_EMAIL_SHA_256`, `HASHED_PHONE_SHA_256`, `HASHED_IPV4_SHA_256`, `CRM_ID`, `LOYALTY_ID`, `ADFIXUS_ID`.
- **Hashing requirements:** All match key values must be trimmed, lowercased, and SHA256-hashed before upload. Collaboration does not hash or normalize data before ingestion.
- **Column consistency:** All files under your configured path must use identical column structures.

All match keys present in your audience files must also be enabled for your Collaboration account. See [Set up match keys](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-account#set-up-match-keys).

>[!IMPORTANT]
>
> Match keys enabled for a data connection cannot be removed after the connection is created. To change the active set of match keys, you must delete the connection and create a new one. Confirm your complete match key configuration before starting the wizard.

### Values required before you begin {#values-required}

Have the following values ready before starting the configuration wizard.

| Value | Description |
|---|---|
| **Storage account** | The name of the Azure storage account that hosts your audience files. |
| **Container** | The name of the storage container within that account where your audience files are stored. |
| **Path** | The folder path prefix within the container (for example, `sourcing/audiences/path1/`). Use a trailing `/` to include all files under the prefix. |
| **Tenant ID** | The Microsoft Entra tenant ID associated with your Azure storage account. |

## Set up Azure permissions {#set-up-azure-permissions}

Complete the steps in this section to prepare your Azure environment. Adobe requires read access to your storage container before the Collaboration configuration workflow can establish a connection. This work is performed in the Azure portal and may need to be completed by your Azure administrator.

After you complete this section, proceed to [Configure your Azure connection](#configure-your-azure-connection).

### Obtain Adobe's Azure service principal identifier {#obtain-principal-identifier}

Before you can complete the role assignment steps below, you need the Azure service principal identifier that Adobe uses to access your storage. This identifier is specific to your region and is provided by Adobe.

**Before continuing:** Contact your Adobe account team to request the Azure service principal identifier for your region (North America, EMEA, or Australia). Have this value available before proceeding with the permission steps.

### Set up Azure Blob Storage permissions {#set-up-azure-blob-storage-permissions}

>[!IMPORTANT]
>
> You need permission to assign roles on the storage account or container (for example, **Owner** or **User Access Administrator**, or equivalent).

1. In the [Azure portal](https://portal.azure.com/), open **Storage account** > **Containers** > your **container**.
2. Select **Access control (IAM)**, then select **Add role assignment**.
3. Assign Adobe's principal:

    | Role | Purpose |
    |---|---|
    | **Storage Blob Data Reader** | Read and list blobs in the container. |

4. Select **Save**.

    | Field | Example |
    |---|---|
    | Storage account | `customerdatastore` |
    | Container | `audience-ingest` |
    | Path | `sourcing/audiences/path1/` |

### Set up ADLS Gen2 permissions {#set-up-adls-gen2-permissions}

**Requirements:**

- Storage account has **hierarchical namespace** enabled (Data Lake Storage Gen2).
- Firewall / private endpoint rules allow Adobe access per your Adobe network guidance.

**Role assignment:**

1. Open **Storage account** > **Containers** > your **filesystem**.
2. Select **Access control (IAM)**, then select **Add role assignment** > **Storage Blob Data Reader** for Adobe's principal at filesystem or directory scope.
3. Select **Save**.

| Field | Example |
|---|---|
| Storage account | `datalake-prod` |
| Container | `audiences` |
| Path | `sourcing/inbound/` |

After you complete the permission setup for your source type, proceed to [Configure your Azure connection](#configure-your-azure-connection).

## Configure your Azure connection {#configure-your-azure-connection}

Create a data connection to [!DNL Microsoft Azure] to source audience data into Real-Time CDP Collaboration. The onboarding workflow validates your Azure storage credentials, confirms authorized access through the consent workflow, and automatically maps supported identity fields from your audience files.

This is a one-time import workflow. After the connection is created, Collaboration performs a single import of audience data from the configured container path. No recurring schedule is configured.

### Add a new data connection {#add-new-data-connection}

Navigate to **[!UICONTROL Setup]** > **[!UICONTROL My audiences]**, then select the add icon and choose **[!UICONTROL Audience]**.

The **[!UICONTROL Add audience]** workflow appears. Select **[!UICONTROL Add a new data connection]**, then select **[!UICONTROL Next]**.

![The My audiences view showing the Add audience option used to create a new audience or data connection.](../../assets/my-audiences-add-audience-entry-point.png){zoomable="yes"}

### Select your Azure data source {#select-azure-data-source}

Select **[!UICONTROL Azure Blob Storage]** or **[!UICONTROL Azure Data Lake Storage Gen2]**, then select **[!UICONTROL Next]**.

The connection wizard opens and displays the onboarding steps:

- **[!UICONTROL Credentials]**
- **[!UICONTROL Consent]**
- **[!UICONTROL Field Mapping]**
- **[!UICONTROL Review]**

![The Add audience workflow showing Azure Blob Storage selected as the data connection type and the onboarding steps Credentials, Consent, Field Mapping, and Review.](../../assets/azure-source-selection-step.png){zoomable="yes"}

### Enter connection credentials {#enter-connection-credentials}

In the **[!UICONTROL Credentials]** step, provide the information required to access your Azure storage location.

| Field | Description |
|---|---|
| **[!UICONTROL Storage Account]** | The Azure storage account that contains your audience files. |
| **[!UICONTROL Container]** | The storage container that contains your audience files. |
| **[!UICONTROL Path]** | The folder path within the container where your audience files are stored. |
| **[!UICONTROL Tenant ID]** | The Azure tenant identifier associated with your storage account. |

After you enter the required values, select **[!UICONTROL Connect to Azure]**.

A confirmation message indicates that the connection was established successfully. Select **[!UICONTROL Next]** to continue.

![The Credentials step showing completed Storage Account, Container, Path, and Tenant ID fields with a Connected to Azure confirmation message.](../../assets/azure-credentials-step.png){zoomable="yes"}

### Grant Adobe access to your Azure storage {#grant-adobe-access}

In the **[!UICONTROL Consent]** step, you confirm that Adobe has authorized access to your storage container.

>[!NOTE]
>
> This step uses the Azure RBAC permissions you configured in [Set up Azure permissions](#set-up-azure-permissions). The consent URL initiates an Azure authorization workflow that confirms Adobe has access to the specified container. Both the RBAC setup and this consent step are required to establish the connection.

Select the launch icon next to **[!UICONTROL Consent URL]** to open the Azure authorization workflow.

The page displays the Adobe application that requires access. In Azure, assign the **Storage Blob Data Reader** role to the displayed application on the container that contains your audience files.

After you complete the role assignment, return to Collaboration and select **[!UICONTROL Confirm consent]**.

When the consent validation succeeds, a **[!UICONTROL Consent granted]** confirmation message appears. Select **[!UICONTROL Next]** to continue.

>[!NOTE]
>
> Azure role assignments can take several minutes to propagate. If consent validation does not succeed immediately, wait a few minutes and then try again.

![The Consent step showing a Consent URL, the Azure application identifier, and a Consent granted confirmation message.](../../assets/azure-consent-granted-step.png){zoomable="yes"}

### Review field mappings {#review-field-mappings}

In the **[!UICONTROL Field Mapping]** step, Collaboration automatically maps supported identity fields from your source files.

No manual configuration is required.

Review the displayed mappings and confirm that the source fields match the identity columns in your audience files. Select **[!UICONTROL Next]** to continue.

>[!IMPORTANT]
>
> Collaboration automatically maps identity fields based on the Audience Sourcing Specification. If the displayed mappings are incorrect, update your source files before completing the onboarding workflow.

![The Field Mapping step showing automatically mapped source fields and target identity fields with no manual configuration required.](../../assets/azure-field-mapping-step.png){zoomable="yes"}

### Review and complete the connection {#review-and-complete}

In the **[!UICONTROL Review]** step, verify the connection details and field mappings.

The review page displays:

- Storage account
- Container
- Source path
- Tenant ID
- Field mappings

The review page also indicates that this is a one-time import and that no schedule is configured.

When the configuration is correct, select **[!UICONTROL Complete]**.

![The Review step showing connection details, field mappings, and a message indicating that the audience import is a one-time import with no schedule configured.](../../assets/azure-review-connection-step.png){zoomable="yes"}

## Confirm and review your connection {#confirm-and-review}

After you select **[!UICONTROL Complete]**, Collaboration creates the data connection and navigates you to **[!UICONTROL Setup]** > **[!UICONTROL My data connections]**.

### Confirm the connection was created {#confirm-connection-created}

The connection card in **[!UICONTROL My data connections]** is the first confirmation that the connection was created successfully. The card displays the source type (**[!UICONTROL Azure Blob Storage]** or **[!UICONTROL Azure Data Lake Storage Gen2]**), creation date, match keys, audience count, and current connection status.

![The My data connections view showing a newly created Azure Blob Storage connection card with connection details, match keys, audience count, and status information.](../../assets/azure-data-connection-card.png){zoomable="yes"}

### View sourced audiences {#view-sourced-audiences}

After the connection is created, Collaboration begins sourcing audiences from the configured Azure location. Navigate to **[!UICONTROL Setup]** > **[!UICONTROL My audiences]** to monitor sourcing progress and review sourced audiences.

Sourced audiences appear in the **[!UICONTROL My audiences]** table. For each audience, the table displays information such as:

- Audience name
- Identity count
- Status
- Source
- Data connection
- Connection access
- Creation date
- Last updated date

>[!TIP]
>
> Sourcing time varies with data volume. If audiences have not appeared after 24 hours, see [Troubleshooting](#troubleshooting).

## Known limitations {#known-limitations}

- **Match key constraints:** Match keys cannot be removed from an existing connection. To change the active match keys, delete the connection and create a new one.
- **One active connection per Azure source type:** Typically one active Blob connection and one active ADLS Gen2 connection at a time per account. To change storage location, delete the existing connection and create a new one.
- **Subfolder support:** Files must be at the configured path prefix; Collaboration does not traverse arbitrary subfolders beyond that prefix.
- **Separate source types:** Blob and ADLS Gen2 are distinct connections—do not mix configuration between them in a single wizard run.

## Troubleshooting {#troubleshooting}

### Audiences are not appearing or sourcing is slow {#audiences-not-appearing}

- Confirm files exist at the configured path and comply with the Audience Sourcing Specification.
- Check **[!UICONTROL My data connections]** for errors.
- Contact Adobe support with the connection name, storage account, and container details if issues persist after 24 hours.

### Audiences source but show zero or unexpected identities {#zero-identities}

- Verify that all match key values in your audience files were trimmed, lowercased, and SHA256-hashed before upload. Collaboration does not hash or normalize data on ingestion.
- Confirm that the match keys present in your files are enabled for your Collaboration account. See [Set up match keys](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-account#set-up-match-keys).

### Connection failed after initial success {#connection-failed}

- Verify that the Azure RBAC role assignment for Adobe's principal was not removed or narrowed.
- Confirm files still exist at the path and match the specification.

### Refresh or format errors {#format-errors}

- Ensure new files keep the same column structure and hashing rules as the initial ingest.

## Next steps {#next-steps}

After sourcing completes, audiences are available in **[!UICONTROL My audiences]** for collaboration projects (activate, overlap, measurement).

For other audience sourcing methods, see:

- [Configure Google Cloud Storage for audience sourcing](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/source-audiences/configure-gcs-audience-sourcing)
- [Configure Snowflake for audience sourcing](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/source-audiences/configure-snowflake-audience-sourcing)
- [Configure AWS S3 for audience sourcing](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/source-audiences/configure-aws-s3-audience-sourcing)
- [Source audiences from Experience Platform](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/source-audiences/onboard-audiences)
- [Upload a CSV file for audience sourcing](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/source-audiences/upload-csv-audience-sourcing)
