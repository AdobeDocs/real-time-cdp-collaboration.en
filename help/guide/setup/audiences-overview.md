---
title: Audiences overview
description: Learn about audiences in Real-Time CDP Collaboration, including where they can be sourced from.
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
# Audiences overview

{{limited-availability-release-note}}

In Adobe Real-Time CDP Collaboration, audiences are groups of users or customers you bring into Collaboration. After sourcing, you can use audiences to discover overlap with collaborators, activate audiences, and measure campaign performance. You can source audiences from a variety of source types, including Adobe Experience Platform, cloud storage and sharing systems, and file upload workflows, depending on where your audience data already lives.

## What you can do with audiences {#audiences-in-collaboration}

After an audience is sourced into Collaboration, it becomes available for use in supported collaboration workflows.

Use audiences in Collaboration to:

* Compare your audience with collaborator audiences
* Identify overlaps and opportunities
* Activate audiences
* Measure outcomes and campaign performance
* Manage audience visibility and related settings

## How audiences fit into Collaboration {#conceptual-diagram}

>[!NOTE]
>
> The following diagram provides a high-level view of how sourced audiences fit into Collaboration and are used in projects.

```text
Source → Data connection → Audience → Project
                                         │
                          ┌──────────────┼──────────────┐
                          ▼              ▼              ▼
                      Discover       Activate       Measure
                                         │
                                         ▼
                                    Destination
```

## Core concepts {#core-concepts}

The following concepts describe the key objects involved in audience sourcing and collaboration workflows.

**Source**  
The system or location where your audience data originates, such as Adobe Experience Platform, a cloud storage location, or a file upload.

**Data connection**  
The configured connection that Collaboration uses to access audience data from a source. A data connection includes source-specific configuration details such as authentication, field mapping, and scheduling.

**Audience**  
A group of users or customers that has been sourced into Collaboration and is available for use in projects.

**Connection**  
The collaboration relationship between your organization and another organization.

**Project**  
The workspace where collaborators use audiences together for supported use cases, such as discovery, activation, and measurement.

**Destination**  
The external platform or system where activated audiences are sent.

**Match keys**
Identifiers that Collaboration uses to match records across datasets and collaborators. Match keys support workflows such as audience overlap, activation, and measurement.

## Audience lifecycle {#audience-lifecycle}

In Collaboration, you source audiences through data connections, manage them in **[!UICONTROL Setup]**, and use them in projects for supported use cases.

1. **Source audiences**: Bring audience data into Collaboration through a data connection.
2. **Manage audiences**: Review and manage audience details, visibility, and related settings.
3. **Use audiences in projects**: Use sourced audiences in projects for supported use cases, including **Discover**, **Activate**, and **Measure**.

Not every audience is used in every use case. For example, an audience can be sourced and used for **Discover** without being activated, or it can be used in **Measure** workflows without being sent to a destination.

For more information about sourcing and managing audiences, see [Source and manage audiences](./onboard-audiences.md). For information about managing data connections, see [Manage data connections](./manage-data-connection.md).

## Where audiences come from {#supported-sources}

Collaboration supports multiple audience source types. The source you choose determines the setup flow, prerequisites, authentication requirements, data format, field mapping, refresh behavior, and available configuration options for bringing audiences into Collaboration.

* Adobe Experience Platform
* Cloud storage, including Amazon S3, Google Cloud Storage, and Azure storage
* Data-sharing services, including Snowflake and Databricks Delta Share
* Adobe Audience Manager
* CSV file upload

For a list of supported sources and source-specific setup steps, see [Sources overview](./source-overview.md#available-sources).

## What audiences are made up of {#match-keys}

Audiences in RTCDP Collaboration are made up of match keys. Depending on your account configuration, supported match keys can include **People IDs**, **Device IDs**, and **Partner IDs**. Match keys support workflows such as **audience overlap**, **activation**, and **measurement**.

To learn more, see [Set up match keys](../setup/onboard-account.md#set-up-match-keys) and [Manage data connections](../setup/manage-data-connection.md#match-keys)

## Use audiences in projects {#audiences-in-projects}

Projects provide the context for collaborating with another organization. Within a project, you can use audiences for supported collaboration use cases:

* **Discover**: Compare audiences and review overlap insights. See [Discover audience overlap](../collaborate/discover.md).
* **Activate**: Activate selected audiences for campaign use. Activation is initiated from the [!UICONTROL Activate] tab in the project workspace and sends audiences to the connection's configured destination. See [Activate audiences](../collaborate/activate.md). 
* **Measure**: Review campaign delivery and conversion reports associated with the project. See [Measure performance](../collaborate/measure.md).

For more information about creating and managing projects, see [Create and manage projects](../collaborate/manage-projects.md). For information about configuring destinations, see [Destinations overview](../destinations/overview.md).

## Next steps {#next-steps}

* [Review available audience sources](./source-overview.md)
* [Source and manage audiences](./onboard-audiences.md)
* [Create and manage projects](../collaborate/manage-projects.md)
* [Discover audience overlap](../collaborate/discover.md)
* [Activate audiences](../collaborate/activate.md)
* [Measure performance](../collaborate/measure.md)
* [Destinations overview](../destinations/overview.md)
