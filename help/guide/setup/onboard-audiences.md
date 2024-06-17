---
title: Add audiences
description: Learn how to onboard audiences into 
audience: admin, publisher, advertiser
badgealpha: label="Alpha" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
---

# Onboard audiences

## Overview

This document outlines the steps to add an audience using Adobe Real-Time CDP Collaboration.

## Select audience source

![Select audience source screen showing options for AEP RTCDP, CSV File, Amazon S3, and Snowflake.](/help/assets/setup/add-audiences/Step-Select-Audience-Source.png)

In this step, you will choose the source of your audience data. The available sources include:

- **AEP RTCDP**: Adobe Experience Platform Real-Time CDP, ideal for leveraging integrated data within Adobe's ecosystem.
- **CSV File**: Upload a CSV file containing your audience data for quick and straightforward data ingestion.
- **Amazon S3**: Connect to your Amazon S3 storage to import audience data directly from your S3 buckets.
- **Snowflake**: Use your Snowflake data warehouse to pull in audience data seamlessly.

## Select audience

![Select audience screen showing a list of available audiences with checkboxes to select them.](/help/assets/setup/add-audiences/Step-Select-Audience.png)

After selecting the audience source, you will choose specific audiences to include. Use the search and filter options to find the relevant audiences.

## Map fields

![Map fields screen showing source fields mapped to target fields.](/help/assets/setup/add-audiences/Step-Map-Fields.png)

Here are the target fields you can map for your audiences. You can change the mapping by selecting a different field:

- **Source fields**: The fields from your data source.
  - **HEM**
  - **HASHED PHONE**
  - Add additional fields as needed.

- **Target fields**: The fields in Adobe Real-Time CDP.
  - **Hashed email**
  - **Hashed phone number**
  - **Email**
  - **Phone number**
  - **IP Address v4**
  - **ECID**

You can add more fields as necessary to ensure accurate data mapping.

### Identity crosswalks

![Identity crosswalks screen showing a list of available identity crosswalks with details.](/help/assets/setup/add-audiences/Step-Identity-Crosswalks.png)

An identity crosswalk is a tool used to connect different identifiers across datasets to enrich your audience data with additional attributes or dimensions. Select **[!UICONTROL Add identity crosswalks]** to see a screen where you can choose from various identity crosswalks. Each entry includes details such as the table name, type, description, and creation date.

For further reading, see the [glossary](#).

## Manage privacy

![Manage privacy screen showing options for setting connection access and metadata visibility.](/help/assets/setup/add-audiences/Step-Manage-Privacy-1.png)

![Manage privacy screen showing options for setting connection access and metadata visibility with selected connections.](/help/assets/setup/add-audiences/Step-Manage-Privacy-2.png)

Define the privacy settings of the selected audiences. You can change the connection access and metadata visibility from the audience inventory.

- **Connection access**: Choose how your audiences can be accessed:
  - **Private audiences**: None of the connections can use them.
  - **Public audiences**: All connections can use them self-serve.
  - **Custom audiences**: Only selected connections can use them.

- **Metadata visibility**: Control what metadata is visible to connections:
  - Show Audience Name.
  - Show Audience Counts.
  - Show Audience Overlap %.

- **Use cases for identities**: Configure use cases for different identity fields:
  - **Hashed email**: Discover, Share, Activate, Measure.
  - **Hashed phone number**: Discover, Share, Activate, Measure.
  - **Email**: Discover, Share, Activate.
  - **Phone number**: Discover, Share, Activate.
  - **IP Address v4**: Discover, Share, Activate, Measure.
  - **ECID**: Discover, Share, Activate, Measure.

## Schedule

![Schedule screen showing start and end dates for populating the audiences.](/help/assets/setup/add-audiences/Step-Schedule.png)

Schedule when to start and end populating the audiences. The audience will be updated according to this schedule.

- **Start date**: Set the start date for populating the audience.
- **End date**: Set the end date for populating the audience.

## Review

Review all the configurations and settings before finalizing the audience addition. Ensure all details are correct and complete the process.

## Next steps

After onboarding audiences, connect with a collaborator. 

