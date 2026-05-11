---
title: Sources overview
description: Learn about source connectors in Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
---
# Sources overview

In Adobe Real-Time CDP Collaboration, a source (or data connection) is where your audience data comes from. You can connect to various source types such as Adobe applications, cloud-based storages, or files from your local system. 

This page provides a high-level overview of each source type that you can use in Collaboration and links to the setup guides for each.

## Source catalog {#source-catalog}

The following source types are currently available in the Real-Time CDP Collaboration source catalog.

### Adobe Experience Platform {#adobe-experience-platform}

Adobe Experience Platform is Adobe's real-time customer data platform. Use this source to bring in audiences from your connected Experience Platform instance and reuse your existing customer segments for audience activation, overlap analysis, and collaborative campaigns.

For detailed instructions, see [Source and manage audiences guide](./onboard-audiences.md).

### Adobe Audience Manager {#adobe-audience-manager}

Adobe Audience Manager is Adobe's data management platform that builds rich audience profiles and segments for targeted advertising and analytics. Use this source to bring existing Audience Manager segments into your Collaboration projects. Support for sourcing audiences from Audience Manager is coming soon.

### Amazon S3 {#amazon-s3}

Amazon S3 is a cloud-based storage service provided by [!DNL Amazon Web Services (AWS)]. Connect your S3 buckets as a source to bring audience data into Collaboration. This method is well suited for:

* Ingesting large first-party datasets directly from your cloud infrastructure. 
* Scaling and securing audience onboarding workflows.

Collaboration supports authentication to your S3 storage and sourcing audience files in the supported format. 

For detailed instructions, see [Configure AWS S3 for audience sourcing](./configure-aws-s3-audience-sourcing.md).

### [!DNL Snowflake] {#snowflake}

[!DNL Snowflake] is a cloud-based data warehouse platform. Connect your [!DNL Snowflake Secure Data Share] as a source to bring large-scale audience datasets directly into Collaboration. This workflow is well suited for secure, high-volume data exchange for audience analysis and activation within your collaborative projects.

For detailed instructions, see [Configure Snowflake for audience sourcing](./configure-snowflake-audience-sourcing.md).

### [!DNL Google Cloud Storage] {#gcs}

[!DNL Google Cloud Storage] (GCS) is [!DNL Google]'s scalable cloud storage service. Connect your GCS buckets to Collaboration to bring in audience data stored in your [!DNL Google Cloud] environment. This enables direct ingestion of first-party audiences for collaboration use cases.

For detailed instructions, see [Configure [!DNL Google Cloud Storage] for audience sourcing](./configure-gcs-audience-sourcing.md).

### CSV files {#csv}

You can source your audiences directly from your local system by uploading a properly formatted CSV file. This method is ideal when:

* Your audience data is exported as files 
* Your data is not currently stored in a supported cloud or Adobe application. 

The upload workflow supports mapping identity fields for activation and overlap analysis, and ensures your audience data is ready for use in Collaboration projects.

See [Upload CSV file for audience sourcing](./upload-csv-audience-sourcing.md) for step-by-step instructions.
