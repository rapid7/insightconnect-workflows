# Description

This workflow blocks or unblocks a IPv4 and IPv6 addresses with Cisco ASA via Slack command and reports information back to Slack.
The workflow works by adding and removing address objects from an existing network group tied to a Deny firewall policy in your Cisco ASA Firewall.
When an address is added to the group, it's blocked; when an address is removed from a group, it's unblocked. These are best practices for automating the blocking of hosts.

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

Once the workflow has been imported,

1. Update the first step with the channel name to suit your Slack environment by editing the input with the preset text of `change_me` to match the channel to monitor. Leave empty to run in all channels where the Slack bot is a member
2. Update the preset text of `change_me` in the `Group` field to the Network Group you want the workflow to manage in the following steps:

* **Block IP Address**
* **Block IP**
* **Check if IP Address in Group**
* **Unblock IP Addresses**

Additional customization can be provided with the following options:

1. An optional whitelist can be added to the Cisco `Create Address Object` action. To skip blocking these hosts, add IP addresses or CIDR IP addresses in the following format `["198.51.100.100", "198.51.100.1/32"]`
2. By default this workflow will automatically skip blocking private IP addresses. To block these, set the `Skip Private Addresses` option to false in the `Create Address Object` step.

After configuring the Slack steps, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Slack workflow steps, or from any channel if left empty.*

To run the workflow, send a formatted message to the specified Slack channel. Your chat bot will reply when the workflow completes.

Examples shown below

To block a host:
* `@Rapid7 InsightConnect block-host 198.51.100.100`
* `@Rapid7 InsightConnect block-host 2001:db8:8:4::2`

To unblock a host:
* `@Rapid7 InsightConnect unblock-host 198.51.100.100`
* `@Rapid7 InsightConnect unblock-host 2001:db8:8:4::2`

You can also block and unblock multiple hosts in a single command:
* `@Rapid7 InsightConnect block-host 198.51.100.100 2001:db8:8:4::2 198.51.100.101`
* `@Rapid7 InsightConnect unblock-host 198.51.100.0 2001:db8:8:4::2 198.51.100.101`

The workflow will reply in Slack as it runs.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Cisco Adaptive Security Appliance|1.4.1|5|
|Type Converter|1.6.0|1|

## Troubleshooting

The REST API server must be installed and enabled on the Cisco ASA device this plugin connects to. Cisco provides online documentation for this available [here](https://www.cisco.com/c/en/us/td/docs/security/asa/api/qsg-asa-api.html). In addition, the user account must have the necessary permissions for the intended actions:

* Actions that retrieve or check data require Cisco privilege level 5 or greater
* Actions that change or modify data require Cisco privilege level 15

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Cisco Adaptive Security Appliance](https://www.cisco.com/c/en/us/products/security/adaptive-security-appliance-asa-software/index.html)
* [Rapid7 Slack Chatbot](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
