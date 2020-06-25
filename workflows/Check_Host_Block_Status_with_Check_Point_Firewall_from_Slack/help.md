# Description

This workflow accepts a Slack command containing an IP address. This IP address will be checked against a pre-defined address group in Check Point to determine if the IP address is present or not. It is assumed that this address group will be used to store IP addresses for a block policy. A message with the results will be returned.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect block-status 198.51.100.100`

# Key Features

* Check if an IP is currently blocked by the firewall

# Requirements

* [Slack connection](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Check Point firewall username and password

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.
And then in the _Check for IP_ step edit the Address Group Name input from `change_me` to an appropriate address group to monitor.

To run the workflow, @ your Slackbot in the chosen channel or in a direct message along with the command "block-status <IP>". The workflow will post responses in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Check Point NGFW|2.0.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.1 - Pass channel name from trigger to all subsequent steps so user only has to configure channel once
* 1.1.0 - Update to make the Check Point NGFW plugin the latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Check Point](https://www.checkpoint.com/)
* [Slack](https://slack.com)
