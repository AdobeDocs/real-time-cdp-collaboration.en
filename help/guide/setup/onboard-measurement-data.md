---
title: Add and manage measurement data
description: Learn how to add measurement data to Adobe Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
hidefromtoc: yes
hide: yes
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

## Edit measurement data {#edit-measurement-data}

After sourcing your measurement data, you can edit the details and condition rules of a conversion event at anytime.

From the **[!UICONTROL My measurement data]** tab, select the ellipsis option (![More icon](/help/assets/icons/more.png)) within the relevant conversion event card. Then select **[!UICONTROL View conversion]** from the dropdown menu to open the detailed page for that conversion event.

![My measurement data tab with the ellipsis menu open and the View conversion option highlighted.](/help/assets/setup/add-manage-measurement-data/conversion-event-list.png){zoomable="yes"}

### Edit name and description {#edit-name-and-description}

To update the event's name and description, select the edit icon (![Edit icon](/help/assets/icons/edit.png)) at the top right of the page.

![The Site Visit event page with the Edit icon on the top right highlighted.](/help/assets/setup/add-manage-measurement-data/edit-name-description.png){zoomable="yes"}

In the **[!UICONTROL Edit name and description]** dialog, update the fields with the desired values, then select **[!UICONTROL Save]** to apply your changes. 

![The Edit name and description dialog with the Save option highlighted.](/help/assets/setup/add-manage-measurement-data/edit-name-description-dialog.png){zoomable="yes"}

A confirmation dialog appears to confirm that the details are successfully updated.

### Edit conversion details {#edit-conversion-details}

You can update the following conversion details of the event:

| Field             | Description |
|-------------------|-------------|
| Conversion type   | The category of the conversion event, such as a site visit, purchase, or sign-up. |
| Duplication key   | Identifier for rows in the event dataset belonging to the same conversion event (for example, same timestamp). Prevents duplicate counts. |
| Conversion value  | The value associated with each conversion. |

{style="table-layout:auto"}

To start editing, select **[!UICONTROL Edit]** within the **[!UICONTROL Conversion details]** panel.

![The Site Visit event page highlighting the Edit option within the Conversion details panel.](/help/assets/setup/add-manage-measurement-data/edit-conversion-details.png){zoomable="yes"}

In the **[!UICONTROL Edit conversion details]** dialog, use the dropdown menu to update the conversion type. You can enter a value for the conversion, or leave it empty if you do not wish to assign a value. To edit the duplication key, select the existing key option.

![The Edit conversion details dialog with the Example Person ID option highlighted.](/help/assets/setup/add-manage-measurement-data/edit-conversion-details-dialog.png){zoomable="yes"}

The **[!UICONTROL Duplication key]** dialog displays a list of available fields grouped under options such as **[!UICONTROL Identity namespace]** and **[!UICONTROL Event schema]**. Find and choose the desired key, followed by **[!UICONTROL Select]**.

![The Duplication key dialog showing the chosen key and the Select option.](../../assets/setup/add-manage-measurement-data/edit-duplication-key-dialog.png){zoomable="yes"}

Once finished, review the updates and select **[!UICONTROL Save]** to apply your changes. 

![The Edit conversion details dialog with the Save option highlighted.](/help/assets/setup/add-manage-measurement-data/edit-conversion-details-save.png){zoomable="yes"}

A confirmation dialog appears to confirm that the details are successfully updated.

### Edit conditions {#edit-conditions}

Condition rules specify which data rows from your event dataset are included as conversions. Update these rules as needed to ensure your measurement reflects only the most relevant data for your analysis.

To edit conditions, select **[!UICONTROL Edit]** within the **[!UICONTROL Conditions]** panel.

![The Site Visit event page highlighting the Edit option within the Conditions panel.](/help/assets/setup/add-manage-measurement-data/edit-conditions.png){zoomable="yes"}

In the **[!UICONTROL Edit conversion rules]** dialog, you can view the current details of all conditions. Select an existing condition option to update its details including source field, logic rule and value.

![The Edit conversion rules dialog highlighting the options to edit source field, logic rule and value of an exisiting condition.](/help/assets/setup/add-manage-measurement-data/edit-exisiting-condition.png){zoomable="yes"}

To include additional conversion rules, select **[!UICONTROL Add condition]**. Then select the new empty condition option.

![The Edit conversion rules dialog showing the new empty condition option after selecting the Add condition option.](/help/assets/setup/add-manage-measurement-data/edit-conversion-rules-add-condition.png){zoomable="yes"}

In the **[!UICONTROL Select source field]** dialog, you can see available fields grouped under options such as **[!UICONTROL Identity namespace]** and **[!UICONTROL Event schema]**. Select the appropriate field you want to use for your condition, then choose **[!UICONTROL Select]**. You can use the **[!UICONTROL Search]** option to quickly find your preferred field.

![The Select source field dialog showing the chosen field and the Select option.](../../assets/setup/add-manage-measurement-data/edit-condition-source-key.png){zoomable="yes"}

Next, use the dropdown menu to select a logic operator from the available list and enter a value for the condition.

![The Edit conversion rules dialog highlighting the logic dropdown menu.](../../assets/setup/add-manage-measurement-data/edit-condition-logic-dropdown.png){zoomable="yes"}

Use **[!UICONTROL Include all conditions]** if all specified conditions are required for each conversion, or use **[!UICONTROL Include any of the conditions]** to allow conversions that match at least one condition. When you finish updating, review and select **[!UICONTROL Save]** to apply the changes.

![The Edit conversion rules dialog with the Save option highlighted.](/help/assets/setup/add-manage-measurement-data/edit-conversion-rules-save.png){zoomable="yes"}

A confirmation dialog appears to confirm that the details are successfully updated.

## Delete measurement data {#delete-measurement-data}

Deleting measurement data removes the associated conversion event and all linked measurement details from your project permanently. Any measurement reports that rely on this event will lose corresponding conversion metrics and can no longer be updated. This action cannot be undone.

To delete an existing conversion event, navigate to the **[!UICONTROL My measurement data]** tab in the **[!UICONTROL Setup]** workspace. In grid view, select **[!UICONTROL Delete]** within the relevant event card. In table view, select the delete icon (![Delete icon](/help/assets/common/delete.svg)) next to the event name.

![My measurement data tab highlighting the Delete option in a conversion event row.](/help/assets/setup/add-manage-measurement-data/delete-measurement-data.png){zoomable="yes"}

The **[!UICONTROL Delete measurement]** dialog appears, prompting you to confirm the deletion of the event. Select **[!UICONTROL Delete]**.

![The Delete measurement dialog with the Delete option highlighted.](/help/assets/setup/add-manage-measurement-data/delete-measurement-dialog.png){zoomable="yes"}

A confirmation dialog appears to confirm that the conversion event is successfully deleted.
