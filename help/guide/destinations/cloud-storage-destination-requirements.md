---
title: Destination connection requirements
description: Review the connection information required to configure supported destinations in Real-Time CDP Collaboration.
audience: admin, publisher
---
# Destination connection requirements

Before configuring a destination in Real-Time CDP Collaboration, obtain the credentials and connection information required by the destination provider.

This page summarizes the authentication methods available in Collaboration. For instructions on creating credentials, assigning permissions, configuring network access, or preparing the destination system, refer to the linked Adobe Experience Platform destination documentation.

>[!NOTE]
>
>The linked Adobe Experience Platform documentation describes the standard destination workflow. Some steps, fields, or options might not apply when configuring the destination in Real-Time CDP Collaboration.

## Requirements at a glance {#requirements-at-a-glance}

| Destination | Authentication or connection method | Prepare before starting | Detailed requirements |
|---|---|---|---|
| [!DNL Amazon S3] | Access key and secret key, or assumed role | AWS access key pair or IAM role ARN; bucket and folder information | [[!DNL Amazon S3] destination documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3) |
| SFTP | Password or SSH key | Server domain, port, username, authentication credential, and folder path | [SFTP destination documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp) |
| [!DNL Azure Blob Storage] | Connection string | Azure storage connection string, container, and folder information | [[!DNL Azure Blob Storage] destination documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob) |
| [!DNL Google Cloud Storage] | Access key ID and secret access key | [!DNL Google Cloud Storage] interoperability credentials, bucket, and folder information | [[!DNL Google Cloud Storage] destination documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage) |
| [!DNL Snowflake Batch] | [!DNL Snowflake] data sharing | [!DNL Snowflake] account ID, region, Private Link status, and access to private listings | [[!DNL Snowflake Batch] destination documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch) |
| [!DNL Data Landing Zone] | No separate authentication required | Destination folder path and file output preferences | [[!DNL Data Landing Zone] destination documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone) |

## Connector notes {#connector-notes}

Review the following connector-specific authentication methods and workflow differences before configuring a destination.

### [!DNL Amazon S3] {#amazon-s3}

Collaboration supports **[!UICONTROL Access Key]** and **[!UICONTROL Assumed Role]** authentication. Access-key authentication requires an access key and secret access key. Assumed-role authentication requires the ARN of an AWS IAM role that Adobe can assume.

For credential, role, and permission setup, see [Authenticate to the [!DNL Amazon S3] destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#authenticate).

### SFTP {#sftp}

Collaboration supports **[!UICONTROL SFTP with Password]** and **[!UICONTROL SFTP with SSH Key]** authentication. Both methods require the server domain, port, and username. The port defaults to `22`.

For SSH-key format, server, network, and allowlist requirements, see [SFTP authentication information](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp#authentication-information).

### [!DNL Azure Blob Storage] {#azure-blob-storage}

Collaboration authenticates to [!DNL Azure Blob Storage] by using a storage-account connection string.

For instructions on obtaining the connection string and assigning storage permissions, see [Authenticate to the [!DNL Azure Blob Storage] destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob#authenticate).

### [!DNL Google Cloud Storage] {#google-cloud-storage}

Collaboration requires a [!DNL Google Cloud Storage] access key ID and secret access key generated through [!DNL Google Cloud Storage] interoperability settings.

For credential-generation and bucket-permission requirements, see [Authenticate to the [!DNL Google Cloud Storage] destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage#authenticate).

### [!DNL Snowflake Batch] {#snowflake-batch}

[!DNL Snowflake Batch] uses [!DNL Snowflake] data sharing instead of exporting files to customer-managed storage. In Collaboration, there is no separate authentication step. Enter the Snowflake account ID, region, Private Link status, and account-ownership confirmation during destination creation.

For account preparation and private-listing requirements, see [[!DNL Snowflake Batch] destination documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch).

### [!DNL Data Landing Zone] {#data-landing-zone}

[!DNL Data Landing Zone] is provisioned by Adobe and does not require a separate authentication step in Collaboration. During destination creation, specify the destination folder path and file output settings.

For information about accessing an AWS-provisioned [!DNL Data Landing Zone], see [Authenticate to the AWS-provisioned Data Landing Zone](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone#authenticate-dlz-aws).

## Next steps {#next-steps}

After you obtain the required connection information, [configure and manage a destination](./manage-destinations.md).
