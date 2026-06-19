---
title: Sources overview
description: Learn about source connectors in Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
---
# Sources overview

In Adobe Real-Time CDP Collaboration, a source (or data connection) is where your audience data comes from. You can connect to various source types such as Adobe applications, cloud-based storages, or files from your local system, to [source and manage audiences](./onboard-audiences.md) for your Collaboration projects. During the audience sourcing workflow, you can choose and set up your preferred source based on your organization's needs.

## Connect a source {#connect-a-source}

To connect a source, you need to enter the sourcing workflow. First, navigate to the **[!UICONTROL My audiences]** tab within the **[!UICONTROL Setup]** workspace.

Select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Audience]** to start the sourcing workflow.

![My audiences workspace with the Add option and Audiences option highlighted.](/help/assets/setup/add-manage-audiences/add-audiences.png)

During the workflow, you will be prompted to add a new data connection by selecting a source. The source you choose determines how your audience data is brought into Collaboration. See the [available sources](#available-sources) table for a list of all supported sources.

![The Add audiences workspace with the Add a new data connection option highlighted.](/help/assets/setup/add-manage-audiences/add-data-connection.png)

After selecting a source, the workflow guides you through the connection-specific setup steps, including authentication, field mapping, scheduling, and audience selection.

### Available sources {#available-sources}

The following sources are available in Collaboration. To view the step-by-step sourcing guide for that source, select the source name in the table below. If you are interested in a source that is not currently available, please contact your Adobe representative.

| Source | Description | Availability |
| --- | --- | --- |
| [Adobe Experience Platform](./onboard-audiences.md) | Bring in audiences from your connected Experience Platform instance and reuse existing customer segments. | Available |
| [Amazon S3](./configure-aws-s3-audience-sourcing.md) | Connect your S3 buckets to source large first-party datasets from your cloud infrastructure. | Available |
| [[!DNL Snowflake]](./configure-snowflake-audience-sourcing.md) | Connect your [!DNL Snowflake Secure Data Share] to bring in large-scale audience datasets. | Available |
| [[!DNL Google Cloud Storage]](./configure-gcs-audience-sourcing.md) | Connect your GCS buckets to bring in audience data stored in your [!DNL Google Cloud] environment. | Available |
| [CSV file upload](./upload-csv-audience-sourcing.md) | Upload a formatted CSV file directly from your local system. | Available |
| Adobe Audience Manager | Bring existing Audience Manager segments into your Collaboration projects. | *Coming soon* |
| [[!DNL Azure Blob Storage]](./configure-azure-storage-audience-sourcing.md) | Connect your [!DNL Azure Blob Storage] containers to source first-party datasets from your [!DNL Microsoft Azure] environment. | Available |
| [[!DNL Azure Data Lake Storage]](./configure-azure-storage-audience-sourcing.md) | Connect your [!DNL Azure Data Lake Storage Gen 2] account to bring in audience data stored in your [!DNL Azure] data lake. | Available |

{style="table-layout:auto"}

## Next steps

After you connect a source and bring in your audiences, you can view details, update configurations, or delete existing sources. For more information, see the [Manage data connections](./manage-data-connection.md) guide.
