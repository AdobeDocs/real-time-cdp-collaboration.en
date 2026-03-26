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

## Prerequisites

Before you can access the measurement reports in Collaboration, you have already:

* [Connected](/help/guide/connect/establishing-connections.md) with a collaborator with the **Measurement** use case enabled and started collaborating on [projects](/help/guide/collaborate/manage-projects.md)
* Run a campaign and [uploaded measurement data](/help/guide/setup/onboard-measurement-data.md) into Collaboration.

<!--

## Create a report {#create-report}

Hidden until functionality is live. At that point, move the contextualhelp from below into this section. 

The syntax rtcdp_collaboration_measurement_create_report is currently implemented in the UI. However, a preference would be to imlement the other contextualhelp ID from below instead, since that explicitly includes campaignID in the syntax. Need to sync up with UI team. More details in CORE-116991.

-->

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

## Edit measurement report {#edit-measurement-report}

>[!IMPORTANT]
>
>You can edit the settings of a measurement report only if it is scheduled to run in the future. For reports that have already been executed, settings cannot be changed.

Update a measurement report settings to ensure the report provides the correct analysis of your campaign within a specific period and runs on a desired date.

To begin, navigate to the workspace of the measurement report you want to update. Select the edit icon (![Edit icon](/help/assets/icons/edit.png)) next to the delete icon.

![The measurement report workspace with the Edit icon highlighted.](/help/assets/collaborate/measure/edit-report.png)

>[!TIP]
>
>In the **[!UICONTROL Measure]** tab, navigate to the report section you wish to edit. Select the edit icon (![Edit icon](/help/assets/icons/edit.png)) next to **[!UICONTROL View full report]** to update its settings.
>![The Measure tab highlighting the Edit icon within a report section.](/help/assets/collaborate/measure/measure-tab-edit-report.png)

The **[!UICONTROL Edit measurement report]** dialog appears with the current settings of the report in the following sections:

* [**Billing details**](#billing-details): Displays information about credits when running measurement reports. No configuration is required.
* [**Campaign details**](#campaign-details): Displays settings for the advertiser, campaign ID, reporting period, and a user-friendly report name.
* [**Report details**](#report-details): Displays settings for the report type, report run date, and configuration options specifically for attribution reports.

![The Edit measurement report dialog showing the current settings under Billing details, Campaign details, and Report details sections.](/help/assets/collaborate/measure/edit-measurement-report-dialog.png)

### Edit campaign details {#edit-campaign-details}

In the **[!UICONTROL Edit measurement report]** dialog, use the **[!UICONTROL Advertiser ID (Name)]** and **[!UICONTROL Campaign ID]** dropdown menus to edit the advertiser and campaign ID for your report.

![The Edit measurement report dialog highlighting the Campaign ID dropdown menu open.](/help/assets/collaborate/measure/edit-campaign-id.png)

Next, select **[!UICONTROL Report date range]** and use the calendar to change the start and end dates of the report.

![The Edit measurement report dialog highlighting the Report date range calendar open.](/help/assets/collaborate/measure/edit-report-date-range.png)

Enter an updated friendly report name to capture your recent changes. This helps you recognize and find this report in the future.

![The Edit measurement report dialog highlighting the updated friendly report name.](/help/assets/collaborate/measure/edit-friendly-report-name.png)

### Edit report details {#edit-report-details}

To schedule the report for a different date, navigate to the **[!UICONTROL Report details]** section. Select the current run date option, then use the calendar to choose your preferred date.

![The Edit measurement report dialog highlighting the Report run date calendar.](/help/assets/collaborate/measure/edit-report-run-date.png)

As an advertiser, you have the option to select or remove the **[!UICONTROL Attribution]** report type in addition to **[!UICONTROL Campaign summary]**. If you choose **[!UICONTROL Attribution]**, your attribution report includes both standard Campaign Summary metrics and in-depth Attribution insights. For more information about the **Campaign summary** and **Attribution** report types, refer to the [create measurement report](#create-measurement-report) section.

>[!IMPORTANT]
>
>If you are a **publisher**, the default report type is **[!UICONTROL Campaign summary]** and cannot be changed at this time.

* If you choose **[!UICONTROL Attribution]** as the report type, you must fill out the required fields in the **[!UICONTROL Attribution]** section. For setup instructions, see the [attribution report details](#report-details-attribution) section.
* If you previously configured attribution settings when creating the report, you can choose to edit the lookback window (measured in days) and select which conversion events to report on.

To update **[!UICONTROL Lookback window in days]**, enter a numeric value, or adjust it with the increment/decrement options. Next, select the conversion events you want to report on. You can choose up to **3** conversions from the available list.

![The Edit measurement report dialog highlighting the updated conversion events.](/help/assets/collaborate/measure/edit-conversion-events.png)

Once finished, review the updates and select **[!UICONTROL Edit]** to apply your changes.

![The Edit measurement report dialog with the Edit option highlighted.](/help/assets/collaborate/measure/edit-report-confirm.png)

A confirmation dialog confirms that your report has been successfully saved.

## Delete measurement report {#delete-measurement-report}

Deleting a measurement report in Collaboration permanently removes it from the system. This action cannot be undone. To do this, select the report you wish to delete in the **[!UICONTROL Measure]** tab.

In the measurement report workspace, select the delete icon (![Delete icon](/help/assets/common/delete.svg)).

![The measurement report workspace with the Delete icon highlighted.](/help/assets/collaborate/measure/delete-report.png)

The **[!UICONTROL Delete report]** dialog appears, prompting you to confirm the deletion. Select **[!UICONTROL Delete]**.

![The Delete report dialog with the Delete option highlighted.](/help/assets/collaborate/measure/delete-report-confirm.png)

A confirmation dialog confirms the report was successfully deleted.
