---
title: Share audiences
description: Learn how to share audiences with your collaborators for advertising campaigns.
audience: admin, publisher, advertiser
badgealpha: label="Alpha" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
---

# Share audiences

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently an alpha product, available to select customers. Contact your Adobe representative to learn more.
>
>You are at all times bound by the terms and conditions in the non-disclosure agreement(s) you have executed. Contact your Adobe representative if you have any questions.

Learn how to share audiences with your publishers so they can run campaigns. Ensure that you've already run overlap reports in the [Discover tab](/help/guide/collaborate/discover.md) to identify the best audiences for sharing.

## Share new audiences

To start sharing audiences, navigate to the **[!UICONTROL Share]** tab in your project workspace. In this tab, you can review and manage shared audiences.

![Default view with no audiences shared.](/help/assets/collaborate/share/share-new-audiences.png)

Select the **Plus symbol (+)** to begin the audience sharing process. A new panel appears, allowing you to select the audiences you want to share with your collaborators. 

![Share new audiences workflow.](/help/assets/collaborate/share/share-audiences-workflow.png)

### Select audiences to share

In the audience selection window, you can search for specific audiences to share by entering the audience name in the search bar. Select **[!UICONTROL Browse audiences]** and use the available sorting options to find the exact audiences you need.

![Browse audiences view with audiences selected.](/help/assets/collaborate/share/browse-audiences-view.png)

### Edit match kays and set targeting options

After selecting the desired audiences to share, you can now select other configuration options for the sharing activity.

![Edit match keys and target or suppress selector highlighted](/help/assets/collaborate/share/match-keys-and-targeting.png)

Select **[!UICONTROL Edit match keys]** to indicate which match keys should be used for the identities in the audience. These options are inherited from the settings that were selected when the connection between collaborators was initially set up. You can remove match keys that were selected at that point if they don't apply to this specific campaign, but you cannot add new match keys at this point. 

![Edit match keys.](/help/assets/collaborate/share/update-match-keys.png)

For each audience, select whether you would like the members of that audience to be targeted or suppressed in the campaign. Suppressed audiences will specifically not be part of the activated audience.

### Set audience refresh frequency and interval

Finally, set the desired frequency and date range for the audience refresh. The currently supported modes for audience refresh are **[!UICONTROL Once]** and **[!UICONTROL Daily]**. 

When selecting **[!UICONTROL Once]**, the audience membership is not refreshed throughout the duration of a campaign. When selecting **[!UICONTROL Daily]**, the audience membership is refreshed once per day throughout the duration of a campaign.

![Frequency options highlighted.](/help/assets/collaborate/share/audience-refresh-frequency.png)

When satisfied with your selections, select **[!UICONTROL Share]** to complete the workflow. 

>[!SUCCESS]
>
>You can now see a new audience sharing activity in the **[!UICONTROL Sharing]** tab. If desired, you can go back and edit any of the selections you made. 

## View currently shared audiences

In the Sharing tab, you can view the audiences that are currently being shared between the collaborators, grouped together in audience sharing activities. 

![Overview of the sharing tab.](/help/assets/collaborate/share/share-tab-overview.png)

The banner at the top of the page shows figures across all audience sharing modules. Within each audience sharing activity, you can get information about each shared audience. 

|Metric | Description |
|---------|----------|
| **[!UICONTROL Identity count]** | Indicates the number of profiles across all identities tied to this audience, as per the latest identity count evaluation. These numbers are refreshed every 24-hours. |
| **[!UICONTROL Overlapping identities]** | Indicates the number of overlapping identities between the members of this audience and the total population of profiles across the collaborator's inventory. |
| **[!UICONTROL Match key breakdown]** | Shows the identity count for each identity used in the audience. For example, a total identity count of 500k users might consist of 400k users keyed off the hashed email identity and 100k users keyed off a mobile ID identity. Note that the same person might be present in the audience twice in this case with their email and mobile ID identities. |
| **[!UICONTROL Objective]** | **[!UICONTROL Suppress]** or **[!UICONTROL Target]**. Indicates if the members of an audience should be targeted or excluded from campaigns. |

The page also provides controls for you to **[!UICONTROL Pause sharing]** and **[!UICONTROL Edit audiences]**.

![The hero banner in the sharing tab.](/help/assets/collaborate/share/share-hero-banner.png)


|Metric | Description |
|---------|----------|
| **[!UICONTROL Shared audiences]** | Indicates the number of audiences shared between collaborators in this project, across all audience sharing modules. |
| **[!UICONTROL Estimated addressable reach]** | Indicates the approximate number of profiles that you can reach across all the audiences that are currently shared in the project. [TODO: ADD INFORMATION ABOUT HOW THIS IS CALCULATED] |
| **[!UICONTROL Target identities]** | The number of identities across all audiences shared in this project for which you selected to target the profiles. |
| **[!UICONTROL Suppress identities]** | The number of identities across all audiences shared in this project for which you selected to suppress the profiles and thereby not target them in campaigns. |

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


