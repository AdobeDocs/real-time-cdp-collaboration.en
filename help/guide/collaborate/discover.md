---
title: Discover overlaps and compare audiences
description: Discover overlaps between your and your collaborators' audiences. Learn how to discover the best audiences for use in your campaigns.
audience: admin, publisher, advertiser
badgebeta: label="Beta" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
---
# Discover overlaps and compare audiences

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently a beta product, available to select customers. The product and documentation are subject to change. Contact your Adobe representative to learn more.

After [creating a project](/help/guide/collaborate/manage-projects.md) within a collaboration space between an advertiser and a publisher, you can now compare your audiences against your collaborator's audiences. This way, you can discover overlaps between audiences and get insights broken down by match keys or identities. This helps advertisers decide which audiences to share with publishers for activation, depending on the desired use case.

![Discover overlaps](/help/assets/collaborate/discover-overlaps/discover-overlaps.png)

The match keys used to discover and compare audiences are set when you [connect with a publisher](/help/guide/connect/establishing-connections.md#connection-settings). To change the overlap percentages indicated in preparation for running campaigns, you can remove match keys, but you cannot add new match keys at this point. To do that, head to the [connection settings](/help/guide/connect/establishing-connections.md#connection-settings) between the collaborators.

![Edit match keys screen](/help/assets/collaborate/discover-overlaps/edit-match-keys.png)

## Prerequisites {#prerequisites}

To fully utilize the functionality in the **[!UICONTROL Discover]** tab of the **[!UICONTROL Collaborate]** workflow, you have already:

* [Imported audiences](/help/guide/setup/onboard-audiences.md)
* [Connected](/help/guide/connect/establishing-connections.md) with a desired advertiser or publisher
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

>[!TIP]
>
>The overlap percentage figure may not be always available for all audiences. The visibility of the overlap percentage indicator depends on the setting that your collaborator chose for an audience in the [metadata visibility section](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Relevant audiences {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Relevant audiences"
>abstract="Based on overlap percentages, these publisher audiences might be a good fit for your campaign. <br><br> The <b>identity count</b> is the publisher's audience size. <br><br> <b>Overlapping identities</b> represents the overlap between the recommended publisher audience and all advertiser audiences. <br><br> The <b>Overlap %</b> represents the number of overlapping identities divided by the size of <i>all</i> advertiser audiences."

The **[!UICONTROL Relevant audiences]** view in the **[!UICONTROL Discover]** module provides a curated list of the top five audiences based on overlap percentage. This feature helps you quickly identify the audiences with the highest overlap with your current data, enabling you to target your campaigns more effectively.

* **[!UICONTROL Identity count]** is the publisher's audience size.
* **[!UICONTROL Overlapping identities]** represents the overlap between the recommended publisher audience and all advertiser audiences.
* **[!UICONTROL Overlap %]** represents the number of overlapping identities divided by the size of *all* advertiser audiences.

<!--

For extensive information about the overlapping identities count and percentages, read the [overlap calculations reference documentation](/help/guide/reference/overlap-calculations.md).

-->

![Relevant audiences view](/help/assets/collaborate/discover-overlaps/relevant-audiences-highlighted.png)

## Discover overlaps {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Discover overlaps with individual audiences"
>abstract="Get insights around the population of this audience and its overlaps with the collaborator's universe of identities."

![Discover overlaps with different audiences view](/help/assets/collaborate/discover-overlaps/discover-overlaps-cards-view.png)

Get extensive information about any of your collaborator's audiences and view overlap information comparing these audiences against either your entire population count across all your audiences, or against specific audiences of yours.

>[!TIP]
>
>Some of the numbers indicated in the screenshot may not be always available for all audiences. Their visibility depends on the setting that your collaborator chose for an audience in the [metadata visibility section](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Next steps

After exploring and discovering the desired audiences, it's time to [share](/help/guide/collaborate/share.md) with the publisher the audiences that should be used in the campaigns.
