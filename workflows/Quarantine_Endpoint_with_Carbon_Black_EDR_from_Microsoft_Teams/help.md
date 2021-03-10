# Description

This workflow quarantines or unquarantines endpoints with Carbon Black EDR via Microsoft Teams command and reports information back to the message thread.
This workflow supports endpoints in the form of hostnames.

Sample Microsoft Teams Trigger Commands:

`!quarantine-endpoint example-host`

`!unquarantine-endpoint example-host`

To check the device quarantine status in Carbon Black EDR, log into the Carbon Black EDR product web interface and choose the Sensors under the Manage section from the left hand side menu.
Find the host name on the list and check the Status column for the quarantine status. 

# Key Features

* Quarantine and unquarantine endpoints

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Carbon Black EDR account with [API Client configured](https://developer.carbonblack.com/reference/enterprise-response/authentication/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After configuring the first step, activate the workflow and then issue a Microsoft Teams command to trigger it. 

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the configured Microsoft Teams channel starting with the command `!quarantine-endpoint` or `!unquarantine-endpoint` and then provide the identifier for the host you would like to take the action on.

For example:
* `!quarantine-endpoint example-host`
* `!unquarantine-endpoint example-host`

The workflow will reply when it completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|VMware Carbon Black EDR|3.1.10|2|
|Microsoft Teams|3.1.0|6|
|HTML|1.2.2|1|
|Markdown|3.1.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Carbon Black EDR](https://www.carbonblack.com/products/endpoint-detection-and-response/)
* [VMware Carbon Black EDR plugin](https://extensions.rapid7.com/extension/carbon_black_response)
* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
