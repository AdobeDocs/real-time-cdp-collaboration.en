---
title: Real-Time CDP Collaboration Onboarding Quick Start
description: Learn how to onboard your organization in RTCDP Collaboration, from role setup and branding to audience provisioning, activation, and optional measurement. This guide helps Brands and Publishers configure collaboration settings and begin using shared audiences securely and efficiently.
audience: admin, publisher, advertiser
---
# Real-Time CDP Collaboration onboarding quick start

This guide helps you set up your organization in RTCDP Collaboration and prepare audiences for privacy-preserving activation and measurement.

## Prerequisites

Before you begin, ensure that you have completed or own the following:

- An active RTCDP Collaboration license.
- Admin access to Adobe Experience Platform.
- Your organization has designated roles and user access configured.
- Access to branding assets (name, logo, banner, description).
- A match key strategy defined (e.g., hashed email).
- (Optional) Access to a supported cloud source (Amazon S3 or Snowflake).

## Step 1: Complete role-based setup

>[!NOTE]
>
>This step applies to both Brand and Publisher roles.

Complete RTCDP Collaboration access provisioning before proceeding.

**Resources:**

- [User Access Documentation](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/permissions/manage-user-access)
- [Role Setup Documentation](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/permissions/manage-roles)
- [Set permissions walkthrough video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/set-permissions-for-collaboration)

## Step 2: Set up RTCDP Collaboration org

>[!NOTE]
>
>This step applies to both Brand and Publisher roles.

Finalize your organization's configuration so it can initiate or receive collaboration requests.

To begin, define your organization's role in collaboration. 

After setting your organization's role and branding, you can send or receive connection invitations with collaborators. These invitations trigger a connection setup workflow, which includes selecting match keys, defining use cases, assigning billing responsibilities, and verifying legal agreements. To learn more about each step, see the [Connect with advertisers or publishers guide](./connect/establishing-connections.md){target="_blank"} for detailed instructions. For a visual walkthrough, including how to browse collaborators and manage connection settings in the UI, watch the [Advertiser account setup video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}.

### Create a collaboration entity

Complete the following actions to define your collaboration role and prepare your organization for partner engagement.

- **Assign a role** – Controls visibility and UI experience.
- **Branding assets** – Provide the following to Adobe:
  - Brand name (max 100 characters)
  - Brand description (max 1,000 characters)
  - Brand logo (SVG <20KB, ideally square)
  - Brand banner (JPG 2688x1536 or similar)

  >[!NOTE]
  >
  >Publishers must email their custom banner to Adobe. The UI currently only supports default banners.

- **Configure match keys** – Select identifiers used for audience matching (e.g., hashed email).

<!-- For a visual overview of the setup process from the advertiser perspective, including how to send collaboration invites, configure connection settings, and activate your first publisher connection, watch the [Advertiser account setup video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}. This walkthrough reinforces key concepts like role assignment, connection workflows, and readiness to collaborate on projects. -->

For a detailed walkthrough, see the [initial organization setup document](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-organization#initial-organization-setup){target="_blank"} and the [Advertiser account setup video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/set-up-an-advertiser-account){target="_blank"}.

## Step 3: Source audiences (from RTCDP or cloud)

Choose one of the following data sources to begin audience provisioning. Use either the self-service UI or coordinate with Adobe to provision audiences in a privacy-preserving format.

### Connect a source

- **RTCDP** – Use the self-service UI to link a sandbox that contains audiences.
- **Cloud** – Coordinate with Adobe to configure a connection to your external data source (e.g., Amazon S3 or Snowflake).

### Provision audiences

- **Select audiences** *(RTCDP only)* – Choose audience segments with supported identifiers.
- **Map match keys** – Align audience fields with the configured match keys.
- **Apply transformations** – Hash plaintext values (e.g., email) if needed.
- **Schedule refreshes** – Define update frequency (e.g., daily).
- **Configure consent settings** – Determine which profiles are eligible for collaboration by selecting a consent mode: opt-in, opt-out, or none.

**Notes:**

- Brand: Can provision up to 25 audiences.
- Publisher: Can provision up to 250 audiences (minimum size: 5,000 IDs each).
- Review the [audience sourcing specification](#) for required formatting and integration details.

To see a full walkthrough of how to reference audiences using the Collaboration UI, including data connection setup, match key mapping, and audience selection, watch the [RTCDP Collaboration Audience Referencing demonstration video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/reference-audiences-as-an-advertiser). It visually guides you through the end-to-end process and reinforces key setup decisions like consent enforcement and data transformations.

Alternatively, see the document on [making audiences available in RTCDP Collaboration](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-audiences#import-audiences).

## Step 4: Activate audiences (to Real-Time CDP or cloud)

>[!NOTE]
>
>This step applies to both Brand and Publisher roles.

Use Real-Time CDP Collaboration to activate audiences to either your Real-Time CDP instance or a cloud destination.

### Option A: Activate to Real-Time Customer Data Platform

Complete the following steps outlined in the [Configure Adobe Experience Platform as a destination](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/destinations/experience-platform) guide.

- **Create a destination** – Use the UI to set up an Real-Time CDP destination (sandbox-level).
- **Map match keys** – Select the identifier (e.g., `hashedEmail`).
- **Define TTL** – Set expiration (1–30 days).
- **Schedule refresh (optional)** – Enable automatic updates.
- **Verify in Audience Portal** – Once a collaborator sends you an audience, verify that it appears in the Audience Portal under the origin "RTCDP Collaboration."

### Option B: Activate to cloud

Complete the following steps in coordination with your Adobe support team.

- **Coordinate with Adobe** to configure a cloud delivery destination.
- **Provide destination details** – Path, credentials, file format.
- **Map match keys** – Select the identifier (e.g., `hashedEmail`).
- **Define TTL and refresh cadence** – Finalized in collaboration with Adobe.
- **Confirm delivery** – Ensure audiences are delivered and compliant.

### Key differences

The following list highlights the differences between Real-Time Customer Data Platform and cloud activation options:

- Real-Time CDP is fully self-service and visible in Audience Portal.
- Cloud destinations require Adobe coordination and are not visible in the UI.
- TTL enforcement is automatic in Real-Time CDP, and manual in cloud destinations.

## Step 5: Set up measurement (optional)

>[!IMPORTANT]
>
>The **[!UICONTROL Measure]** workspace is only available if the **[!UICONTROL Campaign measurement]** use case was enabled [during the connection process](../connect/establishing-connections.md#connection-settings). For more information about use cases, refer to the [manage projects](./manage-projects.md#project-use-cases) guide.

>[!NOTE]
>
>Complete this step only if your collaboration includes campaign performance analysis or attribution measurement.

Real-Time CDP Collaboration offers a variety of reports to measure and analyze the performance of your marketing campaigns across various channels. 

### Configure measurement workflow

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

**Notes:**

- Brand: Shares the measurement specification with Publisher.
- Publisher: Shares the measurement specification with Brand.

## Verification

- Verify that your audiences appear in the Audience Portal (for RTCDP activation).
- Confirm successful cloud delivery through external destination logs or confirmation.

## Next steps

Explore the following resources for advanced configuration and governance practices:

- [Audience activation workflow documentation](#)  
- [Measurement use cases](#)  
- [Collaboration governance best practices](#)
