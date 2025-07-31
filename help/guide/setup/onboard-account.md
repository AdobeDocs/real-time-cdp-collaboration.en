---
title: Configure and manage your account
description: Learn how to configure and manage various aspects of your account in Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
---
# Configure and manage your account 

{{limited-availability-release-note}}

Learn how to set up your account in Real-Time CDP Collaboration to prepare for connections with other collaborators. This guide covers the initial setup of your account, including adding account details, selecting match keys, and managing your account's settings.

![The setup workspace showing a configured account.](/help/assets/setup/manage-account/my-account.png){zoomable="yes"}

## Set up your account {#set-up-account}

When you first access Collaboration, you are prompted to set up your account. This is a one-time process that allows you to configure your account details and match keys. If this is your organization's first account, you'll be directed through the onboarding process immediately, starting with setting up your [account details](#set-up-details).

To add additional organizations, navigate to **[!UICONTROL Setup]** in the left rail and select the add icon (![Add icon.](/help/assets/icons/plus.png)) in the upper right corner. Next, select **[!UICONTROL Account]**.

![The setup workspace with the My account tab and Account option highlighted.](/help/assets/setup/manage-account/add-new-account.png){zoomable="yes"}

### Set up details {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="Contact email"
>abstract="Please provide a team or role-based email, such as **collaboration@yourcompany.com**. Personal or individual email addresses should not be used."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="Connect code"
>abstract="The connect code is a unique identifier for your account. It is used to establish connections with other collaborators in Real-Time CDP Collaboration."

To begin configuring your account, you must first set up the account details. This requires you to add the following information:

* Add an **[!UICONTROL Account name]** that clearly represents your brand.
* Add a **[!UICONTROL Description]** about your brand. This is optional, but it helps other collaborators understand your brand better.
* Select your **[!UICONTROL Role]**. You can select between **[!UICONTROL Advertiser]** and **[!UICONTROL Publisher]**. Read the [roles](/help/guide/overview/roles.md) guide to see similarities and slight differences in workflow between the two account role types.
<!-- The above will need to be updated when I update things for B2B -->
* Select the **[!UICONTROL Industry]** for your account. Some examples include **[!UICONTROL Retail]**, **[!UICONTROL Telecommunications]**, or **[!UICONTROL Financial services]**.
* The **[!UICONTROL Region]** is automatically set based on your Adobe Experience Cloud account. This cannot be changed at anytime.
* Add a **[!UICONTROL Contact email]** for your account. This should be a team or role-based email address. Personal email addresses should not be provided.
* Upload a **[!UICONTROL Logo]** for your account. Currently, SVG-type images are supported. This is optional, but uploading a logo helps to visually represent your brand in the Collaboration interface
* Select an image for your account header picture.

>[!NOTE]
>
>While you're able to edit most of these details at anytime, the **[!UICONTROL Role]** is not editable after the initial setup. When you're finished, use **[!UICONTROL Next]** to proceed to the next page to select the desired match keys your organization will use.

![The Set up account workspace with the Details section displayed and the Next option highlighted.](/help/assets/setup/manage-account/add-account-details.png){zoomable="yes"}

### Set up match keys {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Match keys"
>abstract="Match keys are identifiers used to reconcile members across audiences from different data sources. Include any match keys that your brand can work with."

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

>[!IMPORTANT]
>
>The match keys that you select during the account setup will determine the available match keys for the connections that you create with other collaborators. While you can remove match keys during the connection setup, you cannot add new match keys. It is important to select **all** match keys that you plan to use in future campaigns during the account setup.

Match keys, such as email addresses, device IDs, or customer IDs, help collaborators work together by enabling accurate and privacy-centric data synchronization, allowing for more precise audience targeting and measurement.

![Slide showing the available identifiers for the first release of Collaboration.](/help/assets/setup/manage-account/available-identifiers.png)

<!-- Eventually replace this image above to match branding better. -->

Select any match keys that you want to use when reconciling audience profiles. Include any match keys that you can work with. Plan for the future and select the match keys that you anticipate you will be using in future campaigns. If you do need to select additional match keys for your account at a later time, you can do so in the [edit account](#edit-account) workflow.

Select up to five match keys that you plan to use. Later, when setting up connections, you can remove unwanted match keys but cannot add new ones.

There are three types of available match keys:

* First-party people IDs
* First-party device IDs
* Partner IDs

>[!IMPORTANT]
>
>Currently, the only match key supported is hashed email.

When ready, select **[!UICONTROL Complete]** to finish the organization setup workflow. 

![The Set up organization workspace with the Match keys section displayed.](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## Edit account {#edit-account}

After setting up your account, you edit certain aspects and details of the account at any time. To edit your account, select **[!UICONTROL Edit]** in the **[!UICONTROL My account]** section of the **[!UICONTROL Setup] workspace**.

![The Setup workspace with the My account tab and Edit option highlighted.](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

You can now edit your account details, with the exception of the **[!UICONTROL Role]**. Please note that the region is automatically set based on your Adobe Experience Cloud account and cannot be changed at any time.

![The Edit account details dialog.](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

You can also update the match keys that you initially selected when onboarding your organization. Select **[!UICONTROL Edit]** in the **[!UICONTROL Match keys]** section to add any additional desired match keys.

![The Setup workspace with the Edit option highlighted within the account's Match keys section.](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

## Next steps

After setting up your accounts, you are ready to [source audiences](/help/guide/setup/onboard-audiences.md) into Real-Time CDP Collaboration.
