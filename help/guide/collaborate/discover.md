---
title: Discover overlaps and compare audiences
description: Discover overlaps between your and your collaborators' audiences. Learn how to discover the best audiences for use in your campaigns.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
---
# Discover overlaps and compare audiences

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>The **[!UICONTROL Discover]** workspace is only available if the **Audience discovery** use case was enabled [during the connection proccess](../connect/establishing-connections.md#connection-settings). For more information about use cases, refer to the [manage projects](./manage-projects.md#project-use-cases) guide.

After [creating a project](/help/guide/collaborate/manage-projects.md), you can now compare your audiences and against your collaborators. This helps you identify relevant audiences for campaigns and decide which audiences to send to publishers for activation.

>[!IMPORTANT]
>
>Any [data sketches](/help/guide/glossary.md#sketches) that are not updated or refreshed will be deleted after 7 days. When this happens, the figures displayed in the various overlap reports on this page go to zero and audience sharing becomes unavailable for these expired audiences. Data sketches are refreshed automatically for audiences with an [active refresh schedule](/help/guide/setup/onboard-audiences.md#schedule).

The match keys used to discover and compare audiences are set up [during the connection process](/help/guide/connect/establishing-connections.md#connection-settings). Match keys are use to calculate the overlap between your audiences, and can toggled on and off. To edit the match keys, select the **[!UICONTROL Edit match keys]** option. This 

![The Dicover tab workspace, showcasing the Audience insights.](/help/assets/collaborate/discover/discover-overview.png)

The **[!UICONTROL Edit match keys]** dialog opens, where you can toggle off the match keys that you don't want to use. Select **[!UICONTROL Save]** to save your changes.

![The Edit match keys dialog in the Discover workspace.](/help/assets/collaborate/discover/edit-match-keys.png)

## Prerequisites {#prerequisites}

To begin using the **[!UICONTROL Discover]** tab within your project, you should have:

* [Imported audiences](/help/guide/setup/onboard-audiences.md) into your organization
* [Connected](/help/guide/connect/establishing-connections.md) with a collaborator with the **Audience discovery** use case enabled
* [Created a project](/help/guide/collaborate/manage-projects.md) between you and a collaborator

Once these prerequisites are met, you can start exploring and comparing the overlap between you and your collaborator's audiences.

## Compare audiences {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="Compare audiences"
>abstract="Discover overlaps between your and your collaborator's audiences. You can adjust the settings in the dropdown selector to discover overlaps between one or more of your audiences against one or more of your collaborator's audiences."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="Your identity count"
>abstract="The number of unique IDs within your selected audience, based on the match keys that you and your collaborator agreed on for the project."
>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="Collaborator identity count"
>abstract="The number of unique IDs within your collaborator's audience, based on the match keys that you and your collaborator agreed on for the project."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="Overlapping identities count"
>abstract="The number of unique IDs that are present in both your and your collaborator's audiences, based upon the match keys that you and your collaborator agreed on for the project."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="Overlapping identities percentage"
>abstract="The percentage of overlapping identities between you and your collaborator's selected audience."

Use the compare audiences section to get rich information about the overlap between your and your collaborator's audiences. To change the audience selection, use the dropdown selector at the top of the **[!UICONTROL Compare audiences]** section. You can select one or all of your audiences and one or all of your collaborator's audiences to compare against each other. 

![The Discover workspace with the audience selector highlighted in the Compare audiences section.](/help/assets/collaborate/discover/compare-audiences-selector.png)

In the compare audiences section, you can see the following metrics, which are based on the match keys that you and your collaborator agreed on for the project:

| Metric | Description |
|---------|----------|
| **[!UICONTROL Identity count]** (yours) | The number of unique IDs within your selected audience(s). |
| **[!UICONTROL Identity count]** (your collaborator) | The number of unique IDs within your collaborator's audience(s). |
| **[!UICONTROL Overlapping identities]** | The number of unique IDs that are present in both your and your collaborator's audiences. |
| **[!UICONTROL Overlap %]** | The percentage of profiles overlapping between your and your collaborator's selected audience. |
| **[!UICONTROL Identities breakdown by match key]** | The breakdown of identites for each match key chosen in the project, based on the select audiences for each collaborator. |

{style="table-layout:auto"}

>[!TIP]
>
>The overlap percentage figure may not be always available for all audiences. The visibility of the overlap percentage indicator depends on the setting that your collaborator chose for an audience in the [metadata visibility section](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Relevant audiences {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Relevant audiences"
>abstract="Based on overlap percentages, these publisher audiences might be a good fit for your campaign. <br><br> The <b>identity count</b> is the publisher's audience size. <br><br> <b>Overlapping identities</b> represents the overlap between the recommended publisher audience and all advertiser audiences. <br><br> The <b>Overlap %</b> represents the number of overlapping identities divided by the size of <i>all</i> advertiser audiences."

The **[!UICONTROL Relevant audiences]** section in the **[!UICONTROL Discover]** tab provides a curated list of the top five audiences based on the overlap percentage between the your collaborator's recommended audience, and all your audiences. This feature helps you quickly identify the audiences with the highest overlap with your current data, enabling you to target your campaigns more effectively. Switch between the recommended audiences using the page selectors in the top right of the section.

![The Discover workspace with the Relevant audiences section highlighted.](/help/assets/collaborate/discover/relevant-audiences.png)

>[!NOTE]
>
>The visibility of your collaborator's audiences depends on the setting that your collaborator chose for an audience in the [metadata visibility section](/help/guide/setup/onboard-audiences.md#metadata-visibility). If your collaborator has set all audiences to private, this section will not display any audiences.

The **[!UICONTROL Relevant audiences]** section displays the following information for each recommended audience:

| Metric | Description |
|---------|----------|
| **[!UICONTROL Identity count]** | The name unique IDs within the audience. |
| **[!UICONTROL Overlapping identities]** | The number of unique IDs that overlap between the recommended audience and all your audiences. |
| **[!UICONTROL Overlap %]** | The percentage of overlapping identities between the recommended audience and all your audiences. |
| **[!UICONTROL Audience categories]** | The categories your collaborator has assigned to the audience. |
| **[!UICONTROL Match keys]** | The match keys your collaborator selected for the audience. |

{style="table-layout:auto"}

>[!NOTE]
>
>The visibility of your collaborator's audiences depends on the setting that your collaborator chose for an audience in the [metadata visibility section](/help/guide/setup/onboard-audiences.md#metadata-visibility). If your collaborator has set all audiences to private, this section will not display any audiences.

## Discover overlaps {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Discover overlaps with individual audiences"
>abstract="Get insights into overlaps between your audiences and your collaborator's audiences."

Discover overlaps to get insights into how your audiences compare against your collaborator's audiences. By default, this section compares all of your audiences against each of your collaborator's audiences. Use the pagination control at the bottom of the section to navigate through the available audiences.

![The Discover workspace with the Discover overlaps section highlighted.](/help/assets/collaborate/discover/discover-overlaps.png)

>[!NOTE]
>
>The visibility of your collaborator's audiences depends on the setting that your collaborator chose for an audience in the [metadata visibility section](/help/guide/setup/onboard-audiences.md#metadata-visibility). If your collaborator has set all audiences to private, this section will not display any audiences.

To change your audience selection, select **[!UICONTROL Change audience]**.

![The Discover workspace with the Change audience option highlighted.](/help/assets/collaborate/discover/change-audience.png)

The **[!UICONTROL Change audience]** dialog opens, where you can a specific audience to compare against your collaborator's audiences. Select the desired audiences, or clear your selections to select all audiences, and then select **[!UICONTROL Save]**.

![The Change audience dialog in the Discover workspace.](/help/assets/collaborate/discover/change-audience-selection.png)

Once you've selected the desired audiences, the **[!UICONTROL Discover overlaps]** section displays the following information for each audience:

| Metric | Description |
|---------|----------|
| **[!UICONTROL Identity count]** | The name unique IDs within the audience. |
| **[!UICONTROL Overlapping identities]** | The number of unique IDs that overlap between the recommended audience and all your audiences. |
| **[!UICONTROL Overlap %]** | The percentage of overlapping identities between the recommended audience and all your audiences. |
| **[!UICONTROL Audience categories]** | The categories your collaborator has assigned to the audience. |
| **[!UICONTROL Match keys]** | The match keys your collaborator selected for the audience. |

{style="table-layout:auto"}

## Next steps

After exploring and discovering the desired audiences, it's time to [activate](/help/guide/collaborate/activate.md) the audiences that should be used in the campaigns.
