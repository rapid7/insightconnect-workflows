# Description

This workflow blocks or unblocks IPv4 and IPv6 addresses with Cisco ASA via Microsoft Teams command and reports information back to Microsoft Teams.

The workflow works by adding and removing address objects from an existing network group tied to a Deny firewall policy in your Cisco ASA Firewall.

When an address is added to the group, it's blocked; when an address is removed from a group, it's unblocked. These are best practices for automating the blocking of hosts.

Sample Microsoft Teams Trigger Commands:

`!block-host 198.51.100.100`

`!unblock-host 198.51.100.100`

`!block-host 198.51.100.0 2001:db8:8:4::2`

`!unblock-host 198.51.100.0 2001:db8:8:4::2`

# Key Features

* Block and unblock IPv4 and IPv6 addresses

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Cisco ASA device with credentials and the REST API enabled

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported,

1. Update the first step with the channel name to suit your Microsoft Teams environment by editing the input with the preset text of `change_me` to match the channel to monitor. Leave empty to run in all channels where the Microsoft Teams bot is a member
2. Update the preset text of `change_me` in the `Group` field to the Network Group you want the workflow to manage in the following steps:

* **Block IP Address**
* **Block IP**
* **Check if IP Address in Group**
* **Unblock IP Addresses**

Additional customization can be provided with the following options:

1. An optional whitelist can be added to the Cisco `Create Address Object` action. To skip blocking any specified important hosts, add their IP addresses or CIDR network addresses in the following list format `["198.51.100.100", "198.51.100.1/32"]`
2. By default this workflow will automatically skip blocking private IP addresses. To remove this safety check, set the `Skip Private Addresses` option to false in the `Create Address Object` step.

After configuring the Microsoft Teams steps, activate the workflow.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps, or from any channel if left empty.*

To run the workflow, send a formatted message to the specified Microsoft Teams channel. Your chat bot will reply when the workflow completes.

Examples shown below

To block a host:
* `!block-host 198.51.100.100`
* `!block-host 2001:db8:8:4::2`

To unblock a host:
* `!unblock-host 198.51.100.100`
* `!unblock-host 2001:db8:8:4::2`

You can also block and unblock multiple hosts in a single command:
* `!block-host 198.51.100.100 2001:db8:8:4::2 198.51.100.101`
* `!unblock-host 198.51.100.0 2001:db8:8:4::2 198.51.100.101`

The workflow will reply in Microsoft Teams as it runs.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Cisco Adaptive Security Appliance|1.4.1|5|
|Type Converter|1.6.0|1|
|Microsoft Teams|2.2.1|8|

## Troubleshooting

The REST API server must be installed and enabled on the Cisco ASA device this plugin connects to. Cisco provides online documentation for this available [here](https://www.cisco.com/c/en/us/td/docs/security/asa/api/qsg-asa-api.html). In addition, the user account must have the necessary permissions for the intended actions:

* Actions that retrieve or check data require Cisco privilege level 5 or greater
* Actions that change or modify data require Cisco privilege level 15

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Cisco Adaptive Security Appliance](https://www.cisco.com/c/en/us/products/security/adaptive-security-appliance-asa-software/index.html)
* [Microsoft Teams](https://teams.microsoft.com)
