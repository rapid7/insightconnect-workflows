# Description

Use the simplicity of a chat command in Slack to block or unblock a host in your Palo Alto Firewall.

Multiple hosts can be specified within one command.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect block-host 198.51.100.100`

`@Rapid7 InsightConnect block-host 198.51.100.100 198.51.100.101`

`@Rapid7 InsightConnect unblock-host 198.51.100.100`

# Key Features

* **Block and Unblock a Host** - Use Slack and Insight Connect to make firewall rules easy. 

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/chatops-step)
* Palo Alto Firewall username and password

# Documentation

## Setup

The workflow works by adding and removing address objects from an address object group in your Palo Alto Firewall. When using this workflow, you will need to setup a policy on your firewall that blocks IPs from an address group. 

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.
And then **Edit Each Palo Alto Firewall step to specify the group you are using** In these steps, specify the group you would like to add and remove host objects from. 

By default this workflow will automatically skip blocking private IP addresses, if you’d like to block these as well, set `Skip RFC 1918` option to false in the `Create Network Object` step.

After import, activate the workflow in order to trigger it.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

For example:
* `@Rapid7 InsightConnect block-host 198.51.100.100`

You can also unblock a host. For example: 
* `@Rapid7 InsightConnect unblock-host 198.51.100.100`

You can also block and unblock domains:
* `@Rapid7 InsightConnect block-host www.example.com`

The workflow will reply when it completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Palo Alto Firewall|6.0.1|4|
|Type Converter|1.6.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.2.0 - Add automatic indicator extraction, allow for multiple hosts
* 1.1.1 - Pass channel name from trigger to all subsequent steps so user only has to configure channel once
* 1.1.0 - Update Palo Alto Firewall to latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Palo Alto Firewall](https://www.paloaltonetworks.com/)
