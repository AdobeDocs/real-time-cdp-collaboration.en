---
title: Managing data connections
description: Learn how to manage data connections, including match keys, scheduling, use cases, and audience filtering in Real-Time CDP Collaboration.
audience: administrator, data engineer
badgealpha: label="Alpha" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html" newtab=true
---

# Managing data connections in Real-Time CDP Collaboration

## Overview
Data connections in Real-Time CDP Collaboration allow you to import audiences from various sources, enabling seamless integration for data activation and collaboration across platforms. In this guide, you'll learn how to manage match keys, schedule data imports, and configure use cases for your connections. Additionally, you'll be able to filter audiences by different attributes for more granular insights.

> [!TIP]
> Make sure to define your match keys carefully, as they impact how data will be matched and used across collaborations.

Before managing your data connections here, you should initially set them up during the [audience onboarding workflow](./onboard-audiences.md). This will ensure the correct data sources are connected for use in Real-Time CDP Collaboration.

## Match keys {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Match keys"
>abstract="Match keys determine how data from different sources will be matched. Choose the match keys that are most relevant to your use cases and privacy guidelines."

>[!CONTEXTUALHELP]
> Match keys determine how data from different sources will be matched. Choose the match keys that are most relevant to your use cases and privacy guidelines.

Match keys are identifiers used to reconcile members across audiences from different data sources. Available match keys include:

- **Identity crosswalk** (e.g., lookup_1)
- **Hashed email**
- **Hashed phone number**
- **IP Address v4**
- **ECID**

You can edit the match keys by selecting the pencil icon next to the match key name. Ensure that the match keys align with the identity data in your source.

## Scheduling {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Scheduling"
>abstract="Scheduling ensures that your data is always up-to-date without manual intervention. Make sure to choose a frequency that fits the pace of your campaign needs."

Set the date range and frequency for importing data from your connections. This allows you to control how often new data will be pulled into the platform.

- **Date range**: Specify the start and end date (e.g., 05/15/2024 - 05/15/2025)
- **Frequency**: Set how often the data import occurs (e.g., Daily, Weekly)

To adjust the scheduling details, click the **Edit** button next to the scheduling section.

## Use cases {#use-cases}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_usecases"
>title="Use cases"
>abstract="Configuring use cases allows you to specify what actions can be taken on the data, from simple sharing to full activation in advertising campaigns. Not available in alpha"

Use cases define how the imported audience data can be leveraged in Real-Time CDP Collaboration. Available use cases include:

- **Discover**
- **Share**
- **Activate**
- **Measure**

You can configure different use cases for each match key (e.g., hashed email, hashed phone number). To modify use case settings, click the **Edit** button in the Use Cases section.

## Filtering audiences {#filtering-audiences}

>[!CONTEXTUALHELP]
> Filtering audiences by source, access level, and category helps you focus on the data that matters most to your specific collaboration needs.

When viewing the list of audiences from your data connection, you can filter them by several criteria:

- **Source**: Filter by the data connection source (e.g., Real-Time CDP, Sandbox1, Sandbox2).
- **Access level**: Filter by access level (e.g., Custom, Standard).
- **Category**: Filter by audience category (e.g., Marketing, Product, Service).

Use the dropdown menus in the audience list table to apply filters, helping you narrow down the displayed audiences to the most relevant ones.

## Next steps
Once you've configured your data connections, you can proceed with audience activation or data sharing as needed. For more advanced options, explore the [Audience Configuration](/help/audience-configuration) guide.
