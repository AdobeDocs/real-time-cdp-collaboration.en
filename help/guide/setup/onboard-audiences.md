---
title: Source and manage audiences
description: Learn how to source and manage audiences in Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
---
# Source and manage audiences

{{limited-availability-release-note}}

Audiences are specific groups of users or customers segmented based on various attributes. These enable collaborators to work together on targeted marketing and personalized experiences for more effective advertising campaigns. This guide covers how to source audiences into Real-Time CDP Collaboration, view the audiences dashboard, and manage individual audiences.

>[!BEGINSHADEBOX]

What you'll find on this documentation page:

* [Source audiences into Collaboration](#source-audiences)
* [View audiences dashboard](#view-audiences-dashboard)
* [View individual audiences](#view-individual-audiences)

>[!ENDSHADEBOX]

## Source audiences into Collaboration {#source-audiences}

>[!IMPORTANT]
>
>To source audiences, your user needs to be assigned to a role containing two Profile Management permissions - **[!UICONTROL View Profiles]** and **[!UICONTROL View Segments]**. For information about assigning the necessary permissions, refer to the [audience sourcing](../permissions/overview.md#audience-sourcing) guide in permissions.

Before you can activate audiences with collaborators and run overlap calculations, the audiences need to be sourced into Collaboration. To source audiences, follow the workflow steps in the section below.

From the **[!UICONTROL My audiences]** tab within the **[!UICONTROL Setup]** workspace, select the add icon (![Add icon.](/help/assets/icons/plus.png)) and then select **[!UICONTROL Audience]**. If this is your first audience, you may also select the **[!UICONTROL Add] option**.

![My audiences workspace with the Add option and Audiences option highlighted.](/help/assets/setup/add-manage-audiences/add-audiences.png)

### Select data connection {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Marketing actions"
>abstract="<p>Use marketing actions to control which audience data to import into Real-Time CDP Collaboration from Experience Platform. The <strong>Data Collaboration</strong> marketing action supports C4, C5 and C9 data usage labels. The <strong>Data Science</strong> marketing action supports the C9 data usage label.</p> <p> <ul><li> With the checkbox <em>enabled</em>, any data that is marked with the labels called out above in Experience Platform is excluded and is <strong>not</strong> brought into Real-Time CDP Collaboration.</li><li> With the checkbox <em>disabled</em>, there is no restriction on data from Experience Platform that can be imported into Real-Time CDP Collaboration.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html" text="Data usage labels overview"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html" text="Data usage labels glossary"

>[!IMPORTANT]
>
>After establishing to your first data connection and importing your first audience, you can then import multiple audiences from the existing data connection. When adding additional audiences, you'll begin from the [select audience](#select-audiences) step, since the data connection has already been established.

A data connection is the source of data from where you are sourcing audiences. Currently, the only supported data connection is Adobe Experience Platform.

Any settings such as scheduling that you configure for your data connection are applied to all the audiences sourced from this data connection. 

>[!TIP]
>
>There is a separate workflow where you can view and edit your data connections. For more information, follow the [managing data connections](/help/guide/setup/manage-data-connection.md) guide.

To begin adding your data connection, select **[!UICONTROL Add a new data connection]** and then select **[!UICONTROL Next]**.

![The Add audiences workspace with the Add a new data connection option highlighted.](/help/assets/setup/add-manage-audiences/add-data-connection.png)

#### Select data source 

Next, you'll choose the source for your data connection. The available sources include:

* **Adobe Experience Platform**: Select this option to bring in your audiences from Adobe Experience Platform. 
* **CSV File** (Future release): Upload a CSV file containing your audience data for quick and straightforward data ingestion.
* **Amazon Web Services** (Future release): Connect to your Amazon S3 storage to source audience data directly from your S3 buckets.
* **Snowflake** (Future release): Use your Snowflake data warehouse to pull in audience data seamlessly.
* **Google Cloud Platform** (Future release): Connect to your Google Cloud Storage to source audience data directly from your GCS buckets.

Select your data souce and then select **[!UICONTROL Next]**.

![The Add audiences workspace with the Adobe Experience Platform option highlighted.](/help/assets/setup/add-manage-audiences/select-data-connection-source.png)

#### Select sandbox

After selecting your data source, you must select the sandbox that includes the audiences that you to use Collaboration. Select the sandbox from the list of available sandboxes and then select **[!UICONTROL Next]**

![The Add audiences workspace with a sandbox selected.](/help/assets/setup/add-manage-audiences/select-sandbox.png)

#### Governance policy and enforcement actions {#governance-policy-and-enforcement-actions}

Next, you must make sure that the correct marketing actions are set on the sourced data. You are also required to provide consent for data sourced from Experience Platform to be used for data collaboration.

Use marketing actions to control which audience data to bring into Collaboration from Experience Platform. The **[!UICONTROL Data Collaboration]** marketing action supports C4, C5 and C9 data usage labels. The **[!UICONTROL Data Science]** marketing action supports the C9 data usage label.

Read more about the [C4, C5, and C9 data usage labels](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}.

* When the checkbox is ***enabled***, any data labeled in Experience Platform as described above is excluded and **not** brought into Collaboration.
* With the checkbox ***disabled***, there is no restriction on data sourced from Experience Platform.

Read more about data usage labels in the Experience Platform documentation:

* [Data usage labels overview](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [Data usage labels glossary](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference){target="_blank"}

Additionally, you'll want to select your consent rules to apply to data being sourced into Collaboration.

![The Add audiences workspace at the Governance policy and enforment actions section.](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png)

Once you have selected the marketing actions and consent rules, select **[!UICONTROL Next]** to proceed to the next step. A confirmation dialog will appear, asking you to accept the terms. Select the checkbox and then select **[!UICONTROL OK]** to confirm.

![The Governance policy and enforment actions dialog with the checkbox and OK option highlighted.](/help/assets/setup/add-manage-audiences/data-collaboration-consent-confirmation.png)

### Provide details

Next, provide a name and a description for your data connection. This information will help you identify the data connection later on.

![The Add audiences workspace with the option to provide a name and description.](/help/assets/setup/add-manage-audiences/data-connection-details.png)

### Map fields {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Source fields"
>abstract="Source fields are identity namespaces and attributes from your implementation of Experience Platform. You can map these to target fields defined in Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Target fields"
>abstract="Currently, hashed emails are the only supported match keys."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Apply transformation"
>abstract="When sourcing *non-hashed* fields, use this option to have Collaboration apply the hashing and transform the plain fields into hashed fields."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_identity_namespaces"
>title="Identity namespaces"
>abstract="Select an identity namespace from the standard and custom identity namespaces available in your Experience Platform organization."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html#standard" text="Standard and identity namespaces in Experience Platform"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_profile_attributes"
>title="Profile attributes"
>abstract="Select attributes from the Union Schema for the Profile class in Experience Platform. This view displays attributes that are present in the Union Schema and belong to the XDM Individual Profile class."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html" text="Union schema in Experience Platform"

Next you'll select source fields to map to target fields in Collaboration.

![The Add audiences workspace with the option to map source fields to target fields.](/help/assets/setup/add-manage-audiences/add-map-fields.png)

>[!TIP]
>
>You can map multiple source fields to the same target field. For example, if you have email addresses in two separate fields in Experience Platform, you can map each of those to the **[!UICONTROL Hashed email]** target field as two separate rows.

>[!BEGINSHADEBOX]

**[!UICONTROL Source fields]** are identity namespaces and attributes from Experience Platform. These are how the identities exist in the platform you're sourcing data from. Source fields get mapped to the target fields defined in Collaboration.

**[!UICONTROL Target fields]** indicate how the identities are referred to in Collaboration. Currently, hashed emails are the only supported match keys.

Use the **[!UICONTROL Apply transformation]** option when you are importing *non-hashed* fields from your source. In this case, Collaboration will apply the hashing and transform the fields. The hashing algorithm used by Adobe is SHA256.

>[!ENDSHADEBOX]

Select the empty source field next to the target field. The **[!UICONTROL Select source field]** dialog will appear. Select between the **[!UICONTROL Identity namespaces]** and **[!UICONTROL Profile attributes]** options to find the desired source field and then select the field from the list. You can also make use of the search option to find the desired field.

![The Select source field dialog with the email options displayed.](/help/assets/setup/add-manage-audiences/select-source-field.png)

To handle multiple email fields, map the non-hashed email source field using **[!UICONTROL Apply transformation]**.

![The Add audiences workspace with the email source fields mapped to the target field, with Apply transformation toggled on for one.](/help/assets/setup/add-manage-audiences/apply-transformation.png)

Continue adding mapping pairs as needed and then select **[!UICONTROL Next]**.

### Schedule {#schedule}

Next, schedule when to start and end populating the audiences. The audience will be refreshed according to this schedule. 

![The Add audience workspace with the scheduling options displayed.](/help/assets/setup/add-manage-audiences/audience-scheduling.png)

>[!IMPORTANT]
>
>Adjusting the frequency of audience updates will help manage the [Audience Management credit activity](/help/guide/setup/my-activity.md#types-of-activities), which is calculated per audience refresh. Selecting a higher frequency can impact of the freshness of the data available for audience discover reports and audience activation.

Select the frequency of the audience refresh from the **[!UICONTROL Frequency]** dropdown. 

![The Add audiences scheduling workspace with the Frequency dropdown open.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png)

Next, select the **[!UICONTROL Date range]**. The start date is the date when the audience will begin populating with profiles, and the end date is when the audience will stop refreshing.

![The Add audiences scheduling workspace with the Date range option displayed.](/help/assets/setup/add-manage-audiences/audience-scheduling-date-range.png)

>[!IMPORTANT]
>
>After the end date in the date range, all audiences sourced from this data connection will stop refreshing. To renew the connection, follow the [manage data connection](/help/guide/setup/manage-data-connection.md) guide.

### Select audiences {#select-audiences}

After selecting the audience source, you will choose specific audiences to include. Use the search and filter options to find the relevant audiences from your data source. Select your desired audiences and then select **[!UICONTROL Next]**.

![The Add audiences workspace with a list of available audiences.](/help/assets/setup/add-manage-audiences/select-audience.png)

### Review

Review all the configurations and settings before finalizing the audience addition. Ensure all details are correct and then select **[!UICONTROL Complete]** to finish creating your data connection.

![The Add audiences workspace with the all select configurations displayed.](/help/assets/setup/add-manage-audiences/review-connection.png)

## View audiences dashboard {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Missing identities"
>abstract="The identities count will be available after the next data connection refresh following the configured schedule. The initial refresh usually occurs within 24 hours after the data connection is set up. Ongoing refreshes will follow the configured schedule."

After sourcing audiences, the **[!UICONTROL My audiences]** workspace displays all audiences currently sourced into Collaboration.

Each audience contains an overview of the following information:

| Item | Description|
|----------|---------|
| **[!UICONTROL Identities]** | Indicates the number of identities present in this audience. Note that if the same profile has two or more identities, and these identities are used as match keys in the project, then the profile will appear twice in the count. |
| **[!UICONTROL Status]** | Indicates if the audience is active and can be used in projects. A **[!UICONTROL Pending]** status indicates that the audience has just recently been sourced and identities have yet to populate. The sourced audiences will populate with profiles after the initial refresh, which usually occurs within 24 hours after the data connection is set up. |
| **[!UICONTROL Source]** | Indicates where the audience was sourced from. In the current release of Collaboration, Experience Platform is the only supported source. |
| **[!UICONTROL Data connection]** | The data connection the audience is sourced from. You can select the name to view the data connection.  |
| **[!UICONTROL Connection access]** | Defines whether the audience is private or public. Public audiences are discoverable in overlap reports and can be activated within a project. |
| **[!UICONTROL Created]** | Indicates when the audience was initially sourced into Collaboration. |
| **[!UICONTROL Last updated]** | Indicates the last date and time when the audience was updated in Collaboration. This does not refer to when the audience was last refreshed, but rather when the audience's configuration or metadata was last changed. |

![The My audience workspace showing all audiences sourced.](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

To perform quick actions on an audience, select the ellipsis **...** next to the audience name. The following options are available:

* **[!UICONTROL Edit categories]** allows you to add different category tags to the audience. For more information, refer to the [categories](#categories) section below.
* **[!UICONTROL Delete]** will delete the audience from the data connection.

![The My audiences workspace with the ellipsis menu open and the Edit categories and Delete options highlighted.](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png)

## View individual audiences {#view-individual-audiences}

To view more information and edit configurations for an individual audience, select the audience from the **[!UICONTROL My audiences]** workspace. The audience workspace displays detailed information about the selected audience, including its details, identities, categories, connection access, and metadata visbility settings.

### Audience details

The following information is displayed for each individual audience:

| Item | Description|
|----------|---------|
| **[!UICONTROL Status]** | Indicates if the audience is active and can be used in projects. |
| **[!UICONTROL Source]** | Indicates where the audience was sourced from. In the current release of Collaboration, Experience Platform is the only supported source. |
| **[!UICONTROL Data connection]** | The data connection the audience is sourced from. |
| **[!UICONTROL Last updated]** | Indicates the last date and time when the audience was updated in Collaboration. This does not refer to when the audience was last refreshed, but rather when the audience's configuration or metadata was last changed |
| **[!UICONTROL Last updated by]** | Indicates the user who last updated the audience. |
| **[!UICONTROL Created]** | Indicates when the audience was initially sourced into Collaboration. |
| **[!UICONTROL Created by]** | Indicates the user who sourced the audience into Collaboration. |

![An individual audience's workspace.](/help/assets/setup/add-manage-audiences/audience-details.png)

Additionally, the following controls are available in the audience workspace:

* **[!UICONTROL Delete]**: Remove the audience from your data connection.
* **[!UICONTROL Edit]**: Edit audience's name or description.

![An individual audience's workspace with the Edit and Delete option highlighted.](/help/assets/setup/add-manage-audiences/audience-details-edit-delete.png)

Next, you can update the following sections within the audience's workspace:

* [Identities](#identities)
* [Categories](#categories)
* [Connection access](#connection-access)
* [Metadata visibility](#metadata-visibility)

### Identities {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identities"
>abstract="A breakdown view of the identities that make up this audience, as well as a total count of profiles with the respective identities."

The **[!UICONTROL Identities]** section indicates the number of profiles present in the audience with any of the identities you selected when sourcing the audience. The section also contains an identity breakdown so you can tell which identities make up the most of the audience population.

![The Identities section of an individual audience's workspace.](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

### Categories {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Categories"
>abstract="Tag your audiences for easy organization, filtering, and retrieval. You can tag an audience with multiple categories and then you can use these category tags to filter your desired audiences in other areas of the product."

For easy audience organization, filtering, and retrieval, you can tag your audiences. You can tag an audience with multiple categories and then you can use these category tags to filter your desired audiences in the [discover](/help/guide/collaborate/discover.md) product area, when running audience overlap reports. 

To add categories, select the **[!UICONTROL Edit]** option within the **[!UICONTROL Categories]** section. 

![The Categories section of an individual audience's workspace.](/help/assets/setup/add-manage-audiences/audience-details-categories.png)

The **[!UICONTROL Categories]** dialog will appear, allowing you to select the categories you want to add to the audience. To select an individual category, select the checkbox next to the category name. 

![The Categories dialog with the available categories displayed.](/help/assets/setup/add-manage-audiences/audience-details-categories-select.png)

### Connection access {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Connection access"
>abstract="<p>Audiences can be of three types: public, private, and custom.</p><p> Their availability for use in projects with collaborators differs based on the connection access setting. You can always change the connection access from private to public, but you cannot change that setting back once an audience is activated with collaborators.</p>"

An audience's availability for use in projects with collaborators differs based on the connection access setting. In the **[!UICONTROL Connection access]** section, you can select if the audience should be private or public. Public audiences are usable and discoverable in connections.

To update the audience's connection access, select the **[!UICONTROL Edit]** option within the **[!UICONTROL Connection access]** section.

![The Connection access section of an individual audience's workspace.](/help/assets/setup/add-manage-audiences/audience-details-connection-access.png)

The **[!UICONTROL Connection access]** dialog appears, with three available connection access options:

* **[!UICONTROL Private audience]**. These audiences are *not* available for use in overlap reports or for activation in connections with any collaborators. While the audiences are not available for collaborators to view or use, the population of the audiences still contributes to the total population in the **[!UICONTROL All audiences]** view in the [compare audiences section](/help/guide/collaborate/discover.md#compare-audiences). Change the setting to public or custom to use the audiences in connections with collaborators.
* **[!UICONTROL Public audience]**. These audiences are available for use in overlap reports and for activation in connections with any collaborators.
* **[!UICONTROL Custom audience]**. These audiences are available for use in overlap reports and for activation in specified connections only. While the audiences are not available for collaborators to view or use, the population of the audiences still contributes to the total population in the **[!UICONTROL All audiences]** view in the [compare audiences section](/help/guide/collaborate/discover.md#compare-audiences).

Select the desired connection access option and then select **[!UICONTROL Save]** to apply the changes.

![The Connection access dialog with the available options displayed.](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

>[!IMPORTANT]
>
>Regardless of access status (public, private, or custom), the population of any audience contributes to the **[!UICONTROL All audiences]** population in the **[!UICONTROL Compare audiences]** section within a project.

Audience availability for use in projects with collaborators differs based on the connection access setting. You can always change the connection access from private to public, but you cannot change that setting back once an audience is activated.

### Metadata visibility {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Metadata visibility"
>abstract="<p>Indicates which of the audience's metadata is visible to other collaborators before they connect with you or within project views.</p> <p> **Identity count** controls whether your collaborator can view identity counts for your audiences when viewing overlap reports in the discovery tab. **Audience overlap %** controls whether collaborators are able to discover overlap percentages between their audiences and yours."

>[!NOTE]
>
>If your collaborator has all audiences set to private, a project's **[!UICONTROL Relevant audiences]** section in the **[!UICONTROL Discover]** workspace will be blank. For more information, read the [discover](/help/guide/collaborate/discover.md#relevant-audiences) guide.

Metadata visibility indicates the visibility of an audience's metadata to other collaborators before they connect with you, or within different project views. To update the audience's metadata visibility, select the **[!UICONTROL Edit]** option within the **[!UICONTROL Metadata visibility]** section.

![The Metadata visibility section of an individual audience's workspace.](/help/assets/setup/add-manage-audiences/audience-details-metadata.png)

The **[!UICONTROL Metadata visibility]** dialog appears, allowing you to configure the visibility settings for the audience. There are two metadata visibility settings that you can configure for each audience:

**[!UICONTROL Show identity count]**: This setting controls whether your collaborator can view identity counts for your audiences when [viewing overlap reports in the discovery tab](/help/guide/collaborate/discover.md#discover-overlaps) within a project. 

**[!UICONTROL Show audience overlap %]**: This setting controls whether collaborators are able to [discover overlap percentages](/help/guide/collaborate/discover.md#compare-audiences) between their audiences and your audiences. 

![The Metadata visibility dialog with the available options displayed.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

## Next steps

After sourcing audiences, it's time to discover publishers to [connect](/help/guide/connect/establishing-connections.md) with to collaborate on projects.
