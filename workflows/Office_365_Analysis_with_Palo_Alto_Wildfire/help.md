# Description

This workflow is designed to automatically analyze incoming emails to determine if they are malicious. This workflow assumes a user is using their report phishing button to send an email to an administrative account with the suspicious email attached. The workflow will then analyze the attached email for any suspicious links or files. If any malicious indicators are found the email will be remediated across the organization.

# Key Features

* Identifies malicious emails
* Removes identified emails from the entire organization
* Blocks sender from the organization

# Requirements

API and account credentials for

* Microsoft Office365
* Palo Alto Wildfire

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and "Import" it into the workflow builder.  Once imported, you will initially be prompted to configure the connections for each of the plugins.

The remediation steps are disabled due to their destructive nature. To use them, they must be manually enabled after importing the workflow.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Basename|1.0.0|1|
|ExtractIt|1.1.6|1|
|Microsoft Office 365 Email|4.0.0|2|
|Microsoft Office 365 Email Security|2.1.0|2|
|Palo Alto Wildfire|1.0.2|4|
|Sleep|1.0.0|2|
|Storage|1.0.0|6|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## Source Code

* https://github.com/rapid7/insightconnect-workflows/tree/master/workflows/Office_365_Analysis_with_Virus_Total

## References

* [Microsoft Office365](https://www.office.com)