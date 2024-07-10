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

Understand all the relevant metrics that you can view related to your audiences, as well as the workflow steps to import an audience into Adobe Real-Time CDP Collaboration.

## View audiences dashboard

The default view in the **[!UICONTROL My audiences]** page displays all audiences currently imported by your organization into Real-Time CDP Collaboration. 

| Item | Description|
|----------|---------|
| **[!UICONTROL Identities]** | Indicates the number of identities present in this audience. Note that if the same profile has two or more identities, and these identities are used as match keys in the project, then the profile will appear twice in the count. |
| **[!UICONTROL Projects]** | Indicates the number of projects in which this audience is being used. |
| **[!UICONTROL Source]** | Indicates the source where this audience was imported from. |
| **[!UICONTROL Schedule]** | Indicates how often the audience is scheduled to refresh. Available options are ... |
| **[!UICONTROL Created]** | Indicates the source where this audience was imported from |
| **[!UICONTROL Last updated]** | Indicates the latest date and time when any aspect of this audience was updated. |

Select **[!UICONTROL View]** to inspect or edit individual audiences. 

## Inspect individual audiences

## Import audiences into Real-Time CDP Collaboration

Before you can share audiences with collaborators, these need to be imported into Real-Time CDP Collaboration. To import audiences, follow the workflow steps in the following sections.

From the **[!UICONTROL My audiences]** tab, select the Plus **+** symbol, and select **Audience**

### Select data connection

![Select audience source screen showing options for AEP RTCDP, CSV File, Amazon S3, and Snowflake.](/help/assets/setup/add-audiences/Step-Select-Audience-Source.png)

In this step, you will choose the source of your audience data. The available sources include:

- **Adobe Experience Platform**: Select this option to bring in your audiences from Adobe Experience Platform Real-Time CDP. 
- **CSV File** (Future release): Upload a CSV file containing your audience data for quick and straightforward data ingestion.
- **Amazon S3** (Future release): Connect to your Amazon S3 storage to import audience data directly from your S3 buckets.
- **Snowflake** (Future release): Use your Snowflake data warehouse to pull in audience data seamlessly.

### Provide details

Next, provide a name and a description for you to recognize this data connection name in the future. 

### Map fields

![Map fields screen showing source fields mapped to target fields.](/help/assets/setup/add-audiences/Step-Map-Fields.png)

In the mapping step, you can select how any identity fields for the profiles brought in from the data connection should map to the match keys that you selected in your organization. 

Add as many mapping pairs as you need and select **[!UICONTROL Next]** to proceed to the next step.

You can add more fields as necessary to ensure accurate data mapping.

#### Identity crosswalks

![Identity crosswalks screen showing a list of available identity crosswalks with details.](/help/assets/setup/add-audiences/Step-Identity-Crosswalks.png)

An identity crosswalk is a tool used to connect different identifiers across datasets to enrich your audience data with additional attributes or dimensions. Select **[!UICONTROL Add identity crosswalks]** to see a screen where you can choose from various identity crosswalks. Each entry includes details such as the table name, type, description, and creation date.

For further reading, see the [glossary](/help/guide/glossary.md).

### Manage use cases

![Manage use cases screen.](/help/assets/setup/add-audiences/Step-manage-use-cases.png)

For every identity selected in the mapping step, select the use cases thst you can use the identity for. Available use cases are: 

* Discover
* Share
* Activate
* Measure

After selecting the desired use cases for each identity, proceed to the next step. 

### Select audience

![Select audience screen showing a list of available audiences with checkboxes to select them.](/help/assets/setup/add-audiences/Step-Select-Audience.png)

After selecting the audience source, you will choose specific audiences to include. Use the search and filter options to find the relevant audiences.

### Schedule

![Schedule screen showing start and end dates for populating the audiences.](/help/assets/setup/add-audiences/Step-Schedule.png)

Schedule when to start and end populating the audiences. The audience will be updated according to this schedule. For the first release of Real-Time CDP Collaboration, a daily audience import is the only available option

- **Start date**: Set the start date for populating the audience.
- **End date**: Set the end date for populating the audience.

### Review

Review all the configurations and settings before finalizing the audience addition. Ensure all details are correct and complete the process.

## Next steps

After onboarding audiences, connect with a collaborator. 

