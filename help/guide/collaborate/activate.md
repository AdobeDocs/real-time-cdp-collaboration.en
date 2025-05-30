---
title: Activate audiences
description: As a publisher, learn how to activate in campaigns audiences shared with you by your collaborator. 
audience: admin, publisher
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
---
# Activate audiences

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>The **[!UICONTROL Activate]** workspace is only available if the **Audience activation** use case was enabled [during the connection process](../connect/establishing-connections.md#connection-settings). For more information about use cases, refer to the [manage projects](./manage-projects.md#project-use-cases) guide.

Audience activation allows you activate audiences in campaigns. The activiation process is a collaboration between advertisers and publishers. Advertisers send audiences to publishers, who then activate these audiences in campaigns.

## Activate new audiences

To start activating audiences, navigate to the **[!UICONTROL Activate]** tab in your project workspace. 

>[!NOTE]
>
>Only **advertisers** can activate audiences in a project. 

Select the **+** symbol, or the **[!UICONTROL Activate audience]** option if no previous audiences have been sent for activation.

![The Activate workspace in a project with no audiences added.](/help/assets/collaborate/activate/activate-new-audiences.png)

The activate audiences workflow opens, where you can select the audience that you want to send to your collaborator. Use the dropdown to select an audience, or search for a specific audience. To see more information about the audiences before making your select, select **[!UICONTROL Browse audiences]**

![The Audience activation workflow with the dropdown and Browse audiences options highlighted.](/help/assets/collaborate/activate/audience-activation.png)

In the **[!UICONTROL Browse audiences]**, you can see the **[!UICONTROL Identity count]**, **[!UICONTROL Overlapping identities]**, and **[!UICONTROL Overlap %]** for each audience.

![The Browse audiences dialog showing the available audiences.](/help/assets/collaborate/activate/browse-audiences.png)

Select the audience that you want to activate in campaigns, and then select **[!UICONTROL Save]**. The audience is now, displayed and you can see the **[!UICONTROL Identity count]**, **[!UICONTROL Overlapping identities]**, and **[!UICONTROL Overlap %]** for the selected audience.

![The Audience activation workflow with the selected audience displayed.](/help/assets/collaborate/activate/selected-audience.png)

### Edit match keys

Next, you can edit the audience's match keys by selecting **[!UICONTROL Edit match keys]** within the select audience. These options are inherited from your match key selections when the connection between collaborators was initially set up. You can remove match keys that were selected if they don't apply to a specific campaign, but you cannot add new match keys.

![The Audience activation workflow with the Edit match keys option highlighted.](/help/assets/collaborate/activate/edit-match-keys.png)

The **[!UICONTROL Edit match keys]** dialog opens, where you can toggle off the match keys that you don't want to use. Select **[!UICONTROL Save]** to save your changes.

>[!NOTE]
>
>At least one match key must be selected. In the current release, the only match keys available is **[!UICONTROL Hashed email]**, so you cannot remove this match key.

![The Edit match keys dialog in the Audiece activation workflow.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Set audience refresh frequency and interval

Finally, set the desired frequency and date range for the audience to refresh. In the current release, the only supported frequency option is **[!UICONTROL Once]**. The **[!UICONTROL Once]** frequency means the audiences are activated a single time and are not refreshed throughout the duration of a campaign. The **[!UICONTROL Date]** option is auto-populated with the current date.

![The Audience activation workflow with the Frequency section highlighted.](/help/assets/collaborate/activate/audience-frequency.png)

When satisfied with your selections, select **[!UICONTROL Activate]** to complete the workflow. The audience is now activated and you can view it in the **[!UICONTROL Activate]** tab. It will also be available to your collaborator in their **[!UICONTROL Activate]** tab, where they can use it in campaigns.

You can edit the audience's name edit icon (![Pencil icon.](/help/assets/icons/edit.png)) or deactivate the audience by selecting **[!UICONTROL Deactivate]**.

![The Activate tab with the activated audience displayed and the Edit and Deactivate options highlighted.](/help/assets/collaborate/activate/activated-audience.png)

## View activated audiences

In the **[!UICONTROL Activate]** tab, both publishers and advertisers can view the audiences that are currently being activated between you and your collaborator.

![Overview of the Activate tab, showcasing an activated audience.](/help/assets/collaborate/activate/activate-overview.png)

Within each activated audience, you can see the following metrics:

| Metric | Description |
|---------|----------|
| **[!UICONTROL Activated identities]** | Indicates the number of activated identities within the audience. |
| **[!UICONTROL Overlapping identities]** | Indicates the number of overlapping identities between this audience and the total population of profiles across the collaborator's inventory. |
| **[!UICONTROL Match key breakdown ]** | Shows the identity count for each identity used in the audience. For example, a total identity count of 500k users might consist of 400k users keyed off the hashed email identity and 100k users keyed off a mobile ID identity. Note that in the example described here, the same person might be present in the audience twice with their email and mobile ID identities. |

## Next steps {#next-steps}

After activating data and running campaigns, work with the Adobe enablement and engineering team to upload measurement data and view the corresponding [measurement reports](/help/guide/collaborate/measure.md).
