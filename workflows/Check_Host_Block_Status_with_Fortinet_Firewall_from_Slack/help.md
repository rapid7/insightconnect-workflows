# Description

This workflow accepts a Slack command containing an IP address. This IP address will be checked against a pre-defined address group in Fortinet to determine if the IP address is present or not. It is assumed that this address group will be used to store IP addresses for a block policy. A message with the results will be returned.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect block-status 198.51.100.100`
`@Rapid7 InsightConnect block-status example.com`

# Key Features

* The ability to see if an IP is currently blocked by the firewall


# Requirements

* Slack connection
* Admin API key to a Fortinet FortiGate firewall

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

In the _Check for IP Message_ step edit the Match Channel input from `change_me` to an appropriate channel.
In the _Check for IP_ step edit the Address Group Name input from `change_me` to an appropriate address group.

To run the workflow, @ your Slackbot in the chosen channel or in a direct message along with the command "block-status <IP>". The workflow will post responses in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Fortinet FortiGate|4.0.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Update Fortinet FortiGate to latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Fortinet](https://www.fortinet.com/)
* [Slack](https://slack.com)
