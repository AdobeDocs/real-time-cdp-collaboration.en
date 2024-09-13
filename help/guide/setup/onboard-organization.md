---
title: Onboard organization
description: Learn how to onboard your organization onto Real-Time CDP Collaboration 
audience: admin, publisher, advertiser
badgealpha: label="Alpha" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
---

# Onboard and manage organization

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently an alpha product, available to select customers. Contact your Adobe representative to learn more. 

Learn how to onboard your organization onto Real-Time CDP Collaboration and manage various aspects of your company. This page outlines the steps to onboard an organization using Adobe Real-Time CDP Collaboration, including setting your match keys, preferred identities, and more options. 

![Setup page](/help/assets/setup/manage-organization/my-organization.png)

## Initial organization setup

As a first step to start using Real-Time CDP Collaboration, you must set up your organization and organizational details. The workflow includes the two pages below.

>[!IMPORTANT]
>
>Any use cases and match keys that you select at the organization level will then trickle down to the project level in the collaboration between advertisers and publishers. At the project level, you are then able to remove any use cases and match keys, but you are *not* able to add any additional ones that were not selected at the organization level in this screen.

### Set up details and use cases {#set-up-details-use-cases}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_usecases"
>title="Supported use cases"
>abstract="Insert content about use cases"

1. Add an **[!UICONTROL organization]** name for your company.
2. Add a **[!UICONTROL description]** about your company.
3. Select your **[!UICONTROL company role]**. You can select between **[!UICONTROL Advertiser]** and **[!UICONTROL Publisher]**. Read the [end-to-end workflow document](/help/guide/end-to-end-workflow.md) to see similarities and slight differences in workflow between the two organizational role types.
4. Select the **[!UICONTROL region]** for your organization. In the alpha release, **[!UICONTROL North America]** is the preset default selection.
5. When onboarding your company, you can select the **[!UICONTROL use cases]** that you will be able to use for your campaigns. In the alpha release of Real-Time CDP Collaboration, this selection is not available or required.
6. Upload a **[!UICONTROL logo]**. Currently, svg type images are supported.
7. Select a **[!UICONTROL background image]** for your organization.

![The details and use cases step to set up an organization](/help/assets/setup/manage-organization/add-organization-details-use-cases.png)

When satisfied with your selection, use **[!UICONTROL Next]** to go to proceed to the next page.

<!--
The available use cases for the first release of Real-Time CDP Collaboration are:

* Audience insights: Add this use case to your organization in order to ...
* Measurement: Add this use case to your organization in order to ...

-->

### Set up match keys {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Match keys"
>abstract="Insert content about match keys"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="Supported people IDs"
>abstract="Insert content about supported people IDs"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="Supported device IDs"
>abstract="Insert content about supported device IDs"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="Supported partner IDs"
>abstract="Insert content about supported partner IDs"

Match keys, such as email addresses, device IDs, or customer IDs, help advertisers and publishers work together by enabling accurate and privacy-compliant data synchronization, allowing for more precise audience targeting and measurement.

Select any match keys that you want to use when reconciling members of publisher and advertiser audiences. Include any match keys that your company can work with. It is important in this step to plan for the future and select the match keys that you anticipate you will be using in future publisher-advertiser campaigns.

![Match keys selection step.](/help/assets/setup/manage-organization/add-organization-match-keys.png)

Select up to five match key thats you plan to use; you can remove unwanted match keys but cannot add new ones later for each connection. Set the minimum count of identities for selected match keys. Identities below the minimum count will not appear in the identity breakdown for some use cases. 

Available match keys in Real-Time CDP Collaboration can be of three types:

* First-party people IDs
* First-party device IDs
* Partner IDs

The available match keys for the first release of Real-Time CDP Collaboration are:

* LiveRamp ID
* Merkury ID
* Hashed Email

[TODO] discuss the supported match keys.

When ready, select **[!UICONTROL Complete]** to finish the organization set up workflow. 

## Edit organization {#edit-organization}

After initially setting up your organization, you can at any time edit certain aspects and details of the organization. To edit your organization, select the pencil icon in the **[!UICONTROL My organization]** view.

![Edit organization control highlighted](/help/assets/setup/manage-organization/edit-organization.png)

At this point, you are able to update the organization name, description, logo, and photo.

## Next steps

After setting up your organization, [import audiences](/help/guide/setup/onboard-audiences.md) into Real-Time CDP Collaboration.
