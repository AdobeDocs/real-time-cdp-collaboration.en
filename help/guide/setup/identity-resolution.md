---
title: Set up and manage identity resolution
description: Learn how to configure and manage identity resolution in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser, agency
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
---
# Set up and manage identity resolution

{{limited-availability-release-note}}

Identity resolution helps you identify customers you have in common with collaborators, even when your organizations use different identifiers. Configure and manage identity resolution with supported identity providers in Real-Time CDP Collaboration, without building custom integrations for each partner.

>[!NOTE]
>
>The steps and screenshots in this guide use [!DNL Epsilon Core ID] as an example. Requirements and available options may differ depending on your identity provider.

>[!AVAILABILITY]
>
>At launch, only [!DNL Epsilon Core ID] is available for configuration. Epsilon Core ID identity resolution is only available for Real-Time CDP Collaboration accounts provisioned in the United States.

## Prerequisites {#prerequisites}

Before you begin, make sure you have:

* **Account-management permissions.** You must have **[!UICONTROL Manage Account]** and **[!UICONTROL Manage Collaboration Instances]** permissions.
* **At least one audience data connection.** You need an existing audience data connection to configure identity resolution. [Set up audience sourcing](./source-overview.md) if needed. Measurement data connections are not supported.
* **Supported match keys and fields.** Each audience data connection you intend to use for identity resolution must contain fields supported by your identity provider. For Epsilon Core ID, you can use hashed email, hashed phone, or name combined with postal address.

  Account-level match keys, such as hashed email and hashed phone, must be enabled for your account and mapped to your audience data. Name and postal address fields are mapped during audience data connection setup and do not require account-level enablement.

  If using name and postal address, map at least one field from each group:

  * **Name:** First name, last name, or full name.
  * **Postal address:** Street address, city, zip code, state, or country.

  Name and postal address values are not hashed. For instructions on enabling account-level match keys, such as hashed email and hashed phone, see [Edit match keys](./onboard-account.md#edit-match-keys). To map supported match keys or name and postal address fields to your audience data, see [Map fields](./onboard-audiences.md#map-fields).
* **Epsilon account number.** Obtain your Epsilon account number from your Epsilon account representative.

## Configure identity resolution {#configure-identity-resolution}

Select an identity provider to begin configuring identity resolution. In this [!DNL Epsilon Core ID] example, you'll authenticate with the provider, select audience data connections, set a date range, and review your configuration before confirming.

To begin, select **[!UICONTROL Setup]** in the left navigation followed by the **[!UICONTROL Identity resolution]** tab to view the available identity providers.

### Select an identity provider {#select-identity-provider}

Locate the card for your identity provider and review its supported region and match keys. Select **[!UICONTROL Setup]** to begin.

![Identity provider catalog with the Epsilon Core ID card and its Setup action.](../../assets/setup/identity-resolution/select-an-identity-provider.png){zoomable="yes"}

Before starting the configuration workflow, Collaboration checks for a data connection and compatible match keys. If a requirement is missing, a dialog appears to guide the process. Follow the action in the dialog:

* **[!UICONTROL Data connection required]:** Select **[!UICONTROL Set up data connection]** to configure an audience data connection. See [Connect a source](./source-overview.md#connect-a-source).
* **[!UICONTROL Match key required]:** Select **[!UICONTROL Edit match keys]** to enable a supported key. See [Edit match keys](./onboard-account.md#edit-match-keys).

If both are missing, the data connection dialog appears first. After fixing the prerequisites, return to **[!UICONTROL Identity resolution]** and select **[!UICONTROL Setup]** again.

### Authenticate with your identity provider {#authenticate-with-provider}

In the **[!UICONTROL Authenticate]** step, provide the information required by your identity provider. For Epsilon Core ID, enter the account number provided by your Epsilon representative in the **[!UICONTROL Epsilon account number]** field. Select **[!UICONTROL Next]** to continue.

![Authenticate step showing the Epsilon account number field.](../../assets/setup/identity-resolution/authenticate.png){zoomable="yes"}

### Select data connections {#select-data-connections}

Next, choose which audience data connections you want to use for identity resolution. This determines which audience data will be used to match your customer identities with your identity provider. Identity resolution automatically uses the supported identifiers mapped in each selected connection.
Next, choose which audience data connections you want to use for identity resolution. The selected connections determine which audience data and mapped fields are available for identity resolution.

Identity resolution applies to all audiences within each selected data connection, including any audiences added later. You cannot select individual audiences at this time.

If the connection you want isn't listed, [set up the audience data connection](./source-overview.md) before continuing.

Under **[!UICONTROL Data source(s)]**, select the checkbox for each connection you want to include in **[!UICONTROL Audience sources]**. You must select at least one connection. Select **[!UICONTROL Next]** to continue.

![Audience source cards showing selected and unselected data connections.](../../assets/setup/identity-resolution/source-selection.png){zoomable="yes"}

### Set an identity resolution schedule {#set-schedule}

Choose the start and end dates to define the period during which Adobe refreshes partner IDs. The refresh frequency is determined by the selected audience data connections, so you cannot configure a separate refresh frequency for identity resolution.

In the **[!UICONTROL Schedule]** step, select the calendar control under **[!UICONTROL Date range]** and choose your dates. Select **[!UICONTROL Next]** to continue.

![Schedule step with a date range for Epsilon Core ID identity resolution.](../../assets/setup/identity-resolution/schedule-identity-resolution-job.png){zoomable="yes"}

### Review and confirm the configuration {#review-and-confirm}

In the **[!UICONTROL Review]** step, check your authentication details, selected audience data connections, and schedule. To make changes, select **[!UICONTROL Edit]** beside the relevant section.

You cannot edit the configuration after setup. To make changes later, you must delete it and set it up again. Once you're satisfied with your selections, select **[!UICONTROL Confirm and schedule]**.

![Review step showing the authentication, data sources, and schedule summary.](../../assets/setup/identity-resolution/review-and-confirm.png){zoomable="yes"}

A confirmation dialog indicates that identity resolution has been configured successfully.

<!-- [Question: Does the first identity resolution run happen immediately after setup, or at the next scheduled audience data connection refresh?] -->

## Manage identity resolution {#manage-identity-resolution}

After confirming your setup, you're automatically returned to the **[!UICONTROL Identity resolution]** tab, where you can view or delete your configuration.

### View configuration details {#view-configuration-details}

To review your configuration, select **[!UICONTROL View details]** on your configured identity provider's card.

Review the authentication details, selected audience data connections, and date range. You can also view the match keys displayed in the configuration details, along with the configuration status and creation and update information.

![Identity resolution configuration details showing status, match keys, schedule, and associated audience connection.](../../assets/setup/identity-resolution/view-connection-details.png){zoomable="yes"}

### Change an existing configuration {#edit-configuration}

You cannot edit a Core ID configuration after setup. To change the Epsilon account number, selected data connections, or date range, [delete the configuration](#delete-configuration) and complete the [setup workflow](#configure-identity-resolution) again.

<!-- Question: Do other providers have the same limitation? -->

### Delete an identity resolution configuration {#delete-configuration}

To delete a configuration, navigate to **[!UICONTROL Setup]** > **[!UICONTROL Identity resolution]** and select **[!UICONTROL Delete]** on your configured identity provider's card. Review the confirmation dialog, then select **[!UICONTROL Delete]** to confirm.

If you want to use this identity provider again, you'll need to [set up a new configuration](#configure-identity-resolution).

<!-- [UNVERIFIED: Does deletion affect previously resolved identifiers, future processing, or both? Confirm before publication.] -->

## Troubleshoot setup issues {#troubleshoot}

If you cannot begin setup because a data connection or match key is missing, follow the instructions under [Select an identity provider](#select-identity-provider).

For Epsilon Core ID, check the following:

* **Not available in your region:** Epsilon Core ID is available only for Collaboration accounts provisioned in the United States.
* **Epsilon account number unavailable:** Contact your Epsilon representative to obtain your account number.
