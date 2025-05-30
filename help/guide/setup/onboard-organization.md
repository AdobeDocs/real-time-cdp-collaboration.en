---
title: Onboard and manage organization
description: Learn how to onboard and manage various aspects of your organization in Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
---
# Onboard and manage your organization 

{{limited-availability-release-note}}

Learn how to onboard your organization onto Real-Time CDP Collaboration and manage various aspects of your company. This page outlines the steps to onboard an organization to Adobe Real-Time CDP Collaboration, including setting your match keys, preferred identities, and more options. 

![The organization's setup workspace showcasing its current settings.](/help/assets/setup/manage-organization/my-organization.png){zoomable="yes"}

## Initial organization setup

You must first set up your organization and organizational details. If this is your first organization, you'll be directed through the onboarding process immediately, starting with setting up your [account details](#set-up-details).

To add additional organizations, navigate to **[!UICONTROL Setup]** in the left rail and select the **+** symbol in the upper right corner. Next, select **[!UICONTROL Account]**.

![The setup workspace with the Account option highlighted.](/help/assets/setup/manage-organization/add-new-account.png){zoomable="yes"}

### Set up details {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="Contact email"
>abstract="Please provide a team or role-based email, such as `collaboration@yourcompany.com`. Personal or individual email addresses should not be used."

To begin onboarding your organization, you must first set up the organization details. This requires you to add the following information:

* Add an **[!UICONTROL Organization name]** for your company.
* Add a **[!UICONTROL Description]** about your company.
* Select your **[!UICONTROL Company role]**. You can select between **[!UICONTROL Advertiser]** and **[!UICONTROL Publisher]**. Read the [end-to-end workflow document](/help/guide/end-to-end-workflow.md) to see similarities and slight differences in workflow between the two organizational role types.
* Select the **[!UICONTROL Industry]** for your organization. Some examples include **[!UICONTROL Retail]**, **[!UICONTROL Telecommunications]**, or **[!UICONTROL Financial services]**.
* Select the **[!UICONTROL Region]** for your organization. In the current version of the product, **[!UICONTROL North America]** is the preset default selection.
* Add a **[!UICONTROL Contact email]** for your organization. This should be a team or role-based email address. Personal email addresses should not be provided.
* Upload a **[!UICONTROL Logo]** for your company. Currently, SVG-type images are supported.
* Select an image for your company header picture.

>[!NOTE]
>
>While you're able to edit most of these details at anytime, the **[!UICONTROL Role]** and **[!UICONTROL Region]** are not editable after the initial setup.

![The Set up organization workspace with the Details section displayed.](/help/assets/setup/manage-organization/add-organization-details.png){zoomable="yes"}

When you're finished, use **[!UICONTROL Next]** to proceed to the next page to select the desired match keys your organization will use.

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

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_matchkeys"
>title="Activation match keys"
>abstract="Activation match keys are displayed based on your organization's chosen match keys."

>[!IMPORTANT]
>
>The match keys that you select during the organization setup will determine the available match keys for the connections that you create with other organizations. While you can remove match keys during the connection setup, you cannot add new match keys later. It is important to select all match keys that you plan to use in future campaigns during the organization setup.

Match keys, such as email addresses, device IDs, or customer IDs, help advertisers and publishers work together by enabling accurate and privacy-centric data synchronization, allowing for more precise audience targeting and measurement.

![Slide showing the available identifiers for the first release of Real-Time CDP Collaboration.](/help/assets/setup/manage-organization/available-identifiers.png)

Select any match keys that you want to use when reconciling members of publisher and advertiser audiences. Include any match keys that your company can work with. Plan for the future and select the match keys that you anticipate you will be using in future publisher-advertiser campaigns. If you do need to select additional match keys for your organization, you can also do that at a later time, in the [edit organization](#edit-organization) workflow.

![The Set up organization workspace with the Match keys section displayed.](/help/assets/setup/manage-organization/add-organization-match-keys.png){zoomable="yes"}

Select up to five match keys that you plan to use. Later, when setting up connections, you can remove unwanted match keys but cannot add new ones.

Available match keys in Real-Time CDP Collaboration can be of three types:

* First-party people IDs
* First-party device IDs
* Partner IDs

The available match keys for the first release of Real-Time CDP Collaboration are:

* Hashed email

When ready, select **[!UICONTROL Complete]** to finish the organization setup workflow. 

## Edit organization {#edit-organization}

After initially setting up your organization, you can at any time edit certain aspects and details of the organization. To edit your organization, select **[!UICONTROL Edit]** in the **[!UICONTROL My organization]** section of the **[!UICONTROL Setup] workspace**.

![The Setup workspace with the My organization tab and Edit option highlighted.](/help/assets/setup/manage-organization/edit-organization.png){zoomable="yes"}

You can now edit your organization details, with the exception of the **[!UICONTROL Role]** and **[!UICONTROL Region]**.

![The Edit organization details dialog.](/help/assets/setup/manage-organization/editable-options.png){zoomable="yes"}

You can also update the match keys that you initially selected when onboarding your organization. Select **[!UICONTROL Edit]** in the **[!UICONTROL Match keys]** section to add any additional desired match keys.

![The Setup workspace with the Edit option highlighted within the organization's Match keys section.](/help/assets/setup/manage-organization/edit-match-keys.png){zoomable="yes"}

## Next steps

After setting up your organization, you are ready to [import audiences](/help/guide/setup/onboard-audiences.md) into Real-Time CDP Collaboration.
