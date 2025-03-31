---
title: Activate audiences
description: As a publisher, learn how to activate in campaigns audiences shared with you by your collaborator. 
audience: admin, publisher
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
---
# Activate audiences

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>The **[!UICONTROL Activate]** workspace is only available if you're a publisher and the **Audience sharing and activation** use case was enabled [during the connection process](../connect/establishing-connections.md#connection-settings){target="_blank"}. For more information about use cases, refer to the [manage projects](./manage-projects.md#view-projects){target="_blank"} guide.

As a publisher, discover how to activate audiences using Adobe Real-Time CDP Collaboration. Currently, you can activate audiences to Amazon S3 locations. Additional activation channels are planned.

Only **publisher organizations** can activate audiences for campaigns. Advertiser organizations can [share audiences](/help/guide/collaborate/share.md) with publishers, who will activate these audiences in projects. Read more about the [end-to-end workflow](/help/guide/end-to-end-workflow.md) for advertisers and publishers.

## Prerequisites {#prerequisites}

As a publisher using Real-Time CDP Collaboration, you must first work with the Adobe enablement and engineering team to set up a connection to your desired Amazon S3 location. Once this is set up, you are able to activate, or export, audiences from Real-Time CDP Collaboration to your Amazon S3 location. Contact your Adobe representative to kick off this workflow.

Additionally, your connection must have the **Audience sharing and activation** use case enabled.

## Activation behavior {#activation-behavior}

After your advertiser connection shares an audience for activation, this audience immediately shows up in your **[!UICONTROL Activate]** view. The audience will be exported to your indicated location at the interval set by the advertiser in their audience share screen.

![Activate workflow to an Amazon S3 destination.](/help/assets/collaborate/activate/activate-to-amazon-s3.png)

## Next steps {#next-steps}

After activating data and running campaigns, work with the Adobe enablement and engineering team to upload measurement data and view the corresponding [measurement reports](/help/guide/collaborate/measure.md).
