---
title: Activate audiences
description: Learn how to activate audiences in Adobe Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
---
# Activate audiences

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>The **[!UICONTROL Activate]** workspace is only available if the **Audience activation** use case was enabled [during the connection process](../connect/establishing-connections.md#connection-settings). For more information about use cases, refer to the [manage projects](./manage-projects.md#project-use-cases) guide.

Audience activation allows you activate audiences for use in campaigns. Activation can be done by either collaborator depending on the audience activation settings [configured in the connection](/help/guide/connect/establishing-connections.md#configure-connection-settings). After you [discover the best audiences for your campaign](./discover.md), activate the audiences to make them available for use. When you activate an audience, it is sent to your collaborator's pre-configured destination, such as Adobe Experience Platform, where it becomes available for use in campaigns. For more information about setting up destinations, refer to the [destinations overview](../destinations/overview.md) guide.

## Activate new audiences {#activate-new-audiences}

To start activating audiences, navigate to the **[!UICONTROL Activate]** tab in your project workspace. 

>[!IMPORTANT]
>
>**Before** you can activate an audience, your collaborator **must** configure a destination. When you activate an audience, it is automatically sent to your collaborator's configured destination. If no destination is set up, you cannot activate audiences.
>
>![The Activate workspace when the collaborator has no destination configured.](/help/assets/collaborate/activate/no-destination-configured.png)

Select the add icon (![Add icon.](/help/assets/icons/plus.png)), or the **[!UICONTROL Activate audience]** option if no previous audiences have been sent for activation.

![The Activate workspace in a project with no audiences added.](/help/assets/collaborate/activate/activate-new-audiences.png)

The activate audiences workflow opens, where you can select the audience that you want to send to your collaborator. Use the dropdown to select an audience, or search for a specific audience. To see more information about the audiences before making your select, select **[!UICONTROL Browse audiences]**

![The Audience activation workflow with the dropdown and Browse audiences options highlighted.](/help/assets/collaborate/activate/audience-activation.png)

In the **[!UICONTROL Browse audiences]**, you can see the **[!UICONTROL Identity count]**, **[!UICONTROL Overlapping identities]**, and **[!UICONTROL Overlap %]** for each audience.

![The Browse audiences dialog showing the available audiences.](/help/assets/collaborate/activate/browse-audiences.png)

>[!IMPORTANT]
>
>When activating audiences where multiple match keys are used, if one (or more) match key has no overlaps, no audience counts, or falls below threshold, activation will fail. Ensure your audiences have sufficient overlap and meet the minimum threshold of 1000 IDs across all match keys before activating.

Select the audience that you want to activate in campaigns, and then select **[!UICONTROL Save]**. The audience is now, displayed and you can see the **[!UICONTROL Identity count]**, **[!UICONTROL Overlapping identities]**, and **[!UICONTROL Overlap %]** for the selected audience.

![The Audience activation workflow with the selected audience displayed.](/help/assets/collaborate/activate/audience-selected.png)

### Edit match keys {#edit-match-keys}

Next, you can edit the audience's match keys by selecting **[!UICONTROL Edit match keys]** within the select audience. These options are inherited from your match key selections when the connection between collaborators was initially set up. You can remove match keys that were selected if they don't apply to a specific campaign, but you cannot add new match keys.

![The Audience activation workflow with the Edit match keys option highlighted.](/help/assets/collaborate/activate/edit-match-keys.png)

The **[!UICONTROL Edit match keys]** dialog opens, where you can toggle off the match keys that you don't want to use. Select **[!UICONTROL Save]** to save your changes.

>[!NOTE]
>
>At least one match key must be selected. In the current release, the only match keys available is **[!UICONTROL Hashed email]**, so you cannot remove this match key.

![The Edit match keys dialog in the Audiece activation workflow.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Set audience refresh frequency {#set-audience-refresh-frequency}

Finally, set the desired frequency and date range for the audience to refresh. In the current release, the only supported frequency option is **[!UICONTROL Once]**. The **[!UICONTROL Once]** frequency means the audiences are activated a single time and are not refreshed. The **[!UICONTROL Date]** option is auto-populated with the current date.

![The Audience activation workflow with the Frequency section highlighted.](/help/assets/collaborate/activate/audience-frequency.png)

When satisfied with your selections, select **[!UICONTROL Activate]** to complete the workflow.

## Activate dashboard {#activate-dashboard}

In the **[!UICONTROL Activate]** tab, you can view all audiences sent to your collaborator, as well as all audiences your collaborator has activated to your destination.

![The Activate dashboard showing the Sent audiences and Activated audiences sections.](/help/assets/collaborate/activate/activate-dashboard.png)

## View sent audiences {#view-sent-audiences}

In the **[!UICONTROL Sent audiences to]** collaborator section, all the audiences you've sent will be listed. Currently, audiences are automatically sent to your collaborator's configured destination after you've sent them. In your collaborator's view, these audiences are displayed in the **[!UICONTROL Activated audiences]** section.

Within each sent audience, you can see the following metrics:

| Metric | Description |
|---------|----------|
| **[!UICONTROL Name]** | The name of the audience. |
| **[!UICONTROL Status]** | The status of the sent audience. |
| **[!UICONTROL Identity count]** | The number of identities in the audience. |
| **[!UICONTROL Overlapping identities]** | The number of overlapping identities between this audience and the total population of profiles across the collaborator's inventory. |
| **[!UICONTROL Created]** | The date when the audience was initially sent. |
| **[!UICONTROL Last sent]** | The date when the audience was last sent to your collaborator. |
| **[!UICONTROL Match keys]** | Indicates the match key used for the audience. |

## View activated audiences {#view-activated-audiences}

In the **[!UICONTROL Activated audiences]** section, you can see all the audiences that have been activated to your destination.

Within each activated audience, you can see the following metrics:

| Metric | Description |
|---------|----------|
| **[!UICONTROL Name]** | The name of the audience. |
| **[!UICONTROL Status]** | The status of the activated audience. |
| **[!UICONTROL Identity count]** | The number of identities that were activated, based off the overlapping identities when your collaborator sent the audience. |
| **[!UICONTROL Created]** | The date when the audience was activated. |
| **[!UICONTROL Last refreshed]** | The date when the audience was last refreshed, based on the refresh schedule chosen during activation. |
| **[!UICONTROL Destination]** | The destination where the audience was activated to. |
| **[!UICONTROL Match keys]** | Indicates the match key used for the audience. |

## Delete sent audiences {#delete-sent-audiences}

You can delete sent audiences that you no longer want to activate. When you delete a sent audience, it is removed from the **[!UICONTROL Sent audiences to]** section, and it will no longer be activated to your collaborator's destination.

To delete a sent audience, select the **[!UICONTROL Delete]** icon (![Delete icon.](/help/assets/icons/delete.png)) next to the audience in the **[!UICONTROL Sent audiences to]** section.

![The Delete option in the Sent audiences to section.](/help/assets/collaborate/activate/delete-sent-audiences.png)

A confirmation dialog opens, asking you to confirm the deletion. Select **[!UICONTROL Delete]** to confirm.

![The Delete confirmation dialog.](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

## Next steps {#next-steps}

After activating audiences and running campaigns, work with the Adobe enablement and engineering team to upload measurement data and view the corresponding [measurement reports](/help/guide/collaborate/measure.md).
