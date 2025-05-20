---
title: Measure performance
description: Measure the performance of your campaigns across different channels. Learn how to use and interpret various reports.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: c92b263e-1f96-49f1-841a-ef2e97a4cb9a
---
# Measure performance

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>The **[!UICONTROL Measure]** workspace is only available if the **Campaign measurement** use case was enabled [during the connection proccess](../connect/establishing-connections.md#connection-settings). For more information about use cases, refer to the [manage projects](./manage-projects.md#project-use-cases) guide.

Learn about the available reports in Real-Time CDP Collaboration and understand how to measure and analyze the performance of your marketing campaigns across various channels.

## Prerequisites

Before you can access the measurement reports in Real-Time CDP Collaboration, you have already:

* [Connected](/help/guide/connect/establishing-connections.md) with a desired advertiser or publisher with the **Campaign measurement** use case enabled and started collaborating on [projects](/help/guide/collaborate/manage-projects.md)
* Run a campaign and [uploaded measurement data](/help/guide/setup/onboard-measurement-data.md) into Real-Time CDP Collaboration.

<!--

## Create a report {#create-report}

Hidden until functionality is live. At that point, move the contextualhelp from bel

-->

## View reports {#view-reports}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report_campaignID"
>title="Campaign IDs"
>abstract="Placeholder to add relevant information in the UI about what the Campaign IDs are."

To view the reports available in the measurement tab: 

1. Navigate to **[!UICONTROL Collaborate]** > **[!UICONTROL My projects]**.
2. For your desired project and select **[!UICONTROL View]**. 
3. In the project, select the **[!UICONTROL Measure]** tab. 

Select **[!UICONTROL View full report]** to access the various available reports, detailed further below.

![How to get to the measurement tab in a project.](/help/assets/collaborate/measure/measurement.gif)

### Summary view

The top-of-page view in the measurement tab shows a campaign summary with some high-level numbers for you to reference:

**[!UICONTROL Impressions]**: The total number of times that the creative was displayed. 
**[!UICONTROL Unique reach]**: The number of individual identities who have seen the creative.
**[!UICONTROL Total average frequency]**: The number of impressions divided by unique identities reached. This figure indicates how often every identity was displayed the creative. 

![Campaign summary view](/help/assets/collaborate/measure/campaign-summary.png)

### Metrics over time {#metrics-over-time}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measure_metricsovertime"
>title="Metrics over time"
>abstract="Use the metrics over time view to understand the total number of impressions displayed for your creative throughout the period of the campaign. You can select a maximum of two dimensions to display in the report."

Use the metrics over time view to understand the total number of impressions displayed for your creative throughout the period of the campaign. Note that you can select a maximum of two metrics to display and analyze in the report.

![Metrics over time view.](/help/assets/collaborate/measure/metrics-over-time.png)

### Frequency distribution {#frequency-distribution}

Use the frequency distribution view to understand the breakdown of how many impressions were shown to each unique user. This view can help you in future campaigns to decide as of which point you want to start suppressing audiences. For example, you may want to suppress profiles who have already seen a creative three times. 

![Frequency distribution view.](/help/assets/collaborate/measure/frequency-distribution.gif)

### Metric by dimension {#metric-by-dimension}

Analyze different metrics like impressions, viewable impressions, unique reach, cost, and more in the context of the placement medium. Analyze which medium (for example mobile streaming, CTV programmatic, or others) are driving the best results for your campaigns. 

![Metric by dimension.](/help/assets/collaborate/measure/metric-by-dimension.png)

### Cumulative reach curve {#cumulative-reach-curve}

As the campaign progressed and the number of impressions went up, understand whether the number of users that you were able to reach has also grown. A common pattern in campaigns is that after a certain point a plateau is reached where the creative is displayed to the same people over and over again. This view can help you adjust the length of future campaigns, depending on the moment that new people were not being reached anymore.

![Cumulative reach curve.](/help/assets/collaborate/measure/cumulative-reach-curve.png)

### Impressions by placement {#impressions-by-placement}

Understand which medium is driving impressions for your creative. This can help you decide where to invest your ad spend in future campaigns.

![Impressions by placement.](/help/assets/collaborate/measure/impressions-by-placement.png)

## Next steps

![Discover, activate, measure for advertisers.](/help/assets/end-to-end-workflow/discover-activate-measure.png)

In the spirit of the cyclicity in the image above, use the insights you obtained from viewing the reports in planning your next campaign. As an advertiser, ff necessary, go back to discover different publishers and run overlaps to discover different audiences for your next campaigns.
