---
title: Amazon Marketing Cloud
description: Learn about collaborating with Amazon Marketing Cloud in Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
---
# Amazon Marketing Cloud

{{limited-availability-release-note}}

After forming a connection with [!DNL Amazon Marketing Cloud] ([!DNL AMC]), advertisers can [create a project](../manage-projects.md#create-project) to collaborate with [!DNL AMC] to leverage its advanced analytics capabilities. After creating a project, you can use the **[!UICONTROL Discover]** section to compare audience insights and discover relevant audiences for your campaigns.

>[!IMPORTANT]
>
>The only use cases supported with [!DNL AMC] are **Audience discovery** and **Measurement**. Currently, only the **[!UICONTROL Discover]** section is available within your project with [!DNL AMC].

## Discover {#discover}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_compare_audiences"
>title="Compare audiences"
>abstract="Compare your audience to all consumers reached by your Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_relevant_audiences"
>title="Relevant audiences"
>abstract="Amazon targeting segments that your audience has the highest overlaps considering only DSP impressions (these segments can only be targeted in the DSP)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_resolved_ids"
>title="Resolved IDs"
>abstract="The number of IDs Amazon’s Identity Resolution was able to resolve using your audience data."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlapping_ad_exposed_ids"
>title="Overlapping ad exposed IDs"
>abstract="This represents the number of ‘Resolved IDs’ from the uploaded audience that have also been exposed to an ad via Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlap_percentage"
>title="Overlap %"
>abstract="The proportion of ‘Resolved IDs’ that have been exposed to an ad via Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_amazon_breakdown"
>title="Breakdown by Amazon ad product"
>abstract="Breakdown of ‘Overlapping ad exposed IDs’ reached by either Amazon Ads Sponsored Product and/or Amazon Ads DSP."

In the **[!UICONTROL Discover]** section, you can compare your AMC audience to all consumers reached by your Amazon Ads. You can also view Amazon targeting segments that your audience has the highest overlaps with, considering only DSP impressions (these segments can only be targeted in the DSP).

>[!IMPORTANT]
>
>Audience data is processed from the audiences uploaded to your [!DNL Amazon Ads] account. To learn how send use Experience Platform's Destinations feature to send yours audiences to your [!DNL Amazon Ads] account, read the [Amazon Ads connection](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/amazon-ads) guide.

![The Discover section in a project with Amazon Marketing Cloud.](/help/assets/collaborate/advertising-platforms/amc-discover.png){zoomable="yes"}

### Compare audiences {#compare-audiences}

The **[!UICONTROL Compare audiences]** section provides insights into how your [!DNL AMC] audience overlaps with consumers reached by your Amazon Ads. Within the **[!UICONTROL Compare audiences]** section, you can view the following metrics:

| Metric                         | Description                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL Resolved IDs]      | The number of IDs [!DNL Amazon’s Identity Resolution] was able to resolve using your audience data. |
| [!UICONTROL Overlapping ad exposed IDs]     | This represents the number of [!UICONTROL Resolved IDs] from the uploaded audience that have also been exposed to an ad via [!DNL Amazon Ads]. |
| [!UICONTROL Overlap %]                      | The proportion of [!UICONTROL Resolved IDs] that have been exposed to an ad via [!DNL Amazon Ads]. |
| [!UICONTROL Breakdown by Amazon ad product] | Breakdown of [!UICONTROL Overlapping ad exposed IDs] reached by either [!UICONTROL Sponsored Product] and/or [!UICONTROL DSP]. Each is represented as an individual percentage from total number of ad exposed IDs. Since an ID can belong to both [!UICONTROL Sponsored Products] and [!UICONTROL DSP], the percentages may not sum to 100%. |


### Relevant audiences {#relevant-audiences}

The **[!UICONTROL Relevant audiences]** section provides insights into [!DNL Amazon] targeting segments, or audiences, that your audience has the highest overlaps with, considering only DSP impressions (these segments can only be targeted in the DSP). You can toggle through all relevant audiences and within each section, you can view the following metrics:

| Metric                         | Description                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL Resolved IDs]      | The number of IDs [!DNL Amazon’s Identity Resolution] was able to resolve using your audience data. |
| [!UICONTROL Overlapping ad exposed IDs]     | This represents the number of [!UICONTROL Resolved IDs] from the uploaded audience that have also been exposed to an ad via [!DNL Amazon Ads]. This only considers DSP impressions. |
| [!UICONTROL Overlap %]                      | The proportion of [!UICONTROL Resolved IDs] that have been exposed to an ad via [!DNL Amazon Ads]. |
| [!UICONTROL Categories]                     | The category or categories that the audience belongs to. An audience can belong to multiple categories. |

### Discover overlaps with [!DNL Amazon Marketing Cloud] {#discover-overlaps}

The **[!UICONTROL Discover overlaps with Amazon Marketing Cloud]** section provides insights into how your audiences overlap with [!DNL Amazon] targeting segments, or audiences. You can view the following metrics:

| Metric                         | Description                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL Resolved IDs]      | The number of IDs [!DNL Amazon’s Identity Resolution] was able to resolve using your audience data. |
| [!UICONTROL Overlapping ad exposed IDs]     | This represents the number of [!UICONTROL Resolved IDs] from the uploaded audience that have also been exposed to an ad via [!DNL Amazon Ads]. This only considers DSP impressions. |
| [!UICONTROL Overlap %]         | The proportion of [!UICONTROL Resolved IDs] that have been exposed to an ad via [!DNL Amazon Ads]. |