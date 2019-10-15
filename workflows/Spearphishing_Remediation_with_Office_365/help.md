# Description

IDR provides built-in machine learning based detections of spearphishing attempts through DNS queries to spoofed domains. On alert generation, this workflow automatically deletes true positive phishing emails across all user inboxes, and also immediately creates a block domain transport rule in Office365 Security & Compliance Center.

# Key Features

* Tag owned domains in IDR
* Alert on DNS queries to spoofed domains and create an investigation to track related alerts
* Prompt the user in Slack to either remediate or close the investigation
* Automatically delete the email across all user inboxes based on a custom search query
* Add a transport rule in Office365 to block the offending domain
* Notify team of all actions performed

# Requirements

* Email provider is Office365 (Gmail does not support bulk deletion)

# Documentation

## Setup

* Tag domains in IDR at #/settings/domains
* Download the workflow or clone the repository `git clone https://github.com/rapid7/insightconnet-workflows.git`
* Login to InsightConnect, and “Import” the .icon file into the workflow builder
* Configure the connections for the Office365 and Office365 Email Security plugins
* Activate your workflow
* Navigate to IDR's alert triggers page at #/automation/alerts
* Click Create Alert Trigger
* Select Spearphishing Remediation with Office365
* While Selecting Alerts, check "Spear Phishing URL Detected"

## Technical Details

* Spear Phishing URL Detected will generate an alert of type SpoofedDomainVisited
* The alert will always provide a domain, and will sometimes provide user and/or asset information

Plugins leveraged by workflow:

* Microsoft Office 365 Email 4.0.1
* Microsoft Office365 Email Security 2.2.0

## Troubleshooting

# Links

## Source Code

* https://github.com/rapid7/insightconnect-workflows/tree/master/workflows/Spearphishing_Remediation_with_Office_365

## References

* [IDR Spearphishing Video](https://www.youtube.com/watch?v=DNUDYfhv5bE)