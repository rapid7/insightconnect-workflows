# Description

This workflow triggers off of InsightIDR's Malicious Hash on Asset alerts and does a lookup of the hash with Team Cymru before banning it with Cb Response.

# Key Features

* Check detection percentage of flagged hashes automatically on alert generation
* Utilize your communications stack (Slack) to pull the trigger on banning the hash
* Leverage your EPP software to ban the file globally

# Requirements

* API access to Carbon Black Response

# Documentation

## Setup

* Download the workflow or clone the repository `git clone https://github.com/rapid7/insightconnet-workflows.git`
* Login to InsightConnect, and “Import” the .icon file into the workflow builder
* Configure the connections for the Cb Response plugin
* Activate your workflow
* Navigate to IDR's alert triggers page at #/automation/alerts
* Click Create Alert Trigger
* Select Malicious Hash Remediation with Cb Response
* While Selecting Alerts, check "Malicious Hash on Asset"

## Technical Details

Plugins leveraged by workflow:

* Cb Response 3.1.7

## Troubleshooting

# Links

## Source Code

https://github.com/rapid7/insightconnect-workflows

## References

* [Cb Response API Auth](https://developer.carbonblack.com/guide/enterprise-response/cbrestapiquickstart/)