# Description

This workflow is designed to automatically analyze incoming emails to determine if they are malicious. This workflow assumes a user is using their report phishing button to send an email to an administrative account with the suspicious email attached. The workflow will then analyze the attached email for any suspicious links or files. If any malicious indicators are found the email will be remediated across the organization.

# Key Features

* Identifies malicious emails
* Removes identified emails from the entire organization
* Blocks sender from the organization

# Requirements

API and account credentials for:

* Microsoft Office365
* VirusTotal
* Hybrid Analysis

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported. **update the first step with the mailbox and subject to suit your environment** by editing the input with the preset text of `change_me`.

Additionally, update the predefined `change_me` inputs in _Send Notification Email_ - you can specify the sender of the notification email and who should be notified. The **Email To** field accepts a list of email addresses, so if you wish you can add multiple mailboxes to notify. 

The remediation steps are disabled due to their destructive nature. To use them, they must be manually enabled after importing the workflow.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Basename|1.0.0|1|
|ExtractIt|1.1.6|1|
|HashIt|2.0.1|1|
|Hybrid Analysis|2.0.0|1|
|Microsoft Office 365 Email|4.0.0|3|
|Microsoft Office 365 Email Security|2.1.0|2|
|Storage|1.0.0|5|
|VirusTotal|5.0.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Workflow improvements | Support for nested EML attachments | Domain headers analysis
* 1.0.1 - Update workflow title to enrichment
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office365](https://www.office.com)
* [VirusTotal](https://www.virustotal.com)
* [Hybrid Analysis](https://www.hybrid-analysis.com/)
