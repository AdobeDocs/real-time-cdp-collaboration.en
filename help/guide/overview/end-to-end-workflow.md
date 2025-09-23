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
- **Use cases**: Uses cases define the ways you can leverage Collaboration to achieve your marketing objectives. There are three collaboration use cases: [Discover](./use-cases.md#discover), [Activate](./use-cases.md#activate), and [Measure](./use-cases.md#measure).

This guide will use three mock collaborators to illustrate the end-to-end workflow:

- **[!UICONTROL Luma]**: An athletic apparel brand. They are an advertiser that wants to reach specific audiences through targeted marketing campaigns.
- **[!UICONTROL TV Tube]**: A digital streaming provider. They are a publisher that provides audience data for use by advertisers.
- **[!UICONTROL Fit Apparel]**: Another athletic apparel brand. They are a second advertiser that wants to collaborate to share audience data and insights for enhanced marketing efforts.

## Advertiser-to-publisher workflow {#advertiser-to-publisher-workflow}

[!UICONTROL Luma], an athletic retail company, wants to form a connection with [!UICONTROL TV Tube], a digital streaming provider, to reach specific audiences through targeted marketing campaigns.

To begin, [!UICONTROL Luma] needs to [create an account](../setup/onboard-account.md) with the advertiser role, while [!UICONTROL TV Tube] creates an account with the publisher role.

After establishing their accounts, both [!UICONTROL Luma] and [!UICONTROL TV Tube] must [create a data connection and source audiences](../setup/onboard-audiences.md). Only [!UICONTROL TV Tube] will activate audiences for marketing campaigns, so they need to [configure a destination](../setup/manage-destinations.md).

Once both collaborators have their accounts set up, they're ready to [form a connection](../connect/establishing-connections.md) within the platform. [!UICONTROL Luma] uses the [discover publishers](../connect/discover-publishers.md) feature to find [!UICONTROL TV Tube] and initiate a connection request. After [!UICONTROL TV Tube] accepts the connection request, [!UICONTROL Luma] configures the connection settings to define how the collaboration. [!UICONTROL TV Tube] accepts the connection request to establish a secure link between the two brands.

After the connection is established, [!UICONTROL Luma] [creates a project](../collaborate/manage-projects.md) to kick off their collaboration with [!UICONTROL TV Tube]. During the project setup, they choose the collaboration use cases that best fit their objectives: [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md), and [Measure](../collaborate/measure.md).

[!UICONTROL Luma] leverages the [Discover](../collaborate/discover.md) use case to gain insights into [!UICONTROL TV Tube]'s audience data. Once [!UICONTROL Luma] has identified the target audience segments, they [Activate](../collaborate/activate.md) these audiences.

After activating the audiences, [!UICONTROL TV Tube] runs targeted marketing campaigns and uploads data to [Measure](../collaborate/measure.md) the results to evaluate the effectiveness of their campaign.

## Brand-to-brand workflow {#brand-to-brand-workflow}

[!UICONTROL Fit Apparel], an athletic apparel brand, wants to collaborate with [!UICONTROL Luma], another athletic apparel brand, to share audience data and insights for enhanced marketing efforts.

After establishing their accounts, both [!UICONTROL Fit Apparel] and [!UICONTROL Luma] need to [create a data connection and source audiences](../setup/onboard-audiences.md). Both [!UICONTROL Fit Apparel] and [!UICONTROL Luma] will activate audiences for marketing campaigns, so they both need to [configure a destination](../setup/manage-destinations.md).

After sourcing their audiences, [!UICONTROL Fit Apparel] and [!UICONTROL Luma] [form a connection](../connect/establishing-connections.md) within the platform to securely share audience data. To do so, they must make use of the [private connection invite](../connect/establishing-connections.md#private-connection-invite) feature. [!UICONTROL Luma] shares their connect code with [!UICONTROL Fit Apparel], who then uses it to initiate a connection request. After [!UICONTROL Luma] accepts the connection request, [!UICONTROL Fit Apparel] configures the connection settings to define how they will collaborate. In the configuration, [!UICONTROL Fit Apparel] specifies that both collaborators can activate audiences for marketing campaigns. To complete the connection, [!UICONTROL Luma] accepts the request to establish a secure link between the two brands.

After the connection is established, [!UICONTROL Fit Apparel] [creates a project](../collaborate/manage-projects.md) to kick off their collaboration with [!UICONTROL Luma]. During the project setup, they choose the collaboration use cases that best fit their objectives: [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md), and [Measure](../collaborate/measure.md).

[!UICONTROL Fit Apparel] and [!UICONTROL Luma] can both use the [Discover](../collaborate/discover.md) use case to gain insights into each other's audience data. Once they have identified valuable audience segments, they [Activate](../collaborate/activate.md) their chosen audiences for marketing campaigns.

Finally, after executing their campaigns, both brands upload data to [Measure](../collaborate/measure.md) the results and evaluate the effectiveness of their collaboration.

## Advertiser-to-advertising platform workflow {#advertiser-to-advertising-platform-workflow}

![UICONTROL Luma], an athletic retail company, wants to connect with [!DNL Amazon Marketing Cloud] ([!DNL AMC]) to enhance their marketing capabilities by leveraging [!DNL AMC]'s identity resolution and targeting tools. Luma already has an active [!DNL Amazon Advertising] account and is approved to use [!DNL AMC].

To begin, [!UICONTROL Luma] needs to [create an account](../setup/onboard-account.md) with the advertiser role. After establishing their account, [!UICONTROL Luma] must [create a data connection and source audiences](../setup/onboard-audiences.md). Since [!UICONTROL Luma] will activate audiences for marketing campaigns, they need to [configure a destination](../setup/manage-destinations.md).

Once [!UICONTROL Luma] has their account set up, they're ready to [form a connection](../connect/establishing-connections.md) with [!DNL AMC] within the platform. [!UICONTROL Luma] uses the [discover collaborators](../connect/discover-publishers.md) feature to find [!UICONTROL Amazon Marketing Cloud] and [initiate a connection request](../connect/advertising-platforms/amc.md). After authenticating and authorizing the connection through the [!DNL Amazon] sign-in page, the connection with [!DNL AMC] is established.

After the connection is established, [!UICONTROL Luma] [creates a project](../collaborate/manage-projects.md) to kick off their collaboration with [!DNL AMC]. Connection settings, including use cases, are pre-configured depending on the advertising platform. For [!DNL AMC], the available use case is [Discover](../collaborate/advertising-platforms/amc.md#discover).

[!UICONTROL Luma] leverages the [Discover](../collaborate/advertising-platforms/amc.md#discover) use case to gain insights and audience data from [!DNL AMC]. Using these insights, [!UICONTROL Luma] can optimize their marketing strategies and improve campaign effectiveness.
