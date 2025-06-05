---
title: Configure Adobe Experience Platform as a destination
description: Learn how to configure and manage Adobe Experience Platform as a destination in Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
---
# Configure Adobe Experience Platform as a destination

{{limited-availability-release-note}}

Configure this destination to activate audiences from your project to Adobe Experience Platform. Activating audiences to Adobe Experience Platform allows you to leverage the platform's capabilities for audience segmentation, analysis, and activation across various marketing channels. To learn more about Adobe Experience Platform, refer to the [Experience Platform overview](https://experienceleague.adobe.com/en/docs/experience-platform/landing/home){target="_blank"}.

>[!NOTE]
>
>Currently, only publishers can configure destinations in Real-Time CDP Collaboration.

## Configure destination {#configure-destination}

To configure Adobe Experience Platform as a destination, navigate to **[!UICONTROL Setup]** and then select the **[!UICONTROL Destinations]** tab. Select **[!UICONTROL Set up]** for Adobe Experience Platform.

![The My destinations workspace with the Set up option highlighted for the Adobe Experience Platform destination.](/help/assets/destinations/adobe-experience-platform/setup-aep.png)

The **[!UICONTROL Create destination]** workflow appears. 

![The Create destination workflow for Adobe Experience Platform.](/help/assets/destinations/adobe-experience-platform/create-destination.png)

### Configure sandbox {#configure-sandbox}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_audience_expiration"
>title="Audience expiration"
>abstract="The time period after which the audience will no longer be available in Adobe Experience Platform. The default expiration is 30 days, but you can set it to any value between 1 and 30 days."

First, you must select the sandbox where your audience data will be sent. 

>![IMPORTANT]
>
>You can only select a sandbox that your user has access to. By default, all Real-Time CDP Collaboration users have access to the **Prod** sandbox. To gain access to additional sandboxes, an administrator must add additional sandboxes to a role assigned to your user. For more information about managing roles, refer to the [manage roles](../permissions/manage-roles.md) guide.

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

Next, you must create an activation mapping to define how the audience data will be sent to Adobe Experience Platform. You can map each [match key](../setup/onboard-organization.md#set-up-match-keys) you selected while creating your organization to an target namespace. The target namespaces specify which [identity namespace](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"} the match key will be mapped to in Adobe Experience Platform.

>![IMPORTANT]
>
>Hashed match keys must be mapped to a target namespace that supports hashed values. For example, the **[!UICONTROL Hashed email]** match key must be mapped to the **[!UICONTROL Email(SHA256, lowercased)]** identity namespace in Adobe Experience Platform. You cannot map the **[!UICONTROL Hashed email]** match key to the **[!UICONTROL Email]** identity namespace, as this namespace does not support hashed values.

Select the **[!UICONTROL Target namespaces]** field next to each match key. The **[!UICONTROL Select source field]** dialog appears. Find the target namespace in the list, or search for a specific namespace. Select the target namespace that you want to use for the match key, and then select **[!UICONTROL Select]**.

![The Select source field dialog with the Select option highlighted..](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

When you've finished mapping all match keys, review your settings and then select **[!UICONTROL Create]** to finish creating your destination.

## Using Adobe Experience Platform as a destination

Once you've configured Adobe Experience Platform as a destination, you can begin [activating audiences](../collaborate/activate.md) to the platform through your projects. Currently, the activation process is a single-step process initiated by the advertiser. When the advertiser activates an audience, it is sent to the publisher's pre-configured destination (in this case, Adobe Experience Platform). The publisher does not need to take any additional steps to send the audience to the destination.

>[!IMPORTANT]
>
>You **must** configure Adobe Experience Platform as a destination *before* your collaborator activates an audience. If the destination is not configured, the audience will be sent to you and visible in the **[!UICONTROL Activate]** tab within a project, but will not be activated to Adobe Experience Platform. 

After the audience is activated, it will be available in Adobe Experience Platform for use in campaigns and customer engagement.

### Audience Portal {#audience-portal}

Now that you have configured Adobe Experience Platform as a destination, you can view the activated audiences in the Audience Portal. Audience Portal is a central hub within Adobe Experience Platform that allows you to view and manage your audiences. Audience portal now provides Real-Time CDP Collaboration as an origin when filtering your audiences. 

![The Audience Portal with Real-Time CDP Collaboration as an origin in the filter options.](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

To learn more about Audience Portal, refer to the [Audience Portal overview](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"} guide.
