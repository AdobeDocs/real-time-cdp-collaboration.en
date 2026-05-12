---
title: RTCDP Collaboration Starter Overview
description: Learn how Adobe Real-Time CDP Collaboration Starter helps you to expand and enhance privacy-centric collaboration with a licensed partner without requiring your own full Real-Time CDP license.
audience: publisher, advertiser, invited users to Real-Time CDP Collaboration Starter
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 7ae0bd3d-eee9-48c0-9f18-a56033fee52d
---
# Adobe Real-Time CDP Collaboration [!DNL Starter] Overview

Use Adobe Real-Time CDP Collaboration [!DNL Starter] to collaborate with a licensed partner on privacy-centric data projects. You do not need your own Collaboration license to participate.

Your licensed partner invites you into Collaboration and uses their credits to fund your joint workflows, across both advertiser-to-publisher and brand-to-brand patterns. To learn more about these patterns and how they work, read the [collaboration patterns](./collaboration-patterns.md) and [end-to-end workflow](./end-to-end-workflow.md) guides.

As an invited [!DNL Starter] user, you can:

* Onboard and manage collaboration data in a [!DNL Starter] account.
* Source and maintain audiences for use in joint projects.
* Gain insights into audience overlaps with your partner to support effective targeting and campaign measurement.
* Activate audiences and share them back to your partner for joint campaign activation and engagement.

## Prerequisites {#prerequisites}

To get started with Collaboration [!DNL Starter], ensure that both your organization and your licensed partner are located in the same region. You must be invited by a partner who holds a Real-Time CDP Prime, Ultimate, or Collaboration license.

To initiate the invitation, provide the following information to your licensed partner:

* Contact name
* Contact email
* Company
* Role (Advertiser/Publisher): Advertiser
* Industry

After you receive and accept the invitation, your organization must review and sign a no-cost Sales Order with Adobe to access Collaboration [!DNL Starter]. For more details on the invitation process, see the [inviting a collaborator to Collaboration [!DNL Starter]](../connect/establishing-connections.md#invite-collaborator) guide.

## Guardrails {#guardrails}

Read the following table to understand the key guardrails that apply to your [!DNL Starter] account. These include limits on audience sourcing, data volume, refresh frequency, audience overlaps and activation capabilities.

|Guardrail | Description |
|----------| ------------|
|Audience source | You can bring audience data into Collaboration with **[!DNL Amazon S3]** as your source. For step-by-step instructions, see [how to configure [!DNL Amazon S3] for audience sourcing](../setup/configure-aws-s3-audience-sourcing.md). |
|Audience | Your [!DNL Starter] account is entitled to a maximum of:<ul><li>10 audiences sourced from an [!DNL AWS S3] bucket</li><li>50 million total identities (calculated by the number of rows in your audience data)</li><li>1 refresh per audience every 6 days</li></ul>|
|Audience overlaps and insights | There is no usage limit on how often you can run audience overlaps and insights across your audiences. Learn how to [discover overlaps and compare audiences](../collaborate/discover.md). |
|Activation | As a [!DNL Starter] user, you can activate and share audiences only with the partner who invited you. Configuration of destinations to external platforms is not available. Learn more about [activating your audiences](../collaborate/activate.md). |

{style="table-layout:auto"}

## Getting started {#getting-started}

After you [accept your invitation and agree to the terms](../connect/establishing-connections.md#accept-invitation-sign-terms), log in to [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} with your credentials. Before you can use Collaboration, your account must be granted the appropriate access and roles.

Use this workflow to set up your [!DNL Starter] account and begin collaborating with your partner.

### Set up administrator access {#setup-admin-access}

First, use the **Admin Access** workspace to grant yourself the necessary access. This ensures you have both administrative rights and user access to Experience Platform products. For detailed steps on how to set up initial access, see the [admin access instructions](../setup/starter-admin-access.md).

Once complete, you should see **[!UICONTROL Permissions]**, **[!UICONTROL Experience Platform]**, and **[!UICONTROL Real-Time CDP Collaboration]** within the **[!UICONTROL Quick access]** section on your [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} homepage.

![The Adobe Experience Cloud workspace showing Permissions, Experience Platform, and Real-Time CDP Collaboration after product administrator access setup.](/help/assets/overview/starter/setup-admin-access.png){zoomable="yes"}

For more details about access roles and different Adobe Experience Cloud products, read the [access control overview](../permissions/overview.md).

### Configure permissions {#configure-permissions}

Now that you have administrator privileges, you can assign roles and permissions to yourself and other users in your organization. This step is required before you can access Real-Time CDP Collaboration or allow others to use it. For detailed instructions, see [how to configure permissions](../setup/starter-permission-controls.md). For more information about the different roles and permissions available in Collaboration, see the [manage roles](../permissions/manage-roles.md) documentation.

Once roles and permissions have been assigned, confirm that you can access Collaboration. Navigate to [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}, and select **[!UICONTROL Real-Time CDP Collaboration]** within the **[!UICONTROL Quick access]** section. This opens the **[!UICONTROL Adobe Real-Time CDP Collaboration]** workspace, where you can begin using Collaboration features.

### Set up connections {#set-up-connections}

Next, follow steps in the following guides to set up connection and start collaborating with your partner:

* [Set up your Collaboration account](../setup/onboard-account.md)
* [Establish a connection with your inviting collaborator](../connect/overview.md)
* [Create a new project and begin collaborating with your partner](../collaborate/overview.md)

### Understand credit usage {#understand-credit-usage}

All Collaboration [!DNL Starter] activities use credits. However, as an invited user, you do not need to purchase or manage these credits. The collaborator who invited you covers all credit usage associated with your activities. To learn more, see the [credit usage and consumption in Collaboration [!DNL Starter]](../setup/starter-credit-usage.md) documentation.

## Next steps {#next-steps}

You've now completed initial setup and configured your organization for secure collaboration. Next, explore the following resources to learn about audience sourcing and different project use cases  within Collaboration:

* [Source and manage audiences](../setup/onboard-audiences.md)
* [Project use cases](../collaborate/overview.md#project-use-cases):
  * [Discover overlaps and compare audiences](../collaborate/discover.md)
  * [Activate audiences](../collaborate/activate.md)
  * [Measure campaign performance](../collaborate/measure.md) 
