# Description

This workflow accepts a Slack command containing an IP address or domain. This object will be checked against a pre-defined address group in a Palo Alto firewall to determine if the object is present or not. It is assumed that this address group will be used to store address objects for a block policy. A message with the results will be returned.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect block-status 198.51.100.100`

`@Rapid7 InsightConnect block-host example.com`

# Key Features

* The ability to see if an IP is curently blocked by the firewall

# Requirements

* [Slack Connection](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Username and password for a Palo Alto firewall

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.
And in the _Check if IP in Group_ step change the Group input from `change_me` to an appropriate address group to monitor.

To run the workflow, @ your Slackbot or in a direct message along with the command "block-status <IP>". The workflow will post responses in a thread.

For example:

* `@Rapid7 InsightConnect block-host example.com`
* `@Rapid7 InsightConnect block-host 198.10.198.100`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Python 3 Script|2.0.2|1|
|Palo Alto Firewall|6.0.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.1 - Pass channel name from trigger to all subsequent steps so user only has to configure channel once
* 1.1.0 - Update Palo Alto Firewall to latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://www.slack.com/)
* [Palo Alto Networks](https://www.paloaltonetworks.com/)
