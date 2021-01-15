# Description

This workflow accepts a Microsoft Teams command containing a list of IP address or domains. This provided list will be checked against a pre-defined address group in SonicWall to determine if the IP address or domain is present or not. It is assumed that this address group will be used to store IP addresses for a block policy. A reply with the results will be returned.

Sample Microsoft Teams Trigger Commands:

`!block-status 198.51.100.100 198.51.100.101`

`!block-status example.com example2.com 198.50.100.1`

# Key Features

* The ability to see if an IP is currently blocked by the firewall

# Requirements

The following connections will need to be setup:

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Credentials to a SonicWall firewall

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **update the first step with the channel and team name to suit your Microsoft Teams environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

And in the _Check Block Status_ step edit the Address Group Name input from `change_me` to an appropriate address group to monitor.

To run the workflow, post the command "!block-status", in your chosen team channel, followed by a list of IP addresses or domains to be checked, separated by a space. The workflow will post responses in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|SonicWall Firewall|1.3.0|1|
|Type Converter|1.6.1|1|
|Microsoft Teams|3.1.0|7|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [SonicWall Firewall](https://www.sonicwall.com/)
* [Microsoft Teams Configuration](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Teams](https://teams.microsoft.com)
