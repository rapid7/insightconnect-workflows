# Description

This workflow accepts a Microsoft Teams command containing an IP address. This IP address will be checked against a pre-defined address group in Fortinet to determine if the IP address is present or not. It is assumed that this address group will be used to store IP addresses for a block policy. A message with the results will be returned.

Sample Microsoft Teams Trigger Commands:

`!block-status 198.51.100.100`

# Key Features

* The ablity to see if an IP is curently blocked by the firewall


# Requirements

* Microsoft Teams connection
* An admin API key to a Fortigate firewall

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

In the _Check for IP Message_, _IP Blocked Message_, and _IP Not Blocked Message_ steps edit the Team Name and Channel Name input from `change_me` to an appropriate team and channel.

In the _Check for IP_ step edit the Address Group Name input from `change_me` to an appropriate address group.

To run the workflow,  Use the command "!block-status <IP>". The workflow will post responses in the channel.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Fortinet FortiGate|1.1.0|1|
|HTML|1.2.1|1|
|Microsoft Teams|2.0.2|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Fortinet](https://www.fortinet.com/)
* [Slack](https://slack.com)
