---
title: Import and manage audiences
description: Learn how to import and manage audiences
audience: admin, publisher, advertiser
badgealpha: label="Alpha" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
---

# Import and manage audiences

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently an alpha product, available to select customers. Contact your Adobe representative to learn more. 

Audiences are specific groups of users or customers segmented based on various attributes. These enable advertisers and publishers to collaborate on targeted marketing and personalized experiences for more effective advertising campaigns.

Use this page as your go-to for understanding all the relevant metrics that you can view related to your audiences, as well as the workflow steps to import an audience into Adobe Real-Time CDP Collaboration.

>[!TIP]
>
>Use the information in this screen to get all the information you need about your audiences, and the [discover and overlaps screens](/help/guide/collaborate/discover.md) to get insights regarding which of your audiences would work best for different campaign types, when intersected with publisher inventory.

## View audiences dashboard

The default view in the **[!UICONTROL My audiences]** page displays all audiences currently imported by your organization into Real-Time CDP Collaboration. 

![Audiences overview page showing all audiences imported by an advertiser](/help/assets/setup/add-manage-audiences/audiences-overview.png)

You can view the following relevant information about each audience:

| Item | Description|
|----------|---------|
| **[!UICONTROL Identities]** | Indicates the number of identities present in this audience. Note that if the same profile has two or more identities, and these identities are used as match keys in the project, then the profile will appear twice in the count. |
| **[!UICONTROL Projects]** | Indicates the number of projects in which this audience is being used. |
| **[!UICONTROL Source]** | Indicates the source where this audience was imported from. |
| **[!UICONTROL Schedule]** | Indicates how often the audience is scheduled to refresh. Available options are ... |
| **[!UICONTROL Created]** | Indicates the source where this audience was imported from |
| **[!UICONTROL Last updated]** | Indicates the latest date and time when any aspect of this audience was updated. |

Select **[!UICONTROL View]** to inspect or edit individual audiences. 

## View individual audiences {#view-individual-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identities"
>abstract="Insert content about the identities that make up this audience"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Categories"
>abstract="The audience is tagged with several category tags"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Connection access"
>abstract="Insert content about the connection access for this audience"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Metadata visibility"
>abstract="Indicates which of the audience metadata information is visible to other organizations before they connect with your organization."

The audience view reveals further information about your audience.

![View and inspect individual audience.](/help/assets/setup/add-manage-audiences/view-inspect-audience.png)

Metrics that you can view in this screen are described below:

| Item | Description|
|----------|---------|
| **[!UICONTROL Source]** | Indicates the source where this audience was imported from. |
| **[!UICONTROL Created]** | Indicates the source where this audience was imported from |
| **[!UICONTROL Created by]** | Indicates the source where this audience was imported from |
| **[!UICONTROL Last updated by]** | Indicates the source where this audience was imported from |
| **[!UICONTROL Status]** | Indicates the status of the audience. For example, the audience in the screenshot above is **[!UICONTROL archived]**. |
| **[!UICONTROL Identities]** | Indicates the number of identities present in this audience. Note that if the same profile has two or more identities, and these identities are used as match keys in the project, then the profile will appear twice in the count. |
| **[!UICONTROL Audience overlap]** | Indicates if overlap calculations should be computed between this audience and all collaborators or only a subset of collaborators. |
| **[!UICONTROL Shared in Projects]** | Indicates the number of projects in which this audience is being used. |

In this scree, three controls are available to you:

* **[!UICONTROL Archive]**: TODO - get information about what the Archive control does
* **[!UICONTROL Delete]**: Remove the audience from your inventory
* **[!UICONTROL Edit]**: Edit audience metadata like its name. or description.

## Import audiences into Real-Time CDP Collaboration

Before you can share audiences with collaborators and run overlap calculations, the audiences need to be imported into Real-Time CDP Collaboration. To import audiences, follow the workflow steps in the section below.

From the **[!UICONTROL My audiences]** tab, select the Plus **+** symbol, and select **Audience**.

### Select data connection

>[!IMPORTANT]
>
>After connecting to your first data connection and importing your first audience, you can then select to add multiple audiences from this existing data connection. In this case, the workflow will take you directly to the [select audience](#select-audience) step, since all the prerequisite information from the other steps will be imported from the existing connection.

A data connection is the source of data from where you are importing audiences into Real-Time CDP Collaboration. For the first release of Real-Time CDP Collaboration, the only supported data connection is Real-Time CDP.

Any settings such as identity mapping or scheduling that you configure for your data connection are applied to all audiences imported from the data connection. 

![Select audience source screen showing options for AEP RTCDP, CSV File, Amazon S3, and Snowflake.](/help/assets/setup/add-manage-audiences/Step-Select-Audience-Source.png)

#### Select data source 

In this step, you will choose the source of your audience data. The available sources include:

TODO: settle on available data sources for milestone one

* **Adobe Experience Platform**: Select this option to bring in your audiences from Adobe Experience Platform Real-Time CDP. 
* **CSV File** (Future release): Upload a CSV file containing your audience data for quick and straightforward data ingestion.
* **Amazon S3** (Future release): Connect to your Amazon S3 storage to import audience data directly from your S3 buckets.
* **Snowflake** (Future release): Use your Snowflake data warehouse to pull in audience data seamlessly.

#### Select sandbox

When selecting **Adobe Experience Platform** as data source, you must select the sandbox which includes the audiences that you will be importing. 

![Select sandbox for importing audiences](/help/assets/setup/add-manage-audiences/import-audiences-select-sandbox.png)

Select **[!UICONTROL Next]** after you selected the desired sandbox.

#### Provide consent to data use

Next, you must provide consent for data imported from Real-Time CDP to be used for data collaboration. Check the required marketing actions as shown below.

![Required marketing actions for data collaboration.](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png)

### Provide details

Next, provide a name and a description for you to recognize this data connection in the future. 


>[!IMPORTANT]
>
>Note a difference in terminology difference where the sandbox is considered a dataset in the UI

### Map fields {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Source fields"
>abstract="Insert content about apply transformation"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Target fields"
>abstract="Insert content about apply transformation"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Apply transformation"
>abstract="Insert content about apply transformation"

![Map fields screen showing source fields mapped to target fields.](/help/assets/setup/add-manage-audiences/Step-Map-Fields.png)

In the map fields step, you can select how any identity fields for the profiles brought in from the data connection should map to the match keys that you selected in your organization. 

>[!BEGINSHADEBOX]

**[!UICONTROL Source fields]** indicate how the identities are referred to in the source where you are importing data from.

**[!UICONTROL Target fields]** indicate how the identities are referred to in Real-Time CDP Collaboration. The values that you can select here correspond to the match keys that you set up in the company onboarding workflow. 

>[!ENDSHADEBOX]

Add as many mapping pairs as you need and select **[!UICONTROL Next]** to proceed to the next step.

In this step, you can also add any identity crosswalks that you would like to use.

#### Add identity crosswalk

Use identity crosswalks to connect different identifiers across datasets to enrich your audience data with additional attributes or dimensions. 

TODO add GIF Identity crosswalks screen showing a list of available identity crosswalks with details.

Select **[!UICONTROL Add identity crosswalk]** to see a screen where you can choose from various identity crosswalks that you have previously [imported into Real-Time CDP Collaboration](/help/guide/setup/identity-crosswalk.md#import-crosswalk). Each entry includes details such as the table name, type, description, and creation date.

After selecting the desired crosswalk, use a source field join key to map to the crosswalk table join key. 

>[!NOTE]
>
>After selecting an identity crosswalk, the **[!UICONTROL Add identity crosswalk]** control is greyed out. 

For further reading about identity crosswalks, refer to the [glossary](/help/guide/glossary.md).

### Manage use cases {#manage-use-cases}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_usecases"
>title="Use cases for identities"
>abstract="Insert content about use cases"

![Manage use cases screen.](/help/assets/setup/add-manage-audiences/Step-manage-use-cases.png)

For every identity selected in the mapping step, select the use cases that you can use the identity for. Available use cases are: 

* Discover
* Share
* Activate
* Measure

After selecting the desired use cases for each identity, proceed to the next step. 

### Schedule

![Schedule screen showing start and end dates for populating the audiences.](/help/assets/setup/add-manage-audiences/Step-Schedule.png)

Schedule when to start and end populating the audiences. The audience membership will be refreshed according to this schedule. For the first release of Real-Time CDP Collaboration, a daily audience import is the only available option

* **Start date**: Set the start date for populating the audience.
* **End date**: Set the end date for populating the audience.

### Select audience {#select-audience}

![Select audience screen showing a list of available audiences with checkboxes to select them.](/help/assets/setup/add-manage-audiences/Step-Select-Audience.png)

After selecting the audience source, you will choose specific audiences to include. Use the search and filter options to find the relevant audiences from your selected data source.

### Review

Review all the configurations and settings before finalizing the audience addition. Ensure all details are correct and complete the process.

## Next steps

After onboarding audiences, use the [Connect](/help/guide/connect-publisher-advertiser/establishing-connections.md) section to discover publishers to connect with and start collaborating on projects.

