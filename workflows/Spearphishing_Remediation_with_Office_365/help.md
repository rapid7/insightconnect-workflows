# Description

IDR provides built-in machine learning based detections of spearphishing attempts through DNS queries to spoofed domains. On alert generation, this workflow automatically deletes true positive phishing emails across all user inboxes, and also immediately adds a domain to a block transport rule in Office365 Security & Compliance Center.

# Key Features

* **Know the Blast Radius** - More often than not with phishing attacks, where there’s one email, there’s many. Quickly block all emails from the same domain.

* **Eliminate the Threat** - Once a phishing message is verified, automatically remove that message from every inbox in your organization.

* **Rapidly Respond** - Every second wasted adds more risk to your environment. Rather than hopping from tool to tool to respond, take action directly from Slack.

# Requirements

* InsightConnect License  
* [Microsoft Office365](https://insightconnect.help.rapid7.com/docs/office365)
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Create Office 365 Exchange Mail Flow Rule `InsightConnect Block List` and set it to `Delete the message without notifying the recipient or sender`

Tag domains in IDR at `#/settings/domains`

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, edit the workflow and **update the `Remediate or Close` Slackbot step, replace `change_me` with a Slack channel or user name** that matches your Slack environment. Once that's done, activate the workflow.

Navigate to Insight IDR's alert triggers page at `#/automation/alerts` and click `Create Alert Trigger`. Select the newly created workflow - `Spearphishing Remediation with Office365`. When Selecting Alerts, check `Spear Phishing URL Detected`.

## Technical Details

* Spear Phishing URL Detected will generate an alert of type SpoofedDomainVisited
* The alert will always provide a domain, and will sometimes provide user and/or asset information

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Office365 Email Security|2.2.1|1|
|ExtractIt|2.0.0|1|
|Rapid7 InsightIDR|1.3.0|2|

## Troubleshooting

# Version History

* 1.0.2 - Updated plugin versions and documentation
* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office365](https://www.office.com)
* [IDR Spearphishing Video](https://www.youtube.com/watch?v=DNUDYfhv5bE)
* [Slack](https://slack.com)
