# Description

This workflow accepts a Slack command containing an IP address. This IP address will be checked against a pre-defined address group in Cisco ASA to determine if the IP address is present or not. It is assumed that this address group will be used to store IP addresses for a block policy. A message with the results will be returned.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect !block-status 198.51.100.100`

`@Rapid7 InsightConnect !block-status example.com`

`@Rapid7 InsightConnect !block-status 198.51.100.100 example.com`

# Key Features

* See if an IP address is currently blocked by the firewall

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Cisco ASA firewall username, password, URL, port and User Agent.

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.
And in the _Check Host Block Status_ step edit the Group input from `change_me` to an appropriate address group to monitor.

To run the workflow, @ your Slackbot in the chosen channel or in a direct message along with the command "block-status <host_address>". The workflow will post responses in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Cisco Adaptive Security Appliance|1.3.0|1|
|Type Converter|1.6.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update default channel
* 1.0.0 - Initial workflow

# Links

## References

* [Cisco ASA](https://www.cisco.com)
* [Cisco ASA Extension](https://extensions.rapid7.com/extension/cisco_asa)
* [Slack](https://slack.com)
