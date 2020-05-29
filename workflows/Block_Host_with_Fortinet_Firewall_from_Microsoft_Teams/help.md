# Description

This workflow blocks or unblocks a host with Fortinet Firewall via Microsoft Teams command and reports information back to Microsoft Teams.

Sample Microsoft Teams Trigger Commands:

`!block-host 198.51.100.100/32`
`!block-host 198.51.100.0/24`
`!block-host example.co `

`!unblock-host 198.51.100.100/32`
`!unblock-host 198.51.100.0/24`
`!unblock-host example.com`

# Key Features

* Block and unblock hosts 

# Requirements


* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* A Fortigate firewall

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `change_me` in each Teams step in the workflow.

After configuring the Teams steps, activate the workflow in order to trigger it.
 
A optional whitelist can be added to the FortiGate Add Host to be Blocked action. To add this list add IP's or domains in the following format `["198.51.100.100", "example.com", "198.51.100.1"]`

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!block-host`.

Your chat bot will reply when the workflow completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|HTML|1.2.1|1|
|Fortinet FortiGate|4.0.0|3|
|Microsoft Teams|2.0.2|6|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [FortiGate](https://www.fortinet.com/products/next-generation-firewall.html)
* [Microsoft Teams](https://teams.microsoft.com)
