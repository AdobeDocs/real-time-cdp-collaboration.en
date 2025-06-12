---
title: Quick Start Guide
description: get set up quickly.
audience: admin, publisher, advertiser
---
# Quick start guide

Step 1: Complete role-based setup
(Prerequisite) Ensure admin has completed RTCDP Collaboration access provisioning.
User Access Documentation
Notes:
Same for both Brand and Publisher.
Step 2: Submit branding assets (temporary step)
Provide to Adobe the visual and descriptive assets used to identify and represent your organization within RTCDP Collaboration:
*    Brand Name (max 100 characters)
*    Brand Description (max 1,000 characters)
*    Brand Logo (SVG <20KB, ideally square)
*    Brand Banner (JPG 2688x1536 or similar)
Notes:
*    Brand: Used to identify the org in the collaboration UI.
*    Publisher: Also used in the public connections catalog (requires written Adobe approval).
Step 3: Set up RTCDP Collaboration org
Finalize your organization's configuration in RTCDP Collaboration so it can initiate or receive collaboration requests.
Includes:
*    Create a Collaboration Entity – Define your org as a Brand, Publisher, or both
*    Assign a Role – Controls visibility and UI experience
*    Link Branding Assets – Reference assets submitted in Step 2
*    Configure Match Keys – Choose identifiers for matching (e.g., hashed email)
*    Consent Settings – Select opt-in, opt-out, or no consent enforcement
Notes:
Same for both Brand and Publisher.
Step 4: Audience sourcing (from RTCDP)
Use the self-service UI to connect your RTCDP instance and source audiences from AEP into RTCDP Collaboration in a privacy-preserving format (Clean Sketches).
Includes:
*    Connect to RTCDP – Link a sandbox that contains audiences
*    Select Audiences – Choose audiences with supported identifiers
*    Map Match Keys – Align AEP fields with match keys
*    Apply Transformations (if needed) – Convert plaintext (e.g., emails) to hashed format
*    Schedule Refreshes – Choose update frequency (e.g., daily)
Notes:
Same for both Brand and Publisher.
Step 5: Audience sourcing (from cloud)
If sourcing from cloud storage (e.g., Amazon S3 or Snowflake):
*    Review and follow the RTCDP Collaboration audience sourcing specification
*    Coordinate with the RTCDP Collaboration team to set up the clean room and generate Clean Sketches
Key Differences from Step 4:
*    Data Location: External cloud storage
*    Setup Process: Requires Adobe engineering
*    Audience Format: Must follow ingestion requirtements
*    Technical Lift: Involves pipelines and clean room integration
Notes:
*    Brand: Expected to provision ~25 audiences
*    Publisher: Can provision up to 250 audiences (≥5,000 IDs each)
Step 6: Audience activation (to RTCDP)
Use the self-service UI to activate audiences from collaboration back into an RTCDP instance (typically for personalization or further activation).
Includes:
*    Create a Destination – Set up an RTCDP destination (sandbox-level)
*    Map Match Keys – Specify identifier (e.g., hashedEmail)
*    Select Audiences – Choose from provisioned collaboration audiences
*    Define TTL (Time to Live) – 1 to 30 days
*    Schedule Refresh (Optional) – Keep audience data synced
*    Verify in Audience Portal – Check that activated audiences appear with origin "RTCDP Collaboration"
Notes:
Same for both Brand and Publisher.
Step 7: Audience activation (to cloud)
If activating to cloud destinations (e.g., Amazon S3 or Snowflake):
*    Review the RTCDP Collaboration audience activation specification
*    Coordinate with the RTCDP Collaboration team to set up the destination
Includes:
*    Coordinate with Engineering – Initiate configuration
*    Provide Destination Details – Path, credentials, file format
*    Map Match Keys – Select identifier (e.g., hashedEmail)
*    Select Audiences – Choose from project audiences
*    Set TTL and Refresh Cadence – Defined with Adobe
*    Verify Delivery – Ensure audiences are delivered and compliant
Notes:
Applies equally to Brands and Publishers.
Step 8: Measurement setup
Coordinate with your collaborator to define and execute a measurement strategy.
Includes:
*    Share the Measurement Specification – Define schema, ID types, windows
*    Define Use Case – e.g., impressions, conversions, retail attribution
*    Set Up Clean Room – Work with Adobe to securely connect measurement data
*    Align Matching Logic – Use consistent identifiers
*    Validate Data Readiness – Format (e.g., Parquet), source approval, TTL compliance
*    Run and Review Queries – Measure reach, lift, attribution
*    Apply Learnings – Use insights to improve future campaigns
Notes:
*    Brand: Shares Measurement Specification with Publisher
*    Publisher: Shares Measurement Specification with Brand
