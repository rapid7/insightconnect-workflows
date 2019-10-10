# Description

This workflow is designed to automatically analyze incoming emails to determine if they are malicious. This workflow assumes a user is using their report phishing button to send an email to an administrative account with the suspicious email attached. The workflow will then analyze any URLs or files in the attached email to find malicious links. If any malicious indicators are found the email will be remediated across the organization.

# Key Features

* Bulleted list

# Requirements

_There are no special requirements for this workflow_

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder.  Once imported, you will initially be prompted to configure the connections for Office 365 and VirusTotal.

## Technical Details

Plugins leveraged by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Office 365|1.1.1|2|
|VirusTotal|1.0.0|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## Source Code

* https://github.com/rapid7/insightconnect-workflows/tree/master/workflows/Office_365_Analysis_with_Virus_Total

## References

* [Microsoft Office365](https://www.office.com)