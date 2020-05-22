# Description

Use the simplicity of a chat command in Slack to block or unblock a host in your Palo Alto Firewall.

Sample Slack Trigger Commands:

`block-host 198.51.100.100`

`unblock-host 198.51.100.100`

# Key Features

* **Block and Unblock a Host** - Use Slack and Insight Connect to make firewall rules easy. 

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/chatops-step)
* Palo Alto Firewall username and password

# Documentation

## Setup

The workflow works by adding and removing address objects from an address object group in your Palo Alto Firewall. When using this workflow, you will need to setup a policy on your firewall that blocks IPs from an address group. 

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

**Edit Each Palo Alto Firewall step to specify the group you are using** In these steps, specify the group you would like to add and remove host objects from. 

After import, activate the workflow in order to trigger it.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow in a direct message to the Rapid7 InsightConnect bot use `block-host <host>` or `unblock-host <host>`.

For example:
* `block-host 198.51.100.100`

You can also unblock a host. For example: 
* `unblock-host 198.51.100.100`

You can also block and unblock domains:
* `block-host www.example.com`

The workflow will reply when it completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Palo Alto Firewall|5.1.1|4|
|Python 3 Script|2.0.1|1|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Palo Alto Firewall](https://www.paloaltonetworks.com/)
