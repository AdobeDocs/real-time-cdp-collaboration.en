---
Title: Set up and manage identity resolution with Epsilon Core ID
Description: Learn how to configure and manage identity resolution with Epsilon Core ID in Adobe Real-Time CDP Collaboration.
---
# Set up and manage identity resolution with Epsilon Core ID

*Writer guidance:* Introduce the user's objective, explain what identity resolution with Core ID accomplishes, and establish how it relates to existing data connections and match keys. Keep the introduction brief and avoid backend implementation details or unsupported performance claims.

## Prerequisites {#prerequisites}

*Writer guidance:* Identify the permissions, US account eligibility, supported data connections, required match keys, and Epsilon customer account number needed before starting. Distinguish account-level match key enablement from source field mapping, and link to existing configuration guides rather than repeating their instructions.

## Configure identity resolution {#configure-identity-resolution}

*Writer guidance:* Introduce the end-to-end setup workflow and explain that users configure identity resolution for selected data connections. Organize the procedure around the supported configuration stages and their expected outcomes.

### Select an identity provider {#select-identity-provider}

*Writer guidance:* Explain how to access the Identity resolution tab, review provider availability and supported match keys, and select Epsilon Core ID. Describe the prerequisite checks and direct readers to the relevant remediation guidance when required.

### Authenticate with Epsilon {#authenticate-with-epsilon}

*Writer guidance:* Explain how to provide the Epsilon customer account number and where users obtain it. Describe the purpose of this identifier without implying unsupported credential validation.

### Select data connections {#select-data-connections}

*Writer guidance:* Explain how to select one or more eligible data connections and how that selection determines the data included in identity resolution. Validate whether audience and measurement connections are both supported before specifying eligible source types.

### Configure match keys {#configure-match-keys}

*Writer guidance:* Explain how to review and select supported match keys for each selected data connection, including the requirement to retain at least one eligible key per connection. Briefly describe Core ID's supported identifiers and link to the existing account and audience-mapping guidance for configuration details.

### Set an identity resolution schedule {#set-schedule}

*Writer guidance:* Explain the available scheduling options, including a defined date range and continuing until cancellation, and clarify how scheduling frequency is determined. Include the connection-dependent scheduling hold only after its availability and behavior are confirmed.

### Review and confirm the configuration {#review-and-confirm}

*Writer guidance:* Explain how to review authentication, selected data connections, match keys, and scheduling before confirming the configuration. Describe the resulting confirmation and expected next state, subject to validation of the final UI and job lifecycle.

## Manage identity resolution {#manage-identity-resolution}

*Writer guidance:* Explain how users return to an existing Core ID configuration and what management actions are available. Distinguish changes that can be made in place from those requiring deletion and reconfiguration.

### View configuration details {#view-configuration-details}

*Writer guidance:* Explain how to access and interpret an existing configuration, including its selected data connections, match keys, and schedule. Use the final UI to verify the displayed information and available actions.

### Edit an existing configuration {#edit-configuration}

*Writer guidance:* Document which settings users can modify after initial setup and how to save supported changes. Confirm the editing restrictions and exact UI controls before writing the procedure.

### Delete an identity resolution configuration {#delete-configuration}

*Writer guidance:* Explain how to delete an existing configuration, including the confirmation step and any irreversible consequences. Validate what deletion removes or stops, and distinguish those effects from any previously resolved data.

## Troubleshoot setup issues {#troubleshoot}

*Writer guidance:* Address the documented prerequisite failures, particularly missing data connections, unsupported or missing match keys, and regional unavailability. Keep remediation instructions concise and cross-reference existing setup guides instead of duplicating full workflows.

## Next steps {#next-steps}

*Writer guidance:* Direct readers to relevant existing account, match key, and data connection guidance where further configuration may be necessary. Include post-configuration verification or monitoring links only when the supported workflow and destination are confirmed.
