---
title: Real-Time CDP Collaboration Onboarding Quick Start
description: Learn how to onboard your organization in Real-Time CDP Collaboration, including setting up roles and organizations, audience provisioning, activation, and measurement. This guide helps advertisers and publishers configure collaboration settings and begin using shared audiences securely and efficiently.
audience: admin, publisher, advertiser
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
---
# Real-Time CDP Collaboration onboarding quick start

Get started with Real-Time Customer Data Platform (CDP) Collaboration by configuring your organization, provisioning audiences, and enabling privacy-focused activation and measurement.

## Prerequisites

Before you begin, ensure you have the following:

- An active Real-Time CDP Collaboration license.
- [System or product administrator access to Adobe Experience Platform](./permissions/overview.md#use-cases).
- [Access provisioned for end users](./permissions/manage-user-access.md).
- [Roles created for your organization and assigned to users](./permissions/manage-roles.md).
- Access to branding assets, such as your organization's name, logo, and banner.
- A [defined match key strategy](./setup/onboard-organization.md#set-up-match-keys) (currently, hashed email is the only supported match key).
- (Optional) Access to a supported cloud source (Amazon S3 or Snowflake) if you're not using Experience Platform as a destination.

## Step 1: Complete role-based setup {#complete-role-based-setup}

>[!NOTE]
>
>This step applies to both advertisers and publishers.

Your organization's access roles determine what users can see and do in Real-Time CDP Collaboration. Before proceeding, make sure role-based permissions are set up correctly to ensure appropriate access and visibility in the platform.

**Resources:**

- [User Access Documentation](./permissions/manage-user-access.md)
- [Role Setup Documentation](./permissions/manage-roles.md)


Watch this video to learn how to assign product access and permissions for Collaboration using the Admin Console and Experience Platform UI.

>[!VIDEO](https://video.tv.adobe.com/v/3452216/?learn=on&enablevpops)

## Step 2: Set up your Real-Time CDP Collaboration organization {#set-up-your-organization}

>[!NOTE]
>
>This step applies to both advertisers and publishers.

Before you can add audiences, you must configure your organization in Collaboration. This governs how your organization appears and behaves in the interface. 

If you don't have admin access to Experience Platform, contact your organization's administrator for help completing this setup.

Define your organization's role in Collaboration, provide branding assets, and configure match keys to align audiences across connections. Then, complete the steps below to finalize setup and prepare your organization to engage with your connections.

>[!NOTE]
>
>You can create one or more collaborators (such as advertiser or publisher profiles) during setup. Certain fields, like branding assets and contact email, can be updated later in the **[!UICONTROL Settings]** workspace. Match keys can be removed at the project level, but not added, so plan them carefully.

- **Assign a role** – Determines whether your organization acts as an advertiser, publisher, or both. Your role defines which collaboration capabilities you have, such as initiating audience sharing (advertiser) or making audiences available (publisher). To learn more about how roles impact the collaboration workflow, see the [End-to-end workflow guide](./end-to-end-workflow.md).
- **Branding assets** – Add the following to your account:
  - Brand name (max 100 characters)
  - Brand description (max 1,000 characters)
  - Brand logo (SVG <20KB, ideally square)
  - Brand banner (JPG 2688x1536 or similar)
- **Contact email** – Provide a business email for collaborators to use after a connection is established.

  >[!NOTE]
  >
  >If you are creating a publisher account and would like to be publicly visible in Collaboration's connections catalog, please contact your Adobe account representative. Publisher accounts require a custom brand banner (JPG 2688x1536); this file can be shared directly with your representative.

- **Configure match keys** – Select the identifiers used for audience matching (currently, hashed email is the only supported match key).

Once your organization is created and your branding and match keys are configured, your organization is ready to begin provisioning audiences and activating data.

To learn more about initial organization setup, including how to define roles, upload branding assets, and configure match keys, see the [initial organization setup document](./setup/onboard-organization.md#initial-organization-setup){target="_blank"}.

Watch a step-by-step walkthrough of advertiser setup, including account creation, branding, and match key configuration.

>[!VIDEO](https://video.tv.adobe.com/v/3452264/?learn=on&enablevpops)

## Step 3: Source audiences (from Experience Platform or a cloud source) {#source-audiences}

Choose one or both of the following data stores to source audiences. Use either the Collaboration UI or coordinate with Adobe to provision audiences in a privacy-preserving format.

### Option A: Source from Experience Platform

[Use the Collaboration destinations UI to link a sandbox that contains audiences](./setup/onboard-audiences.md). Use this self-service method to reference existing audience segments from within your Experience Platform instance.

### Option B: Source from Snowflake or Amazon S3

To configure a cloud source (for example, [!DNL AWS S3] or [!DNL Snowflake]), prepare your audience data using the following [Audience Specification PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Onboarding_Spec_v1.0.pdf). Once complete, or if you have questions, contact your Adobe account representative to finalize the setup. This method is not self-service and requires Adobe assistance.

>[!IMPORTANT]
>
>Cloud-based audience files must follow the required schema outlined in the Audience Specification PDF. Files must include hashed identifiers (lowercased SHA256), required metadata fields such as `segment_name` and `activation_id`, and use supported formats such as CSV or Parquet. Adobe does not normalize data before activation. TTL is enforced based on the audience's lifespan.
>
>All audiences in the uploaded file are fully sourced at this stage. Access to specific partner organizations is provisioned separately through the Collaboration UI.

### Provision audiences

Configure how audiences are prepared, matched, and governed for use in connections.

- **Select audiences** *(Experience Platform only)* – Choose audience segments with supported identifiers.
- **Map match keys** – Align audience fields with the configured match keys.
- **Apply transformations** – Hash plaintext values (for example, email) if needed.
- **Schedule refreshes** – Define update frequency (for example, daily).
- **Configure consent settings** – Determine which profiles are eligible to be included in connections by selecting a consent mode: opt-in, opt-out, or none.

>[!NOTE]
>
>You can add or remove audiences and update the refresh schedule directly in the Collaboration UI. To change other settings, such as match keys or consent mode, you must delete and recreate the data connection.

>[!IMPORTANT]
>
>**Maximum number of audiences per collaborator role:**
>
>- **Advertisers** can provision up to 25 audiences.
>- **Publishers** can provision up to 250 audiences (each with a minimum of 5,000 IDs).

>[!IMPORTANT]
>
>**Match key requirements:**
>
>All match keys must be **trimmed**, **lowercased**, and **SHA256-hashed**.  
>If you provide hashed values that use uppercase characters, Collaboration automatically converts them to lowercase.  
>If your source contains **plaintext identifiers**, use the **[!UICONTROL Apply transformation]** option in the UI to apply hashing. This option is only available when sourcing audiences from Experience Platform and is not supported for cloud-based sources.
>
>For more information, see the [map fields](./setup/onboard-audiences.md#map-fields) section of the import and manage audiences guide.

To see a full walkthrough of how to reference audiences using the Collaboration UI, watch the Collaboration Audience Referencing demonstration video below.

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

Alternatively, see the document on [making audiences available in Real-Time CDP Collaboration](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-audiences#import-audiences).

## Step 4: Activate audiences (to Experience Platform or a cloud destination) {#activate-audiences}

>[!NOTE]
>
>This step applies to both advertisers and publishers.

Use the Collaboration UI to activate audiences to either your Experience Platform instance or a cloud destination.

### Option A: Activate to Experience Platform

Complete the following steps outlined in the [Configure Adobe Experience Platform as a destination](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/destinations/experience-platform) guide.

- **Create a destination** – Use the UI to set up an Experience Platform destination (sandbox-level).
- **Map match keys** – Select the identifier (e.g., `hashedEmail`).
- **Define TTL** – Set expiration (1–30 days).
- **Verify in Audience Portal** – Once a collaborator sends you an audience, verify that it appears in the Audience Portal under the origin "[!UICONTROL Real-Time CDP Collaboration]."

### Option B: Activate to cloud

To activate audiences to a cloud destination (such as [!DNL AWS S3] or [!DNL Snowflake]), contact your Adobe account representative to initiate the setup process. You will need to provide destination details such as file path, credentials, and expected file format. During setup, you must also specify a match key (e.g., `hashedEmail`) and define the desired TTL and refresh cadence. Once configuration is complete, Adobe will provision the destination and ensure data is delivered correctly.

Audience data sent to a cloud destination follows a predefined schema. For a detailed description of the required fields and format, download the [Collaboration Audience Activation Guide](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf).

### Key differences

The following list highlights the differences between Experience Platform and cloud activation options:

- Activations to Experience Platform are fully self-service and visible in the Audience Portal.
- Cloud destinations require Adobe coordination and are not visible in the UI.

## Step 5: Set up measurement (optional) {#set-up-measurement}

>[!AVAILABILITY]
>
>This feature is in **beta** and available exclusively to customers in the Limited Availability program. Contact your Adobe representative to request access.

>[!IMPORTANT]
>
>The **[!UICONTROL Measure]** workspace is only available if the **[!UICONTROL Measurement]** use case was enabled [during the connection process](./connect/establishing-connections.md#connection-settings). For more information about use cases, refer to the [manage projects](./collaborate/manage-projects.md#project-use-cases) guide.

Collaboration offers a variety of reports to analyze campaign reach, frequency, and effectiveness. While the **[!UICONTROL Measure]** workspace is available in the UI, full reporting functionality may require backend enablement.

To learn how to view and interpret measurement reports, see the [Measurement guide](./collaborate/measure.md). It covers attribution, campaign summary metrics, and dashboards such as reach curves and frequency distribution.

<!-- Commenting out the below information as this workflow is not yet in Beta but will be imminently. A guided measurement configuration workflow will be available in a future release."
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
   - Submit the report. It will run on the selected date and populate within 24 hours. -->

## Verification

After activation, verify that audiences were successfully delivered or made available in the appropriate destination.

- Verify that your audiences appear in the Audience Portal (for Experience Platform activation).
- Confirm successful cloud delivery through external destination logs or confirmation.

## Step 6: Connect with collaborators {#connect-with-collaborators}

With setup and data provisioning complete, your organization is now ready to connect with collaborators by sending or accepting invitations and submitting project settings for approval. This connection process involves sending or receiving invitations, reviewing and submitting connection settings (such as use cases and credit consumption), and confirming the relationship.

Use the **[!UICONTROL Connect]** workspace from the left navigation menu in the Collaboration UI to browse available publishers (advertisers cannot currently be browsed). For an overview of this flow, see the [Connect with advertisers or publishers guide](./connect/establishing-connections.md){target="_blank"}. For a visual walkthrough of the connection process, including browsing collaborators and managing connection settings, watch the [advertiser account setup video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}.

## Next steps

You've now completed onboarding and configured your organization for secure collaboration. Next, explore the following resources to deepen your understanding of activation, measurement, and data governance:

- [Audience activation workflow documentation](./collaborate/activate.md)  
- [Measurement use cases](./collaborate/measure.md)  
- [Collaboration governance best practices](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
