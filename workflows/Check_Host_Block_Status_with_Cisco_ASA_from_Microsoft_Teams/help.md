# Description

This workflow accepts a Microsoft Teams command containing a list of hosts. These hosts will be checked against a pre-defined address group in Cisco ASA to determine whether or not the IP address is present. It is assumed that this address group will be used to store IP addresses for a block policy. A message with the results will be returned.

Sample Microsoft Teams Trigger Commands:

`!block-status 198.51.100.100`

`!block-status example.com`

`!block-status 198.51.100.100 example.com`

# Key Features

* See if an IP address is currently blocked by the firewall

# Requirements

* [Microsoft Teams connection](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Cisco ASA firewall username, password, URL, port and User Agent.

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

In the _Check Host Block Status_ step edit the Group input from `change_me` to an appropriate address group.

To run the workflow,  Use the command `!block-status <host_address>`. The workflow will post responses in the channel.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|3.1.0|6|
|Cisco Adaptive Security Appliance|1.3.0|1|
|Type Converter|1.6.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Cisco ASA](https://www.cisco.com)
* [Cisco ASA Extension](https://extensions.rapid7.com/extension/cisco_asa)
* [Microsoft Teams](https://teams.microsoft.com)
