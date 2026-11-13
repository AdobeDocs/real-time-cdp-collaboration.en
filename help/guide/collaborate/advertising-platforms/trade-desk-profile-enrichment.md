---
title: Enrich profiles with paid media signals from [!DNL The Trade Desk] (Alpha)
description: Learn how to export paid-media enrichment attributes, ingest the delivered CSV, and update first-party profiles for audience building and personalization.
audience: advertiser
hide: true
badge: Alpha
---

# The Trade Desk profile enrichment (Alpha)

Use the Raw Event Data Stream (REDS) impression log data feed from [!DNL The Trade Desk] to export enrichment attributes and paid media context to your first-party profiles.

After the CSV file arrives in your [!DNL Amazon S3] export destination, ingest it into [!DNL Adobe Real-Time CDP]. In this release, exporting the file does not automatically update profiles or activate experiences. Automated profile enrichment in [!DNL Adobe Real-Time CDP] is planned for a subsequent release.

Ad exposure adds context to customer profiles. It does not confirm engagement, purchase intent, or long-term interests.

## Prepare for enrichment {#prepare-for-enrichment}

Before you begin, work with your administrator, media team, and data team to ensure that you have:

* Access to [!DNL Adobe Real-Time CDP Collaboration] and a signed participation agreement.
* An access letter completed with [!DNL The Trade Desk] to authorize REDS feed provisioning.
* First-party audiences available in [!DNL Adobe Real-Time CDP Collaboration] that use hashed email addresses or hashed phone numbers. Other identifiers are not supported in this release.
* An [!DNL Amazon S3] destination configured to receive enrichment output.
* A process to ingest the delivered file into [!DNL Adobe Real-Time CDP].

### Authorize the source feed {#authorize-source-feed}

Complete the access letter provided by [!DNL The Trade Desk] to authorize [!DNL The Trade Desk] to send REDS logs directly to Adobe.

[!DNL The Trade Desk] provisions the source feed, and Adobe configures access and ingestion. Before you create a project, confirm that the connection is active and the feed is ready.

After processing, the enrichment output file arrives in your export destination.

### Prepare downstream ingestion {#prepare-downstream-ingestion}

After delivery, ask your [!DNL Adobe Real-Time CDP] administrator or technical support team to ingest the file.

## Connect and create projects {#connect-create-projects}

Complete the access letter in the connection dialog and save your Partner ID. Wait for Adobe to confirm receipt of your REDS logs before creating a project. Creating a project starts the enrichment job, which requires both your Partner ID and the logs.

### Connect with the partner {#connect-partner}

To connect with [!DNL The Trade Desk], open **[!UICONTROL Discover collaborators]** in **[!UICONTROL Connect]** and search for the partner.

![The collaborator catalog lists [!DNL The Trade Desk] and its [!UICONTROL Connect] option.](../../../assets/collaborate/advertising-platforms/discover-collaborators-trade-desk.png){zoomable="yes"}

Select **[!UICONTROL Connect]** for [!DNL The Trade Desk] and follow the instructions in the connection dialog.

![The connection dialog explains REDS authorization and Partner ID setup for [!DNL The Trade Desk].](../../../assets/collaborate/advertising-platforms/trade-desk-connection-instructions.png){zoomable="yes"}

After the connection is active, open **[!UICONTROL Connection settings]** and go to **[!UICONTROL Advertiser info]**. To update existing information, select **[!UICONTROL Edit]**. To enter new information, select **[!UICONTROL Add]**.

![The active connection settings show [!UICONTROL Advertiser info] and the [!UICONTROL Edit] control.](../../../assets/collaborate/advertising-platforms/trade-desk-connection-settings.png){zoomable="yes"}

 To save your advertiser information, enter the ID and partner name in **[!UICONTROL Partner ID]** and **[!UICONTROL Partner name]**, then select **[!UICONTROL Save]**. You can find your Partner ID under **[!UICONTROL Seat Identifiers]** in your [!DNL The Trade Desk] account.

![The Advertiser info dialog has required Partner ID and Partner name fields and a [!UICONTROL Save] control.](../../../assets/collaborate/advertising-platforms/trade-desk-advertiser-partner-info-dialog.png){zoomable="yes"}

After you save the advertiser information, wait for Adobe to confirm receipt of your REDS logs before creating a project.

### Create a project {#create-project}

To create a project, go to **[!UICONTROL Collaborate]** and select **[!UICONTROL My Projects]**, then **[!UICONTROL Create a project]** or the add icon (![Add a project.](/help/assets/icons/plus.png)).

In **[!UICONTROL Create project]**, select [!DNL The Trade Desk] from **[!UICONTROL Collaborator]**.

![The [!UICONTROL Create project] form lists [!DNL The Trade Desk] and includes project name, description, and image fields.](../../../assets/collaborate/advertising-platforms/trade-desk-create-project.png){zoomable="yes"}

To identify the project, enter a **[!UICONTROL Project name]** and **[!UICONTROL Description]**, then select an image. When the project details are complete, select **[!UICONTROL Create]**.

For general project management, see the [Create and manage projects guide](/help/guide/collaborate/manage-projects.md).

## Select and export attributes {#select-export-attributes}

To select enrichment attributes for export, open the project and select **[!UICONTROL Enrich]**. To understand signal availability, review coverage values for each attribute before selecting the attributes you want to use.

![The [!UICONTROL Enrich] page groups selectable signals by category and displays coverage values.](../../../assets/collaborate/advertising-platforms/enrich-attribute-selection.png){zoomable="yes"}

<!-- TODO: Replace the destination screenshot with one showing the [!UICONTROL Export Attributes] action. -->

Select the [!DNL Amazon S3] export destination configured for enrichment output. If you need to configure a destination, see [Configure and manage cloud storage destinations](/help/guide/destinations/manage-destinations.md).

<!-- ![The [!UICONTROL Choose a destination] screen lists a destination and the [!UICONTROL Export Attributes] action.](../../../assets/collaborate/advertising-platforms/enrich-choose-destination.png){zoomable="yes"} -->

Review the selected attributes and destination, then select **[!UICONTROL Export Attributes]**.

<!-- ![The destination screen confirms that enrichment has started.](../../../assets/collaborate/advertising-platforms/enrich-request-confirmation.png){zoomable="yes"} -->

Submitting an export starts delivery if your destination is configured correctly. After you submit the export, verify successful file delivery outside [!DNL Adobe Real-Time CDP Collaboration].

Adobe processes enrichment attributes when you create a project and then weekly. Each run uses the last 90 days of available [!DNL The Trade Desk] data. Each export includes your selected attributes from the most recent completed run. To export refreshed attributes, request another export after a later run completes.

### Available enrichment signals {#available-signals}

Select from 18 curated signals across four categories. Custom enrichment expressions are not supported.

| Category | Signal | Description |
| --- | --- | --- |
| Core | [!UICONTROL Last exposed date] | The date an identity was most recently exposed to an ad. |
| Core | [!UICONTROL Exposure count] | An exposure-frequency category, rather than a raw impression count. |
| Core | [!UICONTROL Prospecting vs retargeting] | An inferred classification of exposure as prospecting or remarketing. |
| Core | [!UICONTROL Product category shown] | An inferred category for the products promoted in the ads. |
| Core | [!UICONTROL Dominant inventory channel] | The main inventory channel associated with ad exposure. |
| Core | [!UICONTROL Dominant device type] | The main device type associated with ad exposure. |
| Geography | [!UICONTROL City] | City information derived from advertising context, not a verified location. |
| Geography | [!UICONTROL Region / State] | Region or state information from advertising context. |
| Geography | [!UICONTROL DMA] | Designated market area (DMA) information derived from advertising context. |
| Connected television (CTV) | [!UICONTROL CTV exposed] | Ad exposure on a connected television device. |
| Connected television (CTV) | [!UICONTROL Live stream viewer] | Ad exposure in live-stream inventory, not proof of viewing or engagement. |
| Connected television (CTV) | [!UICONTROL PMP / premium exposure] | Private marketplace (PMP) or private-contract exposure, not independently verified premium inventory. |
| Content affinity | [!UICONTROL Connected TV / Streaming] | Ad exposure associated with streaming content. |
| Content affinity | [!UICONTROL Gamer] | Ad exposure associated with gaming content, sites, or apps. |
| Content affinity | [!UICONTROL Sports fan] | Ad exposure associated with sports content, sites, or apps. |
| Content affinity | [!UICONTROL News follower] | Ad exposure associated with news content, sites, or apps. |
| Content affinity | [!UICONTROL Music lover] | Ad exposure associated with music content, sites, or apps. |
| Content affinity | [!UICONTROL Content genre] | The content genre associated with ad exposure. |

Geography signals describe advertising context rather than a verified home or current location. Content affinity signals do not confirm personal interests or preferences. Some attributes may not contain values when source information is unavailable.

### Attribute coverage {#attribute-coverage}

Coverage describes how often processed records include an attribute value. For yes/no signals, such as **[!UICONTROL CTV exposed]**, coverage counts records with a true value. Coverage does not indicate identity match rates or the proportion of first-party profiles that receive an attribute.

Identity matching, source-signal availability, and ingestion affect profile updates. Coverage does not confirm export completion or profile updates.

### Workflow scope {#workflow-scope}

Use the curated catalog to enrich data from [!DNL The Trade Desk]. You cannot export raw logs or create custom attribute expressions. Other demand-side platform (DSP) and supply-side platform (SSP) integrations are not supported.

This workflow does not support enrichment opportunity discovery, audience overlap analysis, or attribution and incrementality measurement.

## Ingest and validate results {#ingest-validate-results}

After delivery, ask your [!DNL Adobe Real-Time CDP] administrator or technical support team to ingest the file.

### Output file {#output-file}

The export delivers a CSV file to your configured [!DNL Amazon S3] destination.

<!-- 
TODO: replace this placeholder with the engineering-confirmed output specification:
* Required hashing and normalization for each identifier, including whether email requires SHA-256 after trimming and lowercasing.
* Exact CSV headers, the file naming pattern, and the delivery bucket and path.
* Each identifier column in the delivered file and the identity namespace to map that column to during ingestion.
Do not treat example formats or supported input match keys as confirmed output requirements.
-->

Verify the export separately from profile updates:

1. Confirm that the CSV file has arrived in the intended [!DNL Amazon S3] location.
1. Check that the file contains the expected identifiers and selected attributes.
1. Ingest the file using the confirmed identity and schema mappings for the target sandbox and dataset.
1. Review ingestion results and verify that a sample of expected profiles contains the enrichment attributes.

Exporting a file does not confirm that ingestion updated profiles. Ingest each later export separately to update profiles.

## Troubleshoot enrichment {#troubleshoot-enrichment}

Use these checks to troubleshoot source data, export, and ingestion issues:

| Issue | What to check |
| --- | --- |
| The connection or **[!UICONTROL Enrich]** is unavailable | Ask your administrator to confirm your connection and project access. Confirm that source feed setup is complete. |
| No export destination is available | Ask your administrator to confirm that a destination is configured and available for enrichment output. |
| An attribute has limited coverage | Review source-data availability with your media team. Do not interpret coverage as a profile match rate. |
| An export was requested, but no file is present | Verify the intended destination with your data team. Request submission does not confirm delivery. |
| A delivered file has not updated profiles | Review ingestion results and confirm the identity and schema mappings. Export and ingestion are separate operations. |
| You cannot request an export | Select at least one attribute and a destination. If an export is already processing, wait until it finishes before requesting another. |
| Coverage is high, but few profiles receive attributes | Coverage is not an identity match rate. Confirm that the source feed is ready, the audience uses supported match keys, and your identity mapping is correct during ingestion. |
| No attributes or coverage appear after you create a project | The project setup is fixed when you create it. If Adobe had not received your REDS logs from [!DNL The Trade Desk] at that time, the project cannot use them later. After Adobe confirms receipt of your logs, create a new project. |
| Profiles have the attributes, but an audience or experience does not reflect them | Check audience evaluation, identity, consent, and downstream experience targeting rules. |

## Next steps {#next-steps}

After you ingest and validate the attributes, build audiences in [!DNL Adobe Real-Time CDP] by combining enrichment signals with first-party data. For more information, see the [Audience Builder guide](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-builder){target="_blank"}.

To activate audiences for destinations, personalization, or customer journeys, see the [audience activation guide](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activation-overview){target="_blank"}.
