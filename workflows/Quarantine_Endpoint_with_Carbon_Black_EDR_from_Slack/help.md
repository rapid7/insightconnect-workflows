# Description

This workflow quarantines or unquarantines endpoints with Carbon Black EDR via Slack command and reports information back to Slack.
This workflow supports endpoints in the form of hostnames.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect quarantine-endpoint example-host`

`@Rapid7 InsightConnect unquarantine-endpoint example-host`

To check the device quarantine status in Carbon Black EDR, log into the Carbon Black EDR product web interface and choose the Sensors under the Manage section from the left hand side menu.
Find the host name on the list and check the Status column for the quarantine status. 

# Key Features

* Quarantine and unquarantine endpoints

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Carbon Black EDR account with [API Client configured](https://developer.carbonblack.com/reference/enterprise-response/authentication/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring those steps, activate the workflow and then issue a Slack command to trigger it. 

### Usage

*This workflow will only trigger in the channel specified in the ChatOps workflow steps.*

To run the workflow, send a message to the specified Slack channel starting with the command `@Rapid7 InsightConnect quarantine-endpoint` or `@Rapid7 InsightConnect unquarantine-endpoint` and then provide the hostname for the host you would like to take the action on.

Your chat bot will reply to the message thread when the workflow completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|VMware Carbon Black EDR|3.1.10|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Carbon Black EDR](https://www.carbonblack.com/products/endpoint-detection-and-response/)
* [VMware Carbon Black EDR plugin](https://extensions.rapid7.com/extension/carbon_black_response)
* [Slack](https://slack.com)
