# Description

Use the simplicity of a chat command in Microsoft Teams to block or unblock a host in your Palo Alto Firewall.

Multiple hosts can be specified within one command.

Sample Microsoft Teams Trigger Commands:

`!block-host 198.51.100.100`

`!block-host 198.51.100.100 198.51.100.101`

`!unblock-host 198.51.100.100`

# Key Features

* **Block and Unblock a Host** - Use Microsoft Teams and Insight Connect to make firewall rules easy. 

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Palo Alto Firewall username and password

# Documentation

## Setup

The workflow works by adding and removing address objects from an address object group in your Palo Alto Firewall. When using this workflow, you will need to setup a policy on your firewall that blocks IPs from an address group. 

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages InsightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow. 

There are three parameters you will need to configure in order to complete setup of your workflow:

* Teams Channel - enter the Teams channel name matching your environment ex: `channelname`
* Teams Team - enter the Teams team name matching your environment ex: `teamname`
* Palo Alto Object Group Name - enter the name of the group you would like to add and remove host objects from, ex: `ICON Block List`

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the parameters, activate the workflow in order to trigger it.

By default this workflow will automatically skip blocking private IP addresses, if you’d like to block these as well, set `Skip RFC 1918` option to false in the `Create Network Object` step.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, in the channel you are monitoring send a message to Insight Connect using `!block-host <host>` or `!unblock-host <host>`.

For example:
* `!block-host 198.51.100.100`

You can also unblock a host. For example: 
* `!unblock-host 198.51.100.100`

You can also block and unblock domains:
* `!block-host www.example.com`

The workflow will reply when it completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Palo Alto Firewall|6.1.0|5|
|Type Converter|1.8.0|1|
|Microsoft Teams|3.1.1|7|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 2.0.0 - Leverage Parameters Feature | Update Palo Alto Firewall to latest version | Update Type Converter to latest version | Update Microsoft Teams to latest version
* 1.2.1 - Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.2.0 - Add automatic indicator extraction, allow for multiple hosts
* 1.1.1 - Update to make Microsoft Teams plugin the latest version
* 1.1.0 - Update Palo Alto Firewall to latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Palo Alto Firewall](https://www.paloaltonetworks.com/)
