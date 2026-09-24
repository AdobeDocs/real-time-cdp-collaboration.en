---
title: Create expansion audiences in Expand
description: Learn how to create expansion audiences from a seed audience using a collaborator's audience population in Adobe Real-Time CDP Collaboration.
---
# (Beta) Create expansion audiences in Expand

Use the **[!UICONTROL Expand]** tab within a project to create an expansion audience from one of your audiences. Collaboration uses your collaborator's audience population to find profiles that resemble your seed audience, helping you reach new prospects without exposing your collaborator's underlying audience data. The resulting expansion audience is sent to your collaborator for activation.

## Prerequisites {#prerequisites}

Before you can use the **[!UICONTROL Expand]** tab, you should have:

* [Sourced](/help/guide/setup/onboard-audiences.md) at least one audience to use as a seed audience
* [Connected](/help/guide/connect/establishing-connections.md) with a collaborator
* [Created a project](/help/guide/collaborate/manage-projects.md) with that collaborator
* If you are receiving an expansion audience, a [destination](/help/guide/destinations/overview.md) configured to receive activated audiences

## Expand overview {#expand-overview}

Navigate to **[!UICONTROL Collaborate]** > **[!UICONTROL My projects]**, open a project, and select the **[!UICONTROL Expand]** tab.

The **[!UICONTROL Expand]** page shows the expansion audiences created for this collaborator and the option to create a new one.

![The Expand tab showing the Expansion audiences table with the Name, Status, Model size, Audience reach, and Last updated columns.](/help/assets/collaborate/expand/expand-overview.png){zoomable="yes"}

The **[!UICONTROL Expansion audiences]** table lists every expansion audience created in the project:

| Column | Description |
|---|---|
| **[!UICONTROL Name]** | The name of the expansion audience. Defaults to the seed audience name until edited. |
| **[!UICONTROL Status]** | The current status of the expansion audience. See [expansion audience status](#expansion-audience-status) for details. |
| **[!UICONTROL Model size]** | The size of the generated expansion audience. Not available until the model finishes processing. |
| **[!UICONTROL Audience reach]** | The audience reach setting used for the expansion audience. |
| **[!UICONTROL Last updated]** | The date and time the expansion audience was last updated. |

{style="table-layout:auto"}

### Expansion audience status {#expansion-audience-status}

An expansion audience moves through the following statuses:

| Status | Description |
|---|---|
| **[!UICONTROL Processing]** | The expansion model is still generating the expansion audience. |
| **[!UICONTROL Draft]** | The model has finished, and the expansion audience is ready for you to review and send to your collaborator. |
| **[!UICONTROL Active]** | You've sent the expansion audience to your collaborator. |

{style="table-layout:auto"}

>[!NOTE]
>
>The status doesn't update in real time. Reopen or refresh the **[!UICONTROL Expand]** tab to see the latest status.

## Create an expansion audience {#create-expansion-audience}

To create a new expansion audience, select the add icon (![Add icon.](/help/assets/icons/plus.png)) on the **[!UICONTROL Expand]** page, then select **[!UICONTROL Create an expanded audience]**.


The **[!UICONTROL Generate an expansion audience]** dialog appears. Complete every field to generate the expansion audience.

![The Generate audience expansion dialog with the Seed audience, Audience reach, Match key, and Seed audience members fields.](/help/assets/collaborate/expand/generate-expansion-audience-dialog.png){zoomable="yes"}

### Select your seed audience {#select-seed-audience}

Select one of your own audiences from the **[!UICONTROL Select your seed audience]** dropdown. Collaboration uses this audience as the basis for finding similar profiles in your collaborator's population.

![The Seed audience field in the Generate audience expansion dialog.](/help/assets/collaborate/expand/select-seed-audience.png){zoomable="yes"}

### Select a match key {#select-match-key}

Enable one match key for the expansion audience. You can't enable more than one.

| Person IDs | Device IDs |
|---|---|
| **[!UICONTROL Hashed email]** | **[!UICONTROL Hashed IPv4]** |
| **[!UICONTROL Hashed phone]** | **[!UICONTROL GAID]** |
| **[!UICONTROL Loyalty ID]** | **[!UICONTROL IDFA]** |
| **[!UICONTROL CRM ID]** | **[!UICONTROL Demdex ID]** |

{style="table-layout:auto"}

>[!NOTE]
>
>If your seed audience doesn't include a given match key, that option appears disabled and can't be selected.

![The Match key section in the Generate audience expansion dialog with the available match key options.](/help/assets/collaborate/expand/select-match-key.png){zoomable="yes"}

### Select your audience reach {#select-audience-reach}

Use the **[!UICONTROL Audience reach]** dropdown to balance similarity to your seed audience with overall reach. Select **[!UICONTROL Balanced]** for  a middle ground between similarity to your seed audience and overall reach.

![The Audience reach field in the Generate audience expansion dialog with the Balanced option selected and the description text below it.](/help/assets/collaborate/expand/select-audience-reach.png){zoomable="yes"}

### Include or exclude your seed audience {#include-exclude-seed-audience}

Use the **[!UICONTROL Seed audience]** radio buttons to choose whether your original seed audience is included in or excluded from the final expansion audience.

![The Seed audience members field in the Generate audience expansion dialog with the Yes and No radio buttons.](/help/assets/collaborate/expand/include-exclude-seed-audience.png){zoomable="yes"}

### Generate the expansion audience {#generate-expansion-audience}

Once all fields are complete, select **[!UICONTROL Generate expansion audience]**. A confirmation message confirms that Collaboration is creating the expansion audience, and that you can track its progress on the **[!UICONTROL Expand]** page.

## Review and send an expansion audience {#review-send-expansion-audience}

Once an expansion audience's status updates to **[!UICONTROL Draft]**, select its name from the **[!UICONTROL Expansion audiences]** table to open it.

![The Expansion Audience A detail page showing the audience metadata, model size, seed audience size, and Send button.](/help/assets/collaborate/expand/expansion-audience-detail.png){zoomable="yes"}

From this view, you can:

* Edit the expansion audience name
* View the creation date and time
* Compare the seed audience size against the generated expansion audience size
* Review the match key used to generate the audience

When you're ready, select **[!UICONTROL Send to partner]** to send the expansion audience to your collaborator. The audience remains in **[!UICONTROL Draft]** status until you send it, then updates to **[!UICONTROL Active]**.

>[!NOTE]
>
>If your collaborator doesn't have a destination configured, **[!UICONTROL Send to partner]** is unavailable. A message explains that your collaborator needs to set up a destination first.

>[!IMPORTANT]
>
>An expansion audience expires 7 days after it's generated if it isn't sent to your collaborator.

## Receive and activate an expansion audience {#receive-activate-expansion-audience}

When you send an expansion audience, Collaboration delivers it to your collaborator according to the activation setting configured for the connection:

* If **automatic activation** is enabled, Collaboration activates the expansion audience automatically to your collaborator's configured destination, and it appears in their [Activate tab](./activate.md#activated-audiences).
<!-- Beta release: automatic activation is the only available activation setting. Uncomment the manual activation guidance below when manual activation is introduced with the GA release. -->
<!-- * If **manual activation** is enabled, the expansion audience appears in your collaborator's [Received audiences](./activate.md#received-audiences) section of the **[!UICONTROL Activate]** tab, and your collaborator must manually activate it. -->

## Next steps

Once you send your expansion audience, use the [Discover tab](./discover.md) to compare it against other audiences, or the [Activate tab](./activate.md) to track its activation.
