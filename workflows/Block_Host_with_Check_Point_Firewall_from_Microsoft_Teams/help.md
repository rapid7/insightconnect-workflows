# Description

This workflow blocks or unblocks a host with Check Point Firewall via Microsoft Teams command and reports information back to Microsoft Teams.

Sample Microsoft Teams Trigger Commands:

`!block-host 198.51.100.100`
`!block-host 198.51.100.100/32`
`!block-host 198.51.100.0/24`

`!unblock-host 198.51.100.100`
`!unblock-host 198.51.100.100/32`
`!unblock-host 198.51.100.0/24`

# Key Features

* Block and unblock hosts 

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Check Point firewall
* Check Point username and password

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `change_me` in each Teams step in the workflow.

After configuring the Teams steps, activate the workflow in order to trigger it.
 
An optional whitelist can be added to the Check Point `Add Host to be Blocked` action. To use this list add IP addresses or CIDR IP addresses in the following format `["198.51.100.100", "198.51.100.1/32"]`

By default this workflow will automatically skip blocking private IP addresses. To block these, set the `Skip RFC 1918` option to false in the `Add Host to be Blocked` step.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!block-host` or `!unblock-host`.

Your chat bot will reply when the workflow completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|HTML|1.2.1|1|
|Check Point NGFW|2.0.1|3|
|Microsoft Teams|2.0.4|11|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update to make Microsoft Teams plugin the latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Check Point](https://www.checkpoint.com/)
* [Microsoft Teams](https://teams.microsoft.com)
