---
title: Connect with advertisers or publishers
description: After discovering potential collaborators, learn how to establish connections and start collaborating on projects.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
---
# Connect with advertisers or publishers

{{limited-availability-release-note}}

Establishing a connection between two parties of a collaboration (most commonly an advertiser and a publisher) is the prerequisite in Real-Time CDP Collaboration to companies working together on campaigns. Publishers and advertisers alike can set up connections. Whichever party initiates the connection will afterwards be the *connection owner*. 

## High-level workflow

At a high level, to establish a connection between an advertiser and a publisher, the workflow looks like below:

1. The advertiser [browses publishers and discovers](/help/guide/connect/discover-publishers.md) one that they would like to work with 
2. The advertiser sends a connection invite.
3. The publisher accepts the invite.
4. The advertiser sends connection settings including match keys and others. These connection settings represent the in-product terms of the collaboration.
5. The publisher accepts connection settings. If desired, the publisher can reject the initial connection settings and request that the advertiser submits revised connection settings.

![High-level diagram of the advertiser-publisher connection process.](/help/assets/connect/establish-connection/advertiser-publisher-connection-process.png){zoomable="yes"}

Once the items above are completed, the collaborators can proceed to [create a project](/help/guide/collaborate/manage-projects.md#create-project) to [run overlap reports](/help/guide/collaborate/discover.md) and kick off advertising campaigns.

>[!IMPORTANT]
>
>Once the connection between two collaborators has been established, the connection settings cannot be revised anymore. 

## Send invite {#send-invite}

To set up a connection, select **[!UICONTROL Connect]** when browsing the publisher inventory in the discover publishers screen.

![Connect selector](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

At this point, the invite is out and you can preview the connection settings, but cannot edit them. You can view the pending invite in the **[!UICONTROL My connections]** tab. The status of the connection is **[!UICONTROL Invite sent]**.

![Pending invite sent to publisher displayed in the My connections view.](/help/assets/connect/establish-connection/pending-invite-sent.png){zoomable="yes"}

Once the collaborator accepts the invite, you can configure the connection settings and send them to the collaborator to review and accept.  

## Connection settings {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="Use cases"
>abstract="The use cases are prefilled with all options. You can edit the use cases before submitting your connection settings."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="Match keys"
>abstract="Match keys are prefilled with the ones that you selected at your organizational level. You can toggle off any match keys that you do not want to use in this connection."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit"
>title="Credit split"
>abstract="This section determines who is paying for the corresponding activities within Real-Time CDP Collaboration. Currently, only the audience sharing use case is configurable."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Audience sharing"
>abstract="Audience Sharing is the activity that a party takes when requesting their matched data to be activated by their collaboration partner."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="Measurement"
>abstract="This use case enables you to execute activities in Real-Time CDP Collaboration to generate campaign performance reports and insights."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="Legal agreement"
>abstract="Verify that a data sharing agreement between the two parties exists."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="Advertiser names"
>abstract="<p>Optional setting. Indicates the name and ID by which the advertiser is known to the publisher.</p><p>The advertiser name that you add here will be prefilled in the create project step.</p><ul><li>If the publisher configured multiple names, select one from the list.</li><li>If only one name is configured, it's preselected automatically.</li><li>If no names are configured, the field will be prefilled with the advertiser account name from Real-Time CDP Collaboration.</li></ul>"
>additional-url="https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="Create a project"

After the invite is sent, you can preview the connection settings. The invite must be accepted before you can finish setting up the connection.

![The connection settings view in the preview state.](/help/assets/connect/establish-connection/preview-connection-settings.png){zoomable="yes"}

Once the connection is accepted by your collaborator, you can now start setting up the connection settings for the connection. The connection settings define the terms of your collaboration, such as the use cases that you will accomplish together, the match keys that you will use in projects, and more. 

To set up and share connection settings with your collaborator, navigate to **[!UICONTROL My connections]**. For any connections with the status **[!UICONTROL Pending]**, you can select **[!UICONTROL Set up connection]** to configure the connection settings. 

![The My connections view with a Pending connection and its Set up connection option highlighted.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

You can edit and define the fields below: 

![Set up connection view](/help/assets/connect/establish-connection/connection-view.png){zoomable="yes"}

+++Use cases

Use cases are prefilled with all available use cases. You can choose which use cases your connection will use by selecting **[!UICONTROL Edit]** and toggling off any use cases you do not want. Selected use cases will affect which views and options are [available within your projects](../collaborate/manage-projects.md#project-use-cases).

![Use cases](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

+++

+++Match keys

Match keys are prefilled with the ones that you [selected at your organizational level](/help/guide/setup/onboard-organization.md#set-up-match-keys). You can toggle off any match keys that you do not want used in this connection, but you cannot add any match keys that were not selected when setting up the organization.

![Match keys](/help/assets/connect/establish-connection/match-keys.png)

+++

+++Credit split

Use the credit split section to determine which of the two collaborating parties will cover the costs for the activities.

![Credit split](/help/assets/connect/establish-connection/edit-billing-ownership.png)

+++

+++Agreements

Before you can proceed with this connection, you must acknowledge that a data sharing agreement between the two parties exists. 

![Legal agreements.](/help/assets/connect/establish-connection/legal-agreement.png)

+++

+++Advertiser names

As a publisher working on the connection settings, you can select to add any advertiser names by which the advertiser is known to you in your systems. As a publisher, you can add multiple advertiser names to a connection, for example, in cases where the advertiser you work with has a presence in multiple geographies. Later in the process, when [creating a project](/help/guide/collaborate/manage-projects.md#create-project) to collaborate on, you or your collaborator will be able to select the advertiser name to associate with the project.

![Add advertiser names modal.](/help/assets/connect/establish-connection/add-advertiser-names-modal.png)

Here's how the advertiser name selection works when creating a project:

1. **No advertiser name set**: If no advertiser names are added, Real-Time CDP Collaboration defaults to using the advertiser's name as the advertiser name.
2. **One advertiser name set**: If a single advertiser name is added, Real-Time CDP Collaboration automatically uses that name as the advertiser name for the project.
3. **Multiple advertiser names set**: If more than one advertiser name is added, you or your collaborator can select any of the provided names when creating the project.

![Advertiser names.](/help/assets/connect/establish-connection/advertiser-names.png)

+++

After you have made your selection, select **[!UICONTROL Submit]** to send the suggested settings to your collaborator for review.

If you are receiving proposed connection settings from your collaborator, you can either **[!UICONTROL Accept]** or **[!UICONTROL Reject]** those settings. Before accepting the connection settings, you need to acknowledge and confirm that a legal agreement is in place between you and the collaborator. If you are rejecting connection settings, reach out to your collaborator outside of the product and discuss how they should revise the connection settings for you to accept them.

## Delete connections {#delete-connections}

You can delete any connections with collaborators that you do not want to continue working with. To delete existing connections: 

1. Navigate to **[!UICONTROL Connect]** > **[!UICONTROL My connections]**.
2. Select **[!UICONTROL View connection]** on the connection card to access the connection that you want to delete.
3. Select the delete icon ![delete icon](/help/assets/common/delete.svg) to bring up the delete connection confirmation dialog.
    ![Delete connection icon highlighted.](/help/assets/connect/establish-connection/delete-icon-highlighted.png){zoomable="yes"}
4. Confirm the deletion by selecting **[!UICONTROL Delete]**.
    ![Dialog to confirm deletion of a connection. ](/help/assets/connect/establish-connection/delete-connection-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Once the connection is deleted, you will no longer be connected with the collaborator and all existing projects that are part of the collaboration will be permanently deleted and unrecoverable.

## Next steps

After establishing a connection with your collaborator, you and your collaborator can now [create projects](/help/guide/collaborate/manage-projects.md#create-project).
