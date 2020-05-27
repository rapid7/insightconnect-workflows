# Description

This workflow accepts a Slack command containing an IP address. This IP address will be checked against a pre-defined address group in a Palo Alto firewall to determine if the IP address is present or not. It is assumed that this address group will be used to store IP addresses for a block policy. A message with the results will be returned.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect block-status 198.51.100.100`

# Key Features

* The ability to see if an IP is curently blocked by the firewall

# Requirements

* [Slack Connection](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Username and password for a Palo Alto firewall

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

In the _Check if IP in Group_ step change the Group input from `change_me` to an appropriate address group.

To run the workflow, @ your Slackbot or in a direct message along with the command "block-status <IP>". The workflow will post responses in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Slack|2.0.2|4|
|String Operations|1.2.1|3|
|Palo Alto Firewall|5.1.1|1|
|HTML|1.2.1|1|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://www.slack.com/)
* [Palo Alto Networks](https://www.paloaltonetworks.com/)
