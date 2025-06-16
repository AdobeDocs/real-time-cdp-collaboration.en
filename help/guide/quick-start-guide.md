---
title: Real-Time CDP Collaboration Onboarding Quick Start
description: Learn how to onboard your organization in RTCDP Collaboration, from role setup and branding to audience provisioning, activation, and optional measurement. This guide helps Brands and Publishers configure collaboration settings and begin using shared audiences securely and efficiently.
audience: admin, publisher, advertiser
---
# Real-Time CDP Collaboration onboarding quick start

Get started with RTCDP Collaboration by configuring your organization, provisioning audiences, and enabling privacy-focused activation and measurement.

## Prerequisites

Before you begin, ensure that you have completed or own the following:

- An active RTCDP Collaboration license.
- Admin access to Adobe Experience Platform.
- Your organization has designated roles and user access configured.
- Access to branding assets (name, logo, banner, description).
- A match key strategy defined (e.g., hashed email).
- (Optional) Access to a supported cloud source (Amazon S3 or Snowflake).

## Step 1: Complete role-based setup {#complete-role-based-setup}

>[!NOTE]
>
>This step applies to both Brand and Publisher roles.

Your organization's role determines how you interact with collaborators in RTCDP Collaboration. Before proceeding, you must complete role-based setup to ensure proper access, permissions, and visibility in the platform.

**Resources:**

- [User Access Documentation](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/permissions/manage-user-access)
- [Role Setup Documentation](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/permissions/manage-roles)
- [Set permissions walkthrough video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/set-permissions-for-collaboration)

## Step 2: Set up RTCDP Collaboration organization

>[!NOTE]
>
>This step applies to both Brand and Publisher roles.

Before you can provision audiences, you must configure your organization in RTCDP Collaboration. This setup governs how your organization appears and behaves in the interface.

To begin, define your organization's role in collaboration and provide the necessary branding assets. Then, configure match keys that will be used to align audiences across collaborations.

### Create a collaboration entity {#create-collaboration-entity}

Complete the following actions to define your collaboration role and prepare your organization for partner engagement:

- **Assign a role** – Determines whether your organization acts as a Brand, Publisher, or both. This selection controls your visibility and experience in the UI.
- **Branding assets** – Add the following to your account:
  - Brand name (max 100 characters)
  - Brand description (max 1,000 characters)
  - Brand logo (SVG <20KB, ideally square)
  - Brand banner (JPG 2688x1536 or similar)
- **Contact email** – Provide a business email alias for collaborators to use after a connection is established.

  >[!NOTE]
  >
  >If you are creating a Publisher account and would like to be publicly visible in RTCDP Collaboration's connections catalog, please contact your Adobe account representative. Publisher accounts require a custom brand banner (JPG 2688x1536); this file can be shared directly with your representative.

- **Configure match keys** – Select the identifiers used for audience matching (e.g., hashed email).

Once your collaboration entity is created and your branding and match keys are configured, your organization is ready to begin provisioning audiences and activating data.

To learn more about initial organization setup, including how to define roles, upload branding assets, and configure match keys, see the [initial organization setup document](./setup/onboard-organization.md#initial-organization-setup){target="_blank"}.

To watch a visual demonstration of the end-to-end process from the advertiser perspective, view the [Advertiser account setup video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/set-up-an-advertiser-account){target="_blank"}.

## Step 3: Source audiences (from Real-Time CDP or cloud) {#source-audiences}

Choose one of the following data sources to begin audience provisioning. Use either the RTCDP Collaboration UI or coordinate with Adobe to provision audiences in a privacy-preserving format.

### Option A: Source from Real-Time CDP

[Use the RTCDP Collaboration UI to link a sandbox that contains audiences](./setup/onboard-audiences.md). Use this self-service method to reference existing audience segments from within your Real-Time CDP instance.

### Option B: Source from cloud

To configure a cloud source (for example, [!DNL AWS S3] or [!DNL Snowflake]), prepare your audience data using the following [Audience Specification PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Onboarding_Spec_v1.0.pdf). Once complete, or if you have questions, contact your Adobe account representative to finalize the setup. This method is not self-service and requires Adobe assistance.

>[!IMPORTANT]
>
>Cloud-based audience files must follow the required schema outlined in the Audience Specification PDF. Files must include hashed identifiers (lowercased SHA256), required metadata fields such as `segment_name` and `activation_id`, and use supported formats such as CSV or Parquet. Adobe does not normalize data before activation. TTL is enforced based on the audience's lifespan.

### Provision audiences

Configure how audiences are prepared, matched, and governed for collaboration.

- **Select audiences** *(Real-Time CDP only)* – Choose audience segments with supported identifiers.
- **Map match keys** – Align audience fields with the configured match keys.
- **Apply transformations** – Hash plaintext values (e.g., email) if needed.
- **Schedule refreshes** – Define update frequency (e.g., daily).
- **Configure consent settings** – Determine which profiles are eligible for collaboration by selecting a consent mode: opt-in, opt-out, or none.

>[!IMPORTANT]
>
>**Audience provisioning limits by role:**
>
>- **Brands** can provision up to 25 audiences.
>- **Publishers** can provision up to 250 audiences (each with a minimum of 5,000 IDs).

>[!IMPORTANT]
>
>**Match key requirements:**
>
>All match keys must be lowercased and SHA256-hashed. If your audience source contains unhashed values, use the **[!UICONTROL Apply transformation]** option in the UI to apply hashing. This option is only available when sourcing from Real-Time CDP and is not supported for cloud-based audiences.
>
>For more information, see the [Map fields](./setup/onboard-audiences.md#map-fields) section of the Import and manage audiences guide.

To see a full walkthrough of how to reference audiences using the Collaboration UI, watch the [RTCDP Collaboration Audience Referencing demonstration video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/reference-audiences-as-an-advertiser).

Alternatively, see the document on [making audiences available in RTCDP Collaboration](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-audiences#import-audiences).

## Step 4: Activate audiences (to Real-Time CDP or cloud) {#activate-audiences}

>[!NOTE]
>
>This step applies to both Brand and Publisher roles.

Use Real-Time CDP Collaboration to activate audiences to either your Real-Time CDP instance or a cloud destination.

### Option A: Activate to Real-Time Customer Data Platform

Complete the following steps outlined in the [Configure Adobe Experience Platform as a destination](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/destinations/experience-platform) guide.

- **Create a destination** – Use the UI to set up a Real-Time CDP destination (sandbox-level).
- **Map match keys** – Select the identifier (e.g., `hashedEmail`).
- **Define TTL** – Set expiration (1–30 days).
- **Verify in Audience Portal** – Once a collaborator sends you an audience, verify that it appears in the Audience Portal under the origin "RTCDP Collaboration."

### Option B: Activate to cloud

To activate audiences to a cloud destination (such as [!DNL AWS S3] or [!DNL Snowflake]), contact your Adobe account representative to initiate the setup process. You will need to provide destination details such as file path, credentials, and expected file format. During setup, you must also specify a match key (e.g., `hashedEmail`) and define the desired TTL and refresh cadence. Once configuration is complete, Adobe will provision the destination and ensure data is delivered correctly.

Audience data sent to a cloud destination follows a predefined schema. For a detailed description of the required fields and format, download the [RTCDP Collaboration Audience Activation Guide](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf).

### Key differences

The following list highlights the differences between Real-Time Customer Data Platform and cloud activation options:

- Real-Time CDP is fully self-service and visible in Audience Portal.
- Cloud destinations require Adobe coordination and are not visible in the UI.

## Step 5: Set up measurement (optional) {#set-up-measurement}

>[!IMPORTANT]
>
>The **[!UICONTROL Measure]** workspace is only available if the **[!UICONTROL Campaign measurement]** use case was enabled [during the connection process](./connect/establishing-connections.md#connection-settings). For more information about use cases, refer to the [manage projects](./collaborate/manage-projects.md#project-use-cases) guide.

>[!NOTE]
>
>Complete this step only if your collaboration includes campaign performance analysis or attribution measurement.

Real-Time CDP Collaboration offers a variety of reports to measure and analyze the performance of your marketing campaigns across various channels.

### Configure measurement workflow

Use the following steps to define, validate, and execute your campaign measurement strategy in collaboration with your partner.

- **Share the measurement specification** – Align on schema, ID types, and lookback windows.
- **Define use case** – Examples:
  - Impressions vs. conversions
  - Click-through rate
  - Online-to-offline attribution
  - Retail media measurement
- **Set up clean room** – Work with Adobe to enable a secure clean room connection.
- **Align matching logic** – Use consistent match keys across datasets.
- **Validate data readiness** – Ensure correct format (e.g., Parquet or CSV), approved sources, and TTL compliance.
- **Run and review queries** – Assess reach, overlap, lift, and attribution.
- **Apply insights** – Use results to refine targeting and activation strategy.

>[!NOTE]
>
>In a measurement workflow, the Brand shares the measurement specification with the Publisher, and the Publisher shares the measurement specification with the Brand.

## Verification

After activation, verify that audiences were successfully delivered or made available in the appropriate destination.

- Verify that your audiences appear in the Audience Portal (for RTCDP activation).
- Confirm successful cloud delivery through external destination logs or confirmation.

## Step 6: Connect with collaborators {#connect-with-collaborators}

With setup and data provisioning complete, your organization is now ready to connect with collaborators by sending or accepting invitations and submitting project settings for approval. This connection process involves sending or receiving invitations, reviewing and submitting connection settings (such as use cases and credit consumption), and confirming the relationship.

Use the **[!UICONTROL Connect]** workspace from the left navigation menu in the Experience Platform UI to browse publishers or advertisers. For an overview of this flow, see the [Connect with advertisers or publishers guide](./connect/establishing-connections.md){target="_blank"}. For a visual walkthrough of the connection process, including browsing collaborators and managing connection settings, watch the [Advertiser account setup video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}.

## Next steps

You've now completed onboarding and configured your organization for secure collaboration. Next, explore the following resources to deepen your understanding of activation, measurement, and data governance:

- [Audience activation workflow documentation](./collaborate/activate.md)  
- [Measurement use cases](./collaborate/measure.md)  
- [Collaboration governance best practices](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
