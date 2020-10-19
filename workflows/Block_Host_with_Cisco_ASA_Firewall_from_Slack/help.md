# Description

This workflow blocks or unblocks a IPv4 and IPv6 addresses with Cisco ASA via Slack command and reports information back to Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect block-host 198.51.100.100`

`@Rapid7 InsightConnect unblock-host 198.51.100.100`

`@Rapid7 InsightConnect block-host 198.51.100.0 2001:db8:8:4::2`

`@Rapid7 InsightConnect unblock-host 198.51.100.0 2001:db8:8:4::2`

# Key Features

* Block and unblock IPv4 and IPv6 addresses

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Cisco ASA device with credentials and the REST API enabled

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Slack steps, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Slack workflow steps.*

To run the workflow, send a message to the specified Slack channel starting with the command `@Rapid7 InsightConnect block-host` or `@Rapid7 InsightConnect unblock-host` followed with an IPv4 or IPv6 address to take action on.

Your chat bot will reply when the workflow completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Cisco Adaptive Security Appliance|1.4.1|5|
|Type Converter|1.6.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Cisco Adaptive Security Appliance](https://www.cisco.com/c/en/us/products/security/adaptive-security-appliance-asa-software/index.html)
* [Rapid7 Slack Chatbot](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
