---
title: End-to-end workflow
description: Understand the end-to-end workflow of using Real-Time CDP Collaboration based on your collaboration pattern.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 90f9341e-5dd7-4521-a602-edb0263838c5
---
# End-to-end workflow

{{limited-availability-release-note}}

In Adobe Real-Time CDP Collaboration, the end-to-end workflow varies based on the collaboration pattern you choose. The workflow outlines the steps involved in setting up and executing a collaboration project, from creating accounts and sourcing audiences to forming connections and creating projects. Understanding this workflow is essential for effectively leveraging the platform's capabilities to achieve your marketing goals.

## Getting started

Before you begin, ensure you have a solid understanding of these key concepts:

- **Collaboration patterns**: These patterns define how collaborators work together. There are two distinct patterns: [advertiser-to-publisher](./collaboration-patterns.md#advertiser-to-publisher) and [brand-to-brand](./collaboration-patterns.md#brand-to-brand).
- **Account roles**: Account roles determine your capabilities within the platform. They should align with your organization's objectives, brand, and goals. There are two account roles: [advertiser](./roles.md#advertiser) and [publisher](./roles.md#publisher).
- **Use cases**: Uses cases define the ways you can leverage Collaboration to achieve your marketing objectives. There are three collaboration use cases: [discover](./use-cases.md#discover), [activate](./use-cases.md#activate), and [measure](./use-cases.md#measure).

This guide will use three mock collaborators to illustrate the end-to-end workflow:

- **Luma**: An athletic apparel brand. They are an advertiser that wants to reach specific audiences through targeted marketing campaigns.
- **TV Tube**: A digital streaming provider. They are a publisher that provides audience data for use by advertisers.
- **Fit Apparel**: Another athletic apparel brand. They are a secondary advertiser that wants to collaborate to share audience data and insights for enhanced marketing efforts.

## Advertiser-to-publisher workflow {#advertiser-to-publisher-workflow}

Luma, an athletic retail company, wants to form a connection with TV Tube, a digital streaming provider, to reach specific audiences through targeted marketing campaigns. 

To begin, Luma will need to [create an account](../setup/onboard-account.md) with the advertiser role, while TV Tube will create an account with the publisher role.

After establishing their accounts, both Luma and TV Tube will need to [create a data connection and source audiences](../setup/onboard-audiences.md). Only TV Tube will activate audiences for marketing campaigns, so they will need to [configure a destination](../setup/manage-destinations.md).

Once both collaborator's have their accounts set up, they can [form a connection](../connect/establishing-connections.md) within the platform. Luma can use the [discover publishers](../connect/discover-publishers.md) feature to find TV Tube and initiate a connection request. After TV Tube accepts the connection request, Luma can configure the connection settings to define how they will collaborate. TV tube can then accept the connection request to establish a secure link between the two brands.

After the connection is established, Luma can [create a project](../collaborate/manage-projects.md) to kick off their collaboration with TV Tube. During the project setup, they can choose the collaboration use cases that best fit their objectives, such as [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md), and [Measure](../collaborate/measure.md).

Depending on the use cases chosen during the project creation, Luma can leverage the [Discover](../collaborate/discover.md) use case to gain insights into TV Tube's audience data. Once Luma has identified the target audience segments, they can [Activate](../collaborate/activate.md) these audiences.

After activating the audiences, TV Tube can run targeted marketing campaigns and then upload data to [Measure](../collaborate/measure.md) the results to evaluate the effectiveness of their campaign. 

## Brand-to-brand workflow {#brand-to-brand-workflow}

Fit Apparel, an athletic apparel brand, wants to collaborate with Luma, another athletic apparel brand, to share audience data and insights for enhanced marketing efforts.

After establishing their accounts, both Fit Apparel and Luma will need to [create a data connection and source audiences](../setup/onboard-audiences.md). Both Fit Apparel and Luma will activate audiences for marketing campaigns, so they will both need to [configure a destination](../setup/manage-destinations.md).

After sourcing their audiences, Fit Apparel and Luma will [form a connection](../connect/establishing-connections.md) within the platform to securely share audience data. To do so, they must make use of the [private connection invite](../connect/establishing-connections.md#private-connection-invite) feature. Luma can share their connect code with Fit Apparel, who can then use it to initiate a connection request. After Luma accepts the connection request, Fit Apparel can configure the connection settings to define how they will collaborate. In the configuration, Fit Apparel must specify that both collaborators can activate audiences for marketing campaigns. To complete the connection, Luma can then accept the request to establish a secure link between the two brands.

Fit Apparel can then [create a project](../collaborate/manage-projects.md) to kick off their collaboration with Luma. During the project setup, they can choose the collaboration use cases that best fit their objectives, such as [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md), and [Measure](../collaborate/measure.md).

Depending on the use cases chosen during the project creation, Fit Apparel and Luma alike can leverage the [Discover](../collaborate/discover.md) use case to gain insights into each other's audience data. Once they have identified valuable audience segments, they can [Activate](../collaborate/activate.md) their chosen audiences for marketing campaigns.

Finally, after executing their campaigns, both brands can upload data to [Measure](../collaborate/measure.md) the results and evaluate the effectiveness of their collaboration.
