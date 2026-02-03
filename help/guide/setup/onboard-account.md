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
>abstract="Match keys are identifiers used to reconcile audience profiles from different data sources. Include any match keys that your brand can work with."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_setup_match_keys"
>title="match keys"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="First-party people IDs"
>abstract="First-party people IDs, such as hashed email addresses, hashed phone numbers or CRM IDs, are directly connected to an individual profile."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="First-party device IDs"
>abstract="First-party device IDs, such as ECID or IP addresses, are directly connected to devices that may be shared between several individuals."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="Supported partner IDs"
>abstract="Partner IDs are identifiers provided by external partners for audience reconciliation. Partner IDs are not directly connected to an individual profile."

![Supported match keys.](/help/assets/setup/manage-account/match-keys.png){zoomable="yes"}

>[!IMPORTANT]
>
>The match keys that you select during the account setup will determine the available match keys within your connections. While you can [remove unwanted match keys](../connect/establishing-connections.md#connection-settings) during the connection setup, match keys cannot be added after a connection has been established. It is important that you select **all** match keys that you plan to use in future campaigns during the account setup.

Match keys help collaborators work together by enabling accurate and privacy-centric data synchronization, allowing for more precise audience targeting and measurement. Match keys selected during account setup will determine which match keys are available in future connections. They are also used to [map fields](./onboard-audiences.md#map-fields) from your data connection to the target fields in Collaboration when sourcing audiences.

Select any match keys that you want to use when reconciling audience profiles. Plan for the future and include any match keys you can work with and anticipate using in future campaigns. If you do need to select additional match keys for your account at a later time, you can do so in the [edit account](#edit-account) workflow. However, any match keys added after the initial setup will not be available for use in existing connections.

#### Supported match keys {#supported-match-keys}

Collaboration supports three types of match keys: first-party people IDs, first-party device IDs, and partner IDs. All match keys must meet the following requirements:

* Match keys must be **trimmed**, **lowercased**
* Hashed match keys must be **SHA256-hashed**.
* If you provide hashed values that use uppercase characters, Collaboration automatically converts them to lowercase.
* If your source contains **plaintext identifiers**, use the **[!UICONTROL Apply transformation]** option during your [data connection setup](./manage-data-connection.md#match-keys) to apply hashing. This option is only available when sourcing audiences from Experience Platform and is not supported for cloud-based sources.

##### First-party people IDs

First-party people IDs are directly connected to an individual profile. Currently supported IDs are:

* **[!UICONTROL Hashed email]**
* **[!UICONTROL Hashed phone]**
* **[!UICONTROL CRM IDs]**
* **[!UICONTROL Loyalty IDs]**
<!-- * **[!UICONTROL Custom ID]**: Custom identifiers -->

##### First-party device IDs

First-party device IDs are identifiers connected to a specific device. Currently supported IDs are:

* **[!UICONTROL Hashed IPv4]**: Hashed IPv4 addresses
* **[!UICONTROL IDFA]**: The Identifier for Advertisers (IDFA) used in Apple iOS devices
* **[!UICONTROL GAID]**: Google Advertiser ID used in Android devices

##### Partner IDs

Partner IDs are identifiers provided by external partners for audience reconciliation. Currently supported IDs are:

* **[!UICONTROL AdFixus ID]**

>[!NOTE]
>
>Adobe's integration with [!DNL AdFixus] maps the unique [!UICONTROL AdFixus IDs] for each account to a common Adobe-encoded format. These mappings are used to identify overlaps between collaborators. When activating audiences using **[!UICONTROL AdFixus ID]**, the original IDs are used. The Adobe-encoded format never leaves Collaboration.

When selecting **[!UICONTROL AdFixus ID]**, you will need to provide the corresponding ID from your external partner in the **[!UICONTROL Account credentials]** section. This option will only be available *after* toggling on **[!UICONTROL AdFixus ID]**. Enter your AdFixus ID into the **[!UICONTROL Account ID]** field, being sure to double check the value for accuracy.

![The Match keys dialog with AdFixus ID toggled on and the Account credentials section highlighted.](/help/assets/setup/manage-account/adfixus-settings.png){zoomable="yes"}

After you've selected all desired match keys, select **[!UICONTROL Complete]** to finish the account setup workflow.

![The Set up account workspace with the Match keys section displayed.](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## Edit account {#edit-account}

After setting up your account, you can edit the details and match keys at anytime.

### Edit details {#edit-details}

You can edit most details of your account at any time, with the exception of the **[!UICONTROL Role]**. The region is automatically set based on your Adobe Experience Cloud account and cannot be changed.

To edit your account, select **[!UICONTROL Edit]** in the **[!UICONTROL My account]** section of the **[!UICONTROL Setup]** workspace.

![The Setup workspace with the My account tab and Edit option highlighted.](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

You can now edit your account details. Update any fields you want to change and then select **[!UICONTROL Save]** to confirm the changes.

![The Edit account details dialog.](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

### Edit match keys {#edit-match-keys}

>[!IMPORTANT]
>
>Editing match keys will not affect your existing connections. Once a connection has been established, the match keys that you select during the connection setup are fixed. It is important that you select **all** match keys that you plan to use in future campaigns during the account setup.

You can also update the match keys that you initially selected when creating your account. These match keys will determine the match keys available to future connections.

Select **[!UICONTROL Edit]** in the **[!UICONTROL Match keys]** section.

![The Setup workspace with the Edit option highlighted within the account's Match keys section.](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

The **[!UICONTROL Match keys]** dialog appears. Toggle on and off any match keys, or update your **[!UICONTROL Account ID]** for your [!UICONTROL AdFixus ID's],and then select **[!UICONTROL Save]** to confirm the changes.

>[!IMPORTANT]
>
>Changing your [!UICONTROL AdFixus ID] will not trigger a [data sketch](../glossary.md#sketches) refresh for your existing data connections using the match key. Once your data has been sketched, any changes to your [!UICONTROL AdFixus ID] will not be reflected until your next audience refresh following your [data connection schedule](./manage-data-connection.md#scheduling) settings. If you require changes before your next refresh, you can delete and recreate your data connection.

![The Match keys dialog with the Save option highlighted.](/help/assets/setup/manage-account/match-key-dialog.png){zoomable="yes"}

## Next steps

After setting up your accounts, you are ready to [source audiences](/help/guide/setup/onboard-audiences.md) into Real-Time CDP Collaboration.
