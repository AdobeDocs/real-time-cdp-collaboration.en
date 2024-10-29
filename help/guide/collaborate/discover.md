---
title: Discover overlaps
description: Discover overlaps between your and your collaborators' audiences
audience: admin, publisher, advertiser
badgealpha: label="Alpha" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
---

# Discover overlaps and compare audiences

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently an alpha product, available to select customers. Contact your Adobe representative to learn more.
>
>You are at all times bound by the terms and conditions in the non-disclosure agreement(s) you have executed. Contact your Adobe representative if you have any questions.

After [creating a project](/help/guide/collaborate/manage-projects.md) within a collaboration space between an advertiser and a publisher, you can now compare your audiences against your collaborator's audiences. Thereby, you can discover overlaps between audiences and get insights broken down by match keys or identities. This helps advertisers decide which audiences to share with publishers for activation, depending on the desired use case.

![Discover overlaps](/help/assets/collaborate/discover-overlaps/discover-overlaps.png)

The match keys are set when you connect with a publisher. To change the overlap percentages indicated in preparation for running campaigns, you can remove match keys but you cannot add new match keys at this point. To do that, head to the [connection settings](/help/guide/connect-publisher-advertiser/establishing-connections.md#connection-settings) between the collaborators.

![Edit match keys screen](/help/assets/collaborate/discover-overlaps/edit-match-keys.png)

## Prerequisites {#prerequisites}

To fully utilize the functionality in the **[!UICONTROL Discover]** tab of the **[!UICONTROL Collaborate]** workflow, you have already:

* [Imported audiences](/help/guide/setup/onboard-audiences.md)
* [Connected](/help/guide/connect-publisher-advertiser/establishing-connections.md) with a desired advertiser or publisher
* [Created a project](/help/guide/collaborate/manage-projects.md) between you and a collaborator

Once the prerequisites noted above are met, you can start exploring and comparing the overlap between your and your collaborator's audiences.

## Compare audiences {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="Compare audiences"
>abstract="Discover overlaps between your and your collaborator's audiences. You can adjust the settings in the dropdown selector to discover overlaps between one or more of your audiences against one or more of your collaborator's audiences."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="Your identity count"
>abstract="The number of profiles with that selected identity that are part of your selected audience"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="Collaborator identity count"
>abstract="The number of profiles with that selected identity that are part of your collaborator's selected audience"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="Overlapping identities count"
>abstract="The number of profiles with that selected identity that are present both in your and your collaborator's audience"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="Overlapping identities percentage"
>abstract="The percentage of profiles overlapping between your and your collaborator's selected audience."

Use the compare audiences card to get rich information about the overlap between your and your collaborator's audiences. You can select to compare any of the following combinations:

* One of your audiences against one of your collaborator's audiences
* One of your audiences against all of your collaborator's audiences
* All your audiences against all of your collaborator's audiences
* All your audiences against one of your collaborator's audiences

The information displayed relates to:

|Metric | Description |
|---------|----------|
| Identity count (yours) | The number of profiles with a selected identity that are part of your selected audience. |
| Identity count (your collaborator) | The number of profiles with a selected identity that are part of your collaborator's selected audience. |
| Overlapping identities | The number of profiles with a selected identity that are present both in your and your collaborator's audience |
| Overlap percentage | The percentage of profiles overlapping between your and your collaborator's selected audience. |
| Identities breakdown by match key | Based on the match keys you and your collaborator agreed on for the project, view the composition of the identities in the overlap calculations by individual match keys. |

{style="table-layout:auto"}

## Recommended audiences {#recommended-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_recommended_audiences"
>title="Recommended audiences"
>abstract="Based on overlap percentages and other factors, these publisher audiences are recommended for your campaign. <br> The <b>identity count</b> is the publisher's audience size. <b>Overlapping identities</b> represents the overlap between the recommended publisher audience and all advertiser audiences. The <b>Overlap %</b> represents the overlapping identities number divided by the size of <i>all</i> advertiser audiences."

The **[!UICONTROL Recommended audiences]** view in the **[!UICONTROL Discover]** module provides a curated list of the top five recommended audiences based on overlap percentage. This feature helps you quickly identify the audiences with the highest overlap with your current data, enabling you to target your campaigns more effectively.

<!--

For extensive information about the overlapping identities count and percentages, read the [overlap calculations reference documentation](/help/guide/reference/overlap-calculations.md).

-->

![Recommended audiences view](/help/assets/collaborate/discover-overlaps/recommended-audiences-highlighted.png)

## Discover overlaps {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Discover overlaps with audience"
>abstract="Information related to this audience and its overlaps with the collaborator's universe of identities."

![Discover overlaps with different audiences view](/help/assets/collaborate/discover-overlaps/discover-overlaps-cards-view.png)

Get extensive information about any of your collaborator's audiences and view overlap information comparing these audiences against either your entire population count across all your audiences, or against specific audiences of yours.

## Next steps

After exploring and discovering the desired audiences, it's time to [share](/help/guide/collaborate/share.md) with the publisher the audiences that should be used in the campaigns.
