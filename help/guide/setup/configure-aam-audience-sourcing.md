---
title: Configure Adobe Audience Manager for Audience Sourcing
description: Learn how to connect Adobe Audience Manager as a self-service data source to ingest audience data into Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
---

# Configure Adobe Audience Manager for audience sourcing

Learn how to connect your Adobe Audience Manager (AAM) instance to Adobe Real-Time CDP Collaboration to bring your existing first-party segments directly into the platform. Once connected, Collaboration retrieves your audience data from AAM on a recurring schedule and makes those audiences available for overlap analysis and activation within your collaboration projects.

>[!NOTE]
>
> Audiences sourced from Adobe Audience Manager follow the same governance and data handling rules as audiences sourced from Adobe Experience Platform. Only segments built on first-party data sources are eligible. Third-party data and Audience Marketplace sources are not supported.

## Prerequisites {#prerequisites}

Before you connect Adobe Audience Manager, ensure that your [Collaboration account is set up](./onboard-account.md) and the following prerequisites are satisfied:

### Adobe Audience Manager access and permissions {#aam-access-and-permissions}

Before proceeding, confirm that you have:

  * Active Adobe Audience Manager contract and AAM instance provisioned. 
  * Access to the Audience Manager UI with segment view permissions.
  * Both AAM and Collaboration accounts provisioned under the same Adobe IMS Org. Cross-organization sourcing is not supported.

### Segment eligibility requirements {#aam-segments-requirements}

When you configure the connection, Collaboration automatically filters the segment list based on the following rules.

**First-party data only**

Only segments based on your own first-party data are available for sourcing. Segments that include traits from third-party data providers or AAM Audience Marketplace are excluded. This policy is consistent with the existing AAM-to-Experience Platform connector.

**Recency filter**

Only segments created or updated **within the last 13 months** are available in Collaboration. Older segments are excluded during connection setup and on each subsequent refresh.

### Consent requirements {#consent-requirements}

All AAM segments sourced into Collaboration must be filtered for consent. Only profiles with the required consent in AAM at activation are included. At the time of export, any profiles with an opt-out marker are excluded before reaching Collaboration.

>[!IMPORTANT]
>
>You are responsible for ensuring that consent is correctly configured and enforced within your Audience Manager instance before connecting to Collaboration. Adobe does not re-apply consent rules after data leaves AAM.

## Configure your Audience Manager connection {#configure-aam-connection}

Follow the steps below to connect your Adobe Audience Manager to Collaboration.

### Add a data connection {#add-data-connection}

From the **[!UICONTROL My audiences]** tab within the **[!UICONTROL Setup]** workspace, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Audience]**.  

If this is your first audience, you may also select the **[!UICONTROL Add audience]** option.

![The My audiences tab in the Setup workspace with the add icon and Add audience option displayed.](../../assets/setup/snowflake-audience-sourcing/add-audience.png)

The Add audience workflow appears. Select **[!UICONTROL Add a new data connection]** and then select **[!UICONTROL Next]**.

![The Add audiences workspace with the Add a new data connection option highlighted.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Select Adobe Audience Manager as the data connection {#select-aam}

Next, select **[!UICONTROL Adobe Audience Manager]** as a data connection, followed by **[!UICONTROL Next]**. 

![The data connection selection screen with Adobe Audience Manager available as a selectable option.](../../assets/setup/aam-audience-sourcing/audience-manager-data-source-selection.png)

<!-- A prerequisite checklist dialog appears, reminding you that only first-party segments are supported and that consent must be enforced in AAM before proceeding. Select **[!UICONTROL Start onboarding]** to confirm.  -->

<!-- ![The prerequisite checklist dialog with the Start onboarding option.](../../assets/setup/aam-audience-sourcing/prerequisite-checklist-dialog.png) -->

### Confirm consent and data use {#confirm-consent-data-use}

Before proceeding, you must confirm that your selected AAM segments have been filtered to exclude opt-out profiles in accordance with consent requirements. Check the confirmation box to acknowledge this, then select **[!UICONTROL OK]**.

<!-- SCREENSHOT -->
![alt text](image.png)


### Authenticate Adobe Audience Manager instance {#authenticate-aam-instance}

Collaboration uses your Adobe IMS Organization ID to authenticate Audience Manager, and reads segment data through the AAM Control Plane API. No separate API key or service account is required.

Your IMS Organization ID is auto-populated from your Collaboration account. Verify that it matches the organization ID associated with your AAM instance, then select **[!UICONTROL Next]**.

<!-- SCREENSHOT -->

### Select segments {#select-segments}

Next, you can see a list of eligible segments that are built from first-party data source traits and updated or created within the last 13 months.

Select the segments you want to source into Collaboration. You can also choose to search by name. Select **[!UICONTROL Next]** when you are done.

>[!TIP]
>
>If a segment you expect to see is not listed, ensure it's updated within the last 13 months and contains only first-party data source traits. Segments with third-party or Audience Marketplace traits are excluded.

<!-- SCREENSHOT -->


### Provide connection details {#provide-connection-details}

Next, enter a name and an optional description for this data connection. This helps you identify this source in the future. When finished, select **[!UICONTROL Next]**. 

<!-- SCREENSHOT -->
![alt text](image-3.png)

### Review identity mapping {#review-identity-mapping}

The **[!UICONTROL Mapping]** screen is read-only. Collaboration automatically maps the identity output from your AAM segments to Collaboration identity fields. Audience membership is sourced as a list of Demdex IDs, with each record representing a profile that is a member of each selected segment. See the table below for more details.

| AAM identity output | Collaboration identity field | Notes                                                                         |
| ------------------- | ---------------------------- | ----------------------------------------------------------------------------- |
| `Demdex ID`         | `DEMDEX_ID`                  | Primary identity output for this integration. No ECID translation is applied. |

{style="table-layout:auto"}

<!-- SCREENSHOT -->

![alt text](image-4.png)

### Schedule data fresh {#schedule-data-fresh}

In the **[!UICONTROL Schedule]** screen, set the frequency at which Collaboration retrieves updated audience membership data from your AAM segments, and define the active date range for sourcing.

Use the **[!UICONTROL Frequency]** dropdown to select a refresh interval between one and six days. Then use the calendar to set start and end dates for sourcing audience. When the end date is reached, sourcing stops and previously sourced audiences expire.

Once finished, select **[!UICONTROL Next]**.

>[!IMPORTANT]
>
>AAM segments typically refresh every 24–48 hours based on trait recency and frequency rules. Setting a Collaboration refresh interval shorter than this may consume Collaboration credits without updated results. To monitor your credit usage, see [Track your credit consumption activity](./my-activity.md).

<!-- SCREENSHOT -->
![alt text](image-5.png)

### Review and complete the connection {#review-and-complete}

Finally, review the full configuration summary before creating the connection. The summary screen shows the following sections: 

* **[!UICONTROL Data connection]**: Your IMS Organization ID and the AAM segments you selected. 
* **[!UICONTROL Details]**:: The name and optional description of this data connection. 
* **[!UICONTROL Mapping]**: The identity field mapping from AAM Demdex ID to the Collaboration identity field. 
* **[!UICONTROL Schedule]**: The refresh frequency and active date range. 

Select the pencil icon (![Edit icon](/help/assets/icons/edit.png)) if you need to edit a section. Select **[!UICONTROL Complete]** to confirm all sections.

A confirmation dialog appears, indicating that the data connection was created and that audience sourcing is in progress.

<!-- SCREENSHOT -->

## Review sourced audiences {#review-sourced-audiences}

After the setup is complete, Collaboration begins sourcing the audience membership data from your selected AAM segments. If audience sourcing is in progress, a banner is displayed at the top of the **[!UICONTROL My audiences]** view.

<!-- ![My audiences tab shows the Audience sourcing in progress banner.](../../assets/setup/aam-audience-sourcing/audience-sourcing-in-progress.png) -->

Once sourcing completes, your AAM segments appear in the **[!UICONTROL My audiences]** tab. The **[!UICONTROL Source]** column identifies them as **[!UICONTROL Adobe Audience Manager]**. 

Select a row or the **[!UICONTROL View audience]** option to see an overview of a specific audience. It displays the audience's status, source, and data connection name, along with detailed panels for **[!UICONTROL Identities]**, **[!UICONTROL Categories]**, **[!UICONTROL Connection access]**, and **[!UICONTROL Metadata visibility]**. See [how to view an individual audience](./onboard-audiences.md#view-individual-audiences) for details.

Use this view to confirm audience configuration and visibility settings before using the audience in collaboration projects.

## Troubleshooting {#troubleshooting}

Read this section to resolve common issues after you establish the initial connection.

**Audiences are not appearing or sourcing is taking longer than expected**

* Sourcing time scales with the number of selected segments and the size of each segment population. 
* If audiences do not appear within 24 hours, confirm that the segments you selected are still active in Adobe Audience Manager and have non-zero population counts. 
* Check the **[!UICONTROL My data connections]** tab for any error indicators on the connection. 
* If the issue persists, contact Adobe customer support with your data connection name and the names of the segments that are not appearing.

**A segment I expected to select was not available during setup**

Confirm that the segment:

* Was created or last updated within the past 13 months. Older segments are not shown.
* Uses only first-party traits. Segments with third-party or Audience Marketplace traits are excluded.
* Belongs to the IMS Organization configured for the connection. 

**The data connection shows a failed status after initially succeeding**

* Confirm the IMS organization relationship between your Adobe Audience Manager instance and Collaboration account has not changed.
* Confirm the selected segments still exist in Adobe Audience Manager and have not been deleted.
* If the issue persists, [delete the connection](./manage-data-connection.md#delete-data-connection) and create a new one, or contact Adobe Customer Support.

## Next steps {#next-steps}

You have now successfully configured and connected your Adobe Audience Manager as a data source in Collaboration. After sourcing completes, your audiences are available in the **[!UICONTROL My audiences]** workspace and ready for use in collaboration projects.

From here, you can:

*[Create and manage collaboration projects](../collaborate/manage-projects.md)
*[Activate audiences within a project](../collaborate/activate.md)
*[Review overlaps and measure performance](../collaborate/measure.md)
*[Manage audience settings and visibility](./onboard-audiences.md)
*[Manage your data connections](./manage-data-connection.md)

<!-- Note: Can replace the next section with reference to the Sources overview when Sources overview is published -->

For other audience sourcing methods, see:

* [Source audiences from Experience Platform](./onboard-audiences.md)
* [Configure [!DNL Amazon S3] for audience sourcing](./configure-aws-s3-audience-sourcing.md)
* [Configure [!DNL Google Cloud Storage] for audience sourcing](./configure-gcs-audience-sourcing.md)
* [Configure [!DNL Snowflake] for audience sourcing](./configure-snowflake-audience-sourcing.md)
* [Upload a CSV file for audience sourcing](./upload-csv-audience-sourcing.md)
