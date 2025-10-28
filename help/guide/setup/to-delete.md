1.1 
The user should be able to see AWS S3 as a selectable data connection
Previously created AWS S3 connections should be grayed out and the user should see the following copy within the card:
Copy: To add additional audiences, please update the audiences files within the connected Amazon S3 storage


1.2    
The user should see a pop-up with a link to the Audience Onboarding spec that informs them of how their audience files needs to be structured
Copy:
Title: Prepare Your Data for Sourcing
Body: Before starting audience sourcing from Amazon S3, please ensure that:
You have authorized Adobe as a user so that Adobe can retrieve data from your Amazon S3 storage for processing.
Your data complies with the {Audience Sourcing Specifications}, as the match keys are auto-mapped based on the prescribed format.


1.3    
The user should be able to provide their credentials to connect their AWS S3 bucket to RTCDP Collaboration
Input Fields
IAM role (required)
S3 Bucket Name (required)
Folder Path (required)
Copy:
To connect your Amazon S3 storage, please authorize Adobe's service user to retrieve your audience data for processing. Follow the steps outlined in {Experience League} to grant Adobe access to your Amazon S3 storage.


1.4    
The user should be able to provide an acknowledgement that they have removed consent opt-outs after clicking "Next" on the authentication step
User should be require acknowledge before moving forward


1.5    


The user should be able to connect to their AWS S3
The user should receive a success message if authentication was successful
Copy: Authentication successful. Your connection to Amazon S3 has been established successfully.
The user should receive an error message if authentication failed
Copy: Authentication failed. Please review your credentials and try again.
The user should receive an error message if access was denied
Copy: Access denied. Your credentials don't have the required permissions to access this Amazon S3 bucket. Please verify access settings or contact your administrator.
The user should receive an error message if the audience files are not in the expected format (per the Audience Onboarding spec)
Copy: Invalid file format. The audience data doesn't match the expected structure. Please ensure your files comply with the Audience Sourcing Specifications.
The user should receive an error message if the audience files were not found 
Copy: No audience files found. Please confirm that your audience files exist in the specified folder path and that the path is accessible.
For any other error (e.g., unknown error), the user should see the following
Copy: An internal error has occurred. Please try again. If the problem persists, contact customer support. (ACPS - XXXX-XXX) Reference id: XXXXXXX-XXXXX-XXXX-XXXX-XXXXXXXX


1.6    
The user should be able to provide an account name and description for the S3 bucket they are connecting
Data connection name (required)
Data connection description (optional)


1.8    
The user should be able to see the field mapping screen
The "Apply transformation" toggle should not be visible
The "Add field" CTA should not be visible
The source and target fields should be auto-populated based on the underlying audience tables
Copy across top of page
Copy: Source identity fields from your data connection are auto-mapped to target identity fields in Real-Time CDP Collaboration based on the {Audience Onboarding Specifications}.


1.9    
The user should be able to set the refresh schedule as well as the date range for which the connection is available
Frequency options:
Daily up to every 6 days
The user should see copy that informs them that the refresh cadence should not be more frequent than the refresh cadence of the underlying data


1.11    
The user should see a summary screen that asks them to review the data connection before completing it
Summary sections
Data connection
Details
Mapping
Schedule


1.13    
Audiences sourced through an AWS S3 bucket should be displayed in the "My Audiences" tab and have all of the standard functionality & information as audiences sourced from AEP 
The audience source should be "AWS S3"
If sourcing is in progress, the user should be informed of that
Copy:
Title: Audience sourcing in progress
Body: Audiences are being sourced from [Cloud Source Name] via the [Data Connection Name] data connection and will appear once the process is complete.
The user should be able to see the message above for any/all S3 data connections that are currently sourcing audiences
If sourcing is fails, the user should be informed of that
Copy:
Title: Audience sourcing failed
Body: Audience sourcing from [Cloud Source Name] via the [Data Connection Name] data connection failed. Please try again. If the problem persists, contact customer support. Reference id: XXXXXXX-XXXXX-XXXX-XXXX-XXXXXXXX



1.14    


The AWS S3 data connection should be displayed in the "My data connections" tab and have all of the standard functionality & information as audiences sourced from AEP
The audience source should be "AWS S3"
The "+ Add audience" should not be available for S3 data connections (this is displayed when clicking the ellipses on the "My data connections" tab)
The "+" icon should not be available on the details page of the data connection
The user should be informed if the data connection is currently sourcing audiences.
Copy: 
Title: Audience sourcing in progress
Body: Audiences are being sourced from [Cloud Source Name] and will appear once the process is complete.
