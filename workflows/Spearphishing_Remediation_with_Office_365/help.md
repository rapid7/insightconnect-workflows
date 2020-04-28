# Description

IDR provides built-in machine learning based detections of spearphishing attempts through DNS queries to spoofed domains. On alert generation, this workflow automatically deletes true positive phishing emails across all user inboxes, and also immediately creates a block domain transport rule in Office365 Security & Compliance Center.

# Key Features

* Tag domains in IDR at `#/settings/domains`
* Import the workflow and configure connections in the import wizard
* Activate the workflow
* Navigate to IDR's alert triggers page at #/automation/alerts
* Click Create Alert Trigger
* Select `Spearphishing Remediation with Office365`
* While Selecting Alerts, check "Spear Phishing URL Detected"

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

# Version History

* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [IDR Spearphishing Video](https://www.youtube.com/watch?v=DNUDYfhv5bE)