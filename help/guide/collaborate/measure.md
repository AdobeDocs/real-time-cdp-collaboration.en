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
* Run your campaign and make sure a [Campaign ID is provided for the campaign](../collaborate/manage-projects.md#manage-campaign-id):
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

### Cumulative conversions {#cumulative-conversions}

This view provides a detailed breakdown of the conversion events you choose to measure in a tabular format. The table includes:

* **Conversion event**: Name of each conversion event you are tracking.
* **Conversion count**: Total count of conversions that occurred for each event.
* **Estimated revenue**: Estimated value attributed to each conversion event.

Review this table to evaluate the effectiveness of your campaign in driving the desired actions.

![Cumulative conversions.](/help/assets/collaborate/measure/cumulative-conversions.png)

### Conversions by day {#conversions-by-day}

This chart provides a day-by-day breakdown of conversions for each event set up when you create an Attribution report. Use this view to uncover daily patterns, identify periods of high or low conversion activity, and compare how different conversion events perform across your campaign timeline.

![Conversions by day.](/help/assets/collaborate/measure/conversions-by-day.gif)

## Create measurement report {#create-measurement-report}

In Collaboration, you can create two main types of measurement reports:

* **Campaign Summary**: Provides high-level metrics such as reach, impressions, average frequency, and delivery by channel, giving a quick overview of overall campaign performance.
* **Attribution**: Measures how campaign exposures drive downstream actions like conversions or purchases, helping you understand campaign effectiveness.

You can run Campaign Summary report on its own, while Attribution report requires both report types to be selected together.

### Create campaign summary report {#create-campaign-summary-report}

Both publishers and advertisers can generate **Campaign Summary** reports to evaluate campaign performance. Use these reports to gain insights into key metrics such as [reach](#cumulative-reach-curve), [frequency](#frequency-distribution), and [impressions](#impressions-by-placement), and understand how your campaign was delivered and its overall impact.

To generate a **Campaign Summary** report, navigate to the project workspace from the **[!UICONTROL Collaborator]** workspace. From the **[!UICONTROL Measure]** tab, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Measure]**.

If this is your first report, you may also select the **[!UICONTROL Run report]** option.

![The Measure tab highlighting the Run report option and the Measure option.](/help/assets/collaborate/measure/run-measure-report.png)

The **[!UICONTROL Create measurement report]** screen appears with information and input fields grouped under **[!UICONTROL Billing details]**, **[!UICONTROL Campaign details]**, and **[!UICONTROL Report details]** sections.

#### Billing details {#billing-details}

This section explains how credits are used when generating measurement reports. Credit responsibility is established during [connection setup](../connect/establishing-connections.md#credit-split). Before running any reports, make sure to review and confirm the credit split settings and reporting roles with your collaborator.

#### Campaign details {#campaign-details}

In the **[!UICONTROL Campaign details]** section, select the appropriate **Advertiser ID** to associate with your report. These advertiser names or IDs were added during [connection setup](../connect/establishing-connections.md#advertiser-names). If only one name was configured, it appears by default. If no name was set up, the **[!UICONTROL Advertiser ID (Name)]** field is disabled and prefilled with the advertiser account name.

![The Create measurement report screen showing the Advertiser ID (Name) option disabled.](/help/assets/collaborate/measure/advertiser-id.png)

Then, select the desired campaign from the **[!UICONTROL Campaign ID]** dropdown menu. This menu lists all campaign IDs entered by the publisher for your project. If the campaign you need isn't available, [add it in the UI](./manage-projects.md#manage-campaign-id) before generating the report.

![The Create measurement report screen showing the Campaign ID dropdown menu expanded.](/help/assets/collaborate/measure/campaign-id.png)

Next, specify the period you want the report to cover. Select **[!UICONTROL Report date range]**, then use the calendar to choose the start and end dates.

![The Create measurement report screen showing the Report date range calendar.](/help/assets/collaborate/measure/report-date-range.png)

#### Report details {#report-details}

**Report run date**

In the **[!UICONTROL Report details]** section, choose the date on which the report should run. Select **[!UICONTROL Report run date]** and choose your preferred date from the calendar. 

* If you choose today's date or a date in the past, the **Campaign Summary** report runs right away.
* If you choose a future date, the **Campaign Summary** report is scheduled to run on that day.

![The Create measurement report screen showing the Report run date calendar.](/help/assets/collaborate/measure/report-run-date.png)

**Report type**

* If you're an advertiser, you can select the **[!UICONTROL Campaign summary]** report type from the available options. Only advertisers can generate attribution reports.
* If you're a publisher, the **[!UICONTROL Campaign summary]** report type is preselected and cannot be changed. At this time, publishers cannot run attribution reports.

![The Create measurement report screen showing the Campaign summary option as a preselected and unchangable report type.](/help/assets/collaborate/measure/cs-report-type.png)

Finally, review your settings and select **[!UICONTROL Create]**. Your campaign summary report generates immediately if the run date is today or earlier, or on the chosen future date. You can edit the scheduled report before its run date. For step-by-step instructions, refer to the [Edit measurement report] section.

Once available, you can view your report at any time in the **[!UICONTROL Measure]** tab within your project workspace.

![The Create measurement report screen showing the information and the Create option highlighted.](/help/assets/collaborate/measure/cs-review.png)

### Create attribution report {#create-attribution-report}

As an advertiser, you can generate **Attribution** reports to assess how your campaign exposures contribute to key outcomes such as sign-ups or purchases. Use these reports to understand user interactions with your campaign, identify which touchpoints drive the most impact, and inform more effective marketing strategies.

>[!IMPORTANT]
>
> You must [source your measurement data](../setup/onboard-measurement-data.md#add-measurement-data) into Collaboration before generating Attribution reports.
>![The Measure tab with the requirements for Measurement data and the disabled Measure option.](/help/assets/collaborate/measure/require-measurement-data.png)

To generate an **Attribution** report, navigate to the project workspace from the **[!UICONTROL Collaborator]** workspace. From the **[!UICONTROL Measure]** tab, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Measure]**.

If this is your first report, you may also select the **[!UICONTROL Run report]** option.

![The Measure tab highlighting the Run report option and the Measure option.](/help/assets/collaborate/measure/run-measure-report-attribution.png)

The **[!UICONTROL Create measurement report]** screen appears with information and input fields grouped under **[!UICONTROL Billing details]**, **[!UICONTROL Campaign details]**, and **[!UICONTROL Report details]** sections.

Read and follow steps in the [Create campaign summary report](#create-campaign-summary-report) section to configure the following settings:

* [Billing details](#billing-details) 
* [Campaign details](#campaign-details)

#### Report details for Attribution reports {#report-details-attribution}

**Report run date**

>[!IMPORTANT]
>
> For attribution reports, the report run date must be a future date, and must occur at least one day after the end date of your report date range plus the full duration of the defined lookback window.
> **Report run date ≥ report end date + lookback window + 1**
> 
> For example, if your report date range ends on June 15 and the lookback window is 14 days, the report run date is June 30 or later.

In the **[!UICONTROL Report details]** section, choose the date on which the report should run. Select **[!UICONTROL Report run date]** and choose your preferred date from the calendar.

**Report type**

As an advertiser, you can select **[!UICONTROL Attribution]** as a report type in addition to **[!UICONTROL Campaign summary]**. When you choose the Attribution report, your results include both standard Campaign Summary metrics and detailed Attribution analysis, providing a comprehensive view of campaign performance.

![The Create measurement report screen highlighting both the Campaign summary and Attribution report types selected.](/help/assets/collaborate/measure/attribution-report-type.png)

When you select **[!UICONTROL Attribution]** as the report type, an **[!UICONTROL Attribution]** configuration section appears with additional required settings:

* **Lookback window in days**: Defines how far back the report considers campaign impressions before each conversion. Only impressions within this period are eligible for attribution credit.
* **Conversion events**: Specifies which conversion actions you want to measure, for example, purchases or sign-ups. These events must be set up in advance when you [source your measurement data](../setup/onboard-measurement-data.md#add-conversion-event) into Collaboration.

First, enter a value for the **[!UICONTROL Lookback window in days]** field, or adjust it with the increment/decrement options.

![The Create measurement report screen highlighting the value for Lookback window in days.](/help/assets/collaborate/measure/lookback-window-in-days.png)

Next, choose up to **3** conversion events from the available list. For more information about a particular event, select the **[!UICONTROL i]** icon to view its details.

![The Create measurement report screen highlighting the selected conversion events and the information of the Purchase event.](/help/assets/collaborate/measure/attribution-conversion-events.png)

Finally, review your settings and select **[!UICONTROL Create]** to schedule the report. Your attribution report will be generated on the specified run date. You can edit the scheduled report before its run date. For step-by-step instructions, refer to the [Edit measurement report] section. 

Once available, you can view your report at any time in the **[!UICONTROL Measure]** tab within your project workspace.

![The Create measurement report screen showing the information and the Create option highlighted.](/help/assets/collaborate/measure/attribution-review.png)

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
