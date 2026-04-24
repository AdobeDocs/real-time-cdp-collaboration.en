---
title: Glossary
description: Understand key terminology for Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
hide: true
exl-id: 870c45d0-df68-487f-bbe2-d9862a8ea62e
TQID: https://experienceleague.adobe.com/aamkkPQbkaATqzByHmnTU2QGiUXLOn1yhz1jPA8LgGc
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
    internal-label: Use cases
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
---
# Glossary

{{limited-availability-release-note}}

This glossary provides definitions for key terms identified in the Adobe Real-Time CDP Collaboration product and documentation. Understanding these terms will help you better utilize the product and its features.

## A

### Advertiser

Any entity that will spend marketing budget to reach audiences across publishers or other brand partners to achieve goals of brand awareness, prospecting, re-engagement, and conversions.

## C

### Cloud storage

Cloud storage is a cloud computing solution that enables storing data and files on the internet through a cloud computing provider and is almost always a part of an organization's data stack. Examples include Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP).

### Connection request

A connection request is a formal request sent from one organization to another to establish a data-sharing connection. Once accepted, it allows the two parties to collaborate and share audience data securely.

### Connection settings

After a connection request is accepted, the initiator of that request sends the connection settings to the collaborator for approval. These connection settings govern the way that the collaborators work together on projects and include match keys to be used, billing ownership, and more. 

<!--

### Crosswalk

An identity crosswalk is a tool used to connect different identifiers across datasets to enrich your audience data with additional attributes or dimensions. It creates a bridge between different data points, allowing for a more comprehensive and cohesive view of the data.

-->

## D

### Data clean room

A secure collaboration environment which allows two or more participants to leverage data assets for specific, mutually agreed upon uses, while guaranteeing enforcement of strict data access limitations. This infrastructure layer is often provided by cloud storage providers and/or by data warehouses like Snowflake and Databricks and is best suited for technical users like data engineers and data scientists proficient in skills such as SQL.

### Data collaboration

Data collaboration involves combining and analyzing data within a company or alongside partners for various purposes, such as audience targeting, measurement, and insights. Data collaboration platforms offer secure environments to share data safely while meeting privacy and security concerns.

### Data connection

A data connection is the source from where you can import data into Real-Time CDP Collaboration. Currently, Experience Platform is the only available data connection. Read more about [managing data connections](/help/guide/setup/manage-data-connection.md).

### Data sharing agreement

A data sharing agreement is a formal contract between two or more parties outlining the terms and conditions for sharing data. It ensures that all parties comply with legal and privacy requirements and establishes guidelines for data usage and protection.

### Device identifier

A device identifier is a unique number associated with a device, such as a smartphone or tablet. It is used to track and identify the device across various platforms and services, enabling personalized user experiences and targeted advertising.

## I

### Invite

An invite in Adobe Real-Time CDP Collaboration refers to a request sent to another user or organization to join a project or data collaboration effort. Invites help facilitate secure and controlled access to shared data and resources.

<!--

## J

### Join key

In the context of identity crosswalks, a join key is a unique identifier used to match and link different identifiers across datasets, enabling the integration and unification of audience data from various sources. For example, a hashed email (HEM) can be a join key.

-->

## M

### Match keys

Match keys are unique identifiers used to link records across different datasets. They help ensure that data from different sources can be accurately matched and integrated, facilitating better data analysis and audience segmentation.

## O

### Overlap

An overlap (or audience overlap) refers to the common audience segments that exist between different datasets. Understanding audience overlap helps identify potential collaboration opportunities and allows for more targeted marketing efforts by leveraging shared audience data.

## P

### Project

A project in Adobe Real-Time CDP Collaboration is a workspace where users can collaborate on specific data integration and audience segmentation tasks. Projects help organize and manage data-sharing efforts, making collaboration more efficient and streamlined.

### Public audience

Within the context of projects, this is an audience that is discoverable by your collaborator. Audiences can be private, custom, or public. Private audiences are not discoverable by any other collaborators. Custom audiences can be discovered by certain collaborators only, and public audiences can be discovered by all collaborators. 

### Publisher

A Publisher is an owner or operator of online content or services where personal data is collected with consent and is available for use by other entities for digital advertising and audience measurement.

## S

### Sketches {#sketches}

Sketches (or data sketches) are simplified summaries of audience data used in Real-Time CDP Collaboration. They allow brands and publishers to analyze audience overlaps and insights without sharing actual customer data. Think of them like anonymous headcounts rather than detailed customer profiles.
In Adobe Real-Time CDP Collaboration, data sketches:

* Help determine how similar two audiences are
* Maintain privacy while enabling collaboration
* Need to be refreshed at least every 7 days to remain valid

If sketches aren't refreshed regularly, audience overlap reports will show zero values and audience sharing may become temporarily unavailable. Data sketches are automatically refreshed whenever an audience membership is updated in Real-Time CDP Collaboration.

## U

### Use case

A use case defines a specific business scenario or problem that can be addressed using Adobe Real-Time CDP Collaboration. Within Real-Time CDP Collaboration, sample use cases such as audience discovery or measurement, are available to help achieve a particular goal.
