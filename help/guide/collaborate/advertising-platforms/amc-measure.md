---
title: Create AMC measurement reports
description: Learn how to create and interpret measurement reports for Amazon Marketing Cloud campaigns in Real-Time CDP Collaboration.
audience: advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3b94d263-9748-4e2b-b1c9-7e37e2e51b7f
---

# Create [!DNL AMC] measurement reports {#amc-measurement-reports}

{{limited-availability-release-note}}

After [creating a project with [!DNL Amazon Marketing Cloud]](../manage-projects.md#create-project), you can create retrospective measurement reports that analyze campaign performance using data from your [!DNL AMC] instance. Unlike standard Collaboration measurement, no data upload is required — campaign and conversion event data is sourced automatically via background queries that run when the project is created.

>[!IMPORTANT]
>
>The **[!UICONTROL Measure]** tab is only visible when campaign IDs have been discovered in your [!DNL AMC] instance. If the tab is not visible, see [Troubleshooting](#troubleshooting).

## Prerequisites {#prerequisites}

Before creating a measurement report, ensure you have:

* Established a connection with [!DNL AMC] and created a project. Refer to the [connect to Amazon Marketing Cloud](../../connect/advertising-platforms/amc.md) and [manage projects](../manage-projects.md) guides.
* Campaign IDs available in your [!DNL AMC] instance. If campaigns are missing from the report form, see [Troubleshooting](#troubleshooting).

## Create a report {#create-report}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_create_report"
>title="Create measurement report"
>abstract="Select your campaign, set the date range and run date, choose a report type, and optionally add conversion events for attribution data."

To create an [!DNL AMC] measurement report:

1. Navigate to **[!UICONTROL Collaborate]** > **[!UICONTROL My projects]** and select your [!DNL AMC] project.
2. Select the **[!UICONTROL Measure]** tab.
3. Select **[!UICONTROL Add report]**.

![The Measure tab inside an AMC project, showing an empty report list and the Add report button in the upper-right corner of the workspace.](/help/assets/collaborate/advertising-platforms/PLACEHOLDER.png){zoomable="yes"}

Complete the report form using the sections below.

### Campaign {#campaign}

The **[!UICONTROL Advertiser ID]** is pre-populated from your project settings. From the **[!UICONTROL Campaign ID]** dropdown, select the campaign to include in the report. Available campaigns are populated from your [!DNL AMC] instance at project creation.

### Date range and run date {#dates}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_date_range"
>title="Date range"
>abstract="Set the start and end dates for the campaign data to include in the report. The date range is limited to a 365-day lookback window with a maximum span of 90 days. You can only report on past campaigns."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_run_date"
>title="Run date"
>abstract="The date on which the report executes. Must be at least one day after the report end date and can be up to 46 days in the future."

Set the **[!UICONTROL Date range]** for the campaign data you want to analyze. [!DNL AMC] supports a 365-day lookback window with a maximum span of 90 days. You can only report on past campaigns.

Set the **[!UICONTROL Run date]** — the date on which the report executes. The run date must be at least one day after the report end date and can be up to 46 days in the future. For the full set of date constraints, see [AMC constraints reference](#constraints).

>[!TIP]
>
>For attribution reports, set the run date at least 30 days after the date range end. This ensures all conversions within the fixed 30-day lookback window have been captured before the report runs.

Enter a **[!UICONTROL Report name]** to identify the report.

### Report type {#report-type}

**[!UICONTROL Campaign summary]** is always included in every report. Optionally, select **[!UICONTROL Attribution]** to add conversion data on top of the campaign summary.

| Report type | Description |
| --- | --- |
| **[!UICONTROL Campaign summary]** | Provides reach, frequency, and impression metrics for the selected campaign. Always included. |
| **[!UICONTROL Attribution]** | Adds conversion data to the report. Only available if conversion events exist in your [!DNL AMC] instance. See [Conversion events](#conversion-events). |

### Conversion events (Attribution only) {#conversion-events}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_lookback_window"
>title="Lookback window"
>abstract="The attribution lookback window for AMC reports is fixed at 30 days and cannot be adjusted."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_conversion_events"
>title="Conversion events"
>abstract="Select up to three conversion events to include in the attribution report. Available events are discovered automatically from your AMC instance. If no events appear, your AMC instance may not have any recorded conversion events and Attribution will be unavailable."

If you selected **[!UICONTROL Attribution]**, the **[!UICONTROL Lookback window]** is fixed at 30 days by [!DNL AMC] and cannot be adjusted.

Select up to three **[!UICONTROL Conversion events]** from the list. If no conversion events are available, the [!UICONTROL Attribution] option is grayed out and unavailable for selection.

Once the form is complete, select **[!UICONTROL Create report]**. The report appears in the **[!UICONTROL Measure]** tab with a scheduled or pending status and is only viewable after the run date has passed.

## View a report {#view-report}

Once a report has run, locate your report in the **[!UICONTROL Measure]** tab and select **[!UICONTROL View full report]** to review the results.

![The Measure tab in an AMC project showing a completed report card with its run date, report type, and the View full report button highlighted.](/help/assets/collaborate/advertising-platforms/PLACEHOLDER.png){zoomable="yes"}

The sections available depend on the report type you selected.

### Campaign Summary {#campaign-summary-metrics}

A Campaign Summary report includes the following visualizations. For general guidance on interpreting these metrics, refer to the [measure performance](../measure.md) guide.

| Visualization | Description |
| --- | --- |
| **[!UICONTROL Summary]** | High-level totals for the campaign: total impressions, unique reach, and average frequency. |
| **[!UICONTROL Impressions distribution]** | Breakdown of impressions across [!DNL Amazon] ad products (Sponsored Ads and/or DSP). |
| **[!UICONTROL Frequency distribution]** | How many impressions were shown to each unique user, to help identify saturation and suppression opportunities. |
| **[!UICONTROL Reach curve]** | Cumulative growth in unique users reached over the reporting period. |
| **[!UICONTROL Impressions by placement]** | Which placements drove the most impressions for the campaign. |

### Attribution {#attribution-metrics}

If [!UICONTROL Attribution] was selected, the report also includes:

| Visualization | Description |
| --- | --- |
| **[!UICONTROL Cumulative conversions]** | Total conversions attributed to campaign impressions within the 30-day lookback window. |
| **[!UICONTROL Conversions by day]** | Daily conversion counts attributed to the campaign. |

## AMC constraints reference {#constraints}

The following constraints apply to all [!DNL AMC] measurement reports.

| Constraint | Value |
| --- | --- |
| Date range minimum | 365 days in the past |
| Date range maximum | 45 days after the current date |
| Maximum date range span | 90 days |
| Lookback window | 30 days (fixed, not adjustable) |
| Run date minimum | 1 day after the report end date |
| Run date maximum | 46 days in the future |
| Maximum conversion events per report | 3 |
| Campaign selection | Single campaign per report |
| Report editing | Not available — create a new report instead |

## Troubleshooting {#troubleshooting}

**The Measure tab is not visible or no campaigns appear in the Campaign ID dropdown**

Both symptoms indicate that campaign IDs have not yet been discovered in your [!DNL AMC] instance. Create a new project to trigger a fresh discovery of campaigns and conversion events.

**Conversion events are unavailable and Attribution is grayed out**

Conversion events are discovered dynamically from your [!DNL AMC] instance. If none are listed, your [!DNL AMC] instance may not have any recorded conversion events, and attribution reporting is not available.

**Conversions appear lower than expected**

If the report run date is fewer than 30 days after the end of the date range, conversions within the attribution window may not yet have been captured. Create a new report with a run date at least 30 days after the date range ends.
