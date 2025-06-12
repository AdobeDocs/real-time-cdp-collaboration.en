---
title: Quick Start Guide
description: get set up quickly.
audience: admin, publisher, advertiser
---
# Quick start: Set up RTCDP Collaboration

This guide helps you set up your organization in RTCDP Collaboration and prepare audiences for privacy-preserving activation and measurement.

## Prerequisites

Before you begin, ensure the following:

- You have an active RTCDP Collaboration license.
- You have admin access to Adobe Experience Platform.
- Your organization has designated roles and user access configured.
- You have access to branding assets (name, logo, banner, description).
- You have a match key strategy defined (e.g., hashed email).
- (Optional) You have access to a supported cloud source (Amazon S3 or Snowflake).

## Step 1: Complete role-based setup

Ensure the admin has completed RTCDP Collaboration access provisioning.

**Resources:**

- [User Access Documentation](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/permissions/manage-user-access)
- [Role Setup Documentation](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/permissions/manage-roles)
- Doug's Permissions Walkthrough Video: [PLACEHOLDER - Doug permissions video]

>[!NOTE]
>
>This step applies to both Brand and Publisher roles.

## Step 2: Set up RTCDP Collaboration org

Finalize your organization's configuration so it can initiate or receive collaboration requests.

### Create a collaboration entity

Define your organization as a Brand, Publisher, or both.

- **Assign a role** – Controls visibility and UI experience.
- **Branding assets** – Provide the following to Adobe:
  - Brand name (max 100 characters)
  - Brand description (max 1,000 characters)
  - Brand logo (SVG <20KB, ideally square)
  - Brand banner (JPG 2688x1536 or similar)
  - _Note: Publishers must email their custom banner to Adobe. The UI currently only supports default banners._
- **Configure match keys** – Select identifiers used for audience matching (e.g., hashed email).

>[!NOTE]
>
>This step applies to both Brand and Publisher roles.

## Step 3: Source audiences (from RTCDP or cloud)

Use either the self-service UI or coordinate with Adobe to connect your RTCDP instance or a cloud source. Provision audiences in a privacy-preserving format.

### Connect a source

Depending on your data source, choose one of the following:

- **RTCDP** – Use the self-service UI to link a sandbox that contains audiences.
- **Cloud** – Coordinate with Adobe to configure a connection to your external data source (e.g., Amazon S3 or Snowflake).

### Provision audiences

- **Select audiences** *(RTCDP only)* – Choose audience segments with supported identifiers.
- **Map match keys** – Align audience fields with the configured match keys.
- **Apply transformations** – Hash plaintext values (e.g., email) if needed.
- **Schedule refreshes** – Define update frequency (e.g., daily).
- **Configure consent settings** – Choose a consent mode: opt-in, opt-out, or none.

**Notes:**

- Brand: Can provision up to 25 audiences.
- Publisher: Can provision up to 250 audiences (minimum size: 5,000 IDs each).
- Refer to the [audience sourcing specification](#) for format and integration requirements.

## Step 4: Activate audiences (to RTCDP or cloud)

Use RTCDP Collaboration to activate audiences to either your RTCDP instance or a cloud destination.

### Option A: Activate to RTCDP

- **Create a destination** – Use the UI to set up an RTCDP destination (sandbox-level).
- **Map match keys** – Select the identifier (e.g., `hashedEmail`).
- **Define TTL** – Set expiration (1–30 days).
- **Schedule refresh (optional)** – Enable automatic updates.
- **Verify in Audience Portal** – Once a collaborator sends you an audience, verify that it appears in the Audience Portal under the origin "RTCDP Collaboration."

### Option B: Activate to cloud

- **Coordinate with Adobe** to configure a cloud delivery destination.
- **Provide destination details** – Path, credentials, file format.
- **Map match keys** – Select the identifier (e.g., `hashedEmail`).
- **Define TTL and refresh cadence** – Finalized in collaboration with Adobe.
- **Confirm delivery** – Ensure audiences are delivered and compliant.

**Key differences:**

- RTCDP is fully self-service and visible in Audience Portal.
- Cloud destinations require Adobe coordination and are not visible in the UI.
- TTL enforcement is automatic in RTCDP; manual in cloud destinations.

>[!NOTE]
>
>This step applies to both Brand and Publisher roles.

## Step 5: Set up measurement (optional)

Complete this step if your collaboration includes campaign performance analysis or attribution measurement.

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

For advanced configuration and use cases, see:

- [Audience activation workflow documentation](#)  
- [Measurement use cases](#)  
- [Collaboration governance best practices](#)
