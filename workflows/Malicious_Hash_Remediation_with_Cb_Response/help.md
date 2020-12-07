# Description

This workflow triggers off of InsightIDR's Malicious Hash on Asset alerts and does a lookup of the hash with Team Cymru before banning it with Cb Response.

# Key Features

* Check detection percentage of flagged hashes automatically on alert generation
* Utilize your communications stack (Slack) to pull the trigger on banning the hash
* Leverage your EPP software to ban the file globally

# Requirements

* InsightConnect License
* Carbon Black Response API Key
* [Slack chatops connection](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

* Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect
* Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary
* Once the workflow has been imported **edit the preset text of `change_me` in the Confirm Ban step to specify the Slack channel or user name to suit your Slack environment!** - the workflow will post messages back to this channel/user
* Activate the workflow
* Navigate to IDR's alert triggers page at #/automation/alerts
* Click Create Alert Trigger
* Select Malicious Hash Remediation with Cb Response
* While Selecting Alerts, check "Malicious Hash on Asset"

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Team Cymru MHR|1.1.1|1|
|VMware Carbon Black EDR|3.1.10|1|
|Rapid7 InsightIDR|1.3.0|1|

## Troubleshooting

# Version History

* 1.0.2 - Updated documentation and plugin versions
* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Cb Response API Auth](https://developer.carbonblack.com/guide/enterprise-response/cbrestapiquickstart/)
* [Slack](https://slack.com)
