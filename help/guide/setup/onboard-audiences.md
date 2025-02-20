---
title: Import and manage audiences
description: Learn how to import and manage audiences in Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgebeta: label="Beta" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
---
# Import and manage audiences

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently a beta product, available to select customers. The product and documentation are subject to change. Contact your Adobe representative to learn more.

Audiences are specific groups of users or customers segmented based on various attributes. These enable advertisers and publishers to collaborate on targeted marketing and personalized experiences for more effective advertising campaigns.

Use this page as your go-to for understanding all the relevant metrics that you can view related to your audiences, as well as the workflow steps to import an audience into Adobe Real-Time CDP Collaboration.

>[!TIP]
>
>Use the information in this screen to get all the information you need about your audiences, and the [discover and overlaps screens](/help/guide/collaborate/discover.md) to get insights regarding which of your audiences would work best for different campaign types, when compared with publisher inventory.

>[!BEGINSHADEBOX]

What you'll find on this documentation page:

* [Import audiences into Real-Time CDP Collaboration](#import-audiences)
* [View audiences dashboard](#view-audiences-dashboard)
* [View individual audiences](#view-individual-audiences)

>[!ENDSHADEBOX]

## Import audiences into Real-Time CDP Collaboration {#import-audiences}

>[!IMPORTANT]
>
>To import audiences, your user needs to be assigned to a role containing two Profile Management permissions - View Profiles and View Segments. For information about assigning the necessary permissions, refer to the [audience importation](../permissions/overview.md#audience-importation) guide.

Before you can share audiences with collaborators and run overlap calculations, the audiences need to be imported into Real-Time CDP Collaboration. To import audiences, follow the workflow steps in the section below.

![My audiences screen before any audiences have been added to the org.](/help/assets/setup/add-manage-audiences/org-without-audiences-added.png)

From the **[!UICONTROL My audiences]** tab, select the Plus **+** symbol, and select **Audience**.

### Select data connection {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Marketing actions"
>abstract="<p>Use marketing actions to control which audience data to import into Real-Time CDP Collaboration from Experience Platform. The **Data Collaboration** marketing action supports C4, C5 and C9 data usage labels. The **Data Science** marketing action supports the C9 data usage label.</p> <p> <ul><li> With the checkbox *enabled*, any data that is marked with the labels called out above will be imported into Real-Time CDP Collaboration.</li><li> With the checkbox *disabled*, there is no restriction on data from Experience Platform that can be imported into Real-Time CDP Collaboration.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview" text="Data usage labels overview"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference" text="Data usage labels glossary"

>[!IMPORTANT]
>
>After connecting to your first data connection and importing your first audience, you can then select to import multiple audiences from this existing data connection. In this case, the workflow will take you directly to the [select audience](#select-audience) step, since all the prerequisite information from the other steps will be imported from the existing connection.

A data connection is the source of data from where you are importing audiences into Real-Time CDP Collaboration. For the first release of Real-Time CDP Collaboration, the only supported data connection is Real-Time CDP.

Any settings such as identity mapping or scheduling that you configure for your data connection are applied to all the audiences imported from this data connection. 

>[!TIP]
>
>There is a separate workflow where you can always view and edit all the data connections that you added in this step. Read more about [managing data connections](/help/guide/setup/manage-data-connection.md).

![Select audience source screen showing options for AEP RTCDP, CSV File, Amazon S3, and Snowflake.](/help/assets/setup/add-manage-audiences/Step-Select-Audience-Source.png)

#### Select data source 

In this step, you will choose the source of your audience data. The available sources include:

* **Adobe Experience Platform**: Select this option to bring in your audiences from Adobe Experience Platform Real-Time CDP. 
* **CSV File** (Future release): Upload a CSV file containing your audience data for quick and straightforward data ingestion.
* **Amazon Web Services** (Future release): Connect to your Amazon S3 storage to import audience data directly from your S3 buckets.
* **Snowflake** (Future release): Use your Snowflake data warehouse to pull in audience data seamlessly.

#### Select sandbox

After selecting **Adobe Experience Platform** as data source, you must select the sandbox which includes the audiences that you will be importing. 

![Select sandbox for importing audiences](/help/assets/setup/add-manage-audiences/import-audiences-select-sandbox.png)

Select **[!UICONTROL Next]** after you selected the desired sandbox.

#### Governance policy and enforcement actions {#governance-policy-and-enforcement-actions}

Next, you must make sure that the correct marketing actions are set on the imported data. You are also required to provide consent for data imported from Real-Time CDP to be used for data collaboration.

Use marketing actions to control which audience data to import into Real-Time CDP Collaboration from Experience Platform. The **Data Collaboration** marketing action supports C4, C5 and C9 data usage labels. The **Data Science** marketing action supports the C9 data usage label.

Read more about the [C4, C5, and C9 data usage labels](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target=_blank}.

* With the checkbox *enabled*, any data that is marked with the labels called out above in Experience Platform is excluded and is *not* brought into Real-Time CDP Collaboration.
* With the checkbox *disabled*, there is no restriction on data from Experience Platform that can be imported into Real-Time CDP Collaboration.

Read more about data usage labels in the Experience Platform documentation:

* [Data usage labels overview](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target=_blank}
* [Data usage labels glossary](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference){target=_blank}

![Required marketing actions for data collaboration.](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png)

### Provide details

Next, provide a name and a description for you to recognize this data connection in the future. 

<!--

>[!IMPORTANT]
>
>Note a difference in terminology where the sandbox selected from Real-Time CDP is considered a dataset in the UI in Real-Time CDP Collaboration.

-->

### Map fields {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Source fields"
>abstract="Source fields are identity namespaces and attributes from your existing implementation of Real-Time CDP. You can map these to target fields defined in Real-Time CDP Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Target fields"
>abstract="The target fields correspond to the match keys that you selected when onboarding your company. Currently, hashed emails are the only supported match keys."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Apply transformation"
>abstract="When importing *non-hashed* fields from your source, use this option to have Real-Time CDP Collaboration apply the hashing and transform the plain fields into hashed fields."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_identity_namespaces"
>title="Identity namespaces"
>abstract="Select an identity namespace from the standard and custom identity namespaces available in your Experience Platform organization."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard" text="Standard and identity namespaces in Experience Platform"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_profile_attributes"
>title="Profile attributes"
>abstract="Select attributes from the Union Schema for the Profile class in Experience Platform. This view displays attributes that are present in the Union Schema and belong to the XDM Individual Profile class."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/profile/union-schemas/union-schema" text="Union schema in Experience Platform"

![Map fields screen showing source fields mapped to target fields.](/help/assets/setup/add-manage-audiences/Step-Map-Fields.png)

In the map fields step, you can select how any identity fields for the profiles brought in from the data connection should map to the match keys that you selected in your organization. 

>[!TIP]
>
>You can map multiple source fields to the same target field. For example, if you have email addresses in two separate fields in Experience Platform, you can map both of those to the **[!UICONTROL Hashed email]** target field as two separate rows.

>[!BEGINSHADEBOX]

**[!UICONTROL Source fields]** indicate how the identities are referred to in the source where you are importing data from.

**[!UICONTROL Target fields]** indicate how the identities are referred to in Real-Time CDP Collaboration. The values that you can select here correspond to the match keys that you set up in the company onboarding workflow.

Use the **[!UICONTROL Apply transformation]** option when you are importing *non-hashed* fields from your source. In this case, Real-Time CDP Collaboration will apply the hashing and transform the fields.

>[!ENDSHADEBOX]

Add as many mapping pairs as you need and select **[!UICONTROL Next]** to proceed to the next step.

<!--

In this step, you can also add any identity crosswalks that you would like to use.

Identity crosswalks will be supported after the beta release.

#### Add identity crosswalk

Use identity crosswalks to connect different identifiers across datasets to enrich your audience data with additional attributes or dimensions. 

TODO add GIF Identity crosswalks screen showing a list of available identity crosswalks with details.

Select **[!UICONTROL Add identity crosswalk]** to see a screen where you can choose from various identity crosswalks that you have previously [imported into Real-Time CDP Collaboration](/help/guide/setup/identity-crosswalk.md#import-crosswalk). Each entry includes details such as the table name, type, description, and creation date.

After selecting the desired crosswalk, use a source field join key to map to the crosswalk table join key. 

>[!NOTE]
>
>After selecting an identity crosswalk, the **[!UICONTROL Add identity crosswalk]** control is greyed out. 

For further reading about identity crosswalks, refer to the [glossary](/help/guide/glossary.md).

-->


<!-- will uncomment this part when Manage use cases part becomes available

### Manage use cases {#manage-use-cases}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_usecases"
>title="Use cases for identities"
>abstract="This control is disabled in the initial release of Real-Time CDP Collaboration"

![Manage use cases screen.](/help/assets/setup/add-manage-audiences/Step-manage-use-cases.png)

For every identity selected in the mapping step, select the use cases that you can use the identity for. Available use cases are: 

* Discover
* Share
* Activate
* Measure

Note that this control is disabled in the initial release of Real-Time CDP Collaboration.

After selecting the desired use cases for each identity, proceed to the next step. 

-->

### Schedule {#schedule}

Schedule when to start and end populating the audiences. The audience membership will be refreshed according to this schedule. For the first release of Real-Time CDP Collaboration, a daily audience import is the only available option.

>[!IMPORTANT]
>
>After the end date in the date range, all audiences imported from this data connection will stop refreshing. To renew the connection, go to [Manage data connection](/help/guide/setup/manage-data-connection.md), and set a new end date.

![Schedule screen showing start and end dates for populating the audiences.](/help/assets/setup/add-manage-audiences/Step-Schedule.png)

### Select audiences {#select-audience}

After selecting the audience source, you will choose specific audiences to include. Use the search and filter options on the page to find the relevant audiences from your selected data source.

![Select audience screen showing a list of available audiences with checkboxes to select them.](/help/assets/setup/add-manage-audiences/Step-Select-Audience.png)

### Review

Review all the configurations and settings before finalizing the audience addition. Ensure all details are correct and select **[!UICONTROL Complete]** to finalize the process.

## View audiences dashboard {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Missing identities"
>abstract="The identities count displays a `-` for approximately the first 24-hours after an audience has been imported into Real-Time CDP Collaboration. After this timeframe, the identities count will update with the number of profiles present in the audience."

After importing audiences into Real-Time CDP Collaboration, you can get information about them in a dashboard view. The default view in the **[!UICONTROL My audiences]** page displays all audiences currently imported by your organization into Real-Time CDP Collaboration. 

![Audiences overview page showing all audiences imported by an advertiser](/help/assets/setup/add-manage-audiences/audiences-overview.png)

You can view the following relevant information about each audience:

| Item | Description|
|----------|---------|
| **[!UICONTROL Identities]** | Indicates the number of identities present in this audience. Note that if the same profile has two or more identities, and these identities are used as match keys in the project, then the profile will appear twice in the count. |
| **[!UICONTROL Status]** | Indicates if the audience is active and can be used in projects. A Pending status indicates that the audience has just recently been imported and audience members are yet to populate. The imported audiences usually populate with profiles within 24-hours. |
| **[!UICONTROL Source]** | Indicates the source where this audience was imported from. In the beta release of Real-Time CDP Collaboration, Adobe Experience Platform is the only supported source. |
| **[!UICONTROL Data connection]** | Further drill-down information about where this audience was imported from. For example, when importing audiences from the Experience Platform source, the individual sandboxes that your organization has access to are considered the data connections. |
| **[!UICONTROL Connection access]** | Defines whether this audience is private or public. Public audiences are discoverable in overlap reports and can be shared with collaborators. |
| **[!UICONTROL Created]** | Indicates when this audience was imported into Real-Time CDP Collaboration. |
| **[!UICONTROL Last updated]** | Indicates the last date and time when any aspect of this audience was updated. |

Select **[!UICONTROL Manage data connections]** to view and edit all data connections that you have set up.
Select the elipsis and **[!UICONTROL Delete]** to remove the audience.
Select the elipsis and **[!UICONTROL Edit categories]** to add different category tags to the audience. Get more information in the [categories](/#categories) section below. 
Select the audience name to inspect or edit individual audiences.

## View individual audiences {#view-individual-audiences}

The audience view reveals further information about your audience.

![View and inspect individual audience.](/help/assets/setup/add-manage-audiences/view-inspect-audience.png)

Metrics that you can view in this screen are described below:

| Item | Description|
|----------|---------|
| **[!UICONTROL Status]** | Indicates if the audience is active and can be used in projects. |
| **[!UICONTROL Source]** | Indicates the source where this audience was imported from. In the beta release of Real-Time CDP Collaboration, Adobe Experience Platform is the only supported source. |
| **[!UICONTROL Data connection]** | Further drill-down information about where this audience was imported from. For example, when importing audiences from the Experience Platform source, the individual sandboxes that your organization has access to are considered the data connections. |
| **[!UICONTROL Last updated]** | Indicates the last date and time when any aspect of this audience was updated. |
| **[!UICONTROL Last updated by]** | Indicates the user who last updated this audience. |
| **[!UICONTROL Created]** | Indicates when this audience was imported into Real-Time CDP Collaboration. |
| **[!UICONTROL Created by]** | Indicates the user who imported the audience into Real-Time CDP Collaboration. |


You can use two further controls on the page to edit or remove audiences:

* **[!UICONTROL Delete]**: Remove the audience from your inventory
* **[!UICONTROL Edit]**: Edit audience metadata like its name or description.

![View and inspect individual audience.](/help/assets/setup/add-manage-audiences/audiences-edit-delete-controls.png)

Further information about the audience is available and partially editable in widgets below: 

![View and inspect individual audience.](/help/assets/setup/add-manage-audiences/audiences-further-info-boxes.png)

* [Identities](#identities)
* [Categories](#categories)
* [Connection access](#connection-access)
* [Metadata visibility](#metadata-visibility)

### Identities {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identities"
>abstract="Get a breakdown view of the identities that make up this audience, as well as a total count of profiles with the respective identities."

This section indicates the number of profiles present in the audience with any of the identities that you specified when importing the audiences. The section also contains an identity breakdown so you can tell which identities make up the most of the audience population.

### Categories {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Categories"
>abstract="Tag your audiences for easy organization, filtering, and retrieval. You can tag an audience with multiple categories and then you can use these category tags to filter your desired audiences in other areas of the product."

For easy audience organization, filtering, and retrieval, you can tag your audiences. You can tag an audience with multiple categories and then you can use these category tags to filter your desired audiences in the [discover](/help/guide/collaborate/discover.md) product area, when running audience overlap reports. 

### Connection access {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Connection access"
>abstract="<p>Audiences can be of three types: public, private, and custom.</p><p> Their availability for use in projects with collaborators differs based on the connection access setting. You can always change the connection access from private to public, but you cannot change that setting back once an audience is shared with collaborators.</p>"

Select if the audience should be private to you, or usable and discoverable in connections. The three available options are:

* **[!UICONTROL Public audience]**. These audiences are available for use in overlap reports and for sharing and activation in connections with any collaborators.
* **[!UICONTROL Private audience]**. These audiences are *not* available for use in overlap reports and for sharing and activation in connections with any collaborators. Though not available for collaborators to view or use, the population of this audience still contributes to the total population in the **[!UICONTROL All audiences]** view in the [discover and overlaps section](/help/guide/collaborate/discover.md#compare-audiences). Change the setting to public or custom to use the audiences in connections with collaborators.
* **[!UICONTROL Custom audience]**. These audiences are available for use in overlap reports and for sharing and activation in specified connections only. Though not available for all collaborators to view or use, the population of this audience still contributes to the total population in the **[!UICONTROL All audiences]** view in the [discover and overlaps section](/help/guide/collaborate/discover.md).

>[!IMPORTANT]
>
>Regardless of access status (public, private, or custom), the population of any audience contributes to the **[!UICONTROL All audiences]** population in the Audience Discovery overlap analysis view. <br> ![The system-generated **All audiences** audience in the Audience Discovery overlap analysis is inclusive of audiences with all connection access statuses (public, private, custom).](/help/assets/setup/add-manage-audiences/all-audiences-view.png "The system-generated **All audiences** audience in the **Audience Discovery** overlap analysis is inclusive of audiences with all connection access statuses (public, private, custom)."){width="100" zoomable="yes"}

Audience availability for use in projects with collaborators differs based on the connection access setting. You can always change the connection access from private to public, but you cannot change that setting back once an audience is shared with collaborators.

### Metadata visibility {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Metadata visibility"
>abstract="Indicates which of the audience metadata information is visible to other organizations before they connect with your organization. **Show identity count** controls whether your partner can view identity counts for your audiences when viewing overlap reports in the discovery tab. **Show audience overlap** controls whether collaborators are able to discover overlap percentages between their audiences and yours."

Indicates which of the audience metadata information is visible to other organizations before they connect with your organization or within different project views.

**[!UICONTROL Show identity count]**: This setting controls whether your partner can view identity counts for your audiences when [viewing overlap reports in the discovery tab](/help/guide/collaborate/discover.md#discover-overlaps). 

![Side-by-side images with the show identity count option deselected and selected.](/help/assets/setup/add-manage-audiences/show-identity-count.png)

**[!UICONTROL Show audience overlap %]**: When set to true, collaborators are able to [discover overlap percentages](/help/guide/collaborate/discover.md#compare-audiences) between their audiences and the audience that belongs to you. For example, in the recording below, the audience `agora-advertiser-aud3` has this configuration set to true and a collaborator can view overlap percentages with that audience. The audience `agora-advertiser-aud1` has this setting set to false, so the collaborator cannot view overlap percentages.

![Audience overlap percentage for two different audiences.](/help/assets/setup/add-manage-audiences/audience-overlap-percentage.gif)

## Next steps

After importing audiences, use the [Connect](/help/guide/connect/establishing-connections.md) section to discover publishers to connect with and start collaborating on projects.
