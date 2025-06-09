---
title: Connect with advertisers or publishers
description: After discovering potential collaborators, learn how to establish connections and start collaborating on projects.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
---
# Connect with advertisers or publishers

{{limited-availability-release-note}}

Before collaborators (typically an advertiser and a publisher) can work together on campaigns, they must establish a connection. This connection allows them to activate audiences, create projects, and run reports on campaign performance.

## High-level workflow

To establish a connection between an advertiser and a publisher, the following steps are required:

1. The advertiser [browses publishers and discovers](/help/guide/connect/discover-publishers.md) one that they would like to work with.
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

![The Connect dashboard with the Connect option highlighted on a specific publisher.](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

After the invite is sent, you can preview (but not edit) the connection settings. View pending invites in the **[!UICONTROL My connections]** tab. The connection status appears as **[!UICONTROL Invite sent]**.

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
>abstract="This section determines who is paying for the corresponding activities within Real-Time CDP Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Audience sharing"
>abstract="Audience activation credits are consumed based on the number of matched IDs prepared for activation."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="Measurement"
>abstract="Execute activities to generate campaign performance reports and insights. Credits are consumed based on the number of rows in campaign reports across all campaigns and the frequency of reporting (daily, every three days, or weekly)."

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

### Advertiser connection settings {#advertiser-connection-settings}

After your collaborator accepts the connection, set up the connection settings. These settings define your collaboration terms, including the use cases you'll work on, the match keys for projects, and other configurations. 

To begin, navigate to **[!UICONTROL My connections]**. For any connections with the status **[!UICONTROL Pending]**, you can select **[!UICONTROL Set up connection]** to configure the connection settings. 

![The My connections workspace with a Pending connection and its Set up connection option highlighted.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

You can edit and define the fields below: 

![The connection settings workspace before it's filled in.](/help/assets/connect/establish-connection/connection-view.png){zoomable="yes"}

+++Use cases

Use cases are prefilled with all available options. To customize them, select **[!UICONTROL Edit]** in the **[!UICONTROL Use cases]** section and turn off any you don't want. Selected use cases determine which views and options are [available within your projects](../collaborate/manage-projects.md#project-use-cases).

![The Use cases settings in the connection settings workspace.](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

+++

+++Match keys

Match keys are prefilled with the ones you selected while [setting up your organization](/help/guide/setup/onboard-organization.md#set-up-match-keys). You can toggle off any match keys you don't want to use, but you can't add match keys that weren't selected during organization setup.

![The Match key settings in the connection settings workspace.](/help/assets/connect/establish-connection/match-keys.png){zoomable="yes"}

+++

+++Credit split

Use the credit split section to determine which of the two collaborating parties will cover the costs for the activities. Credit split options are determined by the selected use cases for the connection. While the **[!UICONTROL Measurement]** use case requires one party to cover the costs, the **[!UICONTROL Audience activation]** use case gives an additional option to have each party cover their own costs. For information on the breakdown of costs, read the [credit activity types](/help/guide/setup/my-activity.md#types-of-activities) guide.

>[!NOTE]
>
>Audience - Egress is always covered by the the collaborator that receives the audience, therefore no selection is required.

![The Credit split dialog with options in the connection workspace.](/help/assets/connect/establish-connection/credit-split.png){zoomable="yes"}
+++

+++Agreements

Before you can proceed with this connection, you must acknowledge that a data sharing agreement between the two parties exists. 

![The Legal agreement section highlight and confirmed in the connection workspace.](/help/assets/connect/establish-connection/legal-agreement.png){zoomable="yes"}

+++

After you have made your selections, select **[!UICONTROL Submit]** to send the suggested settings to your collaborator for review.

### Publisher connection settings {#publisher-connection-settings}

The publisher then needs to review the connection settings and either accept or reject them. To review the connection settings, navigate to **[!UICONTROL My connections]** and select **[!UICONTROL Review connection settings]** in the connection card.

![The Review connection settings option highlighted in the My connections view.](/help/assets/connect/establish-connection/review-connection-settings.png){zoomable="yes"}

Review the settings the collaborator has proposed. Before accepting the connection settings, you must acknowledge that a legal agreement is in place between you and the collaborator. Additionally, you can add any advertiser names by which the advertiser is known to you in your systems. 

![The connection settings workspace with the proposed settings from the collaborator and the Advertiser names and Agreements sections highlighted.](/help/assets/connect/establish-connection/publisher-connection-settings.png){zoomable="yes"}

+++Advertiser names

As a publisher working on the connection settings, you can select to add any advertiser names by which the advertiser is known to you in your systems. As a publisher, you can add multiple advertiser names to a connection, for example, in cases where the advertiser you work with has a presence in multiple geographies. Later in the process, when [creating a project](/help/guide/collaborate/manage-projects.md#create-project) to collaborate on, you or your collaborator will be able to select the advertiser name to associate with the project.

![The Advertiser names dialog in the connection settings workspace.](/help/assets/connect/establish-connection/add-advertiser-names-modal.png)

Here's how the advertiser name selection works when creating a project:

1. **No advertiser name set**: If no advertiser names are added, Real-Time CDP Collaboration defaults to using the advertiser's name as the advertiser name.
2. **One advertiser name set**: If a single advertiser name is added, Real-Time CDP Collaboration automatically uses that name as the advertiser name for the project.
3. **Multiple advertiser names set**: If more than one advertiser name is added, you or your collaborator can select any of the provided names when creating the project.

![The connection settings workspace with the Advertiser names section filled in.](/help/assets/connect/establish-connection/advertiser-names.png)

+++

>[!NOTE]
>
> Once you've accepted the connection settings, you are no longer able to add or edit advertiser names.

If you are satisfied with the proposed connection settings, select **[!UICONTROL Accept]** to establish the connection. If you want to request changes to the connection settings, select **[!UICONTROL Reject]**. The collaborator can then revise the connection settings and resend them for review.

## Delete connections {#delete-connections}

You can delete any connections with collaborators that you do not want to continue working with. To delete existing connections, navigate to **[!UICONTROL Connect]**. Advertisers should then navigate to **[!UICONTROL My connections]**. Select **[!UICONTROL View connection]** on the connection card to open the connection you want to delete.

![The View connection option highlighted in the My connections view.](/help/assets/connect/establish-connection/delete-view-connection.png){zoomable="yes"}

Select the delete icon ![delete icon](/help/assets/common/delete.svg) in the connection workspace to delete the connection.

![The delete icon highlighted in the connection workspace.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

A confirmation dialog appears, asking you to confirm the deletion of the connection. Select **[!UICONTROL Delete]** to confirm the deletion.

![The confirmation dialog to delete a connection.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Once the connection is deleted, you will no longer be connected with the collaborator and all existing projects that are part of the collaboration will be permanently deleted and unrecoverable.

## Next steps

After establishing a connection with your collaborator, you and your collaborator can now [create projects](/help/guide/collaborate/manage-projects.md#create-project).
