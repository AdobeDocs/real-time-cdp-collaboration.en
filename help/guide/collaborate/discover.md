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

After [creating a project](/help/guide/collaborate/manage-projects.md), you can compare your audiences against your collaborators. This helps you identify relevant audiences for campaigns and decide which ones to send to collaborators for activation.

>[!IMPORTANT]
>
>Any [data sketches](/help/guide/glossary.md#sketches) that are not updated or refreshed will be deleted after 7 days. When this happens, the figures displayed in the various overlap reports on this page go to zero and audience sharing becomes unavailable for these expired audiences. Data sketches are refreshed automatically for audiences with an [active refresh schedule](/help/guide/setup/onboard-audiences.md#schedule).

The match keys used to discover and compare audiences are set up [during the connection process](/help/guide/connect/establishing-connections.md#connection-settings). Match keys are use to calculate the overlap between your audiences, and can be toggled on and off. To edit the match keys, select the **[!UICONTROL Edit match keys]** option. 

![The Dicover tab workspace, showcasing the Audience insights.](/help/assets/collaborate/discover/discover-overview.png)

The **[!UICONTROL Edit match keys]** dialog opens, where you can toggle off the match keys that you don't want to use. Select **[!UICONTROL Save]** to save your changes.

![The Edit match keys dialog in the Discover workspace.](/help/assets/collaborate/discover/edit-match-keys.png)

## Prerequisites {#prerequisites}

To begin using the **[!UICONTROL Discover]** tab within your project, you should have:

* [Sourced audiences](/help/guide/setup/onboard-audiences.md) into your account
* [Connected](/help/guide/connect/establishing-connections.md) with a collaborator with the **Audience discovery** use case enabled
* [Created a project](/help/guide/collaborate/manage-projects.md) between you and a collaborator

Once these prerequisites are met, you can start exploring and comparing overlaps between you and your collaborator's audiences.

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
| **[!UICONTROL Audience index]** | A score that indicates how strongly one audience relates to another based on underlying audience counts & overlaps. To learn more about what the scores mean, read the [audience index score](#audience-index-score) section. Audience index scores are not available when comparing against all your collaborator's audiences. |
| **[!UICONTROL Identities breakdown by match key]** | The breakdown of identites for each match key chosen in the project, based on the select audiences for each collaborator. |

{style="table-layout:auto"}

>[!NOTE]
>
>The overlap percentage figure and audience index score may not be always available for all audiences. The visibility of the overlap percentage indicator depends on the setting that your collaborator chose for an audience in the [metadata visibility section](/help/guide/setup/onboard-audiences.md#metadata-visibility).

If your collaborator has not enabled either the audience index or the overlap percentage, the audience will not have any comparison data available. 

## Relevant audiences {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Relevant audiences"
>abstract="Based on overlap percentages, these audiences might be a good fit for your campaign. <br><br> The <b>identity count</b> is the collaborator's audience size. <br><br> <b>Overlapping identities</b> represents the overlap between the recommended audience and all your audiences. <br><br> The <b>Overlap %</b> represents the number of overlapping identities divided by the size of <i>all</i> your audiences."

The **[!UICONTROL Relevant audiences]** section in the **[!UICONTROL Discover]** tab provides a curated list of the top five audiences based on the overlap percentage between the your collaborator's audience, and all your audiences. This feature helps you quickly identify the audiences with the highest overlap, enabling you to target your campaigns more effectively. Switch between the relevant audiences using the page selectors in the top right of the section.

![The Discover workspace with the Relevant audiences section highlighted.](/help/assets/collaborate/discover/relevant-audiences.png)

>[!NOTE]
>
>The visibility of your collaborator's audiences depends on the setting that your collaborator chose for an audience in the [connection access section](/help/guide/setup/onboard-audiences.md#connection-access) and the [metadata visibility section](/help/guide/setup/onboard-audiences.md#metadata-visibility). If your collaborator has set all audiences to private, this section will not display any audiences.

The **[!UICONTROL Relevant audiences]** section displays the following information for each recommended audience:

| Metric | Description |
|---------|----------|
| **[!UICONTROL Identity count]** | The name unique IDs within the audience. |
| **[!UICONTROL Overlapping identities]** | The number of unique IDs that overlap between the recommended audience and all your audiences. |
| **[!UICONTROL Overlap %]** | The percentage of overlapping identities between the recommended audience and all your audiences. |
| **[!UICONTROL Audience index]** | A score that indicates how strongly one audience relates to another based on underlying audience counts & overlaps. To learn more about what the scores mean, read the [audience index score](#audience-index-score) section. |
| **[!UICONTROL Audience categories]** | The categories your collaborator has assigned to the audience. |
| **[!UICONTROL Match keys]** | The match keys your collaborator selected for the audience. |

{style="table-layout:auto"}

If audience index is enabled for any of your collaborator's audiences, relevant audiences will be based on the audience index score, and any audiences where the audience index has not been enabled will not be included. Relevant audiences based on the audience index score are sorted so the highest index score is displayed first. If audience index is not enabled for any of your collaborator's audiences, the relevant audiences will be based on the overlap percentage.

## Discover overlaps {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Discover overlaps with individual audiences"
>abstract="Get insights into overlaps between your audiences and your collaborator's audiences."

Discover overlaps to get insights into how your audiences compare against your collaborator's audiences. By default, this section compares all of your audiences against each of your collaborator's audiences. Use the pagination control at the bottom of the section to navigate through the available audiences.

![The Discover workspace with the Discover overlaps section highlighted.](/help/assets/collaborate/discover/discover-overlaps.png)

>[!NOTE]
>
>The visibility of your collaborator's audiences depends on the setting that your collaborator chose for an audience in the [connection access section](/help/guide/setup/onboard-audiences.md#connection-access) and the [metadata visibility section](/help/guide/setup/onboard-audiences.md#metadata-visibility). If your collaborator has set all audiences to private, this section will not display any audiences. 

If your collaborator has not enabled either the audience index or the overlap percentage, the audience will not be displayed. 

To change your audience selection, select **[!UICONTROL Change audience]**.

![The Discover workspace with the Change audience option highlighted.](/help/assets/collaborate/discover/change-audience.png)

The **[!UICONTROL Change audience]** dialog opens, where you can select a specific audience to compare against your collaborator's audiences. Select the desired audiences, or clear your selections to select all audiences, and then select **[!UICONTROL Save]**.

![The Change audience dialog in the Discover workspace.](/help/assets/collaborate/discover/change-audience-selection.png)

Once you've selected the desired audiences, the **[!UICONTROL Discover overlaps]** section displays the following information for each audience:

| Metric | Description |
|---------|----------|
| **[!UICONTROL Identity count]** | The number of unique IDs within the audience. |
| **[!UICONTROL Overlapping identities]** | The number of unique IDs that overlap between the recommended audience and all your audiences. |
| **[!UICONTROL Overlap %]** | The percentage of overlapping identities between the recommended audience and all your audiences. |
| **[!UICONTROL Audience index]** | A score that indicates how strongly one audience relates to another based on underlying audience counts & overlaps. To learn more about what the scores mean, read the [audience index score](#audience-index-score) section. |
| **[!UICONTROL Audience categories]** | The categories your collaborator has assigned to the audience. |
| **[!UICONTROL Match keys]** | The match keys your collaborator selected for the audience. |

{style="table-layout:auto"}

## Audience index score {#audience-index-score}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_audience_index_score"
>title="Audience index score"
>abstract="Audience index scores are a measurement to show how strongly one audience relates to another based on underlying audience counts and overlaps. The index score measures how much of your audience overlaps with a specific collaborator audience compared to what would be expected based on the collaborator's overall audience size, and then adjusts for the size of that collaborator audience within their baseline footprint. "

Audience index scores are a measurement to show how strongly one audience relates to another based on underlying audience counts and overlaps. This score helps you contextualize audience insights and identify high-potential audiences for prospecting and campaign targeting.

The index score is calculated based on the following formula:

![Audience index score formula where A is your audience, B is a collaborator's audience and Bf is the collaborator's baseline footprint.](/help/assets/collaborate/discover/index-score-formula.png)

The formula compares the overlap between your audience (A) and a collaborator's audience (B) against the ratio of that collaborator's audience within their overall baseline footprint (Bf). The baseline footprint is the total number of unique IDs in the collaborator's audience, which is used to normalize the index score for meaningful comparison.

In simpler terms, the index score measures how much of your audience overlaps with a specific collaborator audience compared to what would be expected based on the collaborator's overall audience size, and then adjusts for the size of that collaborator audience within their baseline footprint. 

To enable easy comparison across different audiences and campaigns, z-scores are calculated for each index score. A z-score indicates how far a given index is from the average score in the dataset. This highlights whether an audience relationship is stronger or weaker than average, helping you quickly identify your best targeting opportunities.

The z-scores are then represeted on a scale from very low to very high, as follows:

| Index Score | Z-score range | Description |
|---------|----------|-----------|
| Very low | z < -2 | The overlap is much less prevalent in the target audience compared to the baseline, indicating a very weak relationship. Customers using this audience are much less likely to reach their target audience. |
| Low | -2 ≤ z < -1 | The overlap is somewhat less prevalent in the target audience compared to the baseline, suggesting a weak relationship. Customers using this audience are less likely to reach their target audience. |
| Medium | -1 ≤ z ≤ 1 | The overlap is about as prevalent in the target audience as in the baseline, indicating a typical relationship. Customers using this audience have an average likelihood of reaching their target audience. |
| High | 1 < z ≤ 2 | The overlap is more prevalent in the target audience compared to the baseline, showing a strong relationship. Customers using this audience are more likely to reach their target audience. |
| Very high | z > 2 | The overlap is much more prevalent in the target audience compared to the baseline, reflecting a very strong relationship. Customers using this audience are much more likely to reach their target audience. |

## Next steps

After exploring and discovering the desired audiences, it's time to [activate](/help/guide/collaborate/activate.md) the audiences that should be used in the campaigns.
