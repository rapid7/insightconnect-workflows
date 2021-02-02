# Description

This workflow accepts a Slack command containing a list of IP address or domains. This provided list will be checked against a pre-defined address group in SonicWall to determine if the IP address or domain is present or not. It is assumed that this address group will be used to store IP addresses for a block policy. A reply with the results will be returned.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect block-status 198.51.100.100 198.51.100.101`

`@Rapid7 InsightConnect block-status example.com example2.com 198.50.100.1`

# Key Features

* The ability to see if an IP address is currently blocked by the firewall

# Requirements

The following connections will need to be setup:

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Credentials to a SonicWall firewall

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

And in the _Check Block Status_ step edit the Address Group Name input from `change_me` to an appropriate address group to monitor.

To run the workflow, @ your Slackbot in the chosen channel or in a direct message along with the command "block-status" followed by a list of IP addresses or domains to be checked, separated by a space. The workflow will post responses in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|SonicWall Firewall|1.3.0|1|
|Type Converter|1.6.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [SonicWall Firewall](https://www.sonicwall.com/)
* [Slack Configuration](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Slack](https://slack.com/)
