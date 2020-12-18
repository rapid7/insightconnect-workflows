# Description

This workflow quarantines or unquarantines endpoints with CrowdStrike Falcon via Microsoft Teams command and reports information back to the message thread.
This workflow supports endpoints in the form of Device IDs, hostnames, external IP addresses or MAC addresses.

Sample Microsoft Teams Trigger Commands:

`!quarantine-endpoint example-host`

`!unquarantine-endpoint 198.51.100.100`

`!quarantine-endpoint f5b83fa335f44c38b456fb94d515f196`

`!unquarantine-endpoint 00-50-56-94-6c-3d`

To check the device quarantine status in CrowdStrike Falcon, log into the CrowdStrike Falcon product web interface and choose the Host Management page under the Hosts section from the menu.
Find the host name on the list and check the Status column for the quarantine status. 

# Key Features

* Quarantine and unquarantine endpoints

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* CrowdStrike Falcon account with [API Client configured](https://www.crowdstrike.com/blog/tech-center/get-access-falcon-apis/)

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
* `!unquarantine-endpoint 198.51.100.100`
* `!quarantine-endpoint f5b83fa335f44c38b456fb94d515f196`
* `!unquarantine-endpoint 00-50-56-94-6c-3d`

The workflow will reply when it completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|CrowdStrike Falcon|2.2.0|3|
|Microsoft Teams|3.1.0|7|
|HTML|1.2.2|1|
|Markdown|3.1.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.0.0 - Initial workflow

# Links

## References

* [CrowdStrike Falcon](https://www.crowdstrike.co.uk/endpoint-security-products/)
* [CrowdStrike Falcon plugin](https://extensions.rapid7.com/extension/crowdstrike_falcon)
* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
