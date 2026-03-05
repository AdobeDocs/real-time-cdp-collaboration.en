---
title: Add and manage measurement data
description: Learn how to add measurement data to Adobe Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 739d31b9-3f00-477d-b6be-995c7767c6ca
---
# Add and manage measurement data {#add-and-manage-measurement-data}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_onboard_measurement_data"
>title="Read more"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_data_target_fields"
>title="Target fields"
>abstract="Placeholder for measurement target fields."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_data_source_fields"
>title="Source fields"
>abstract="Placeholder for measurement source fields."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_measurement_mapping_source_fields"
>title="Map source fields"
>abstract="Placeholder for measurement mapping of source fields."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_measurement_mapping_target_fields"
>title="Map target fields"
>abstract="Placeholder for measurement mapping of target fields."

{{limited-availability-release-note}}

This document outlines the steps to add campaign measurement data to Adobe Real-Time CDP Collaboration. Publishers can work with Adobe teams to upload campaign measurement data. After that data is uploaded and processed, both publisher and advertiser will be able to view extensive [campaign measurement reports](/help/guide/collaborate/measure.md).

## Add measurement data {#add-measurement-data}

As an advertiser, you can upload your measurement data containing conversion events to Collaboration for use in campaign measurement reports. Conversion data typically includes fields such as user identifiers (for example, hashed email or device IDs), timestamp of the conversion event, and specific conversion event details such as purchase or sign-up.

To source measurement data, navigate to the **[!UICONTROL My measurement data]** tab within the **[!UICONTROL Setup]** workspace. Select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Measurement data]**. 

If this is your first measurement data, you may also select the **[!UICONTROL Add]** option.

![My Measurement data tab with the Add option and Measurement data option highlighted.](../../assets/setup/add-manage-measurement-data/add-measurement-data.png){zoomable="yes"}

The **[!UICONTROL Add measurement data]** screen appears, displaying a summary of steps to source measurement data. Select **[!UICONTROL Start onboarding]**.

![The Add measurement data screen displaying a summary of steps to source measurement data and the Start onboarding option highlighted.](../../assets/setup/add-manage-measurement-data/add-measurement-data-screen.png){zoomable="yes"}

### Data connection and details {#data-connection-and-details}

In this step, you need to configure your data connection and specify the details for your measurement data.

#### Select measurement data type {#select-measurement-data-type}

The measurement data type defines the kind of events you bring in for campaign measurement. Currently, Conversion Data is the supported type. 

Select **[!UICONTROL Conversion Data]** as your measurement data type, followed by **[!UICONTROL Next]**. 

![The Data connection and details step highlighting the measurement data type and the Next option.](../../assets/setup/add-manage-measurement-data/select-measurement-data-type.png){zoomable="yes"}

#### Select data connection {#select-data-connection}

A data connection is the source from where you source measurement data into Collaboration. Once you have established your initial data connection and sourced your first set of measurement data, you can continue sourcing additional measurement data using the same data connection.

To add a data connection, select **[!UICONTROL Add a new data connection]**, then select **[!UICONTROL Next]**.

![The Data connection and details step highlighting the Add a new data connection option and the Next option.](../../assets/setup/add-manage-measurement-data/select-measurement-data-connection.png){zoomable="yes"}

#### Select data source {#select-data-source}

Next, choose the source for your data connection. At this time, Adobe Experience Platform is the only supported data source.

Select your data source, then select **[!UICONTROL Next]**.

![The Data connection and details step highlighting the Adobe Experience Platform option and the Next option.](../../assets/setup/add-manage-measurement-data/select-measurement-data-source.png){zoomable="yes"}

#### Select sandbox {#select-sandbox}

Select the sandbox that includes the measurement data that you want to use for Collaboration campaign measurement reports. Choose the sandbox from the list of available sandboxes and then select **[!UICONTROL Next]**.

![The Data connection and details step highlighting the Prod sandbox and the Next option.](../../assets/setup/add-manage-measurement-data/select-sandbox.png){zoomable="yes"}

#### Select measurement dataset {#select-measurement-dataset}

A list of datasets in the selected sandbox appears. Select a dataset as your measurement data, then select **[!UICONTROL Next]**. You can use the Search option to filter and find the preferred dataset.

![The Data connection and details step highlighting the Search option, the Example Event Data Dataset, and the Next option.](../../assets/setup/add-manage-measurement-data/select-measurement-dataset.png){zoomable="yes"}

#### Provide name and details {#provide-name-and-details}

Next, provide a name and a description for your data connection. This information will help you identify the data connection later on.

![The Data connection and details step with the option to provide a name and description.](../../assets/setup/add-manage-measurement-data/data-connection-name-details.png){zoomable="yes"}

### Mapping {#mapping}

The next step is to map fields from your measurement data to the corresponding target fields used in Collaboration. You can also choose to enrich your event dataset with attributes from Real‑Time Customer Profile by mapping join keys, and use these attributes to break down measurement reports.

#### Enrich event data {#enrich-event-data}

To enrich your event data, select the **[!UICONTROL Source field join key]** option.

![The Mapping screen with the Source field join key option highlighted.](../../assets/setup/add-manage-measurement-data/select-source-field-join-key.png){zoomable="yes"}

In the **[!UICONTROL Source field join key]** dialog, choose the source field, followed by **[!UICONTROL Select]**.

![The Source field join key dialog highlighting the Source field and the Next option.](../../assets/setup/add-manage-measurement-data/source-field-join-key-dialog.png){zoomable="yes"}

Next, select the **[!UICONTROL Profile join key]** option. In the **[!UICONTROL Profile join key]** dialog, select the profile field from the list. You can use the Search option to find the desired field. Then, choose **[!UICONTROL Select]** to confirm.

![The Profile join key dialog highlighting the Search key, the selected profile field and the Next option.](../../assets/setup/add-manage-measurement-data/profile-join-key-dialog.png){zoomable="yes"}

#### Mapping fields {#mapping-fields}

To start mapping source fields from your measurement data to the target fields in Collaboration, select the empty source field in the **[!UICONTROL Mapping]** screen.

![The Mapping screen with the empty source field highlighted.](../../assets/setup/add-manage-measurement-data/mapping-screen.png){zoomable="yes"}

The **[!UICONTROL Select source field]** dialog appears, displaying a list of available source fields grouped under options such as **[!UICONTROL Identity namespace]** and **[!UICONTROL Event schema]**. You can use the search option to filter and find the source field from the list.

Choose the source field that you want, followed by **[!UICONTROL Select]**. 

![The Select source field dialog highlighting the Emails source field and the Select option.](../../assets/setup/add-manage-measurement-data/select-source-field-dialog.png){zoomable="yes"}

Next, use the dropdown menu to map the selected source field to an appropriate target field. All available target fields are the [match keys configured for your Collaborator account](./onboard-account.md#set-up-match-keys).

![The dropdown menu displaying all available target fields to map with the selected source field.](../../assets/setup/add-manage-measurement-data/select-target-field-dropdown.png){zoomable="yes"}

You can add or remove mapping rows as necessary. If you need to map a non-hashed source field to a hashed target field (for example, mapping a plain text email to [!UICONTROL Hashed email]), use the **[!UICONTROL Apply transformation]** option to apply the required hashing.

When you are done, review the mapped fields and join keys if enrichment is enabled. Then, select **[!UICONTROL Next]**.

![The Mapping screen showing the mapped fields, join keys (when enrichment is enabled), and the highlighted Next option.](../../assets/setup/add-manage-measurement-data/review-mapping.png){zoomable="yes"}

### Manage consent {#manage-consent}

Before proceeding, you must acknowledge that your data usage in Collaboration complies with your Real-Time CDP data governance policies. All data must be pre-filtered according to consent requirements or any applicable custom consent policies, so no further processing is required.

To confirm your acknowledgement, select **[!UICONTROL Next]**.

![The Manage consent screen requiring confirmation with the Next option highlighted.](../../assets/setup/add-manage-measurement-data/manage-consent.png){zoomable="yes"}

If you [enable profile enrichment during the mapping step](#enrich-event-data), you can configure consent policies from a list of pre-defined options. This includes:

* **Marketing actions**: Use these marketing actions to control which audience data to bring into Collaboration from Experience Platform.
* **Consent rules**: Select the consent rules to apply to data being sourced into Collaboration.
* **Audience**: Use the audience filter to include or exclude audience profiles for consent.


>[!NOTE]
>
>**[!UICONTROL Data Collaboration]** supports C4, C5, and C9 data usage labels while **[!UICONTROL Data Science]** supports C9 only. Read more about data usage labels in the Experience Platform documentation:
>
>* [Data usage labels overview](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target="_blank"}
>* [Glossary](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference){target="_blank"}

Select the preferred settings, then select **[!UICONTROL Next]**.

![The Manage consent screen showing consent configuration options when profile enrichment is enabled, with the Next option highlighted.](../../assets/setup/add-manage-measurement-data/manage-consent-configuration-options.png){zoomable="yes"}

Before proceeding, you need to confirm and accept the terms in the **[!UICONTROL Governance policy and enforcement actions]** dialog. Select the checkbox, followed by **[!UICONTROL OK]**.

![The Governance policy and enforcement actions dialog showing the checkbox and the OK option highlighted.](../../assets/setup/add-manage-measurement-data/governance-policy-enforcement-actions-dialog.png){zoomable="yes"}

#### Audience filter {#audience-filter}

To include or exclude certain audience profiles for consent, use the **[!UICONTROL Audience filter]** dropdown menu. Once you select this filter, the UI updates to display the **[!UICONTROL Browse audiences]** option. Select **[!UICONTROL Browse audiences]**.

![The Manage consent screen showing the Browse audiences option after audience filter is selected.](../../assets/setup/add-manage-measurement-data/browse-audiences.png){zoomable="yes"}

The **[!UICONTROL Select audiences]** dialog appears. Choose an audience from the list, followed by **[!UICONTROL Select]**.

![The Select audiences dialog highlighting the selected audience and the Select option.](../../assets/setup/add-manage-measurement-data/select-audiences-dialog.png){zoomable="yes"}

Your chosen audience now appears, with the option to remove it if needed. Review your consent settings, then select **[!UICONTROL Next]**.

![The Manage consent screen highlighting the selected audience for consent and the Next option.](../../assets/setup/add-manage-measurement-data/audience-for-consent.png){zoomable="yes"}

### Add conversion event {#add-conversion-event}

Next, define the conversion events that you want to measure the impact of your campaigns on, for example, site visits, registrations, or completed purchases. You can specify up to **3** distinct conversion events for measurement.

Provide the name of the conversion event, then use the dropdown menu to select the conversion type.

![The Add conversion event screen highlighting the conversion type dropdown menu expanded.](../../assets/setup/add-manage-measurement-data/conversion-type-dropdown.png){zoomable="yes"}

You can enter a value for the conversion, or leave it empty if you do not wish to assign a value at this time.

![The Add conversion event screen highlighting the Conversion value option.](../../assets/setup/add-manage-measurement-data/conversion-value.png){zoomable="yes"}

Next, you need to specify the duplication key to indicate which rows in your event dataset belong to the same underlying conversion event (for example, the same timestamp during a sign-up process). This prevents counting the same conversion multiple times in measurement reports. To do this, select **[!UICONTROL Duplication key]**. In the **[!UICONTROL Duplication key]** dialog, find and choose the key, followed by **[!UICONTROL Select]**.

![The Duplication key dialog showing the selected key and the Select option.](../../assets/setup/add-manage-measurement-data/duplication-key-dialog.png){zoomable="yes"}

After specifying the duplication key, you can add up to **5** conditions to include only relevant rows from the event dataset for the conversion. Choose to apply all or any of these conditions.

Select **[!UICONTROL Add condition]**, then select the condition option.

![The Add conversion event screen highlighting the condition option after selecting Add condition option.](../../assets/setup/add-manage-measurement-data/add-condition.png){zoomable="yes"}

In the **[!UICONTROL Select source field]** dialog, find and choose a source field for the condition rule, followed by **[!UICONTROL Select]**.

![The Select source field dialog highlighting the Event Type field and the Select option.](../../assets/setup/add-manage-measurement-data/select-condition-field.png){zoomable="yes"}

Use the dropdown menu to select a logic operator, then enter the value for the confition rule.

![The Add conversion event screen highlighting the dropdown for logic operator and the Value option.](../../assets/setup/add-manage-measurement-data/logic-operator-dropdown.png){zoomable="yes"}

To add another conversion event, select **[!UICONTROL Add conversion]**. You can include up to **3** conversion events in total. Once finished, review the conversion configurations and select **[!UICONTROL Next]**.

![The Add conversion event screen showing the conversion event configurations and the Next option highlighted.](../../assets/setup/add-manage-measurement-data/add-conversion-event.png){zoomable="yes"}

### Review {#review}

The **[!UICONTROL Review]** screen appears with a summary of measurement data settings. Review and ensure all the information are correct. If you need to change any section, use the **[!UICONTROL Edit]** option.

Finally, select **[!UICONTROL Complete]** to finish adding your measurement data.

![The Review screen showing a summary of measurement data settings and the Complete option highlighted.](../../assets/setup/add-manage-measurement-data/review-measurement-data.png){zoomable="yes"}

A confirmation dialog confirms that your measurement data was created successfully. You can see the new conversion events configured from your measurement data in the **[!UICONTROL My measurement data]** workspace.

![My measurement data workspace showing a list of conversion events configured from your measurement data.](../../assets/setup/add-manage-measurement-data/conversion-event-list.png){zoomable="yes"}

When in grid view or table view, select a row item or the **[!UICONTROL View conversion]** option within an event card to see an overview of a specific conversion event. It displays the event's status, source, and data connection name, along with detailed panels for:

* **[!UICONTROL Conversion details]**: Displays key information about the conversion, including its type, the duplication key used to identify unique events, and the assigned conversion value (if specified).
* **[!UICONTROL Conditions]**: Displays the condition rules applied to this conversion event.

![The Overview screen displaying the details for a conversion event.](../../assets/setup/add-manage-measurement-data/conversion-event-overview.png){zoomable="yes"}

## Next steps {#next-steps}

You have completed sourcing your measurement data in Collaboration. As an advertiser, you can now create Attribution reports to explore how your campaigns drive conversions and measure overall impact. If you're a publisher, request your collaborator to generate an Attribution report for your campaigns. For detailed instructions, see the [Create attribution report](../collaborate/measure.md#create-attribution-report) guide.
