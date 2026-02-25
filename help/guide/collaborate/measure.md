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
>The **[!UICONTROL Measure]** workspace is only available if the **Measurement** use case was enabled [during the connection proccess](../connect/establishing-connections.md#connection-settings). For more information about use cases, refer to the [manage projects](./manage-projects.md#project-use-cases) guide.

Learn about the available reports in Adobe Real-Time CDP Collaboration and understand how to measure and analyze the performance of your marketing campaigns across various channels.

## Prerequisites {#prerequisites}

Before you can access the measurement reports in Collaboration, you must:

* [Connect](/help/guide/connect/establishing-connections.md) with a collaborator with the **Measurement** use case enabled
* Collaborate on at least one project with your collaborator. Learn how to [create a project](/help/guide/collaborate/manage-projects.md#create-project).
* Run your campaign and make sure a [Campaign ID is provided for the campaign](../collaborate/manage-projects.md#update-campaign-id):
    * If you are a publisher, input the Campaign ID linked to your advertiser's campaign.
    * If you are an advertiser, request that your collaborator (publisher) provide the Campaign ID. This is required to [generate reports in the Measure workspace](#create-measurement-report).
* [Upload measurement data](/help/guide/setup/onboard-measurement-data.md) into Collaboration if you want to [create Attribution reports](#create-attribution-report).

## View reports {#view-reports}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report_campaignID"
>title="Campaign IDs"
>abstract="Placeholder to add relevant information in the UI about what the Campaign IDs are."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report"
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

## Create measurement report {#create-measurement-report}

In Collaboration, you can create two main types of measurement reports:

* **Campaign Summary**: Provides high-level metrics such as reach, impressions, average frequency, and delivery by channel, giving a quick overview of overall campaign performance.
* **Attribution**: Measures how campaign exposures drive downstream actions like conversions or purchases, helping you understand campaign effectiveness.

You can run Campaign Summary on its own, while Attribution requires both report types to be selected together.

### Create campaign summary report {#create-campaign-summary-report}

Both publishers and advertisers can generate **Campaign Summary** reports to evaluate campaign performance. Use these reports to gain insights into key metrics such as [reach](#cumulative-reach-curve), [frequency](#frequency-distribution), and [impressions](#impressions-by-placement), and understand how your campaign was delivered and its overall impact.

To generate a **Campaign Summary** report, navigate to the project workspace from the **[!UICONTROL Collaborator]** workspace. From the **[!UICONTROL Measure]** tab, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Measure]**.

If this is your first report, you may also select the **[!UICONTROL Run report]** option.

![The Measure tab highlighting the Run report option and the Measure option.](/help/assets/collaborate/measure/run-measure-report.png)

The **[!UICONTROL Create measurement report]** screen appears with information and input fields grouped under **[!UICONTROL Billing details]**, **[!UICONTROL Campaign details]**, and **[!UICONTROL Report details]** sections.

#### Billing details {#billing-details}

This section explains how credits are used when generating measurement reports. Credit responsibility is established during [connection setup](../connect/establishing-connections.md#credit-split). Before running any reports, make sure to review and confirm the credit split settings and reporting roles with your collaborator.

#### Campaign details {#campaign-details}

In the **[!UICONTROL Campaign details]** section, select the appropriate **Advertiser ID** to associate with your report if advertiser names or IDs were added during [connection setup](../connect/establishing-connections.md#advertiser-names). If a single name was configured, it appears by default. If no name was set up, the **[!UICONTROL Advertiser ID (Name)]** field is disabled and prefilled with the advertiser account name.

![The Create measurement report screen showing the Advertiser ID (Name) option disabled.](/help/assets/collaborate/measure/cs-advertiser-id.png)

Then, select the desired campaign from the **[!UICONTROL Campaign ID]** dropdown menu. This menu lists all campaign IDs entered by the publisher for your project. If the campaign you need isn't available, [add it in the UI](./manage-projects.md#manage-campaign-id) before generating the report.

![The Create measurement report screen showing the Campaign ID dropdown menu expanded.](/help/assets/collaborate/measure/cs-campaign-id.png)

Next, specify the period you want the report to cover. Select **[!UICONTROL Report date range]**, then use the calendar to choose the start and end dates.

![The Create measurement report screen showing the Report date range calendar.](/help/assets/collaborate/measure/cs-report-date-range.png)

#### Report details {#report-details}

In the **[!UICONTROL Report details]** section, choose the date on which the report should run. Select **[!UICONTROL Report run date]** and choose your preferred date from the calendar.

>[!IMPORTANT]
>
> The report run date must be today or later, and must occur at least one day after the end date of your report date range.

![The Create measurement report screen showing the Report run date calendar.](/help/assets/collaborate/measure/cs-report-run-date.png)

Advertisers can select the **[!UICONTROL Campaign summary]** report type from the available options. If you're a publisher, the **Campaign summary** report type is preselected and cannot be changed.

![The Create measurement report screen showing the Campaign summary option as a preselected and unchangable report type.](/help/assets/collaborate/measure/cs-report-type.png)

Finally, review your settings and select **[!UICONTROL Create]** to schedule the report. The **Campaign summary** report will be generated on the specified run date. Once available, you can view your report at any time in the **[!UICONTROL Measure]** tab within your project workspace.

![The Create measurement report screen showing the information and the Create option highlighted.](/help/assets/collaborate/measure/cs-review.png)

### Create attribution report {#create-attribution-report}

As an advertiser, you can generate **Attribution** reports to assess how your campaign exposures contribute to key actions such as sign-ups or purchases. Use these reports to understand user interactions with your campaign, identify which touchpoints drive the most impact, and inform more effective marketing strategies.

>[!IMPORTANT]
>
> You must [source your measurement data](../setup/onboard-measurement-data.md#add-measurement-data) into Collaboration before generating Attribution reports.
>![The Measure tab with the requirements for Measurement data and the disabled Measure option highlighted.](/help/assets/collaborate/measure/require-measurement-data.png)

To generate an **Attribution** report, navigate to the project workspace from the **[!UICONTROL Collaborator]** workspace. From the **[!UICONTROL Measure]** tab, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Measure]**.

If this is your first report, you may also select the **[!UICONTROL Run report]** option.

![The Measure tab highlighting the Run report option and the Measure option.](/help/assets/collaborate/measure/run-measure-report.png)

The **[!UICONTROL Create measurement report]** screen appears with information and input fields grouped under **[!UICONTROL Billing details]**, **[!UICONTROL Campaign details]**, and **[!UICONTROL Report details]** sections.

Read and follow steps in the [Create campaign summary report](#create-campaign-summary-report) section to configure the following settings:

* [Billing details](#billing-details) 
* [Campaign details](#campaign-details)
* Report run date under [Report details](#report-details) section

#### Report details for Attribution reports {#report-details-attribution}

As an advertiser, you can select **[!UICONTROL Attribution]** as a report type in addition to **[!UICONTROL Campaign summary]**. When you choose the Attribution report, your results will include both standard Campaign Summary metrics and detailed Attribution analysis, providing a comprehensive view of campaign performance and user conversion paths.

![The Create measurement report screen highlighting both the Campaign summary and Attribution report types selected.](/help/assets/collaborate/measure/attribution-report-type.png)

When you select **[!UICONTROL Attribution]** as the report type, a **[!UICONTROL Attribution]** configuration section appears with additional required settings:

* **Lookback window in days**: Defines how far back the report considers campaign impressions before each conversion. Only impressions within this period are eligible for attribution credit.
* **Conversion events**: Specifies which conversion actions you want to measure,for example, purchases or sign-ups. These events must be set up in advance when [sourcing your measurement data](../setup/onboard-measurement-data.md#add-conversion-event).

First, enter a value for the **[!UICONTROL Lookback window in days]** field, or adjust it with the increment/decrement options.

![The Create measurement report screen highlighting the value for Lookback window in days.](/help/assets/collaborate/measure/lookback-window-in-days.png)

Next, choose up to **3** conversion events from the available list. For more information about a particular event, select the **[!UICONTROL i]** icon to view its details.

![The Create measurement report screen highlighting the selected conversion events and the information of the Purchase event.](/help/assets/collaborate/measure/attribution-conversion-events.png)

Finally, review your settings and select **[!UICONTROL Create]** to schedule the report. The **Attribution** report will be generated on the specified run date. Once available, you can view your report at any time in the **[!UICONTROL Measure]** tab within your project workspace.

![The Create measurement report screen showing the information and the Create option highlighted.](/help/assets/collaborate/measure/attribution-review.png)
