# Description

Use the simplicity of a chat command in Microsoft Teams to manage the quarantine state of an endpoint with
Broadcom Symantec Endpoint Protection.

Sample Microsoft Teams Trigger Commands:

`!quarantine-endpoint example-host`

`!quarantine-endpoint 00:A0:C9:14:C8:29`

`!unquarantine-endpoint example-host`

`!unquarantine-endpoint 00:A0:C9:14:C8:29`


# Key Features

* Manage the quarantine state of endpoints via hostname or MAC address

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Broadcom Symantec Endpoint Protection
* Credentials for a Broadcom Symantec Endpoint Protection user with System Administrator privileges

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `change_me` in each Teams step in the workflow.

After configuring the Teams steps, activate the workflow in order to trigger it.
 
An optional whitelist can be added to the Broadcom Symantec Endpoint Protection `Quarantine` action. To use this list 
add MAC addresses or hostnames in the following format (colons or hyphens are acceptable for MAC addresses) `["00:A0:C9:14:C8:29", "example-host"]`

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!quarantine-endpoint` or `!unquarantine-endpoint`.

Your chat bot will reply when the workflow completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|HTML|1.2.1|1|
|Broadcom Symantec Endpoint Protection|1.0.2|2|
|Microsoft Teams|2.0.4|9|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Broadcom Symantec Endpoint Protection](https://www.broadcom.com/products/cyber-security/endpoint/end-user)
* [Microsoft Teams](https://teams.microsoft.com)
