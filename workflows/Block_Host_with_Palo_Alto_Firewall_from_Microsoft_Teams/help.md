# Description

Use the simplicity of a chat command in Microsoft Teams to block or unblock a host in your Palo Alto Firewall.

Sample Microsoft Teams Trigger Commands:

`!block-host 198.51.100.100`

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

Once the workflow has been imported, **each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `change_me` in each Teams step in the workflow.

**Edit Each Palo Alto Firewall step to specify the group you are using** In these steps, specify the group you would like to add and remove host objects from. 

By default this workflow will automatically skip blocking private IP addresses, if you’d like to block these as well, set `Skip RFC 1918` option to false in the `Create Network Object` step.

After import, activate the workflow in order to trigger it.

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
|Microsoft Teams|2.0.4|5|
|Palo Alto Firewall|6.0.0|4|
|String Operations|1.2.1|3|
|HTML|1.2.1|1|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.1 - Update Microsoft Teams to latest version
* 1.1.0 - Update Palo Alto Firewall to latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Palo Alto Firewall](https://www.paloaltonetworks.com/)
