# Description

This workflow blocks or unblocks a hosts with SonicWall Firewall via Slack command and reports information back to Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect block-host example.com`

`@Rapid7 InsightConnect block-host example.com 198.51.100.100 2001:db8:8:4::2`

`@Rapid7 InsightConnect unblock-host example.com`

`@Rapid7 InsightConnect unblock-host example.com 198.51.100.100 2001:db8:8:4::2`

# Key Features

* Block and unblock a hosts

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [SonicWall Firewall credentials](https://www.sonicwall.com)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** Edit the input with the preset text of `change_me` in the first Slack step in the workflow.

In the `Check If Host Exists`, `Add Host To Block Group` and `Remove Host From Block Group` steps edit the Group Name input from `change_me` to an appropriate address group to monitor.

After configuring the Slack and SonicWall steps, activate the workflow in order to trigger it.

An optional whitelist can be added to the SonicWall `Add Host to be Blocked` step. To use this list add IP addresses or domains in the following format `["198.51.100.100", "example.com", "2001:db8:8:4::2"]`.

By default, this workflow will automatically skip blocking private IP addresses. To block these, set the `Skip Private Addresses` option to false in the `Add Host to be Blocked` step.

### Usage

*This workflow will only trigger in the channel specified in the Slack workflow steps.*

To run the workflow, send a message to the specified Slack channel starting with the command `@Rapid7 InsightConnect block-host` or `@Rapid7 InsightConnect unblock-host`.

For example:

`@Rapid7 InsightConnect block-host example.com 198.51.100.100 2001:db8:8:4::2`

`@Rapid7 InsightConnect unblock-host example.com 198.51.100.100 2001:db8:8:4::2`

Your Chatbot will reply when the workflow completes.

## Technical Details

Plugins utilized by the workflow:

|Plugin|Version|Count|
|----|----|--------|
|Type Converter|1.7.0|1|
|SonicWall Firewall|1.3.1|4|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [SonicWall Firewall](https://www.sonicwall.com/)
* [Slack](https://slack.com)
* [Rapid7 Slack Chatbot](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
