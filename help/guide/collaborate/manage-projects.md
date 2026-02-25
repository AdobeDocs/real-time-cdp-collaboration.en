---
title: Create and manage projects
description: Learn how to create and manage projects in Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: ae492846-bc0a-4422-86ca-577bcc1fa60c
---
# Create and manage projects

{{limited-availability-release-note}}

Projects are the centerpiece of your workflow in Adobe Real-Time CDP Collaboration. After connecting with collaborators, create a project to run audience overlap calculations and discover relevant audiences for campaigns.

>[!TIP]
>
>Projects should generally be associated with a single campaign.

![The Collaborate dashboard showing all current projects.](/help/assets/collaborate/manage-view-projects/projects-overview-page.png){zoomable="yes"}

You can use filters to view only the projects that you have started with certain collaborators, as shown below:

![Filtered view of projects with a single collaborator.](/help/assets/collaborate/manage-view-projects/filtered-project-view.png){zoomable="yes"}

## Create project {#create-project}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_create_project_advertisername_amc"
>title="Advertiser name (Amazon Marketing Cloud)"
>abstract="For Amazon Marketing Cloud (AMC) connections, this field represents the AMC instance your Amazon Ads login has access to. It does not reflect an advertiser name. If the required instance isn't listed, contact your Amazon Marketing Cloud administrator to request access."

To create a project, you must first [establish a connection](/help/guide/connect/establishing-connections.md) with a collaborator. Once the connection is established, you can create a project with that collaborator.

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_projects_advertisername"
>title="Advertiser Name"
>abstract="Select the advertiser name from the dropdown menu. The options are pre-configured by the publisher in the connection settings to ensure compatibility with their systems."

Navigate to **[!UICONTROL Collaborate]** and then **[!UICONTROL My Projects]**. If this is your first project, you can select **[!UICONTROL Create a project]**. Otherwise you can select the add icon (![Add icon.](/help/assets/icons/plus.png)) to create a new project at anytime.

![Select plus symbol or Create a project to set up a new project.](/help/assets/collaborate/manage-view-projects/create-project.png){zoomable="yes"}

The **[!UICONTROL Create project]** dialog appears. Select the **[!UICONTROL Collaborator]** you are creating the project with via the dropdown. If you're a publisher and you set advertiser names during your connection setup, you can select the **[!UICONTROL Advertiser name]**. 

>[!NOTE]
>
> If you configured a single advertiser name in the connection settings, it appears by default. If no advertiser name was set up, the advertiser's **[!UICONTROL Name]** is preselected as the **[!UICONTROL Advertiser name]**.

![Create project dialog with collaborator selected and advertiser name highlighted.](/help/assets/collaborate/manage-view-projects/create-project-advertiser-names.png){zoomable="yes"}

Next, add a **[!UICONTROL Project name]** and **[!UICONTROL Description]** for your project. Then, select an image to represent the project. This image helps to distinguish the project in the project overview page. Once you're done, select **[!UICONTROL Create]** to create the project.

![Required options to set up a new project](/help/assets/collaborate/manage-view-projects/create-project-required-info.png){zoomable="yes"}

You can now view your new project, its details, and available sections based on the use cases selected during connection setup.

![The project overview workspace.](/help/assets/collaborate/manage-view-projects/project-overview.png){zoomable="yes"}

## Manage campaign ID {#update-campaign-id}

A **Campaign ID** links your project to a specific campaign and is required to [generate measurement reports](./measure.md#create-measurement-report). You can add multiple Campaign IDs to one project if you run several campaigns with the same collaborator. All these campaigns are available for selection in reporting.

- **Publishers**: Enter or update Campaign IDs and associated names in the Collaboration UI before running reports.
- **Advertisers**: Request your collaborator (publisher) to add Campaign IDs as needed.

To add or update Campaign IDs, navigate to the **[!UICONTROL Collaborate]** workspace, then select **[!UICONTROL View]** within the relevant project card.

![The Collaborate workspace highlighting the View option within a project card.](/help/assets/collaborate/manage-view-projects/view-project.png){zoomable="yes"}

The corresponding **[!UICONTROL Project overview]** workspace appears with a **[!UICONTROL Campaign ID and name]** section that lists all campaigns linked to the project. If you have not added a campaign yet, select **[!UICONTROL Add]**. If there are already campaigns present, select **[!UICONTROL Edit]** to update details or add additional ones.

![The project overview workspace displaying the Campaign ID and name section with the Edit option highlighted.](/help/assets/collaborate/manage-view-projects/edit-campaign-id.png){zoomable="yes"}

In the **[!UICONTROL Campaign ID and name]** dialog, select **[!UICONTROL Add campaign ID]**.

![The Campaign ID and name dialog displaying the empty campaign row after selecting the Add campaign ID option.](/help/assets/collaborate/manage-view-projects/add-campaign-row.png){zoomable="yes"}

Provide the **[!UICONTROL Campaign ID]** and **[!UICONTROL Campaign name]**, then select **[!UICONTROL Save]**.

![The Campaign ID and name dialog highlighting the new campaign details and the Save option.](/help/assets/collaborate/manage-view-projects/save-campaign-id.png){zoomable="yes"}

Check the **[!UICONTROL Campaign ID and name]** section to view your latest campaigns and recent changes. You can now use the new Campaign IDs to generate measurement reports.

![The project overview workspace displaying the updated Campaign ID and name section.](/help/assets/collaborate/manage-view-projects/view-updated-campaigns.png){zoomable="yes"}
