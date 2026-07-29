---
title: Destination connection requirements
description: Review the credentials, permissions, and connection information required to configure supported destinations in Real-Time CDP Collaboration.
audience: admin, publisher
---
# Destination connection requirements

Before configuring a destination in Real-Time CDP Collaboration, obtain the credentials, permissions, and connection information required by the destination provider.

This page summarizes the information required when completing the destination configuration workflow in Collaboration. For instructions on creating credentials, assigning provider permissions, configuring network access, or preparing the destination system, see the linked Adobe Experience Platform destination documentation.

>[!NOTE]
>
>The fields and authentication methods available in Real-Time CDP Collaboration vary by destination. The linked Adobe Experience Platform documentation provides the authoritative connector requirements, but some parts of the standard Experience Platform workflow might not apply in Collaboration.

## Requirements at a glance {#requirements-at-a-glance}

Use the following table to identify the information that you need before configuring a destination.

| Destination | Connection method | Prepare before starting | Detailed requirements |
|---|---|---|---|
| Amazon S3 | Access key and secret key, or assumed role | AWS access key pair or IAM role ARN, bucket name, and folder path | [Amazon S3 destination documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3) |
| SFTP | Password or SSH key | Server domain, port, username, authentication credential, and folder path | [SFTP destination documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp) |
| Azure Blob Storage | Connection string | Azure storage connection string, container name, and folder path | [Azure Blob Storage destination documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob) |
| Google Cloud Storage | Access key ID and secret access key | Google Cloud Storage interoperability credentials, bucket name, and folder path | [Google Cloud Storage destination documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage) |
| Snowflake Batch | Snowflake data sharing | Snowflake account ID, region, Private Link status, and access to private listings | [Snowflake Batch destination documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch) |

>[!IMPORTANT]
>
>Use credentials that comply with your organization's security policies and have only the permissions required to connect to and export data to the destination.

## Account information {#account-information}

For Amazon S3, SFTP, Azure Blob Storage, and Google Cloud Storage, you can configure the destination under an existing account or create an account.

When creating an account, provide:

* **[!UICONTROL Account Name]**: A required name that helps users identify the account in Collaboration.
* **[!UICONTROL Account Description]**: An optional description of the account.

New accounts require authentication. When an existing account is available, select it instead of entering the authentication credentials again.

Snowflake Batch does not display a separate authentication step in the current Collaboration workflow. Its connection information is entered during the **[!UICONTROL Create destination]** step.

## Amazon S3 {#amazon-s3}

Amazon S3 supports access-key authentication and assumed-role authentication.

### Authentication requirements {#amazon-s3-authentication}

| Authentication method | Required Collaboration fields | Information to provide |
|---|---|---|
| **[!UICONTROL Access Key]** | **[!UICONTROL s3AccessKey]**, **[!UICONTROL s3SecretKey]** | An Amazon S3 access key and corresponding secret access key |
| **[!UICONTROL Assumed Role]** | **[!UICONTROL Role]** | The Amazon Resource Name (ARN) of the AWS IAM role that Adobe can assume |

For access-key authentication, create an AWS IAM access key pair with permission to access the destination bucket and folder.

For assumed-role authentication, an administrator must create an AWS IAM role that Adobe can assume. The role must have permission to list the bucket and read, write, and delete objects in the destination folder.

For instructions on creating an access key or assumed role, configuring the trust relationship, and granting the required Amazon S3 permissions, see:

* [Authenticate to the Amazon S3 destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#authenticate)
* [Required Amazon S3 permissions](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#required-s3-permission)

<!-- TODO: Confirm whether the absence of the optional encryption-key field available in the standard Experience Platform workflow is intentional and should be documented as a Collaboration limitation. -->

### Destination information {#amazon-s3-destination-information}

The following fields are confirmed in the Collaboration **[!UICONTROL Create destination]** step.

| Field | Requirement | Description |
|---|---|---|
| **[!UICONTROL Destination Name]** | Required | A name that identifies the destination in Collaboration. |
| **[!UICONTROL Destination description]** | Optional | A description that helps users identify the purpose of the destination. |
| **[!UICONTROL Bucket name]** | Required | The name of the Amazon S3 bucket that receives the exported files. |
| **[!UICONTROL Folder path]** | Required | The path to the folder in the bucket that receives the exported files. |
| **[!UICONTROL File Type]** | Required | The file format used for exported audience data. |
| **[!UICONTROL Compression format]** | Required | The compression format applied to exported files. |
| **[!UICONTROL Include Hierarchical Output]** | Optional | Includes hierarchical values, such as arrays, maps, and objects, in supported output formats. |
| **[!UICONTROL Include manifest file]** | Optional | Includes a JSON manifest containing information about the exported files and their location. |

For additional information about these fields, see [Amazon S3 destination details](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#destination-details).

## SFTP {#sftp}

SFTP supports password authentication and SSH-key authentication.

### Authentication requirements {#sftp-authentication}

| Authentication method | Required Collaboration fields | Information to provide |
|---|---|---|
| **[!UICONTROL SFTP with Password]** | **[!UICONTROL domain]**, **[!UICONTROL port]**, **[!UICONTROL username]**, **[!UICONTROL password]** | The SFTP server address, connection port, username, and password |
| **[!UICONTROL SFTP with SSH Key]** | **[!UICONTROL domain]**, **[!UICONTROL port]**, **[!UICONTROL username]**, **[!UICONTROL sshKey]** | The SFTP server address, connection port, username, and private SSH key |

The **[!UICONTROL port]** field defaults to port `22`.

For SSH-key authentication, the private key must be:

* RSA-formatted.
* Base64-encoded.
* Not protected by a password.

Before configuring the destination, ensure that:

* The credentials have permission to write to the destination folder.
* The SFTP server permits connections from Adobe.
* Adobe IP addresses are added to the server allowlist when required.
* The server supports enough concurrent connections for the expected number of audience exports.

For complete authentication, server, and network requirements, see:

* [SFTP authentication information](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp#authentication-information)
* [SFTP server connection requirements](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp#sftp-connection-requirements)
* [IP address allowlist requirements](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp#ip-address-allow-list)

<!-- TODO: Confirm whether the absence of the optional encryption-key field available in the standard Experience Platform workflow is intentional and should be documented as a Collaboration limitation. -->

### Destination information {#sftp-destination-information}

The standard Experience Platform SFTP connector uses the following destination fields.

<!-- TODO: Validate the exact fields, required-field indicators, and output controls in the Collaboration Create destination step. -->

| Field | Expected requirement | Description |
|---|---|---|
| **[!UICONTROL Destination Name]** | Required | A name that identifies the destination in Collaboration. |
| **[!UICONTROL Destination description]** | Optional | A description that helps users identify the purpose of the destination. |
| **[!UICONTROL Folder path]** | Required | The path to the folder on the SFTP server that receives the exported files. |
| **[!UICONTROL File Type]** | Required | The file format used for exported audience data. |
| **[!UICONTROL Compression format]** | Required | The compression format applied to exported files. |
| **[!UICONTROL Include manifest file]** | Optional | Includes a JSON manifest containing information about the exported files and their location. |

<!-- TODO: Confirm whether Include Hierarchical Output is available for SFTP in Collaboration. -->

For additional information, see [SFTP destination details](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp#destination-details).

## Azure Blob Storage {#azure-blob-storage}

Azure Blob Storage uses a connection string to authenticate the destination account.

### Authentication requirements {#azure-blob-storage-authentication}

| Authentication method | Required Collaboration field | Information to provide |
|---|---|---|
| **[!UICONTROL ConnectionString]** | **[!UICONTROL connectionString]** | The connection string for the Azure storage account |

An Azure Blob Storage connection string typically begins with the following pattern:

`DefaultEndpointsProtocol=https;AccountName={ACCOUNT_NAME};AccountKey={ACCOUNT_KEY}`

The connection string must provide access to the storage account and container that receives the exported audience files.

For instructions on obtaining and configuring the connection string, see [Authenticate to the Azure Blob Storage destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob#authenticate).

<!-- TODO: Confirm whether the absence of the optional encryption-key field available in the standard Experience Platform workflow is intentional and should be documented as a Collaboration limitation. -->

### Destination information {#azure-blob-storage-destination-information}

The standard Experience Platform Azure Blob Storage connector uses the following destination fields.

<!-- TODO: Validate the exact fields, required-field indicators, and output controls in the Collaboration Create destination step. -->

| Field | Expected requirement | Description |
|---|---|---|
| **[!UICONTROL Destination Name]** | Required | A name that identifies the destination in Collaboration. |
| **[!UICONTROL Destination description]** | Optional | A description that helps users identify the purpose of the destination. |
| **[!UICONTROL Container]** | Required | The Azure Blob Storage container that receives the exported files. |
| **[!UICONTROL Folder path]** | Required | The path to the folder in the container that receives the exported files. |
| **[!UICONTROL File Type]** | Required | The file format used for exported audience data. |
| **[!UICONTROL Compression format]** | Required | The compression format applied to exported files. |
| **[!UICONTROL Include manifest file]** | Optional | Includes a JSON manifest containing information about the exported files and their location. |

<!-- TODO: Confirm whether Include Hierarchical Output is available for Azure Blob Storage in Collaboration. -->

For additional information, see [Azure Blob Storage destination details](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob#destination-details).

### Private Link connections {#azure-private-link}

Adobe Experience Platform supports routing Azure destination exports through Azure Private Link for organizations with strict network-security requirements.

<!-- TODO: Confirm that Azure Private Link is supported for Azure Blob Storage destinations configured through Collaboration before publishing this section. -->

Private Link requires separate preparation and is not configured through the connection-string field. For prerequisites, guardrails, and setup instructions, see [Private Link for Azure destinations](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-private-link).

## Google Cloud Storage {#google-cloud-storage}

Google Cloud Storage uses an access key ID and secret access key generated through Google Cloud Storage interoperability settings.

### Authentication requirements {#google-cloud-storage-authentication}

| Authentication method | Required Collaboration fields | Information to provide |
|---|---|---|
| **[!UICONTROL Google Cloud Storage authentication credentials]** | **[!UICONTROL accessKeyId]**, **[!UICONTROL secretAccessKey]** | A Google Cloud Storage access key ID and corresponding secret access key |

Before configuring the destination:

1. Enable interoperability for the Google Cloud Storage account.
2. Generate an access key ID and secret access key for a service account.
3. Grant the service account permission to create and list objects in the destination bucket.

For complete credential-generation and permission requirements, see:

* [Google Cloud Storage prerequisite setup](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage#prerequisites)
* [Authenticate to the Google Cloud Storage destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage#authenticate)
* [Required Google Cloud Storage permissions](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage#required-google-cloud-storage-permission)

<!-- TODO: Confirm whether the absence of the optional encryption-key field available in the standard Experience Platform workflow is intentional and should be documented as a Collaboration limitation. -->

### Destination information {#google-cloud-storage-destination-information}

The standard Experience Platform Google Cloud Storage connector uses the following destination fields.

<!-- TODO: Validate the exact fields, required-field indicators, and output controls in the Collaboration Create destination step. -->

| Field | Expected requirement | Description |
|---|---|---|
| **[!UICONTROL Destination Name]** | Required | A name that identifies the destination in Collaboration. |
| **[!UICONTROL Destination description]** | Optional | A description that helps users identify the purpose of the destination. |
| **[!UICONTROL Bucket name]** | Required | The Google Cloud Storage bucket that receives the exported files. |
| **[!UICONTROL Folder path]** | Required | The path to the folder in the bucket that receives the exported files. |
| **[!UICONTROL File Type]** | Required | The file format used for exported audience data. |
| **[!UICONTROL Compression format]** | Required | The compression format applied to exported files. |
| **[!UICONTROL Include manifest file]** | Optional | Includes a JSON manifest containing information about the exported files and their location. |

<!-- TODO: Confirm whether Include Hierarchical Output is available for Google Cloud Storage in Collaboration. -->

For additional information, see [Google Cloud Storage destination details](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage#destination-details).

## Snowflake Batch {#snowflake-batch}

Snowflake Batch uses Snowflake data sharing rather than delivering files to a customer-managed cloud storage location. Adobe grants the configured Snowflake account read-only access to audience data hosted in Adobe's Snowflake environment.

Snowflake Batch does not require a storage access key, password, or connection string.

### Prerequisites {#snowflake-batch-prerequisites}

Before configuring Snowflake Batch, ensure that:

* You have access to a Snowflake account.
* The Snowflake account is subscribed to private listings.
* You know the Snowflake account identifier.
* You know the cloud region where the Snowflake account is provisioned.
* You know whether the account enforces Private Link-only access.
* Someone with the required Snowflake permissions can accept the private listing from Adobe.

For complete account-preparation requirements, see [Snowflake Batch prerequisites](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch#prerequisites).

### Connection information {#snowflake-batch-connection-requirements}

The following fields are confirmed in the Collaboration **[!UICONTROL Create destination]** step.

| Field | Requirement | Description |
|---|---|---|
| **[!UICONTROL Destination Name]** | Required | A name that identifies the destination in Collaboration. |
| **[!UICONTROL Destination description]** | Optional | A description that helps users identify the purpose of the destination. |
| **[!UICONTROL Snowflake Account ID]** | Required | The Snowflake data-sharing account identifier. |
| **[!UICONTROL Private Link Enabled]** | Required | Indicates whether the Snowflake account enforces Private Link-only access. |
| **[!UICONTROL Snowflake Region]** | Required | The cloud region where the Snowflake account is provisioned. |
| Account acknowledgment | Required | Confirms that the entered Snowflake account ID is correct and belongs to the user or their organization. |

Enter the Snowflake account ID in one of the following formats:

* For an account associated with a Snowflake organization: `OrganizationName.AccountName`
* For an account not associated with an organization: `AccountName`

For **[!UICONTROL Private Link Enabled]**, select **[!UICONTROL Yes]** only when the Snowflake account enforces Private Link-only access. Select **[!UICONTROL No]** when the account permits access through public Snowflake service endpoints.

<!-- TODO: Confirm whether the account-acknowledgment control is a dropdown, text field, or another control in the final Collaboration UI. -->

<!-- TODO: Confirm whether the Snowflake Account ID and Snowflake Region cannot be edited after destination creation in Collaboration. -->

<!-- TODO: Confirm whether the regions available in the Collaboration dropdown exactly match the supported regions documented for the standard Experience Platform connector. -->

For field definitions and Snowflake data-sharing requirements, see [Snowflake Batch destination details](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch#destination-details).

## Next steps {#next-steps}

After you obtain the required connection information, [configure and manage a destination](./manage-destinations.md).

<!-- TODO: If Snowflake Batch remains in scope for manage-destinations.md, consider renaming that page and its TOC entry from "cloud storage destinations" to a broader term such as "supported destinations." -->