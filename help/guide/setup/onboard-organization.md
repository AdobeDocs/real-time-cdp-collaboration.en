---
title: Onboard and manage organization
description: Learn how to onboard and manage various aspects of your organization in Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgebeta: label="Beta" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
---
# Onboard and manage organization

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently a beta product, available to select customers. The product and documentation are subject to change. Contact your Adobe representative to learn more.

Learn how to onboard your organization onto Real-Time CDP Collaboration and manage various aspects of your company. This page outlines the steps to onboard an organization to Adobe Real-Time CDP Collaboration, including setting your match keys, preferred identities, and more options. 

![Setup page](/help/assets/setup/manage-organization/my-organization.png)

## Initial organization setup

As a first step to start using Real-Time CDP Collaboration, you must set up your organization and organizational details. The workflow includes the two pages below:

* [Set up details and use cases](#set-up-details-use-cases)
* [Set up match keys](#set-up-match-keys) 

>[!IMPORTANT]
>
>Any *use cases* and *match keys* that you select at the organization level will then trickle down to the [project level](/help/guide/collaborate/manage-projects.md) in the collaboration between advertisers and publishers. At the project level, you are then able to remove any use cases and match keys, but you are *not* able to add any additional ones that were not selected at the organization level in this screen.

### Set up details and use cases {#set-up-details-use-cases}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_usecases"
>title="Supported use cases"
>abstract="This option is disabled in the initial release of Real-Time CDP Collaboration."

1. Add an **[!UICONTROL Organization]** name for your company.
2. Add a **[!UICONTROL Description]** about your company.
3. Select your **[!UICONTROL Company role]**. You can select between **[!UICONTROL Advertiser]** and **[!UICONTROL Publisher]**. Read the [end-to-end workflow document](/help/guide/end-to-end-workflow.md) to see similarities and slight differences in workflow between the two organizational role types.
4. Select the **[!UICONTROL Industry]** for your organization. Some examples include **[!UICONTROL Retail]**, **[!UICONTROL Telecommunications]**, or **[!UICONTROL Financial services]**.
5. Select the **[!UICONTROL Region]** for your organization. In the beta release, **[!UICONTROL North America]** is the preset default selection.
6. When onboarding your company, you can select the **[!UICONTROL Use cases]** that you will be able to use for your campaigns. In the beta release of Real-Time CDP Collaboration, this selection is not available or required.
7. Upload a **[!UICONTROL Logo]** for your company. Currently, SVG-type images are supported.
8. Select an image for your company header picture.

![The details and use cases step to set up an organization](/help/assets/setup/manage-organization/add-organization-details-use-cases.png)

When satisfied with your selection, use **[!UICONTROL Next]** to proceed to the next page.

<!--
The available use cases for the first release of Real-Time CDP Collaboration are:

* Audience insights: Add this use case to your organization in order to ...
* Measurement: Add this use case to your organization in order to ...

-->

### Set up match keys {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Match keys"
>abstract="Match keys are identifiers used to reconcile members across audiences from different data sources. Include any match keys that your company can work with."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="First-party people IDs"
>abstract="First-party people IDs such as hashed email addresses or phone numbers are directly connected to an individual profile. Currently supported IDs are hashed emails and phone numbers."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="First-party device IDs"
>abstract="First-party device IDs such as ECID or IP addresses are directly connected to devices, which may be shared between several individuals. IPv4 is the only first-party device ID currently supported."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="Supported partner IDs"
>abstract="Partner IDs associated with profiles expand the reach to a certain profile."

Match keys, such as email addresses, device IDs, or customer IDs, help advertisers and publishers work together by enabling accurate and privacy-compliant data synchronization, allowing for more precise audience targeting and measurement.

![Slide showing the available identifiers for the beta program of Real-Time CDP Collaboration.](/help/assets/setup/manage-organization/available-identifiers.png)

Select any match keys that you want to use when reconciling members of publisher and advertiser audiences. Include any match keys that your company can work with. Plan for the future and select the match keys that you anticipate you will be using in future publisher-advertiser campaigns. If you do need to select additional match keys for your organization, you can also do that at a later time, in the [edit organization](#edit-organization) workflow.

![Match keys selection step.](/help/assets/setup/manage-organization/add-organization-match-keys.png)

Select up to five match keys that you plan to use. Later, when setting up connections, you can remove unwanted match keys but cannot add new ones. Set the identity count threshold (minimum count) for each selected match key. Match keys with fewer than the minimum count will not appear in the identity breakdowns for some use cases.

Available match keys in Real-Time CDP Collaboration can be of three types:

* First-party people IDs
* First-party device IDs
* Partner IDs

The available match keys for the first release of Real-Time CDP Collaboration are:

* Hashed email
* Hashed phone
* IPv4

<!--[TODO] discuss the supported match keys. -->

When ready, select **[!UICONTROL Complete]** to finish the organization set up workflow. 

## Edit organization {#edit-organization}

After initially setting up your organization, you can at any time edit certain aspects and details of the organization. To edit your organization, select the pencil icon in the **[!UICONTROL My organization]** view.

![Edit organization control highlighted.](/help/assets/setup/manage-organization/edit-organization.png)

At this point, you are able to update the organization name, description, logo, and organization profile picture. 

![Editable options for organizations.](/help/assets/setup/manage-organization/editable-options.png)

You can also update the match keys that you selected initially when onboarding your organization, as well as the minimum threshold for identities corresponding to match keys to be visible and usable in audience overlaps and other product areas. Select **[!UICONTROL Edit]** in the **[!UICONTROL Match kays]** tab to add any additional desired match keys or update identity thresholds.

![Edit match keys](/help/assets/setup/manage-organization/edit-match-keys.png)

## Next steps

After setting up your organization, you are ready to [import audiences](/help/guide/setup/onboard-audiences.md) into Real-Time CDP Collaboration.
