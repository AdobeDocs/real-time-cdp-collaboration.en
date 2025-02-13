---
title: Connect with advertisers or publishers
description: After discovering potential collaborators, learn how to establish connections and start collaborating on projects.
audience: admin, publisher, advertiser
badgebeta: label="Beta" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
---
# Connect with advertisers or publishers

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently a beta product, available to select customers. The product and documentation are subject to change. Contact your Adobe representative to learn more.

Establishing a connection between two parties of a collaboration (most commonly an advertiser and a publisher) is the prerequisite in Real-Time CDP Collaboration to companies working together on campaigns. Publishers and advertisers alike can set up connections. Whichever party initiates the connection will afterwards be the *connection owner*. 

## High-level workflow

At a high level, to establish a connection between an advertiser and a publisher, the workflow looks like below:

1. The advertiser [browses publishers and discovers](/help/guide/connect/discover-publishers.md) one that they would like to work with 
2. The advertiser sends a connection invite.
3. The publisher accepts the invite.
4. The advertiser sends connection settings including match keys and others. These connection settings represent the in-product terms of the collaboration.
5. The publisher accepts connection settings. If desired, the publisher can reject the initial connection settings and request that the advertiser submits revised connection settings.

![High-level diagram of the advertiser-publisher connection process.](/help/assets/connect/establish-connection/advertiser-publisher-connection-process.png "High-level diagram of the advertiser-publisher connection process"){zoomable="yes"}

Once the items above are completed, the collaborators can proceed to [create a project](/help/guide/collaborate/manage-projects.md#create-project) to [run overlap reports](/help/guide/collaborate/discover.md) and kick off advertising campaigns.

>[!IMPORTANT]
>
>Once the connection between two collaborators has been established, the connection settings cannot be revised anymore. 

## Send invite

To set up a connection, select **[!UICONTROL Connect]** when browsing the publisher inventory in the discover publishers screen.

![Connect selector](/help/assets/connect/establish-connection/connect-selection.png)

At this point, the invite is out and you can preview the connection settings, but cannot edit them. You can view the pending invite in the **[!UICONTROL My connections]** tab. The status of the connection is **[!UICONTROL Invite sent]**.

![Pending invite sent to publisher displayed in the My connections view.](/help/assets/connect/establish-connection/pending-invite-sent.png)

Once the collaborator accepts the invite, you can configure the connection settings and send them to the collaborator to review and accept.  

## Connection settings {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="Use cases"
>abstract="The use cases are prefilled with the ones that you selected at your organizational level. You can edit the use cases."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="Match keys"
>abstract="Match keys are prefilled with the ones you selected at your organizational level. You can toggle off any match keys that you do not want to use in this connection."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit"
>title="Credit split"
>abstract="This section determines who is paying for the corresponding activities within Real-Time CDP Collaboration. Currently, only the audience sharing use case is configurable."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Audience sharing"
>abstract="Audience Sharing is the activity a party takes when requesting their matched data to be activated by their collaboration partner."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="Legal agreement"
>abstract="Verify that a data sharing agreement between the two parties exists."

After the invite is sent and accepted by your collaborator, you can now start setting up the connection settings for the connection. The connection settings define the terms of your collaboration, such as the use cases that you will accomplish together, the match keys that you will use in projects, and more. 

To set up and share connection settings with your collaborator, navigate to **[!UICONTROL My connections]**. For any connections with the status **[!UICONTROL Pending]**, you can select **[!UICONTROL Set up connection]** to configure the connection settings. You can edit and define the fields below: 

![Set up connection view](/help/assets/connect/establish-connection/connection-view.png)

+++Use cases

Use cases are prefilled with the ones that you [selected at your organizational level](/help/guide/setup/onboard-organization.md#set-up-details-use-cases).

![Use cases](/help/assets/connect/establish-connection/view-use-cases.png)

+++

+++Match keys

Match keys are prefilled with the ones you [selected at your organizational level](/help/guide/setup/onboard-organization.md#set-up-match-keys). You can toggle off any match keys that you do not want used in this connection, but you cannot at this point add any match keys that were not selected when setting up the organization.

![Match keys](/help/assets/connect/establish-connection/match-keys.png)

+++

+++Credit split

Use the credit split section to determine which of the two collaborating parties will cover the the costs for the activites.

![Credit split](/help/assets/connect/establish-connection/edit-billing-ownership.png)

+++

+++Agreements

Before you can proceed with this connection, you must acknowledge that a data sharing agreement between the two parties exists. 

![Legal agreements.](/help/assets/connect/establish-connection/legal-agreement.png)

+++

After you have made your selection, select **[!UICONTROL Submit]** to send the suggested settings to your collaborator for review.

If you are receiving proposed connection settings from your collaborator, you can either **[!UICONTROL Accept]** or **[!UICONTROL Reject]** those settings. Before accepting the connection settings, you need to acknowledge and confirm that a legal agreement is in place between you and the collaborator. If you are rejecting connection settings, reach out to your collaborator outside of the product and discuss how they should revise the connection settings for you to accept them.

## Next steps

After establishing a connection with your collaborator, you and your collaborator can now [create projects](/help/guide/collaborate/manage-projects.md#create-project).
