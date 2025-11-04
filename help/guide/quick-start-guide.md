---
title: Real-Time CDP Collaboration Quick Start Guide
description: Learn how to onboard your organization in Real-Time CDP Collaboration, including setting up roles and organizations, audience sourcing, activation, and measurement. This guide helps collaborators configure connection settings to begin using their audiences securely and efficiently.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Limited Availability" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
---
# Real-Time CDP Collaboration quick start guide

{{limited-availability-release-note}}

Get started with Real-Time CDP Collaboration by configuring your organization, sourcing audiences, and enabling privacy-focused activation and measurement.

## Prerequisites

Before you begin, ensure you have the following:

- An active Real-Time CDP Collaboration license.
- [System or product administrator access to Adobe Experience Platform](./permissions/overview.md).
- [Access provisioned for end users](./permissions/manage-user-access.md).
- [Roles created for your organization and assigned to users](./permissions/manage-roles.md).
- Access to branding assets, such as your organization's name, logo, and banner.
- A [defined match key strategy](./setup/onboard-account.md#set-up-match-keys)
- (Optional) Access to a supported cloud source (Amazon S3 or Snowflake) if you're not using Experience Platform for audience management.

## Step 1: Complete role-based setup {#complete-role-based-setup}

Your organization's access roles determine what users can see and do in Collaboration. Before proceeding, make sure role-based permissions are set up correctly to ensure appropriate access and visibility in the platform.

**Resources:**

- [User Access Documentation](./permissions/manage-user-access.md)
- [Role Setup Documentation](./permissions/manage-roles.md)


Watch this video to learn how to assign product access and permissions for Collaboration using the Admin Console and Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3452216/?learn=on&enablevpops)

## Step 2: Set up your Collaboration account {#set-up-your-account}

Before you can source audiences, you must configure your account in Collaboration. This governs how you appear and what you have access to in the interface.

If you don't have the necessary access, please refer back to step 1 or contact your organization's administrator for help completing this setup.

Define your account's role in Collaboration, provide branding assets, and configure match keys to align audiences across connections.

>[!NOTE]
>
>You can create one or more accounts (such as advertiser and a publisher) during setup. Certain fields, like branding assets and contact email, can be updated later in the **[!UICONTROL Settings]** workspace.

- **Assign a role** – Determines whether your account is an advertiser or a publisher. Your role defines which capabilities you have in Collaboration. To learn more about how roles impact the collaboration workflow, see the [roles](./overview/roles.md) guide.
- **Branding assets** – Add the following to your account:
  - Account name (max 100 characters)
  - Description (max 1,000 characters)
  - Logo (SVG <20KB, ideally square)

>[!NOTE]
>
>If you're creating a publisher account and would like to be publicly visible in Collaboration's connections catalog, please contact your Adobe account representative. Publisher accounts require a custom brand banner (JPG 2688x1536); this file can be shared directly with your representative.

- **Contact email** – Provide a business email for collaborators to use after a connection is established.
- **Configure match keys** – Select the identifiers used for audience matching.

To learn more about initial account setup, including how to define roles, upload branding assets, and configure match keys, see the [initial account setup](./setup/onboard-account.md#initial-account-setup){target="_blank"} guide.

Watch this video for a step-by-step walkthrough of an advertiser setup, including account creation, branding, and match key configuration.

>[!VIDEO](https://video.tv.adobe.com/v/3452264/?learn=on&enablevpops)

## Step 3: Source audiences (from Experience Platform or a cloud source) {#source-audiences}

Once your account is created and your branding and match keys are configured, you're ready to begin sourcing audiences. Choose one of the following sourcing methods based on your data store and business needs.

### Option A: Source from Experience Platform

[Use Collaboration to link a sandbox that contains audiences](./setup/onboard-audiences.md). Use this self-service method to reference existing audience segments from within your Experience Platform instance.

#### Configure audiences

Configure how audiences are prepared, matched, and governed for use in connections.

- **Select audiences** *(Experience Platform only)* – Choose audience segments with supported identifiers.
- **Map match keys** – Align audience fields with the configured match keys.
- **Apply transformations** – Hash plaintext values (for example, email) if needed.
- **Schedule refreshes** – Define update frequency (for example, daily).
- **Configure consent settings** – Determine which profiles are eligible to be included in connections by selecting a consent mode: opt-in, opt-out, or none.

>[!NOTE]
>
>You can add or remove audiences and update the refresh schedule directly in Collaboration. To change other settings, such as match keys or consent mode, you must delete and recreate the data connection.

>[!IMPORTANT]
>
>**Maximum number of audiences per collaborator role:**
>
>- **Advertisers** can source up to 25 audiences.
>- **Publishers** can source up to 250 audiences (each with a minimum of 1,000 IDs).

>[!IMPORTANT]
>
>**Match key requirements:**
>
>All match keys must be **trimmed**, **lowercased**
>Hashed match keys must be **SHA256-hashed**.  
>If you provide hashed values that use uppercase characters, Collaboration automatically converts them to lowercase.  
>If your source contains **plaintext identifiers**, use the **[!UICONTROL Apply transformation]** option to apply hashing. This option is only available when sourcing audiences from Experience Platform and is not supported for cloud-based sources.
>
>For more information, see the [map fields](./setup/onboard-audiences.md#map-fields) section of the source and manage audiences guide.

To see a full walkthrough of how to source audiences using Collaboration, watch the video below.

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

Alternatively, see the document on [sourcing audiences in Collaboration](./setup/onboard-audiences.md#source-and-manage-audiences).

### Option B: Source from Snowflake or Amazon S3 

To configure a cloud source, such as [!DNL Snowflake] or [!DNL AWS S3], prepare your audience data using the [Audience Specification PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.1)

You can configure [!DNL Amazon S3] as a self-service data source. For setup instructions, see the [Amazon S3 sourcing guide](./setup/configure-aws-s3-audience-sourcing.md)

If you are using [!DNL Snowflake], or other cloud service provider, contact your Adobe account representative to finalize the setup.

>[!IMPORTANT]
>
>Cloud-based audience files must follow the required schema outlined in the Audience Specification PDF. Files must include hashed identifiers (lowercased SHA256), required metadata fields such as `segment_name` and `activation_id`, and use supported formats such as CSV or Parquet. Adobe does not normalize data before activation. TTL is enforced based on the audience's lifespan.
>
>All audiences in the uploaded file are fully sourced at this stage. The [audience visibility setting](/help/guide/setup/onboard-audiences.md#metadata-visibility) determines whether your collaborators can view your audience and is managed through the Collaboration UI.

## Step 4: Activate audiences (to Experience Platform or a cloud destination) {#activate-audiences}

Next, activate audiences to either your Experience Platform instance or a cloud destination.

### Option A: Activate to Experience Platform

Complete the following steps outlined in the [configure Adobe Experience Platform as a destination](/help/guide/destinations/experience-platform.md) guide.

- **Create a destination** – Use the UI to set up an Experience Platform destination (sandbox-level).
- **Map match keys** – Select the identifier (e.g., `hashedEmail`).
- **Define TTL** – Set expiration (1–30 days).
- **Verify in Audience Portal** – Once a collaborator sends you an audience, verify that it appears in the Audience Portal under the origin "[!UICONTROL Real-Time CDP Collaboration]."

### Option B: Activate to cloud

To configure a cloud destination (for example, [!DNL AWS S3] or [!DNL Snowflake]), contact your Adobe account representative to initiate the setup process. Depending on the cloud destination, you will need to provide cloud destination details such as file path, credentials, account locators etc. Once required information is provided, Adobe will configure the cloud destination setup.

Audience data sent to a cloud destination follows a predefined schema. For a detailed description of the required fields and format, download the [Collaboration Audience Activation Guide](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf).

## Step 5: Set up measurement (optional) {#set-up-measurement}

>[!AVAILABILITY]
>
>This feature is in **beta** and available exclusively to customers in the Limited Availability program. Contact your Adobe representative to request access.

>[!IMPORTANT]
>
>The **[!UICONTROL Measure]** workspace is only available if the **[!UICONTROL Measurement]** use case was enabled [during the connection process](./connect/establishing-connections.md#connection-settings). For more information about use cases, refer to the [manage projects](./collaborate/manage-projects.md#project-use-cases) guide.

Collaboration offers a variety of reports to analyze campaign reach, frequency, and effectiveness. While the **[!UICONTROL Measure]** workspace is available in the UI, full reporting functionality may require backend enablement.

To learn how to view and interpret measurement reports, see the [Measurement guide](./collaborate/measure.md). It covers attribution, campaign summary metrics, and dashboards such as reach curves and frequency distribution.

<!-- 
Commenting out the below information as this workflow is not yet in Beta but will be imminently. A guided measurement configuration workflow will be available in a future release."

### Configure measurement workflow

Collaboration supports two measurement workflows:

- **Attribution using Adobe Experience Platform datasets**
- **Campaign summary using only partner-provided data**

Choose the appropriate workflow below based on your campaign measurement goals.

#### Option A: Attribution using Experience Platform datasets

Use this workflow to measure conversion activity using datasets stored in Experience Platform.

1. **Create a measurement data connection**
   - Select the dataset that contains your conversion events.
   - Map identity fields from your dataset to the match keys used in Collaboration.
   - Manage consent and governance settings.
   - Define one or more conversion events to measure.
   - Review and confirm your setup.

2. **Run a measurement report**
   - Go to the **[!UICONTROL Measure]** workspace within the associated project.
   - Input the report name, date range, and report run date.
   - Select **[!UICONTROL Attribution]** as the report type.
   - Select the defined conversion event(s).
   - Submit the report. It will run on the specified date and populate within 24 hours.

#### Option B: Campaign summary using partner-provided data

Use this workflow to generate campaign summary insights based on advertiser-supplied identifiers (for example, campaign ID).

1. **Set up the connection**
   - In the connection settings, ensure **[!UICONTROL Measurement]** is selected as a use case.
   - Create a project under the connection with **[!UICONTROL Measurement]** as an activity.

2. **Provide campaign context**
   - Input required campaign identifiers (for example, **Campaign ID**) for the partner to reference.
   - Align with your partner on campaign scope and reporting timeline.

3. **Run a measurement report**
   - Navigate to the **[!UICONTROL Measure]** workspace within the project.
   - Input the report name, date range, and report run date.
   - Select **[!UICONTROL Campaign summary]** as the report type.
   - Submit the report. It will run on the selected date and populate within 24 hours. 
-->

## Step 6: Connect with collaborators {#connect-with-collaborators}

With setup complete, your organization is now ready to connect with collaborators by sending or accepting invitations and submitting project settings for approval. This connection process involves sending or receiving invitations, reviewing and submitting connection settings (such as use cases and credit consumption), and confirming the connection.

As an advertiser, use the **[!UICONTROL Connect]** workspace from the left navigation menu to browse available publishers. Alternatively, collaborators may connect with each other directly through [private connection invitations](./connect/establishing-connections.md#private-connection-invite){target="_blank"}.

>[!NOTE]
>
>Currently, only advertisers can browse publishers. Publishers cannot browse or initiate connections with advertisers.

For an overview of this flow, see the [establishing connections guide](./connect/establishing-connections.md){target="_blank"}. For a visual walkthrough of the connection process, including browsing collaborators and managing connection settings, watch the [advertiser account setup video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}.

## Next steps

You've now completed initial setup and configured your organization for secure collaboration. Next, explore the following resources to deepen your understanding of activation, measurement, and data governance:

- [Audience activation workflow documentation](./collaborate/activate.md)  
- [Measurement use cases](./collaborate/measure.md)  
- [Collaboration governance best practices](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
