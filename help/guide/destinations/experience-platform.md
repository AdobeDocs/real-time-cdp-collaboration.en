---
title: Configure Adobe Experience Platform as a destination
description: Learn how to configure and manage Adobe Experience Platform as a destination in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 594610a0-9102-448a-b59b-ec162ef9dd57
---
# Configure Adobe Experience Platform as a destination

{{limited-availability-release-note}}

Configure this destination to activate audiences from your project to Adobe Experience Platform. Activating audiences to Adobe Experience Platform allows you to leverage the platform's capabilities for audience segmentation, analysis, and activation across various marketing channels. To learn more about Adobe Experience Platform, refer to the [Experience Platform overview](https://experienceleague.adobe.com/en/docs/experience-platform/landing/home){target="_blank"}.

>[!WARNING]
>
>You cannot update a destination after it has been created. If you need to change any settings, you must delete the existing destination and create a new one.

## Configure destination {#configure-destination}

To configure Adobe Experience Platform as a destination, navigate to **[!UICONTROL Setup]** and then select the **[!UICONTROL My destinations]** tab. Select **[!UICONTROL Set up]** for Adobe Experience Platform.

![The My destinations workspace with the Set up option highlighted for the Adobe Experience Platform destination.](/help/assets/destinations/adobe-experience-platform/setup-aep.png)

The **[!UICONTROL Create destination]** workflow appears. 

![The Create destination workflow for Adobe Experience Platform.](/help/assets/destinations/adobe-experience-platform/create-destination.png)

### Configure sandbox {#configure-sandbox}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_audience_expiration"
>title="Audience expiration"
>abstract="The time period after which the audience will no longer be available in Adobe Experience Platform. The default expiration is 30 days, but you can set it to any value between 1 and 30 days."

First, you must select the sandbox where your audience data will be sent. 

>[!IMPORTANT]
>
>You can only select a sandbox that your user has access to. By default, all Collaboration users have access to the **Prod** sandbox. To gain access to additional sandboxes, an administrator must add additional sandboxes to a role assigned to your user. For more information about managing roles, refer to the [manage roles](../permissions/manage-roles.md) guide.

In the **[!UICONTROL Configure sandbox]** section, select the **[!UICONTROL Sandbox]** dropdown, or type in the name of a sandbox.

![The Sandbox dropdown highlighted in the Create destination workflow.](/help/assets/destinations/adobe-experience-platform/select-sandbox.png)

Alternatively, you can select **[!UICONTROL Browse sandbox]** to view all available sandboxes, as well as their **[!UICONTROL Type]**, **[!UICONTROL Status]**, and **[!UICONTROL Region]**. Select the sandbox that you want to use, and then select **[!UICONTROL Save]**.

Next, configure the **[!UICONTROL Audience Expiration]**. By default, the audience expiration is set to 30 days. You can choose to set the expiration anywhere from 1 to 30 days. After the expiration date, the audience will no longer be available in Adobe Experience Platform.

![The Audience Expiration section highlighted in the Create destination workflow.](/help/assets/destinations/adobe-experience-platform/audience-expiration.png)

### Create activation mapping {#create-activation-mapping}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_matchkeys"
>title="Activation match keys"
>abstract="Activation match keys are displayed based on the match keys you selected when creating your organization."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_target_namespaces"
>title="Target namespaces"
>abstract="Target namespaces specify which identity namespace the match key will be mapped to in Adobe Experience Platform. Hashed match keys must be mapped to a target namespace that supports hashed values."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_linked_key"
>title="Linked key"
>abstract="Linked keys allow you to specify that instead of using a particular match key, a different match key should be used during activation. For a profile to be activated, it must have values for both the original match key and the linked match key."

Next, you must create an activation mapping to define how the audience data will be sent to Adobe Experience Platform. You can map each [match key](../setup/onboard-account.md#set-up-match-keys) you selected while creating your account to a target namespace. The target namespaces specify which [identity namespace](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"} the match key will be mapped to in Adobe Experience Platform. You may utilize the [linked key](#linked-keys) option to replace a match key with a different match key during activation.

#### Select match keys {#select-match-keys}

All match keys enabled for your account are included in the activation mapping by default. If you do not wish to include a match key, you can remove it using the delete icon (![Delete icon](/help/assets/icons/delete.png)) next to the match key.

![The Activation mapping section with the delete icon highlighted next to a match key.](/help/assets/destinations/adobe-experience-platform/delete-mapping.png)

To re-add a match key that you previously removed, you can select **[!UICONTROL Add mapping]**. Alternatively, you can change the **[!UICONTROL Activation match key]** for an existing key using the dropdown menu.

![The Activation match key dropdown and Add mapping highlighted in the Create destination workflow.](/help/assets/destinations/adobe-experience-platform/add-mapping.png)

#### Map target namespaces {#map-target-namespaces}

To map each match key to a target namespace, select the **[!UICONTROL Target namespaces]** field next to the match key. The **[!UICONTROL Select source field]** dialog appears. Find the target namespace in the list, or search for a specific namespace. Select the target namespace that you want to use for the match key, and then select **[!UICONTROL Select]**.

>[!IMPORTANT]
>
>Hashed match keys must be mapped to a target namespace that supports hashed values. For example, the **[!UICONTROL Hashed email]** match key must be mapped to the **[!UICONTROL Email(SHA256, lowercased)]** identity namespace in Adobe Experience Platform. You cannot map the **[!UICONTROL Hashed email]** match key to the **[!UICONTROL Email]** identity namespace, as this namespace does not support hashed values.

![The Select source field dialog with the Select option highlighted..](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

Repeat this process for each match key that you want to include in the activation mapping. If you do not wish to include a match key, you can remove it, or use the linked key option to replace it with a different match key.

#### Linked keys {#linked-keys}

Linked keys allow you to specify that instead of using a particular match key, a different match key should be used during activation. To better understand how linked keys work, consider the following example:

A retailer wishes to send the data being activated to Experience Platform to their CRM system. The retailer has enabled Loyalty ID as a match key for their account to increase the match rate when activating audiences. However, the retailer's CRM system does not support Loyalty ID as an identity namespace, so they want to use the CRM ID match key instead when activating audiences to Experience Platform. The retailer can use the linked key option to activate audiences to Experience Platform using CRM ID instead of Loyalty ID.

>[!NOTE]
>
>For a profile to be activated, it must have values for both the original match key and the linked match key. For example, if Loyalty ID is linked to CRM ID, a profile must have values for both Loyalty ID and CRM ID to be activated. If either value is missing, the profile will not be activated.

To use a linked key, toggle on the **[!UICONTROL Linked key]** option next to the match key that you want to use in its place. The **[!UICONTROL Linked key]** section appears asking you to create the mapping.

![The Linked key option and section highlighted in the Create destination workflow.](/help/assets/destinations/adobe-experience-platform/linked-key.png)

Select the **[!UICONTROL Linked key]** that you want to use from the dropdown menu. Following the above example, the retailer would select **[!UICONTROL CRM ID]** as the linked key.

![The Linked key dropdown highlighted in the Create destination workflow.](/help/assets/destinations/adobe-experience-platform/select-linked-key.png)

Next, you want to specify the target namespace for the linked key if you have not already done so. If you've already selected the target namespace for the match key in the **[!UICONTROL Create activation mapping]** section, this will be autopopulated. If you have not yet selected a target namespace for the linked key, you can do so now.

Select the **[!UICONTROL Target namespaces]** field next to the linked key. The **[!UICONTROL Select source field]** dialog appears. Find the target namespace in the list, or search for a specific namespace. Select the target namespace that you want to use for the linked key, and then select **[!UICONTROL Select]**.

![The Select source field dialog.](/help/assets/destinations/adobe-experience-platform/select-linked-key-target-namespace.png)

The linked key is now configured. 

>[!NOTE]
>
>You can only used one linked key target namespace per activation mapping. For example, if you link Loyalty ID to CRM ID, toggling on the linked key option for another field will also link it to CRM ID.

When you've finished mapping all match keys, review your settings. The **[!UICONTROL Preview]** section provides a summary of your configuration.

![The Preview section in the Create destination workflow.](/help/assets/destinations/adobe-experience-platform/preview.png)

>[!IMPORTANT]
>
>Currently, each match key activates to Experience Platform as a separate audience. For example, if you have [!UICONTROL Hashed email] and [!UICONTROL Hashed phone] as match keys, two separate audiences will be created in Audience Portal when an audience is activated.

When you're satisfied with your configuration, select **[!UICONTROL Create destination]**. A confirmation message appears indicating that the destination was created successfully.

## Using Adobe Experience Platform as a destination

Once you've configured Adobe Experience Platform as a destination, you can begin [activating audiences](../collaborate/activate.md) to the platform through your projects. Currently, the activation process is a single-step process initiated by the advertiser. When the advertiser activates an audience, it is sent to the publisher's pre-configured destination (in this case, Adobe Experience Platform). The publisher does not need to take any additional steps to send the audience to the destination.

>[!IMPORTANT]
>
>You **must** configure Adobe Experience Platform as a destination *before* your collaborator activates an audience. If the destination is not configured, the audience will be sent to you and visible in the **[!UICONTROL Activate]** tab within a project, but will not be activated to Adobe Experience Platform. 

After the audience is activated, it will be available in [Audience Portal](#audience-portal) in Experience Platform with Real-Time CDP Collaboration as the origin.  These audiences can then be used in campaigns and customer engagement.

### Audience Portal {#audience-portal}

Now that you have configured Adobe Experience Platform as a destination, you can view the activated audiences in the Audience Portal. Audience Portal is a central hub within Adobe Experience Platform that allows you to view and manage your audiences. Audience portal now provides Real-Time CDP Collaboration as an origin when filtering your audiences. 

>[!IMPORTANT]
>
>You are responsible for applying any necessary data usage labels to the audiences you activate to Adobe Experience Platform. For more information, refer to the [data usage labels](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target="_blank"} guide.

![The Audience Portal with Real-Time CDP Collaboration as an origin in the filter options.](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

To learn more about Audience Portal, refer to the [Audience Portal overview](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"} guide.
