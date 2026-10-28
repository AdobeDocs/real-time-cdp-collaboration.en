---
title: Set up and manage identity resolution with [!DNL Epsilon Core ID]
description: Learn how to configure, review, and manage Epsilon Core ID identity resolution for audience data connections in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
---
# Set up and manage identity resolution with [!DNL Epsilon Core ID]

{{limited-availability-release-note}}

To configure identity resolution for your audience data, use the **[!UICONTROL Identity resolution]** workflow in Adobe Real-Time CDP Collaboration. You can select [!DNL Epsilon Core ID] as your identity provider, choose the audience data connections and match keys to use, and set the period during which identity resolution runs. After setup, you can view the configuration or delete it if you need to configure it again.

Identity resolution applies to the audience data connections you select, rather than individual audiences within those connections. When additional audiences are added to a selected connection, they are included in subsequent identity resolution runs.

## Prerequisites {#prerequisites}

Before configuring identity resolution with [!DNL Epsilon Core ID], make sure you have the following:

* **An eligible Collaboration account:** [!DNL Epsilon Core ID] identity resolution is available to US-provisioned accounts.
* **Account-management access:** You must be an account administrator or have the appropriate permissions to configure identity resolution. **[UNVERIFIED: Confirm the exact permission name and required permission scope; the KT says "Manage Account," while the repository uses "Manage Collaboration Instances."]**
* **At least one audience data connection:** Set up a connection for [audience sourcing](./source-overview.md) before configuring identity resolution. Measurement data connections are not supported for [!DNL Epsilon Core ID] in this release.
* **Supported match keys:** Enable and map at least one compatible identity option for the data connection: **[!UICONTROL Hashed email]**, **[!UICONTROL Hashed phone]**, or **[!UICONTROL Name]** together with **[!UICONTROL Postal address]**. If you use Name and Postal address, map at least one subcomponent for each key. You can [configure account match keys](./onboard-account.md#set-up-match-keys) and [map fields for audience sourcing](./onboard-audiences.md#map-fields) in the existing setup workflows.
* **Your Epsilon customer number:** Obtain the customer number from your Epsilon account representative. You must enter it during authentication.

>[!NOTE]
>
>Enabling a match key on your account does not map your audience data to that key. Complete the relevant data connection's field mapping before using the key for identity resolution. Name and Postal address values are not hashed.

## Configure identity resolution {#configure-identity-resolution}

To set up [!DNL Epsilon Core ID] identity resolution, select the identity provider in the **[!UICONTROL Setup]** workspace, then complete the authentication, data source, match key, schedule, and review steps. Each step configures part of the identity resolution job; review your selections before submitting because an existing configuration cannot be edited in place.

### Select an identity provider {#select-identity-provider}

1. Navigate to **[!UICONTROL Setup]** and select the **[!UICONTROL Identity resolution]** tab. The identity provider catalog appears.
2. Locate the **[!UICONTROL Epsilon Core ID]** card. Review its supported region and match keys. The catalog displays available identity providers and their accepted keys.
3. Select **[!UICONTROL Setup]** on the **[!UICONTROL Epsilon Core ID]** card to begin.

The wizard checks whether your account has an eligible data connection and supported match keys. If a prerequisite is missing, a dialog identifies the requirement:

* **[!UICONTROL Data connection required]:** Select **[!UICONTROL Set up data connection]** to configure an audience data connection. See [Source and manage audiences](./source-overview.md) for the available sourcing methods.
* **[!UICONTROL Match key required]:** Select **[!UICONTROL Edit match keys]** to enable a key supported by [!DNL Epsilon Core ID]. See [Edit match keys](./onboard-account.md#edit-match-keys) for account-level changes.

After resolving the requirement, return to **[!UICONTROL Identity resolution]** and select **[!UICONTROL Setup]** again. If both prerequisites are missing, the data connection requirement appears first.

>[!NOTE]
>
>If your account is outside the supported region, the provider card shows **[!UICONTROL Not available in your region]** instead of a setup action.

### Authenticate with Epsilon {#authenticate-with-epsilon}

To associate the identity resolution configuration with your [!DNL Epsilon] account, provide the customer number supplied by Epsilon.

1. In the **[!UICONTROL Authenticate]** step, enter the number in the required **[!UICONTROL Epsilon customer number]** field.
2. Select **[!UICONTROL Next]** to continue to data source selection.

The supplied requirements do not specify format validation for this number in the initial release. Verify the value with your Epsilon account representative before continuing.

![The Epsilon Core ID authentication step, with the required Epsilon customer number field and Next action.](../../assets/setup/identity-resolution/epsilon-core-id-authenticate.png){zoomable="yes"}

### Select data connections {#select-data-connections}

Choose which existing audience data connections to use for identity resolution. Each selected connection is included in the configuration, and the workflow does not provide individual audience selection within a connection.

1. In **[!UICONTROL Data source(s)]**, review the available cards under **[!UICONTROL Audience sources]**.
2. Select the checkbox on each audience data connection you want to include. You must select at least one connection.
3. Select **[!UICONTROL Next]** to continue.

If no connection is selected, **[!UICONTROL Next]** remains unavailable. To use an audience source that is not listed, first [set up the audience data connection](./source-overview.md).

![The Data source(s) step, showing audience data connection cards with selection checkboxes.](../../assets/setup/identity-resolution/select-audience-data-connections.png){zoomable="yes"}

**[UNVERIFIED: The supplied audience-only source-selection screenshot was manually modified to omit measurement sources. Replace it with a clean release-candidate screenshot or a clearly cropped capture before publication.]**

### Configure match keys {#configure-match-keys}

For each selected audience data connection, choose which of its available match keys to use for [!DNL Epsilon Core ID] identity resolution. These selections determine which identifiers are considered for that connection's identity resolution job; they do not replace account-level match key configuration or source field mapping.

1. In **[!UICONTROL Match keys]**, review the keys displayed for each selected audience data connection.
2. Use the toggles to disable keys you do not want to use. Leave at least one eligible match key enabled for each selected connection.
3. Select **[!UICONTROL Next]** to continue.

For [!DNL Epsilon Core ID], use a supported email or phone key, or the combination of Name and Postal address. If a required key is missing from the connection, review the [account match keys](./onboard-account.md#edit-match-keys) and the [audience field mapping](./onboard-audiences.md#map-fields) before continuing.

**[UNVERIFIED: Replace the prototype match-key screenshot with a release-candidate capture showing only supported Epsilon Core ID keys. The supplied demo image also displays Device ID, which the launch requirements do not establish as a Core ID match key.]**

### Set an identity resolution schedule {#set-schedule}

Set the date range during which your selected audience data connections are used for identity resolution. Identity resolution follows the underlying data connection's schedule; you cannot set a separate processing frequency in this wizard.

1. In **[!UICONTROL Schedule]**, select the calendar control for **[!UICONTROL Date range]**.
2. Choose the start and end dates for the identity resolution configuration.
3. Select **[!UICONTROL Next]** to review your selections.

**[UNVERIFIED: The prototype also displays "Continue until I cancel the job," but Product described only a date-range control for the October 30 release. Confirm whether indefinite scheduling is available before documenting that option.]**

**[UNVERIFIED: Replace the prototype Schedule screenshot. It shows a connection-dependent hold checkbox that Product indicated is not an independent launch option.]**

### Review and confirm the configuration {#review-and-confirm}

Before submitting, verify that the authentication, audience data connections, match keys, and date range reflect how you want to use identity resolution.

1. In **[!UICONTROL Review]**, expand each configuration section to inspect its values.
2. If you need to change a selection, select **[!UICONTROL Edit]** beside that section, update the relevant step, and return to the review screen.
3. Select **[!UICONTROL Confirm and schedule]** to submit the configuration.

A confirmation dialog indicates that identity resolution has been set up for [!DNL Epsilon Core ID]. After confirmation, the first identity resolution run begins **PLACEHOLDER**. **[UNVERIFIED: Confirm when the first run starts relative to configuration submission and the underlying source schedule.]**

**[UNVERIFIED: Replace the prototype Review screenshot. It refers to an API token, measurement sources, and scheduling-hold details that are inconsistent with the confirmed Core ID launch workflow.]**

## Manage identity resolution {#manage-identity-resolution}

After configuring identity resolution, return to the **[!UICONTROL Identity resolution]** tab to inspect your [!DNL Epsilon Core ID] configuration or delete it. An existing configuration cannot be edited in place; changing it requires deletion followed by setup again.

### View configuration details {#view-configuration-details}

From **[!UICONTROL Setup]** > **[!UICONTROL Identity resolution]**, open the configured [!DNL Epsilon Core ID] card and select **[!UICONTROL View details]** to inspect the saved configuration. **[UNVERIFIED: Confirm the catalog action's final label; the PRD uses "View details," while Product refers to "View."]**

The details view identifies the configuration's status, provider account number, region, creation and update information, match keys, schedule, and associated audience connections. A displayed **[!UICONTROL Active]** status describes the configuration state; it should not be interpreted as confirmation that every identity resolution run has succeeded.

![The Epsilon Core ID details page, showing Active status, provider account information, match keys, schedule, and the associated audience data connection.](../../assets/setup/identity-resolution/epsilon-core-id-view-details-staging.png){zoomable="yes"}

**[UNVERIFIED: Replace this staging screenshot with a publication-ready image that does not show internal account or employee details. Confirm the exact fields displayed in the released view.]**

### Edit an existing configuration {#edit-configuration}

You cannot change an existing [!DNL Epsilon Core ID] configuration after setup. To use a different customer number, audience connection, match key selection, or date range, [delete the configuration](#delete-configuration), then repeat the [setup workflow](#configure-identity-resolution) with the revised values.

>[!IMPORTANT]
>
>Review all settings before selecting **[!UICONTROL Confirm and schedule]**. An existing configuration must be deleted and created again to make changes.

### Delete an identity resolution configuration {#delete-configuration}

To remove an existing [!DNL Epsilon Core ID] configuration:

1. Navigate to **[!UICONTROL Setup]** > **[!UICONTROL Identity resolution]**.
2. On the configured **[!UICONTROL Epsilon Core ID]** card, select **[!UICONTROL Delete]**.
3. Review the confirmation dialog and select **[!UICONTROL Delete]** to confirm.

The configuration is deleted and cannot be restored through the deletion action. Deleting the configuration **PLACEHOLDER**. **[UNVERIFIED: Confirm whether deletion affects previously resolved identifiers, only future processing, or both.]**

To configure identity resolution with this provider again, return to its card and complete the [setup workflow](#configure-identity-resolution).

## Troubleshoot setup issues {#troubleshoot}

Most setup interruptions described in the current workflow concern missing prerequisites or regional eligibility. Check the relevant condition before restarting setup:

* **Data connection required:** Configure at least one [audience data connection](./source-overview.md) with supported match keys, then return to the identity provider catalog.
* **Match key required:** [Enable a compatible key on the account](./onboard-account.md#edit-match-keys) and [map the corresponding source fields](./onboard-audiences.md#map-fields) before trying again. For Name and Postal address, both keys are needed to satisfy the Core ID name-and-address option.
* **Not available in your region:** [!DNL Epsilon Core ID] is limited to US-provisioned Collaboration accounts in this release. The account region is set during account provisioning.
* **Epsilon customer number unavailable:** Obtain the required customer number from your Epsilon account representative before completing authentication.

**[UNVERIFIED: Verify final prerequisite dialog strings and navigation in the release-candidate UI. The demonstration dialogs use other identity providers as examples.]**

## Next steps {#next-steps}

For related account and audience configuration tasks, refer to the following existing guides:

* [Configure and manage account match keys](./onboard-account.md#set-up-match-keys) to enable identifiers available for new data connections.
* [Map fields when sourcing audiences from Experience Platform](./onboard-audiences.md#map-fields) to provide values for the enabled match keys.
* [Manage data connections](./manage-data-connection.md) to review or change the source connections used by Collaboration.
