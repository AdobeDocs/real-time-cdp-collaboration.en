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
>Only **advertisers** can send audience to be activated for campaigns. 

Select the **+** symbol, or the **[!UICONTROL Activate audience]** option if no previous audiences have been sent for activation.

![The Activate workspace in a project with no audiences added.](/help/assets/collaborate/activate/activate-new-audiences.png)

The activate audiences workflow opens, where you can select the audiences that you want to send to your collaborator. Use the dropdown to select an audience, or search for a specific audience. To see more information about the audiences before making your select, select **[!UICONTROL Browse audiences]**

![The Audience activation workflow with the dropdown and Browse audiences options highlighted.](/help/assets/collaborate/activate/audience-activation.png)

In the **[!UICONTROL Browse audiences]**, you can see the **[!UICONTROL Identity count]**, **[!UICONTROL Overlapping identities]**, and **[!UICONTROL Overlap %]** for each audience.

<!-- REPLACE THIS TOMORROW AND THEN KEEP EDITING -->

![The Browse audiences dialog.](/help/assets/collaborate/activate/browse-audiences.png)

### Edit match keys and set targeting options

After selecting the desired audiences to share, you can now select other configuration options for the sharing activity.

![Edit match keys and target or suppress selector highlighted](/help/assets/collaborate/share/match-keys-and-targeting.png)

Select **[!UICONTROL Edit match keys]** to indicate which match keys should be used for the identities in the audience. These options are inherited from the settings that were selected when the connection between collaborators was initially set up. You can remove match keys that were selected at that point if they don't apply to this specific campaign, but you cannot add new match keys at this point. 

![Edit match keys.](/help/assets/collaborate/share/update-match-keys.png)

For each audience, select whether you would like the members of that audience to be targeted or suppressed in the campaign. Suppressed profiles will specifically not be part of the audience activated by the publisher.

### Set audience refresh frequency and interval

Finally, set the desired frequency and date range for the audience refresh. The currently supported modes for audience refresh are **[!UICONTROL Once]** and **[!UICONTROL Daily]**. 

When selecting **[!UICONTROL Once]**, the audience membership is not refreshed throughout the duration of a campaign. When selecting **[!UICONTROL Daily]**, the audience membership is refreshed once per day throughout the duration of a campaign.

![Frequency options highlighted.](/help/assets/collaborate/share/audience-refresh-frequency.png)

When satisfied with your selections, select **[!UICONTROL Share]** to complete the workflow. 

>[!SUCCESS]
>
>You can now see a new audience sharing activity in the **[!UICONTROL Sharing]** tab. If desired, you can go back and edit any of the selections you made. 

## View currently shared audiences

In the **[!UICONTROL Sharing]** tab, you can view the audiences that are currently being shared between the collaborators, grouped together in audience sharing activities. 

![Overview of the sharing tab.](/help/assets/collaborate/share/share-tab-overview.png)

<!--

The banner at the top of the page shows figures across all audience sharing activities. 

![The hero banner in the sharing tab.](/help/assets/collaborate/share/share-hero-banner.png)


|Metric | Description |
|---------|----------|
| **[!UICONTROL Shared audiences]** | Indicates the number of audiences shared between collaborators in this project, across all audience sharing modules. |
| **[!UICONTROL Estimated addressable reach]** | Indicates the approximate number of profiles that you can reach across all the audiences that are currently shared in the project. [TODO: ADD INFORMATION ABOUT HOW THIS IS CALCULATED] |
| **[!UICONTROL Target identities]** | The number of identities across all audiences shared in this project for which you selected to target the profiles. |
| **[!UICONTROL Suppress identities]** | The number of identities across all audiences shared in this project for which you selected to suppress the profiles and thereby not target them in campaigns. |

-->

Within each audience sharing activity, you can get information about each shared audience. 

|Metric | Description |
|---------|----------|
| **[!UICONTROL Identity count]** | Indicates the number of profiles across all identities tied to this audience, as per the latest identity count evaluation. These numbers are refreshed every 24-hours. |
| **[!UICONTROL Overlapping identities]** | Indicates the number of overlapping identities between the members of this audience and the total population of profiles across the collaborator's inventory. |
| **[!UICONTROL Match key breakdown]** | Shows the identity count for each identity used in the audience. For example, a total identity count of 500k users might consist of 400k users keyed off the hashed email identity and 100k users keyed off a mobile ID identity. Note that in the example described here, the same person might be present in the audience twice with their email and mobile ID identities. |
| **[!UICONTROL Objective]** | **[!UICONTROL Suppress]** or **[!UICONTROL Target]**. Indicates if the members of an audience should be targeted or excluded from campaigns. |

The page also provides controls for you to **[!UICONTROL Pause sharing]** and **[!UICONTROL Edit audiences]**.

## Edit audiences {#edit-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_share_edit_audiences_usecases"
>title="Target or suppress use case"
>abstract="<p>Select **Target** if you want the profiles in the audience to be shown ads in the campaign.</p> <p>Select **Suppress** if you want to exclude the profiles in the audience from the campaign messaging.</p>"

Select **[!UICONTROL Edit audiences]** to change which audiences are shared in an audience sharing module, as well as to change several configurations related to how audiences are being shared.

![View of the edit audiences modal](/help/assets/collaborate/share/edit-audiences-modal.png)

<!--

Search for audiences that you want to add to the sharing module. 

For each audience, you can select whether you'd like to target or suppress those profiles in campaigns. 

To remove an audience from the sharing module, select the trash can icon [TODO: add spectrum icon and folder].

Select how often you would like the audience membership to be refreshed and the date range within which you want the membership of the audience to be refreshed. 

TODO: are there any limitations for frequency in the M1 release?

-->

As a publisher, discover how to activate audiences using Adobe Real-Time CDP Collaboration. Currently, you can activate audiences to Amazon S3 locations. Additional activation channels are planned.

Only **publisher organizations** can activate audiences for campaigns. Advertiser organizations can [share audiences](/help/guide/collaborate/share.md) with publishers, who will activate these audiences in projects. Read more about the [end-to-end workflow](/help/guide/end-to-end-workflow.md) for advertisers and publishers.

## Prerequisites {#prerequisites}

As a publisher using Real-Time CDP Collaboration, you must first work with the Adobe enablement and engineering team to set up a connection to your desired Amazon S3 location. Once this is set up, you are able to activate, or export, audiences from Real-Time CDP Collaboration to your Amazon S3 location. Contact your Adobe representative to kick off this workflow.

Additionally, your connection must have the **Audience sharing and activation** use case enabled.

## Activation behavior {#activation-behavior}

After your advertiser connection shares an audience for activation, this audience immediately shows up in your **[!UICONTROL Activate]** view. The audience will be exported to your indicated location at the interval set by the advertiser in their audience share screen.

![Activate workflow to an Amazon S3 destination.](/help/assets/collaborate/activate/activate-to-amazon-s3.png)

## Next steps {#next-steps}

After activating data and running campaigns, work with the Adobe enablement and engineering team to upload measurement data and view the corresponding [measurement reports](/help/guide/collaborate/measure.md).
