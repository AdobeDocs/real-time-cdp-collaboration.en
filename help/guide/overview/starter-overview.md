---
title: RTCDP Collaboration Starter Overview
description: Learn how Adobe Real-Time CDP Collaboration Starter helps you to expand and enhance privacy-centric collaboration with a licensed partner without requiring your own full Real-Time CDP license.
audience: publisher, advertiser, invited users to Real-Time CDP Collaboration Starter
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
hidefromtoc: yes
hide: yes
exl-id: 7ae0bd3d-eee9-48c0-9f18-a56033fee52d
---
# Adobe Real-Time CDP Collaboration Starter Overview

Use Adobe Real-Time CDP Collaboration Starter to collaborate with a licensed partner on privacy-centric data projects. You do not need your own Collaboration license to participate.

Your licensed partner invites you into Collaboration and uses their credits to fund your joint workflows, across both advertiser-to-publisher and brand-to-brand patterns. To learn more about these patterns and how they work, read the [collaboration patterns](./collaboration-patterns.md) and [end-to-end workflow](./end-to-end-workflow.md) guides.

As an invited Starter user, you can:

* Onboard and manage collaboration data in a Starter account.
* Source and maintain audiences for use in joint projects.
* Gain insights into audience overlaps with your partner to support effective targeting and campaign measurement.
* Activate audiences and share them back to your partner for joint campaign activation and engagement.

## Prerequisites {#prerequisites}

To get started with Collaboration Starter, ensure that both your organization and your licensed partner are located in the same region. You must be invited by a partner who holds a Real-Time CDP Prime, Ultimate, or Collaboration license.

To initiate the invitation, provide the following information to your licensed partner:

* Contact name
* Contact email
* Company
* Role (Advertiser/Publisher): Advertiser
* Industry
* Admin name (if different from contact name)
* Admin contact email (if different from contact email)

After you receive and accept the invitation, your organization must review and sign a no-cost Sales Order with Adobe to access Collaboration Starter.

## Guardrails {#guardrails}

Read the following table to understand the key guardrails that apply to your Starter account. These include limits on audience sourcing, data volume, refresh frequency, audience overlaps and activation capabilities.

|Guardrail | Description |
|----------| ------------|
|Audience source | You can bring audience data into Collaboration with **[!DNL Amazon S3]** as your source. For step-by-step instructions, see [how to configure [!DNL Amazon S3] for audience sourcing](../setup/configure-aws-s3-audience-sourcing.md). |
|Audience | Your Starter account is entitled to a maximum of:<ul><li>10 audiences sourced from an [!DNL AWS S3] bucket</li><li>50 million total identities (calculated by the number of rows in your audience data)</li><li>1 refresh per audience every 6 days</li></ul>|
|Audience overlaps and insights | There is no usage limit on how often you can run audience overlaps and insights across your audiences. Learn how to [discover overlaps and compare audiences](../collaborate/discover.md). |
|Activation | As a Starter user, you can activate and share audiences only with the partner who invited you. Configuration of destinations to external platforms is not available. Learn more about [activating your audiences](../collaborate/activate.md). |

{style="table-layout:auto"}

## Getting started {#getting-started}

Once you have accepted the invitation and agreed to the terms, log in to [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} with your credentials. Follow the steps below to complete your Starter account setup and begin collaborating with your partner.

### Set up administrator access {#setup-admin-access}

To access Collaboration, you need administrator privileges. For step-by-step guidance on granting product administrator access to yourself, see the [admin access instructions](https://example.com).
<!-- TODO: link to Admin Access doc -->

Once complete, you should see **[!UICONTROL Permissions]**, **[!UICONTROL Experience Platform]**, and **[!UICONTROL Real-Time CDP Collaboration]** within the **[!UICONTROL Quick access]** section on your [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} homepage.

![The Adobe Experience Cloud workspace showing Permissions, Experience Platform, and Real-Time CDP Collaboration after product administrator access setup.](/help/assets/overview/starter/setup-admin-access.png){zoomable="yes"}

For more details about access roles and different Adobe Experience Cloud products, read the [access control overview](../permissions/overview.md).

### Configure permissions {#configure-permissions}

As a product administrator, you need to assign the appropriate roles and permissions to yourself before you can access Collaboration or grant access to others. See [how to configure permissions](https://example.com) for detailed steps. To learn more about the different roles and permissions available in Collaboration, see the [manage roles](../permissions/manage-roles.md) documentation.
<!-- TODO: link to Configure permissions doc -->

Before proceeding, ensure that you have access to Collaboration. Navigate to [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}, and select **[!UICONTROL Real-Time CDP Collaboration]** within the **[!UICONTROL Quick access]** section. You should now be in the **[!UICONTROL Adobe Real-Time CDP Collaboration]** workspace.

### Set up connections {#set-up-connections}

Next, set up your Collaboration account, establish a connection with your partner, and bring in your audience data as needed. For detailed instructions on completing these tasks, see the [completing connection guide](https://example.com).
<!-- TODO: link to Completing connection doc -->

### Understand credit usage {#understand-credit-usage}

All Collaboration Starter activities use credits. However, as an invited user, you do not need to purchase or manage these credits. The partner who invited you covers all credit usage associated with your activities. To learn more, see the [Starter credit usage and consumption](https://example.com) documentation.
<!-- TODO: link to Understanding credit usage and consumption doc -->
