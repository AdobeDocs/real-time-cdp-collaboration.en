---
title: Connections overview
description: Learn about connections in Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
---
# Connections overview

{{limited-availability-release-note}}

Before collaborators can work together on campaigns, they must establish a connection. This connection allows them to activate audiences, create projects, and run reports on campaign performance.

Connections are established based on your chosen collaboration pattern. Collaboration supports three key collaboration patterns: advertiser-to-publisher, brand-to-brand, and advertiser-to-advertising-platform. To read more about these patterns, see the [collaboration patterns](/help/guide/overview/collaboration-patterns.md) guide.

To learn how to establish a connection, read the section below that corresponds to your collaboration pattern:

- [Advertiser-to-publisher connection](#advertiser-to-publisher-connection)
- [Brand-to-brand connection](#brand-to-brand-connection)
- [Advertiser-to-advertising-platform connection](#advertiser-to-advertising-platform-connection)

## Advertiser-to-publisher connection {#advertiser-to-publisher-connection}

![High-level diagram of the advertiser-publisher connection process.](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

In the advertiser-to-publisher pattern, an advertiser discovers a publisher they want to work with through the **[!UICONTROL Discover publishers]** workspace and sends a connection invite. The publisher then reviews the invite and accepts it, allowing the advertiser to propose connection settings. Once the publisher accepts the connection settings, the connection is established, and both collaborators can begin working together on projects.

### High-level overview 

To establish a connection between an advertiser and a publisher, the following steps are involved:

1. [Discover publishers](./discover-publishers.md): The advertiser identifies potential publishers to collaborate with.
2. [Send invite](./establishing-connections.md#send-invite): The advertiser sends a connection invite to the selected publisher.
3. [Accept invite](./establishing-connections.md#accept-invite): The publisher reviews and accepts the invite.
4. [Configure connection settings](./establishing-connections.md#configure-connection-settings): The advertiser configures the connection settings and sends them to the publisher for review.
5. [Confirm connection settings](./establishing-connections.md#review-connection-settings): The publisher reviews the connection settings and either accepts or rejects them. If accepted, the connection is established. If rejected, the publisher can provide feedback for revisions outside the product. The advertiser can then revise the settings and resend them for review.

Once the connection settings are accepted, the connection is established, and collaborators are ready to [create a project](/help/guide/collaborate/manage-projects.md#create-project) to begin collaborating on campaigns.

## Brand-to-brand connection {#brand-to-brand-connection}

![High-level diagram of the brand-to-brand connection process.](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}

>[!TIP]
>
>The term **brand** is used to refer a company or brand outside of Collaboration. The term **collaborator** refers to any account that can form a connection in Collaboration, regardless of whether they are an advertiser or a publisher.

In the brand-to-brand pattern, two brands that have communicated outside of the product can connect directly in Collaboration using a [private connection invite](#private-connection-invite). A brand can be either an advertiser or a publisher. This pattern is particularly useful for brands that may not fit the traditional advertiser-publisher model, such as two advertisers or two publishers.

To begin, a collaborator sends a private connection invite to another collaborator. The recipient reviews the invite and accepts it, allowing the owner to propose connection settings. Once the recipient accepts the connection settings, the connection is established, and both collaborators can start working together on projects.

### High-level overview

>[!TIP]
>
>When discussing the connection process, there will be a distinction between the **owner** and the **recipient**. The owner is the collaborator who initiates the connection by sending the invite, while the recipient is the collaborator who receives and reviews the invite.

The connection process between two brands involves several steps. Before the connection process begins, a few prerequisites must be met:

1. Two brands communicate outside of the product to discuss the potential connection. 
1. The brands [create accounts](/help/guide/setup/onboard-account.md) in Collaboration if they haven't already, being sure to select the appropriate role type (advertiser or publisher).

Once the prerequisites are met, the connection process can begin. The following steps outline the process:

1. [Send private connection invite](./establishing-connections.md#private-connection-invite): One collaborator sends a private connection invite to another collaborator.
2. [Accept private connection invite](./establishing-connections.md#accept-invite): The recipient reviews and accepts the private connection invite.
3. [Configure connection settings](./establishing-connections.md#configure-connection-settings): The owner configures the connection settings and sends them to the recipient for review and acceptance.
4. [Confirm connection settings](./establishing-connections.md#review-connection-settings): The recipient reviews the connection settings and either accepts or rejects them.

Once the connection settings are accepted, the connection is established, and collaborators are ready to [create a project](/help/guide/collaborate/manage-projects.md#create-project) to begin collaborating on campaigns.

## Advertiser-to-advertising-platform connection {#advertiser-to-advertising-platform-connection}

![High-level diagram of the advertiser-advertising platform connection process.](/help/assets/connect/establish-connection/advertiser-ad-platform-flow.png){zoomable="yes"}

The advertiser-to-advertising-platform connection process allows advertisers to connect with third-party advertising platforms, such as Amazon Marketing Cloud (AMC), to enhance their marketing capabilities.

### High-level overview

The connection process between an advertiser and an advertising platform involves several steps. Before the connection process begins, ensure you have an active account with the advertising platform and are approved to use their services. The following steps outline the connection process:

1. [Discover advertising platforms](./advertising-platforms/overview.md): The advertiser identifies potential advertising platforms to collaborate with.
2. [Connect to advertising platform](./advertising-platforms/overview.md): The advertiser initiates the connection process by selecting the advertising platform they want to connect with and follows the prompts to authenticate and authorize the connection.

<!-- UPDATE LINKS ABOVE -->
