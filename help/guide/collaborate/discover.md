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

>[!NOTE]
>
>This **[!UICONTROL Discover]** workspaces is not relevant for collaborations with advertising platforms. Currently, Amazon Marketing Cloud is the only available advertising platform in Real-Time CDP Collaboration. For more information about the [!DNL AMC] **[!UICONTROL Discover]** workspace, read the [Amazon Marketing Cloud](/help/guide/collaborate/advertising-platforms/amc.md) guide.

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
| **[!UICONTROL Audience index]** | A score that indicates how strongly one audience relates to another based on underlying audience counts & overlaps. To learn more about what the scores mean, read the [audience index score](#audience-index-score) section. Audience index scores are not available when comparing against your collaborator's baseline (all audiences). |
| **[!UICONTROL Identities breakdown by match key]** | The breakdown of identites for each match key chosen in the project, based on the select audiences for each collaborator. |

{style="table-layout:auto"}

>[!NOTE]
>
>The overlap percentage figure and audience index score may not be always available for all audiences. The visibility of the overlap percentage and audience index score depends on the setting that your collaborator chose for an audience in the [metadata visibility section](/help/guide/setup/onboard-audiences.md#metadata-visibility).

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
| **[!UICONTROL Identity count]** | The number of unique IDs within the audience. |
| **[!UICONTROL Overlapping identities]** | The number of unique IDs that overlap between the recommended audience and all your audiences. |
| **[!UICONTROL Overlap %]** | The percentage of overlapping identities between the recommended audience and all your audiences. |
| **[!UICONTROL Audience index]** | A score that indicates how strongly one audience relates to another based on underlying audience counts & overlaps. To learn more about what the scores mean, read the [audience index score](#audience-index-score) section. |
| **[!UICONTROL Audience categories]** | The categories your collaborator has assigned to the audience. |
| **[!UICONTROL Match keys]** | The match keys your collaborator selected for the audience. |

{style="table-layout:auto"}

If audience index score is enabled for any of your collaborator's audiences, relevant audiences will be based on the audience index score, and any audiences where the audience index has not been enabled will not be included. Relevant audiences based on the audience index score are sorted so the highest index score is displayed first. If audience index is not enabled for any of your collaborator's audiences, the relevant audiences will be based on the overlap percentage.

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
>abstract="Audience index scores are a nuanced metric that shows how strongly one audience relates to another based on underlying audience counts and overlaps. The raw index score is translated into relevance bands, which categorize the audience index scores from very low to very high. This allows you to quickly assess the strength of the relationship between your audience and your collaborator's audience."

Audience index scores are a nuanced metric that shows how strongly one audience relates to another based on underlying audience counts and overlaps. This helps you contextualize audience insights and identify high-potential audiences for prospecting and campaign targeting.

The index score is calculated using the following formula:

![The formula for calculating the index score.](/help/assets/collaborate/discover/index-score-formula.png)

Imagine a car manufacturer wants to run an advertising campaign with a large CTV publisher for a new SUV model. The car manufacturer has data on who currently owns a similar model and wants to use that to find additional prospects to convert them to customers. The car manufacturer looks at the CTV publisher's audiences to find a relevant audience that closely matches the current SUV owners.

![The car advertiser versus the CTV publisher audiences.](/help/assets/collaborate/discover/audience-index-score-example.png)

Index score calculations are made and can be used to determine the likely success of the campaign:

| CTV Publisher Audience | Formula | Index Score (i) | Interpretation |
|------------------------|-------------|----------------|----------------|
| Baseline (all audiences) | ((1.3M / 1.3M) / (50M / 50M)) * 100 | 100 | This serves as the baseline against which your collaborator's other audiences are compared to. |
| Binge Watchers | ((500k / 1.3M) / (20M / 50M)) * 100  | 96 | By targeting this audience, you are 4% less likely to reach SUV owners compared to the baseline. |
| Comedy Lovers | ((200k / 1.3M) / (6M / 50M)) * 100 | 128 | By targeting this audience, you are 28% more likely to reach SUV owners compared to the baseline. |
| Males 25-34 | ((700k / 1.3M) / (12M / 50M)) * 100 | 224 | By targeting this audience, you are 124% more likely to reach SUV owners compared to the baseline. |
| Tech Enthusiasts | ((500k / 1.3M) / (8M / 50M)) * 100 | 240 | By targeting this audience, you are 140% more likely to reach SUV owners compared to the baseline. |

{style="table-layout:auto"}

To better understand how the index scores will impact your campaign, relevance bands are provided alongside the scores.

### Relevance bands {#audience-index-relevance-bands}

To enable easy comparison across different audiences and campaigns, Collaboration translates the index scores into relevance bands (very low to very high). This allows you to quickly assess the strength of the relationship between your audience and your collaborator's audience.

| Index Score (i) | Relevance Band | Description |
|---------------|----------|-----------|
| i < 60 | Very low | The overlap is much less prevalent in the target audience compared to your audience, indicating a very weak relationship. Customers using this audience are much less likely to reach their target audience. |
| 60 < i < 80 | Low | The overlap is somewhat less prevalent in the target audience compared to your audience, suggesting a weak relationship. Customers using this audience are less likely to reach their target audience. |
| 80 < i < 120 | Medium | The overlap is about as prevalent in the target audience as in your audience, indicating a typical relationship. Customers using this audience have an average likelihood of reaching their target audience. |
| 120 < i < 140 | High | The overlap is more prevalent in the target audience compared to your audience, showing a strong relationship. Customers using this audience are more likely to reach their target audience. |
| i > 140 | Very high | The overlap is much more prevalent in the target audience compared to your audience, reflecting a very strong relationship. Customers using this audience are much more likely to reach their target audience. |

{style="table-layout:auto"}

Within the discover overlaps section, the audience index score will display the relevance band alongside the score. The score will be color-coded to indicate the relevance band, making it easy to identify the strength of the relationship at a glance. Very low and low relevance bands are displayed in orange, medium relevance bands in black, and high and very high relevance bands in green.

## Next steps

After exploring and discovering the desired audiences, it's time to [activate](/help/guide/collaborate/activate.md) the audiences that should be used in the campaigns.
