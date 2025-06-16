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

## Step 1: Complete role-based setup {#complete-role-based-setup}

>[!NOTE]
>
>This step applies to both Brand and Publisher roles.

Complete RTCDP Collaboration access provisioning before proceeding.

**Resources:**

- [User Access Documentation](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/permissions/manage-user-access)
- [Role Setup Documentation](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/permissions/manage-roles)
- [Set permissions walkthrough video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/set-permissions-for-collaboration)

## Step 2: Set up RTCDP Collaboration organization

>[!NOTE]
>
>This step applies to both Brand and Publisher roles.

Before you can collaborate with partners, you must complete your organization's configuration in RTCDP Collaboration. This setup enables you to initiate or receive collaboration requests and governs how your organization appears and behaves in the interface.

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

Once your collaboration entity is created and your branding and match keys are configured, you can begin connecting with collaborators. This connection process involves sending or receiving invitations, reviewing and submitting connection settings (such as use cases, billing ownership, and legal agreements), and confirming the relationship.

To learn more about each step in the connection process, see the [Connect with advertisers or publishers guide](./connect/establishing-connections.md){target="_blank"}. For a visual walkthrough, including how to browse collaborators and manage connection settings in the UI, watch the [Advertiser account setup video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}.

For a detailed walkthrough of initial organization setup, see the [initial organization setup document](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-organization#initial-organization-setup){target="_blank"} and the [Advertiser account setup video](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/collaboration/set-up-an-advertiser-account){target="_blank"}.

## Step 3: Source audiences (from Real-Time CDP or cloud) {#source-audiences}

Choose one of the following data sources to begin audience provisioning. Use either the RTCDP Collaboration UI or coordinate with Adobe to provision audiences in a privacy-preserving format.

### Connect a source

Select the platform or cloud location where your audience data resides.

- **Real-Time CDP** – [Use the RTCDP Collaboration UI to link a sandbox that contains audiences](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-audiences).
- **Cloud** – To configure a cloud source (for example, [!DNL AWS S3] or [!DNL Snowflake]), prepare your audience data using the following [Audience Specification PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Onboarding_Spec_v1.0.pdf). Once complete, or if you have questions, contact your Adobe account representative to finalize the setup.

### Provision audiences

Configure how audiences are prepared, matched, and governed for collaboration.

- **Select audiences** *(Real-Time CDP only)* – Choose audience segments with supported identifiers.
- **Map match keys** – Align audience fields with the configured match keys.
- **Apply transformations** – Hash plaintext values (e.g., email) if needed.
- **Schedule refreshes** – Define update frequency (e.g., daily).
- **Configure consent settings** – Determine which profiles are eligible for collaboration by selecting a consent mode: opt-in, opt-out, or none.

>[!IMPORTANT]
>
>Audience provisioning limits vary by role.<ul><li>Brands can provision up to 25 audiences.</li><li>Publishers can provision up to 250 audiences (each with a minimum of 5,000 IDs).</li></ul>

>[!IMPORTANT]
>
>All match keys must be lowercased and SHA256-hashed. If the source audience contains unhashed values, use the **[!UICONTROL Apply transformation]** option in the UI to apply hashing. This functionality is only available when the audience source is Real-Time CDP. It is not available for cloud sources. See the [Map fields](./setup/onboard-audiences.md#map-fields) section of the Import and manage audiences document for details.

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

## Next steps

Explore the following resources for advanced configuration and governance practices:

- [Audience activation workflow documentation](#)  
- [Measurement use cases](#)  
- [Collaboration governance best practices](#)
