---
title: Activate audiences
description: Learn how to send audiences to collaborators and manually activate received audiences to destinations in Adobe Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
TQID: https://experienceleague.adobe.com/bfPHtcW8Mf6RhIlg5fKcJmPSEKDyAODjbNRJ5D3SMkQ
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
    internal-label: Use cases
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# Activate audiences

>[!NOTE]
>
>This page covers the **[!UICONTROL Activate]** tab within a project. To configure and manage destinations from the top-level **[!UICONTROL Activation]** workspace, see the [destinations overview](../destinations/overview.md).

>[!IMPORTANT]
>
>The **[!UICONTROL Activate]** tab is only available if the **Audience activation** use case was enabled [during the connection process](../connect/establishing-connections.md#connection-settings). For more information about use cases, see [Manage projects](./manage-projects.md#project-use-cases).

Use the project-level **[!UICONTROL Activate]** tab to send audiences to your collaborator, review audiences your collaborator has sent to you, and manually activate received audiences to a configured destination.

The tab contains the following sections:

| Section | Description |
|---|---|
| **[!UICONTROL Sent audiences to [collaborator]]** | Audiences that you have sent to your collaborator. |
| **[!UICONTROL Received audiences]** | Audiences that your collaborator has sent to you and that are available for activation. |
| **[!UICONTROL Activated audiences]** | Received audiences that you have activated to a destination. |

Sending and activating are separate actions. Sending gives your collaborator access to an audience. The receiving collaborator then selects a destination and manually activates the received audience.

![The project-level Activate tab with summary counts at the top and expanded Sent audiences, Received audiences, and Activated audiences sections. Each section displays status counts and a table of audience details.](/help/assets/collaborate/activate/activate-dashboard.png)

>[!NOTE]
>
>The sections and actions available to you depend on whether your organization is sending or receiving audiences in the project.

## Prerequisites {#prerequisites}

Before you send or activate audiences, ensure that:

- The **Audience activation** use case is enabled in the [connection settings](../connect/establishing-connections.md#connection-settings).
- Audiences are sourced and available for sending. For more information, see [Source and manage audiences](../setup/onboard-audiences.md).
- At least one destination is configured if you need to activate received audiences. For more information, see the [destinations overview](../destinations/overview.md).

## Send audiences {#send-audiences}

Send an audience to give your collaborator access to it. After you send the audience, it appears in your **[!UICONTROL Sent audiences to [collaborator]]** section and in your collaborator's **[!UICONTROL Received audiences]** section.

Navigate to the **[!UICONTROL Activate]** tab in your project.

Select the add icon (![Add icon.](/help/assets/icons/plus.png)). If no audiences have been sent, select **[!UICONTROL Send audience]** from the empty state instead.

![The project-level Activate tab when no audiences have been sent. The empty state explains that you have not sent an audience and displays a Send audience button.](/help/assets/collaborate/activate/activate-new-audiences.png)

The audience send workflow opens. Use the audience selector to find an audience, or select **[!UICONTROL Browse audiences]** to compare the available audiences.

![The Send audiences workflow with an audience selector and a Browse audiences button. The workflow allows the sender to choose an audience before configuring match keys and access settings.](/help/assets/collaborate/activate/audience-activation.png)

In the **[!UICONTROL Browse audiences]** dialog, review the **[!UICONTROL Identity count]**, **[!UICONTROL Overlapping identities]**, and **[!UICONTROL Overlap %]** for each audience.

![The Browse audiences dialog listing available audiences with their identity count, overlapping identity count, and overlap percentage.](/help/assets/collaborate/activate/browse-audiences.png)

>[!IMPORTANT]
>
>If an audience uses multiple match keys, the send operation fails when any selected match key has no audience count, no overlapping identities, or fewer than 1,000 overlapping identities. Use the [Discover tab](./discover.md) to confirm that the audience meets the overlap requirements before sending it.

Select the audience that you want to send, and then select **[!UICONTROL Save]**.

The selected audience appears in the workflow with its identity and overlap information.

![The Send audiences workflow with a selected audience showing its identity count, overlapping identity count, overlap percentage, match keys, and Edit match keys option.](/help/assets/collaborate/activate/audience-selected.png)

### Edit match keys {#edit-match-keys}

Use the match keys configured for the collaborator connection, or remove match keys that do not apply to this audience send.

Select **[!UICONTROL Edit match keys]** in the selected audience.

![The selected audience in the Send audiences workflow with the Edit match keys option highlighted.](/help/assets/collaborate/activate/edit-match-keys.png)

The **[!UICONTROL Edit match keys]** dialog appears. Turn off any match keys that you do not want to use, and then select **[!UICONTROL Save]**.

>[!NOTE]
>
>At least one match key must remain selected.

![The Edit match keys dialog with toggle controls for the match keys available through the collaborator connection and a Save button.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Configure audience access {#configure-audience-access}

Configure how often the audience is sent and how long your collaborator can access it.

Use the **[!UICONTROL Access duration]** control to select a one-time send or a recurring audience send. For a recurring send, use the date controls to define the period during which the audience remains available to your collaborator.

![The Access duration step in the Send audiences workflow with options for a one-time or recurring audience send and date controls for defining the access period.](/help/assets/collaborate/activate/activation-frequency.png)

When the audience and access settings are complete, select **[!UICONTROL Send]**.

The audience appears in your **[!UICONTROL Sent audiences to [collaborator]]** section. Your collaborator can review it in their **[!UICONTROL Received audiences]** section.

## View sent audiences {#view-sent-audiences}

Use the **[!UICONTROL Sent audiences to [collaborator]]** section to review audiences that you have sent and monitor their current access status.

Each sent audience displays the following information:

| Column | Description |
|---|---|
| **[!UICONTROL Audience name]** | The name of the sent audience. |
| **[!UICONTROL Status]** | The current status of the audience. Statuses include **[!UICONTROL Active]** and **[!UICONTROL Expired]**. |
| **[!UICONTROL Identity count]** | The number of identities in the audience. |
| **[!UICONTROL Overlapping identities]** | The number of identities that overlap with your collaborator's inventory. |
| **[!UICONTROL Created]** | The date and time when the audience was first sent. |
| **[!UICONTROL Last sent]** | The date and time when audience data was most recently sent to your collaborator. |
| **[!UICONTROL Access duration]** | The access setting configured when the audience was sent. |
| **[!UICONTROL Match keys]** | The match keys used when sending the audience. |

### Delete a sent audience {#delete-sent-audience}

Delete a sent audience to remove it from the sent-audiences list and revoke your collaborator's access.

Select the delete icon (![Delete icon.](/help/assets/icons/delete.png)) next to the audience in the **[!UICONTROL Sent audiences to [collaborator]]** section.

![The Sent audiences section with the delete icon displayed next to an audience row.](/help/assets/collaborate/activate/delete-sent-audiences.png)

A confirmation dialog appears. Select **[!UICONTROL Delete]** to confirm.

The audience is removed from the section, and your collaborator loses access to it.

![The sent-audience deletion confirmation dialog explaining that the audience will be removed and the collaborator will lose access, with Cancel and Delete buttons.](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

## View received audiences {#received-audiences}

Use the **[!UICONTROL Received audiences]** section to review audiences that your collaborator has sent to you. A received audience must be manually activated before its data is sent to a destination.

Each received audience displays the following information:

| Column | Description |
|---|---|
| **[!UICONTROL Audience name]** | The name of the received audience. |
| **[!UICONTROL Status]** | The current status of the audience. Statuses include **[!UICONTROL Active]** and **[!UICONTROL Expired]**. |
| **[!UICONTROL Identity count]** | The number of identities in the audience. |
| **[!UICONTROL Overlapping identities]** | The number of identities that overlap with your inventory. |
| **[!UICONTROL Last dataflow run]** | The date and time of the most recent dataflow run for the audience. |
| **[!UICONTROL Access duration]** | The access setting configured by the collaborator who sent the audience. |
| **[!UICONTROL Match keys]** | The match keys used for the audience. |

![The Received audiences section with active and expired audience counts. Each audience row shows its name, status, identity information, last dataflow run, access duration, match keys, and an add icon used to begin activation.](/help/assets/collaborate/activate/received-audiences-section.png)

### Activate a received audience {#activate-received-audience}

Activate a received audience to send its data to one of your configured destinations.

Select the add icon (![Add icon.](/help/assets/icons/plus.png)) next to the audience in the **[!UICONTROL Received audiences]** section.

The **[!UICONTROL Activate audience]** dialog appears.

Use **[!UICONTROL Destination]** to select the destination that receives the audience. If the destination list is empty, [configure a destination](../destinations/overview.md) before continuing.

Use **[!UICONTROL Date]** to select the date when the activation runs, and then select **[!UICONTROL Activate]**.

![The Activate audience dialog opened from a received audience. The dialog contains a Destination dropdown for selecting a configured destination, a Date field with a calendar control, and Cancel and Activate buttons.](/help/assets/collaborate/activate/activate-received-audience.png)

The dialog closes and the activation appears in the **[!UICONTROL Activated audiences]** section. The received audience remains available in the **[!UICONTROL Received audiences]** section while its access remains active.

## View activated audiences {#activated-audiences}

Use the **[!UICONTROL Activated audiences]** section to confirm which received audiences have been activated and review their destination and delivery status.

Each activated audience displays the following information:

| Column | Description |
|---|---|
| **[!UICONTROL Audience name]** | The name of the activated audience. |
| **[!UICONTROL Status]** | The current activation status. Statuses include **[!UICONTROL Active]**, **[!UICONTROL Archived]**, and **[!UICONTROL Paused]**. |
| **[!UICONTROL Activated count]** | The number of identities activated to the destination. |
| **[!UICONTROL Last refreshed]** | The date and time when the activated audience was most recently refreshed. |
| **[!UICONTROL Destination]** | The destination that receives the audience data. |
| **[!UICONTROL Frequency]** | The activation frequency. Manual activations display **[!UICONTROL Once]**. |
| **[!UICONTROL Date]** | The date when the activation runs. |
| **[!UICONTROL Match keys]** | The match keys included in the activated audience. |

![The Activated audiences section with active, archived, and paused activation counts. Each row shows the audience name, status, activated count, last refreshed date, destination, frequency, activation date, match keys, and a delete icon.](/help/assets/collaborate/activate/activated-audiences-section.png)

### Delete an activated audience {#delete-activated-audience}

Delete an activated audience to remove the activation from the **[!UICONTROL Activated audiences]** section.

Select the delete icon (![Delete icon.](/help/assets/icons/delete.png)) next to the activated audience.

A confirmation dialog appears. Select **[!UICONTROL Delete]** to confirm.

The activation is removed from the list. You can activate the received audience again later if needed.

![The activated-audience deletion confirmation dialog explaining that the audience will be removed from the activated-audiences list and can be activated again later, with Cancel and Delete buttons.](/help/assets/collaborate/activate/delete-activated-audience-confirmation.png)

## Next steps {#next-steps}

After sending or activating audiences, monitor their status in the **[!UICONTROL Sent audiences to [collaborator]]** and **[!UICONTROL Activated audiences]** sections. When campaigns are complete, work with the Adobe enablement and engineering team to upload measurement data and view the corresponding [measurement reports](./measure.md).
